# AZ-204 Desenvolvendo soluções para certificação Azure

### Seção 1: Desenvolver soluções de computação do Azure – Aplicativos Web do Azure e Funções do Azure

- Serviço de Aplicativo Web do Azure

  - linguagens suportadas: .NET, .NET Core, Java, Python, Node.js, Ruby
  - é um PaaS, você não gerencia as VMs/DBs em que seu aplicativo é executado
  - tem escala
  - alta seguranca
  - Capacidades DevOps como implantação contínua
- Plano de serviço de aplicativo

  - seu aplicativo depende de um plano de serviço de aplicativo (que é um recurso)
  - grátis: 10 aplicativos, 1 GB de espaço em disco, 60 minutos de CPU/dia
  - compartilhado: 100 aplicativos, 1 GB, 240 minutos de CPU/dia
  - básico: aplicativos ilimitados, 10 GB, minutos/dia de CPU ilimitados, 3 instâncias no máximo
    - máximo de instâncias: o número de VMs que você pode ter no plano para executar seus aplicativos, as solicitações são equilibradas entre as instâncias
  - todos os aplicativos da web em um plano precisam estar na mesma região do plano
  - todos os aplicativos da web em um plano precisam ter o mesmo sistema operacional subjacente
- Registro em log do aplicativo Web do Azure

  - tipos de registro
    - registro de aplicativos: registros gerados pelo seu aplicativo
    - registro do servidor web: registra solicitações HTTP
    - mensagens de erro detalhadas: armazena páginas de erro .htm que teriam ido para o cliente
    - registro de implantação: erros que ocorrem durante a publicação
  - os logs são transmitidos em tempo real
  - você pode acessar o fluxo por meio de um URL FTP na página de fluxo de log no recurso do seu aplicativo da web
- você pode habilitar a implantação contínua com GitHub Actions vinculando seu aplicativo web a um repositório GitHub

  - se você vincular seu aplicativo web a um repositório GitHub, a implantação contínua será implementada automaticamente
- Web App CLI commands

  - `$plan="plan-name"`
  - `$appname="app-name"`
  - `$repoulr="https://github.com/[username]/[repo name]"`
  - `az group create --location westeurope --name [group name]`
  - `az appservice plan create --name $plan --resource-group [group name] --sku B1`
  - `az webapp create --name $appname --resource-group [group name] --plan $plan`
  - `az webapp deployment source config --name $appname --resource-group [group name] --repo-url $repourl --branch master --manual-integration`
- custom domain
- compre um nome de domínio

  - vá para a página de domínios personalizados no recurso do aplicativo da web e adicione o domínio personalizado
  - defina o domínio personalizado com o nome que você comprou e salve o domínio personalizado
  - no site do provedor de domínio, você precisa ter um registro CNAME que vincule a URL original do seu aplicativo Web (que o Azure atribui) ao seu novo domínio
  - Domínio personalizado SSL
    - acesse as configurações de TLS/SSL e crie um certificado gerenciado de serviço de aplicativo
    - adicionar ligação SSL (novo certificado ao domínio personalizado)
  - CORS: compartilhamento de recursos entre origens
    - os navegadores percebem quando uma página está tentando solicitar dados de um domínio diferente e impedem que isso aconteça
    - na página CORS no recurso do aplicativo web (que recebe solicitações), você pode adicionar domínios que têm permissão para fazer solicitações
    - Comando CLI: `az webapp cors add -g [nome do grupo] -n [nome do aplicativo] --allowed-origins [domínio que faz solicitações para este aplicativo web]`
- deployment slots

  - implantar várias versões do mesmo aplicativo em ambientes diferentes
  - cada ambiente é um "slot" (por exemplo, produção, preparação, etc.)
  - cada slot tem seu próprio nome DNS (seu próprio URL)
  - você pode trocar slots
  - disponível apenas em planos de serviço de aplicativo padrão ou superiores
  - você usa um perfil de publicação diferente em seu projeto para cada ambiente/slot
  - PowerShell commands
    - `$location="Central US"`
    - `$resourcegrp="newgrp"`
    - `$webappname="demoapp4040"`
    - `New-AzResourceGroup -Name $resourcegrp -Location $location`
    - `New-AzAppServicePlan -Name $webappname -Location $location -ResourceGroupName $resourcegrp -Tier Standard`
    - `New-AzWebApp -Name $webappname -Location $location -ResourceGroupName $resourcegrp -AppServicePlan $webappname`
    - `New-AzWebAppSlot -Name $webappname -ResourceGroupName $resourcegrp -Slot "staging"`
- autoscaling

  - a VM em que seu aplicativo está sendo executado
  - em um plano básico de serviço de aplicativo, você pode ter até três VMs para escalabilidade, mas precisa selecionar manualmente para adicionar/remover uma máquina
  - no nível padrão ou superior, a criação/desalocação de VM (expansão horizontal, redução horizontal) é acionada automaticamente com base nas regras que você cria
  - chamado de "escalonamento automático personalizado"
  - você cria regras no recurso do plano de serviço de aplicativo
  - você pode basear suas regras não apenas nas métricas do plano de serviço, mas também nas métricas provenientes de outros tipos de recursos
    - fila de armazenamento
    - fila de ônibus de serviço
    - etc
  - métricas nas quais você pode criar regras com base
    - CPU %
    - entrada/saída de dados
    - Comprimento da fila HTTP
      -% de memória
    - etc
  - período de resfriamento: o tempo que leva para a nova VM ser adicionada/removida depois que um limite de regra de escalonamento automático for atingido
- cadeias de conexão

  - necessário para conectar um aplicativo Web do Azure a um banco de dados SQL do Azure
  - no seu projeto de API, crie um serviço que defina um SqlConnection, faça uma conexão, execute instruções SQL e depois feche a conexão
    - é aqui que você cola a string de conexão do banco de dados, nome de usuário, senha, etc.
    - OU você pode adicionar a cadeia de conexão completa do Azure em appsettings e, em seguida, passar a cadeia de conexão para o seu serviço
    - OU você pode armazenar a cadeia de conexão completa na página Configuração do aplicativo Web
  - instale o pacote NuGet System.Data.SqlClient (ou qualquer pacote que você queira usar para qualquer estrutura que estiver usando)
  - injete o serviço (junto com o MVC ou o que você estiver usando)
  - crie um controlador para obter os dados e exibi-los em um componente de visualização
- Recurso de configuração de aplicativos

  - usado para armazenar cadeias de conexão no Azure para que fiquem fora de um arquivo appsettings e possam ser usadas por vários aplicativos Web ao mesmo tempo
  - você cria pares de valores-chave neste recurso
  - você precisa do pacote NuGet de configuração de aplicativo do Azure em seu aplicativo
  - você adiciona a string de conexão da chave que deseja acessar (copiada do Azure) em seu código
  - você também pode adicionar sinalizadores de recursos no recurso de configuração de aplicativos
    - métodos/visualizações podem ter um atributo FeatureGate com um valor de sinalizador de recurso específico (que você define em uma enumeração) atribuído a ele
- Azure Functions

  - linguagens: C#, Java, JavaScript, Python, PowerShell
  - maneiras de invocar uma função
    - solicitação HTTP
      - PEGAR
      - PUBLICAR
    - cronômetro
    - eventos de blob
    - eventos de armazenamento de fila
    - eventos do centro de eventos
  - ao criar o aplicativo de funções, você seleciona o idioma em que as funções serão escritas
  - planos
    - você pode adicionar a função a um plano de serviço de aplicativo
    - ou você pode usar um plano baseado em consumo
    - plano premium: instâncias pré-aquecidas e computação com escalonamento automático
  - você pode habilitar o Application Insights no aplicativo de funções
  - adicionando funções ao aplicativo de funções
    - você pode escolher um modelo baseado em um gatilho
    - a função é um arquivo de script C# (se o aplicativo de funções que você criou estiver em C# e você estiver editando no editor do Azure)
    - o arquivo function.json tem o script em conformidade com JSON para o Azure implantar a função
    - você pode testar no Azure ou com Postman
    - você só pode testar GETs através de um navegador normal
    - se você desenvolver a função no VS, publicar a função no Azure apenas enviará o arquivo function.json, pois esse é o único arquivo que o Azure precisa para implantar a função

### Section 2: Develop Azure compute solutions

- benefícios dos contêineres
- teste o aplicativo isoladamente, sem conflito entre dependências quando duas instâncias estão em execução na mesma máquina/VM
- cada contêiner possui seu próprio conjunto de dependências, independente de quaisquer outros contêineres na mesma máquina
- portabilidade, você pode mover contêineres entre VMs facilmente, basta implantar o contêiner em uma VM diferente (assumindo que ele tenha o mesmo sistema operacional base)
- os recipientes são leves
- imagem: o conjunto de instruções, o modelo, para a criação do container
  - a imagem é composta por muitas camadas
  - a camada base é composta de configurações em nível de sistema operacional
  - uma imagem só pode ser executada no sistema operacional ao qual a camada base se destina
- container: a instância executável de uma imagem na qual seu aplicativo pode ser executado
- depois de instalar o tempo de execução do Docker em sua máquina (Linux ou Windows), você pode implantar contêineres com base em uma imagem
- Docker Hub é um site com toneladas de imagens Docker pré-fabricadas
- se quiser acessar um site que está sendo executado em um contêiner Docker, você deverá especificar um mapeamento de porta ao implantar o contêiner
  - o contêiner está isolado da máquina, inclusive de sua rede, por isso você deve informar ao Docker para qual porta deseja encaminhar o site para poder acessá-lo a partir do navegador da máquina
  - você pode então criar uma regra de tráfego de entrada para a VM para poder acessar o aplicativo -> que o contêiner está em execução -> na VM -> através do navegador em sua máquina física
- Subsistema Docker + Windows para Linux
  - instalar o Docker Desktop em uma máquina Windows instala automaticamente o Windows Subsystem para Linux
  - WSL cria um ambiente Linux na máquina, no qual o Docker é executado
- Os contêineres baseados em Windows são muito maiores que os contêineres baseados em Linux
