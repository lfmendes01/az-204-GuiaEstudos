# inscrição

## O que é assinatura

No Microsoft Azure, uma “assinatura” é uma assinatura paga de um serviço do Azure. Ao se inscrever em uma conta do Azure, você precisa criar uma assinatura do Azure. Esta assinatura está associada à sua conta do Azure e permite usar e gerenciar vários serviços de nuvem no Azure. Através de uma assinatura do Azure, você pode criar, implantar e gerenciar vários recursos de nuvem, como máquinas virtuais, armazenamento, bancos de dados e aplicativos Web.

Alguns conceitos-chave:

Grupo de Recursos: Numa subscrição, pode criar um ou mais grupos de recursos para organizar e gerir recursos de nuvem relacionados. Um grupo de recursos é um contêiner lógico que permite organizar e gerenciar recursos.

Faturamento: as assinaturas estão intimamente ligadas ao faturamento e você será cobrado com base no uso da assinatura. O Azure oferece diferentes tipos de assinaturas, incluindo avaliações gratuitas, assinaturas pagas, etc., e cada tipo tem um modelo de cobrança diferente.

Permissões e funções: o acesso aos recursos da sua assinatura pode ser gerenciado por meio de autenticação e autorização no Azure Active Directory (AAD). O Azure utiliza o controlo de acesso baseado em funções (RBAC) para controlar o acesso dos utilizadores aos recursos.

Ferramentas de gerenciamento: você pode usar o portal do Azure, a CLI do Azure, o PowerShell e outras ferramentas para gerenciar e operar os recursos da sua assinatura.

No Azure, cada subscrição tem um identificador único (ID de subscrição) que identifica exclusivamente a subscrição nos serviços do Azure. As assinaturas são um conceito central para organizar e gerenciar recursos do Azure e fornecem aos usuários uma estrutura para utilizar efetivamente os serviços de nuvem do Azure.

## Qual conceito está mais próximo da AWS?

Na AWS, o conceito mais próximo do conceito de assinatura no Azure é a “Conta” na AWS.

Na AWS, uma conta representa uma entidade independente e faturada de forma totalmente independente. Ao se inscrever em uma conta da AWS, você cria uma conta exclusiva da AWS com um ID de conta exclusivo de 12 dígitos. As contas da AWS são usadas para organizar e gerenciar recursos da AWS, bem como faturamento na AWS.

# planos de serviço de aplicativos do Azure

## o que são planos de serviço de aplicativos do Azure

Os Planos de Serviço de Aplicativo do Azure são um plano de serviço no Azure para hospedagem de aplicativos Web. Ele fornece uma maneira de alocar recursos, dimensionar e gerenciar o ambiente no qual os aplicativos são executados. Aqui estão alguns conceitos-chave:

Plano de Serviço de Aplicativo: Este é um contêiner lógico que define um conjunto de aplicativos Web do Serviço de Aplicativo que compartilham os mesmos recursos de computação e definições de configuração. O Plano de Serviço de Aplicativo inclui recursos de computação (como instâncias de máquinas virtuais), sistemas operacionais, recursos de rede, etc. Um Plano de Serviço de Aplicativo pode hospedar um ou mais aplicativos Web, aplicativos API, aplicativos móveis ou serviços de back-end.

Aumentar/diminuir escala: ao alterar o tamanho do Plano de Serviço de Aplicativo, você pode dimensionar o aplicativo verticalmente. Isso significa que você pode ajustar o tamanho dos recursos computacionais de acordo com as necessidades da sua aplicação, por exemplo, atualizar de Compartilhado para Básico, Padrão, Premium, etc.

Scale Out/In: Ao alterar o número de instâncias, você pode dimensionar seu aplicativo horizontalmente. Isso significa que você pode aumentar ou diminuir o número de instâncias de máquinas virtuais executando seu aplicativo em resposta a alterações no tráfego e na carga.

Modelo de preços: os Planos de Serviço de Aplicativo têm diferentes níveis de preços, cada um oferecendo diferentes recursos e recursos de computação. A camada Compartilhada é adequada para desenvolvimento e testes de baixo tráfego, enquanto as camadas Standard, Premium e Advanced Enhanced são adequadas para aplicações de produção em maior escala.

Regiões e disponibilidade específicas: os Planos de Serviço de Aplicações podem ser criados em regiões específicas do Azure para garantir alta disponibilidade e baixa latência para a sua aplicação.

No geral, os Planos de Serviço de Aplicativos do Azure fornecem uma maneira conveniente de gerenciar e ajustar os recursos de computação para atender às necessidades de desempenho e escalabilidade do seu aplicativo. Ao utilizar Planos de Serviço de Aplicações, pode gerir eficazmente os recursos com base nas necessidades da sua aplicação, ao mesmo tempo que minimiza a complexidade de manutenção e configuração.

## Isso é semelhante a algo no serviço de nuvem AWS?

Na AWS, os serviços correspondentes aos planos de serviço de aplicativos do Azure são principalmente AWS Elastic Beanstalk e AWS App Runner. Ambos os serviços fornecem uma forma simplificada e automatizada de hospedar e implementar aplicações web, semelhante à funcionalidade do Azure App Service.

AWS Elastic Beanstalk: Este é um serviço totalmente gerenciado que permite implantar, executar e dimensionar aplicativos facilmente. Semelhante ao Azure App Service Plan, o Elastic Beanstalk fornece o conceito de ambiente, e você pode escolher a escala do ambiente, o tipo de instância, etc. Ele oferece suporte a vários idiomas e estruturas e gerencia automaticamente a infraestrutura subjacente.

AWS App Runner: Este é um serviço totalmente gerenciado focado na criação, implantação e dimensionamento rápido de aplicativos em contêineres. Você apenas fornece o código e a configuração do aplicativo, e o App Runner cuida do contêiner subjacente e do gerenciamento da infraestrutura. Isso o torna ideal para que os desenvolvedores implantem aplicativos rapidamente sem se preocupar com os detalhes operacionais subjacentes.

Embora os planos de serviço de aplicativos do Azure, o AWS Elastic Beanstalk e o AWS App Runner sejam semelhantes em alguns aspectos, também existem algumas diferenças. A escolha de um desses serviços geralmente depende de suas necessidades específicas, conjunto de tecnologia e preferências. Ao comparar esses serviços, você pode considerar os recursos específicos de cada provedor de nuvem, modelos de preços, opções de integração e linguagens e estruturas suportadas.

## documento

[https://learn.microsoft.com/zh-cn/azure/app-service/overview-hosting-plans](https://learn.microsoft.com/zh-cn/azure/app-service/overview-hosting-plans)

O nível de preços de um plano de Serviço de Aplicações determina as funcionalidades do Serviço de Aplicações oferecidas e o custo do plano. Os níveis de preços disponíveis para planos de Serviço de Aplicações dependem do sistema operativo selecionado no momento da criação. Os níveis de preços incluem o seguinte:

* Computação Compartilhada: Gratuita e Compartilhada, essas duas camadas básicas executam aplicativos na mesma VM do Azure que outros aplicativos do Serviço de Aplicativo, incluindo os de outros clientes. Essas camadas alocam cotas de CPU para cada aplicativo em execução em recursos compartilhados, e os recursos não podem ser ampliados. Essas camadas são apenas para fins de desenvolvimento e teste.
* Computação Dedicada: Os níveis Básico, Padrão, Avançado, Avançado V2 e Avançado V3 executam aplicações em VMs Azure dedicadas. Somente aplicativos no mesmo plano do Serviço de Aplicativo podem compartilhar os mesmos recursos de computação. Quanto mais alto for o nível, mais instâncias de VM estarão disponíveis para expansão.
* Autônomo: as camadas Standalone e Standalone V2 executam VMs Azure dedicadas em uma rede virtual Azure dedicada. Ele fornece isolamento de rede para aplicativos baseados em isolamento computacional. Essa camada fornece recursos máximos de expansão.
* Computação partilhada: Gratuita e Partilhada, os dois níveis base, executa uma aplicação no mesmo Azure VM que outras aplicações do Serviço de Aplicações, incluindo aplicações de outros clientes. Essas camadas alocam cotas de CPU para cada aplicativo executado nos recursos compartilhados, e os recursos não podem ser ampliados. Essas camadas devem ser usadas apenas para fins de desenvolvimento e teste.
* Computação dedicada: as camadas Básica, Standard, Premium, PremiumV2 e PremiumV3 executam aplicativos em VMs Azure dedicadas. Apenas as aplicações no mesmo plano do Serviço de Aplicações partilham os mesmos recursos de computação. Quanto mais alto o nível, mais instâncias de VM estarão disponíveis para expansão horizontal.
* Isolado: Os níveis Isolado e IsoladoV2 executam VMs Azure dedicados em Redes Virtuais Azure dedicadas. Ele fornece isolamento de rede além do isolamento de computação para seus aplicativos. Ele fornece os recursos máximos de expansão.

Como o aplicativo é executado e dimensionado?

Nas camadas Gratuita e Compartilhada, os aplicativos aderem à cota de minutos de CPU em instâncias de VM compartilhadas e não podem escalar horizontalmente. Em outras camadas, os aplicativos são executados e dimensionados conforme descrito abaixo.

Quando cria uma aplicação no Serviço de Aplicações, a aplicação torna-se parte de um plano do Serviço de Aplicações. Quando o aplicativo for executado, ele será executado em todas as instâncias de VM configuradas no plano do Serviço de Aplicativo. Se vários aplicativos estiverem incluídos no mesmo plano do Serviço de Aplicativo, os aplicativos compartilharão a mesma instância de VM. Se vários slots de implantação forem usados para um aplicativo, todos os slots de implantação também serão executados na mesma instância de VM. Se você ativar o log de diagnóstico, realizar backups ou executar WebJobs, eles também usarão ciclos de CPU e memória nessas instâncias de VM.

O plano do Serviço de Aplicativo torna-se então a unidade de escala para o aplicativo do Serviço de Aplicativo. Se você configurar um plano para executar cinco instâncias de VM, todos os aplicativos do plano serão executados em todas as cinco instâncias. Se o escalonamento automático estiver configurado para um plano, todos os aplicativos no plano serão dimensionados juntos com base nas configurações de escalonamento automático.

# Configurar serviço de aplicativo

[https://learn.microsoft.com/zh-cn/azure/app-service/configure-common?tabs=portal](https://learn.microsoft.com/zh-cn/azure/app-service/configure-common?tabs=portal)

## Configurações do aplicativo

Variáveis de ambiente: Nas Configurações do Aplicativo, você pode definir as variáveis de ambiente do aplicativo. Essas variáveis podem ser obtidas dinamicamente no código da sua aplicação para configurar diferentes parâmetros de acordo com diferentes ambientes, como strings de conexão de banco de dados, chaves de API, etc.

Cadeia de conexão: se seu aplicativo precisar se conectar a um banco de dados ou outro serviço, você poderá definir a cadeia de conexão em Configurações do aplicativo. Dessa forma, você pode fazer referência a essas cadeias de conexão em seu aplicativo sem precisar codificá-las em seu código.

Chave do aplicativo: para aplicativos que exigem autenticação, você pode definir uma chave ou senha do aplicativo nas Configurações do aplicativo. Essas informações normalmente são usadas para acessar APIs, serviços ou recursos protegidos.

Ajustar configuração: as Configurações do Aplicativo permitem ajustar dinamicamente a configuração do seu aplicativo no portal do Azure ou por meio de ferramentas como CLI do Azure, PowerShell, etc., sem precisar reimplantar todo o aplicativo.

Suporte a vários ambientes: as configurações do aplicativo facilitam a definição de diferentes configurações em diferentes ambientes (como desenvolvimento, teste, produção), evitando assim a necessidade de codificar essas configurações no código.

## documento padrão

Esta configuração se aplica apenas a aplicativos do Windows.

O documento padrão é a página web exibida na URL raiz do aplicativo Serviço de Aplicativo. Use o primeiro arquivo correspondente na lista. Se seu aplicativo usar um módulo que roteia com base na URL em vez de fornecer conteúdo estático, você não precisará usar um documento padrão.

## Mapeamento de caminho

### Mapeie caminhos de URL para diretórios

Por padrão, o Serviço de Aplicativo inicia o aplicativo no diretório raiz do código do aplicativo. Mas alguns frameworks web não iniciam no diretório raiz. Por exemplo, o Laravel começa no subdiretório público. Por exemplo, esse aplicativo estaria acessível em [http://contoso.com/public](http://contoso.com/public) , mas normalmente você precisaria direcionar [http://contoso.com](http://contoso.com/) para o diretório público. Se os arquivos de inicialização do seu aplicativo estiverem em uma pasta diferente ou se o repositório contiver vários aplicativos, você poderá editar ou adicionar aplicativos e diretórios virtuais.

### Configurar mapeamento de manipulador

Para aplicativos do Windows, você pode personalizar o mapeamento do manipulador do IIS e aplicativos e diretórios virtuais. Use o mapeamento de manipulador para adicionar manipuladores de script personalizados para lidar com solicitações de extensões de arquivo específicas.

# endereço IP de entrada e saída

[https://learn.microsoft.com/zh-cn/azure/app-service/overview-inbound-outbound-ips](https://learn.microsoft.com/zh-cn/azure/app-service/overview-inbound-outbound-ips)

No Azure App Service, os endereços IP de entrada e de saída estão relacionados com os endereços IP que a sua aplicação utiliza para comunicar com o mundo exterior. Estes endereços IP estão associados a instâncias específicas do Serviço de Aplicações e podem variar dependendo do tamanho e da configuração do Plano de Serviço de Aplicações.

## Endereço IP de entrada

[](https://github.com/rumia-san/az-204-notes/blob/master/note.md#%E5%85%A5%E7%AB%99-ip-%E5%9C%B0%E5%9D%80)

Conceito: O endereço IP de entrada é o endereço IP usado por solicitações externas para chegar ao seu aplicativo. Isso está relacionado principalmente às solicitações HTTP atendidas pelo aplicativo.

## Endereço IP de saída

Conceito: Um endereço IP de saída é o endereço IP que seu aplicativo usa para fazer solicitações de rede a serviços externos.

# Scale

## Scale automática

[https://learn.microsoft.com/zh-cn/azure/azure-monitor/autoscale/autoscale-get-started?toc=%2Fazure%2Fapp-service%2Ftoc.json](https://learn.microsoft.com/zh-cn/azure/azure-monitor/autoscale/autoscale-get-started?toc=%2Fazure%2Fapp-service%2Ftoc.json)

O Plano de Serviço de Aplicativo do Azure (Plano de Serviço de Aplicativo) fornece recursos de dimensionamento automático, permitindo que o serviço de aplicativo seja ajustado dinamicamente de acordo com a carga e a demanda do aplicativo. A seguir estão as etapas gerais para configurar o escalonamento automático do Plano de Serviço de Aplicativo:

Selecione um plano de Serviço de Aplicativo: Entre no portal do Azure e navegue até seu plano de Serviço de Aplicativo. Selecione “Zoom” no menu esquerdo.

Configurar regras de escalabilidade: na guia Escala, você pode configurar regras de escalabilidade automática. A configuração principal inclui:

Métrica: Selecione um ou mais indicadores de desempenho, como uso de CPU, uso de memória, número de solicitações, etc., como base para acionar o escalonamento automático. Operadores e Limites: Defina as condições que acionam o escalonamento. Por exemplo, você pode definir o uso da CPU para acionar o escalonamento quando exceder um determinado limite. Direção da escala: selecione Aumentar ou Aumentar a escala. Contagem de instâncias: especifica o número de instâncias que devem ser adicionadas ou removidas quando o dimensionamento é acionado. Configuração avançada (opcional): Na configuração avançada, você pode definir ainda mais o comportamento de escalonamento, como o período de resfriamento (Cooldown), que é o tempo de espera após a conclusão da última operação de escalonamento para evitar escalonamento frequente.

Salvar e Aplicar: Após configurar suas regras de dimensionamento, lembre-se de clicar em Salvar e, se necessário, em Aplicar para que as alterações tenham efeito.

# Stage Enviromnment

[https://learn.microsoft.com/zh-cn/azure/app-service/deploy-staging-slots?tabs=portal](https://learn.microsoft.com/zh-cn/azure/app-service/deploy-staging-slots?tabs=portal)

## Staging Environment

Um "ambiente de teste" é um ambiente específico durante o desenvolvimento e implantação de software usado para testes e verificação para garantir que novas versões de código ou aplicativo sejam estáveis e confiáveis antes de serem lançadas para produção. Os ambientes de teste geralmente são um estágio intermediário entre os ambientes de desenvolvimento e produção e possuem algumas características específicas:

Teste novos recursos: um ambiente de teste é onde novos recursos, códigos ou versões de aplicativos são testados. As equipes de desenvolvimento frequentemente simulam o ambiente de produção neste ambiente para garantir a correção e o desempenho dos novos recursos.

Teste de desempenho: O teste de desempenho é realizado em um ambiente de teste para garantir que o aplicativo ainda esteja funcionando corretamente sob condições reais de carga. Isso inclui testar o tempo de resposta, a taxa de transferência e a utilização de recursos do aplicativo.

Teste de regressão: O teste de regressão é realizado em um ambiente de teste para garantir que a introdução de novos recursos não interrompa a funcionalidade existente. Isso ajuda a detectar possíveis problemas que podem ser introduzidos em novas versões.

Teste de integração: teste todos os componentes juntos em um ambiente de teste para garantir que funcionem juntos sem conflitos ou problemas.

Semelhante a um ambiente de produção: os ambientes de teste normalmente são configurados para serem tão semelhantes quanto possível ao ambiente de produção, incluindo hardware, configuração de rede e outros parâmetros do ambiente. Isso ajuda a garantir que não surjam problemas inesperados ao mudar para um ambiente de produção.

Gerenciamento de versão: use o ambiente de teste para gerenciamento de versão para garantir que o código ou a versão do aplicativo implantado no ambiente de produção seja totalmente testado e verificado.

Implantação Azul-Verde: Às vezes, o ambiente de teste é usado para realizar a implantação Azul-Verde, alternando entre os dois ambientes para reduzir interrupções de serviço e garantir a implantação tranquila de novas versões.

Solução de problemas: se um problema for descoberto no ambiente de teste, a equipe poderá corrigi-lo e depurá-lo antes de impactar o ambiente de produção.

No geral, os ambientes de teste desempenham um papel fundamental no processo de desenvolvimento e implantação de software, ajudando as equipes a descobrir e resolver possíveis problemas antes de implantar novos recursos ou versões na produção.

## deployment slot

No Azure App Service, "Slot de Implantação" é um recurso que permite a implantação contínua e o gerenciamento de versão do aplicativo. O Slot de Implantação permite executar vários ambientes independentes (slots) na mesma instância do Serviço de Aplicativo do Azure, e cada slot pode conter diferentes versões do aplicativo.

A seguir estão alguns conceitos-chave do slot de implantação:

Slot Principal: Cada Serviço de Aplicativo do Azure possui um slot principal, que normalmente é usado para hospedar ambientes de produção. O que é executado em produção é a versão principal do seu aplicativo.

Slot de implantação: além do slot principal, você pode criar vários slots de implantação personalizados, cada um com configurações e definições independentes. Esses slots de implantação podem ser usados para diferentes fins, como teste, pré-lançamento, demonstração, etc.

Troca de ambiente: você pode trocar a versão do aplicativo no slot de implantação pela versão no slot principal, permitindo uma implantação sem tempo de inatividade. Dessa forma, você pode enviar novas versões do seu aplicativo para produção sem interromper o tráfego de produção.

Configuração independente: cada slot de implantação pode ter configuração de aplicativo independente, variáveis de ambiente, cadeias de conexão, etc. Isso permite testar configurações diferentes em slots diferentes sem afetar outros slots ou o ambiente de produção.

Implantação contínua: os slots de implantação são frequentemente usados em conjunto com fluxos de trabalho de integração contínua e implantação contínua (CI/CD). Você pode implantar automaticamente em um ou mais slots de implantação sempre que uma nova versão for criada e, em seguida, atualizar o ambiente de produção por meio da troca de ambiente.

Monitoramento de desempenho de aplicativos: Cada slot de implantação possui monitoramento independente de desempenho de aplicativos, que pode ajudá-lo a monitorar e analisar os indicadores de desempenho de cada ambiente.

Ao usar slots de implantação, você pode implantar e testar aplicativos de maneira mais segura e controlável, ao mesmo tempo que minimiza o impacto no ambiente de produção. Este é um recurso poderoso que é particularmente útil em processos modernos de desenvolvimento de aplicativos que exigem implantação e testes frequentes.

# Azure Functions

Semelhante ao aws lambda

[https://learn.microsoft.com/zh-cn/azure/azure-functions/functions-overview?pivots=programming-language-csharp](https://learn.microsoft.com/zh-cn/azure/azure-functions/functions-overview?pivots=programming-language-csharp)

## plano de hospedagem

[https://learn.microsoft.com/en-us/azure/azure-functions/functions-scale](https://learn.microsoft.com/en-us/azure/azure-functions/functions-scale)

### Plano de consumo

Dimensione automaticamente e pague apenas pelos recursos de computação quando suas funções estiverem em execução.

No plano de Consumo, as instâncias do host de Funções são adicionadas e removidas dinamicamente com base no número de eventos recebidos.

✔ Plano de hospedagem padrão. ✔ Pague somente quando suas funções estiverem em execução. ✔ Balança automaticamente, mesmo em períodos de alta carga.

### Plano premium

Escalona automaticamente com base na demanda usando trabalhadores pré-aquecidos, que executam aplicativos sem demora após ficarem inativos, são executados em instâncias mais poderosas e se conectam a redes virtuais.

Considere o plano Azure Functions Premium nas seguintes situações:

✔ Seus aplicativos de funções são executados continuamente ou quase continuamente. ✔ Você tem um número alto de pequenas execuções e uma conta de execução alta, mas poucos GB de segundos no plano de Consumo. ✔ Você precisa de mais opções de CPU ou memória do que as fornecidas pelo plano de Consumo. ✔ Seu código precisa ser executado por mais tempo que o tempo máximo de execução permitido no plano de Consumo. ✔ Você precisa de recursos que não estão disponíveis no plano de Consumo, como conectividade de rede virtual. ✔ Você deseja fornecer uma imagem Linux personalizada na qual executar suas funções.

### Plano dedicado

Execute as suas funções dentro de um plano do Serviço de Aplicações com tarifas normais do plano do Serviço de Aplicações.

Melhor para cenários de longa duração onde as Funções Duradouras não podem ser usadas. Considere um plano de Serviço de Aplicativo nas seguintes situações:

✔ Você tem VMs existentes e subutilizadas que já estão executando outras instâncias do Serviço de Aplicativo. ✔ São necessários dimensionamento e custos preditivos.

[https://learn.microsoft.com/zh-cn/azure/azure-functions/functions-triggers-bindings?tabs=isolated-process%2Cpython-v2&amp;pivots=programming-language-csharp](https://learn.microsoft.com/zh-cn/azure/azure-functions/functions-triggers-bindings?tabs=isolated-process%2Cpython-v2&pivots=programming-language-csharp)

## trigger and binding

[https://learn.microsoft.com/zh-cn/azure/azure-functions/functions-triggers-bindings?tabs=isolated-process%2Cpython-v2&amp;pivots=programming-language-csharp](https://learn.microsoft.com/zh-cn/azure/azure-functions/functions-triggers-bindings?tabs=isolated-process%2Cpython-v2&pivots=programming-language-csharp)

Os gatilhos fazem com que as funções sejam executadas. Os gatilhos definem como uma função é chamada e uma função deve ter exatamente um gatilho. Os gatilhos têm dados associados, que normalmente são fornecidos como a carga útil de uma função.

A vinculação a uma função é uma forma de conectar declarativamente outro recurso à função; as vinculações podem estar na forma de vinculações de entrada, vinculações de saída ou ambas. Os dados na ligação são fornecidos à função como parâmetros.

Misture e combine diferentes encadernações conforme necessário. As ligações são opcionais, uma função pode ter uma ou mais ligações de entrada e/ou ligações de saída.

Use gatilhos e ligações para evitar acesso codificado a outros serviços. As funções recebem dados (por exemplo, conteúdo de mensagens da fila) em parâmetros de função. Use o valor de retorno da função para enviar dados (por exemplo, para criar uma mensagem de fila).

## Padrão nº 1: encadeamento de funções

No modo de encadeamento de funções, uma série de funções são executadas em uma ordem específica. Neste modo, a saída de uma função é aplicada à entrada de outra função. O uso de filas entre cada função garante que o sistema permaneça durável e escalável, mesmo que haja fluxo de controle de uma função para outra.

## Padrão #2: Fan out/fan in

No modo fan-out/fan-in, múltiplas funções são executadas em paralelo e depois aguardam a conclusão de todas as funções. Normalmente, alguma operação de agregação é executada nos resultados retornados por essas funções.

## Padrão nº 3: APIs HTTP assíncronas

[](https://github.com/rumia-san/az-204-notes/blob/master/note.md#pattern-3-async-http-apis)

O padrão API HTTP assíncrono resolve os problemas que surgem ao usar um cliente externo para coordenar o estado de operações de longa duração. Uma maneira comum de implementar esse padrão é fazer com que o endpoint HTTP acione uma operação de longa duração. O cliente é então redirecionado para um endpoint de status que o cliente pode pesquisar para saber quando a operação for concluída.

As Funções Duráveis oferecem suporte nativo a esse padrão, o que pode simplificar ou até mesmo eliminar o código que você precisa escrever para interagir com execuções de funções de longa duração. Por exemplo, os exemplos de início rápido de Funções Duráveis (C#, JavaScript, TypeScript, Python, PowerShell e Java) demonstram comandos REST simples que podem ser usados para iniciar uma nova instância de função do orquestrador. Depois de iniciar uma instância, a extensão expõe uma API Webhook HTTP para consultar o status das funções do orquestrador.

## Padrão #4: Monitor

O modo de monitoramento refere-se a um processo flexível e recorrente em um fluxo de trabalho. Por exemplo, pesquise até que uma condição específica seja atendida. Cenários simples, como trabalhos de limpeza periódicos, podem ser resolvidos usando gatilhos de timer regulares, mas os intervalos para esse cenário são estáticos e o gerenciamento do tempo de vida da instância torna-se complexo. Você pode usar funções duráveis para criar intervalos de recorrência flexíveis, gerenciar tempos de vida de tarefas e criar vários processos de monitoramento a partir de um único processo de negócios.

Um exemplo de modo de observação é a inversão do cenário da API HTTP assíncrona descrito anteriormente. O modo de observação não expõe um ponto final para clientes externos monitorizarem operações de longa duração. Em vez disso, o monitor de longa duração consome o ponto final externo e, em seguida, espera que um estado mude.

Você pode usar funções duráveis para criar vários monitores para monitorar qualquer endpoint escrevendo apenas algumas linhas de código. Um monitor pode encerrar a execução quando uma determinada condição for atendida ou outra função pode encerrar o monitor usando um cliente de orquestração persistente. O intervalo de espera do monitor pode ser alterado com base em condições específicas (como espera exponencial).

## Padrão #5: Interação humana

Muitos processos automatizados envolvem algum tipo de interação humano-computador. A interação homem-máquina envolvida no processo de automação é complicada porque os humanos não estão tão disponíveis e responsivos quanto os serviços em nuvem. Processos automatizados permitem o uso de timeouts e lógica de compensação para implementar essa interação.

O processo de aprovação é um exemplo de processo de negócios que envolve interação humano-computador. Por exemplo, um relatório de despesas acima de um determinado valor requer a aprovação do gestor. Se o gerente não aprovar o relatório de despesas dentro de 72 horas (o gerente pode estar de férias), um processo de escalonamento será iniciado para que outra pessoa (talvez o gerente do gerente) possa aprová-lo.

## Padrão #6:  Aggregator (entidades com estado)

O sexto padrão envolve a agregação de dados de eventos ao longo do tempo em uma única entidade endereçável. Neste modelo, os dados a serem agregados podem vir de múltiplas fontes, ser entregues em lotes ou distribuídos por um longo período de tempo. O agregador pode precisar agir sobre os dados do evento à medida que chegam, e os clientes externos podem precisar consultar os dados agregados.

O complicado de tentar implementar esse padrão usando funções simples sem estado é que o controle de simultaneidade se torna um enorme desafio. Você não só precisa considerar que vários threads modificarão os mesmos dados ao mesmo tempo, mas também precisa considerar como garantir que o agregador seja executado apenas em uma VM por vez.

Este padrão pode ser facilmente implementado como uma função única usando entidades persistentes.

[](https://github.com/rumia-san/az-204-notes/blob/master/note.md#blob-storage)

# Blob Storage

[https://learn.microsoft.com/zh-cn/azure/storage/blobs/storage-blobs-introduction](https://learn.microsoft.com/zh-cn/azure/storage/blobs/storage-blobs-introduction)

Azure Blob Storage é uma solução de armazenamento de objetos para a nuvem da Microsoft. O armazenamento de blobs é mais adequado para armazenar grandes quantidades de dados não estruturados. Dados não estruturados são dados (como texto ou dados binários) que não seguem um modelo ou definição de dados específica.

Contêiner de conta de armazenamento no blob de conta de armazenamento no contêiner

As contas de armazenamento fornecem um namespace exclusivo para dados no Azure. Cada objeto armazenado no Azure Armazenamento tem um endereço que contém um nome de conta exclusivo. A combinação do nome da conta e do ponto final de armazenamento de blobs forma o endereço base dos objetos na conta de armazenamento.

Por exemplo, se a conta de armazenamento se chamar mystorageaccount, o ponto final padrão para armazenamento Blob será: [http://mystorageaccount.blob.core.windows.net](http://mystorageaccount.blob.core.windows.net/)

Um contêiner organiza um conjunto de blobs, semelhante aos diretórios de um sistema de arquivos. Uma conta de armazenamento pode conter um número ilimitado de contêineres e um contêiner pode armazenar um número ilimitado de blobs.

## Tipo de blob

O Armazenamento do Azure dá suporte a três tipos de blobs:

* Block Blobs armazenam texto e dados binários. Block Blobs consistem em blocos de dados que podem ser gerenciados separadamente. Os blobs de blocos podem armazenar até aproximadamente 190,7 TiB.
* Assim como os blobs de blocos, os blobs de acréscimo são feitos de blocos, mas são otimizados para operações de acréscimo. Anexar blobs é ideal para cenários como registrar dados de uma máquina virtual.
* Page Blobs são usados para armazenar arquivos de acesso aleatório de até 8 TiB. Os blobs de páginas armazenam arquivos de disco rígido virtual (VHD) e atuam como discos para máquinas virtuais do Azure. Para obter mais informações sobre blobs de páginas, consulte visão geral dos blobs de páginas do Azure

## Redundância

[https://learn.microsoft.com/zh-cn/azure/storage/common/storage-redundancy#locally-redundant-storage](https://learn.microsoft.com/zh-cn/azure/storage/common/storage-redundancy#locally-redundant-storage)

* O armazenamento localmente redundante (LRS) replica dados de forma síncrona três vezes em um único local físico em uma região primária. LRS é a opção de replicação de menor custo, mas não é recomendada para aplicativos que exigem alta disponibilidade ou persistência.
* O Zone Redundant Storage (ZRS) replica dados de forma síncrona em três zonas de disponibilidade do Azure em uma região primária. Para aplicativos que exigem alta disponibilidade, a Microsoft recomenda usar o ZRS na região primária e replicar para a região secundária.
* Armazenamento com redundância geográfica O armazenamento com redundância geográfica (GRS) usa LRS para replicar dados de forma síncrona três vezes em um único local físico em uma região primária. Em seguida, ele replica os dados de forma assíncrona para um único local físico em uma região secundária a centenas de quilômetros de distância da região primária. O GRS fornece durabilidade de recursos de armazenamento de pelo menos 99,99999999999999% (16 noves) ao longo de um ano.
* Armazenamento com redundância de zona geográfica O armazenamento com redundância de zona geográfica (GZRS) combina a alta disponibilidade fornecida por zonas de disponibilidade redundantes com a proteção contra interrupções de zona fornecida pela replicação geográfica. Os dados na conta de armazenamento GZRS serão replicados em três Zonas de Disponibilidade do Azure na região primária e em regiões geográficas secundárias para proteção contra desastres regionais. A Microsoft recomenda o uso do GZRS para aplicativos que exigem consistência, durabilidade e disponibilidade máximas, excelente desempenho e resiliência de recuperação de desastres.
* Quando RA-GRS ou RA-GZRS está ativado, a região secundária fica disponível para acesso de leitura, para que você possa pré-testar seu aplicativo para garantir que os dados possam ser lidos corretamente da região secundária no caso de uma interrupção do serviço.

## nível de acesso

[https://learn.microsoft.com/zh-cn/azure/storage/blobs/access-tiers-online-manage?tabs=azure-portal](https://learn.microsoft.com/zh-cn/azure/storage/blobs/access-tiers-online-manage?tabs=azure-portal)

### Hot Access Tier

Finalidade: Adequado para dados acessados com frequência, como dados que são lidos ou gravados com frequência. Custo: o Hot Access Tier tem custos de armazenamento mais elevados, mas operações de leitura e gravação mais baixas. Custo de acesso: Aplica-se a operações frequentes de leitura e gravação.

### Cool Access Tier

Finalidade: Adequado para dados acessados com menos frequência que precisam ser armazenados no armazenamento de Blobs do Azure, mas são acessados com pouca frequência. Custo: Os custos de armazenamento para Cool Access Tier são relativamente baixos, mas as operações de leitura e gravação são mais caras. Custo de acesso: aplica-se a dados que são acessados com pouca frequência, mas precisam ser retidos no armazenamento de Blobs do Azure.

### Archive Access Tier

Finalidade: Adequado para dados que raramente são acessados e precisam ser retidos por muito tempo com custos de armazenamento muito baixos. Custo: Archive Access Tier oferece os custos de armazenamento mais baixos, mas as operações de leitura são mais caras. Custo de acesso: Adequado para dados com requisitos de armazenamento muito baixos e quase sem necessidade de leitura.

## Gerenciamento do ciclo de vida

[https://learn.microsoft.com/zh-cn/azure/storage/blobs/lifecycle-management-policy-configure?tabs=azure-portal](https://learn.microsoft.com/zh-cn/azure/storage/blobs/lifecycle-management-policy-configure?tabs=azure-portal)

O Azure Storage Lifecycle Management fornece políticas baseadas em regras para mover dados de blob para o nível de acesso mais apropriado ou dados expirados no final do seu ciclo de vida. As políticas de ciclo de vida atuam no blob subjacente e podem, opcionalmente, atuar em versões ou instantâneos do blob. Para obter mais informações sobre estratégias de gerenciamento do ciclo de vida, consulte Otimizar custos gerenciando automaticamente o ciclo de vida dos dados.

Uma política de gerenciamento do ciclo de vida consiste em uma ou mais regras que definem um conjunto de ações que precisam ser executadas com base nas condições que precisam ser atendidas. Para o blob base, você pode optar por verificar uma das seguintes condições:

O número de dias desde que o blob foi criado. O número de dias desde a última modificação do blob. O número de dias desde que o blob foi acessado pela última vez. Para usar esta condição em uma ação, você deve primeiro habilitar o rastreamento do horário do último acesso (opcional). Quando a condição selecionada for verdadeira, a política de gerenciamento executa a ação especificada. Por exemplo, se você definiu uma operação para mover um blob que não foi modificado por 30 dias da camada quente para a camada fria, a política de gerenciamento do ciclo de vida moverá o blob após 30 dias desde a última gravação no blob .

Para instantâneos ou versões de blob, a condição a ser verificada é o número de dias desde que o instantâneo ou versão foi criado.

# Cosmos DB

O Azure Cosmos DB é um banco de dados relacional e NoSQL totalmente gerenciado, adequado para o desenvolvimento de aplicativos modernos, incluindo o desenvolvimento de IA, comércio digital, IoT, gerenciamento de reservas e outros tipos de soluções. O Azure Cosmos DB oferece tempos de resposta de milissegundos de um dígito, escalabilidade automática e instantânea e velocidade garantida em qualquer escala. A disponibilidade apoiada por SLA e a segurança de nível empresarial garantem a continuidade dos negócios.

O desenvolvimento de aplicativos é mais rápido e eficiente devido a:

* Fornecendo distribuição de dados multirregional pronta para uso em qualquer lugar do mundo
* API de código aberto
* SDKs para linguagens comumente usadas.
* Usado para dar suporte ao aumento de recuperação de recursos de banco de dados de IA gerados, como pesquisa de vetores nativos ou integração perfeita com serviços de IA do Azure

Como um serviço totalmente gerido, o Azure Cosmos DB utiliza gestão automatizada, atualizações e patches para que não tenha de fazer administração de base de dados. Ele também lida com o gerenciamento de capacidade com opções econômicas sem servidor e de escalonamento automático que respondem às demandas dos aplicativos, combinando a capacidade com a demanda.

## Níveis de consistência

[https://learn.microsoft.com/en-us/azure/cosmos-db/consistency-levels](https://learn.microsoft.com/en-us/azure/cosmos-db/consistency-levels)

A maioria dos bancos de dados NoSQL distribuídos comerciais atualmente no mercado só podem fornecer consistência muito consistente e eventual. O Azure Cosmos DB oferece cinco níveis bem definidos. Do mais forte ao mais fraco, os níveis são:

* Forte
* Obsolescência limitada
* Sessão
* Prefixo consistente
* Eventual

Quanto mais abaixo, maior a disponibilidade, mas a consistência é fraca. Quanto mais acima, mais forte é a consistência.

## API

[https://learn.microsoft.com/en-us/azure/cosmos-db/choose-api](https://learn.microsoft.com/en-us/azure/cosmos-db/choose-api)

O Azure Cosmos DB oferece várias APIs de banco de dados, que incluem NoSQL, MongoDB, PostgreSQL, Cassandra, Gremlin e Table.

## Solicitar Unidades

Uma leitura de ponto (busca de um único item por ID e valor de chave de partição) de um item de 1 KB custa 1 unidade de solicitação (ou 1 RU). Todas as outras operações de banco de dados recebem custos de RU de maneira semelhante. Independentemente da API que utiliza para interagir com o seu contentor DB do Azure Cosmos, a RU mede o custo real da utilização dessa API. Independentemente de a operação da base de dados ser uma escrita, uma leitura pontual ou uma consulta, o custo é sempre medido em RUs.

## partição

[https://learn.microsoft.com/en-us/azure/cosmos-db/partitioning-overview](https://learn.microsoft.com/en-us/azure/cosmos-db/partitioning-overview)

No Azure Cosmos DB, a partição é um conceito utilizado para expansão horizontal e armazenamento distribuído. O Cosmos DB usa particionamento para armazenar e gerenciar dados para garantir alto rendimento, baixa latência e escalabilidade.

Conceitos-chave do particionamento do Cosmos DB:

Chave de partição: todo documento possui um atributo chamado chave de partição. A chave de partição determina em qual partição do Cosmos DB o documento será colocado. A escolha da chave de partição é importante porque afeta diretamente a distribuição dos dados e o desempenho da consulta.

Partição lógica: Documentos com a mesma chave de partição são chamados de partições lógicas. Os documentos em partições lógicas partilham a mesma partição física. As chaves de partição devem ser escolhidas para fornecer distribuição uniforme de dados para evitar que certas partições se tornem pontos de acesso, afetando o desempenho.

Partições físicas: o Cosmos DB distribui dados em várias partições físicas para obter escalabilidade horizontal. As partições físicas são a estrutura subjacente usada pelo Cosmos DB para distribuir e gerenciar dados.

Consultas entre partições: o Cosmos DB oferece a capacidade de realizar consultas paralelas em múltiplas partições. A escolha da chave de partição é crítica para o desempenho da consulta. A seleção adequada de chaves de partição pode minimizar a necessidade de consultas entre partições. Ao escolher uma chave de partição adequada, você pode obter uma distribuição uniforme de dados, evitar pontos de acesso e obter a escalabilidade horizontal do Cosmos DB. A escolha da chave de partição deve ser otimizada com base nos padrões de consulta e de acesso a dados do seu aplicativo para garantir o desempenho ideal. Deve-se observar que não é fácil alterar a chave de partição durante o ciclo de vida de um aplicativo, portanto, é necessária uma consideração cuidadosa durante o design.

# Azure Resource Manager

[https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview)

O Azure Resource Manager é o serviço de implementação e gestão do Azure. Fornece uma camada de gestão que lhe permite criar, atualizar e eliminar recursos na sua conta Azure. Você usa recursos de gerenciamento, como controle de acesso, bloqueios e tags, para proteger e organizar seus recursos após a implantação.

Azure Resource Manager (ARM) é um serviço gerenciado no Microsoft Azure para gerenciar e organizar recursos em nuvem. O ARM fornece uma forma unificada de implementar, gerir e monitorizar os recursos do Azure, permitindo aos utilizadores definir e implementar soluções de nuvem complexas de forma consistente.

Na AWS, a contrapartida de serviço do Azure Resource Manager (ARM) é o AWS CloudFormation. Ambos os serviços são ferramentas fornecidas por provedores de serviços em nuvem para simplificar e automatizar a definição, implantação e gerenciamento de infraestrutura.

* recurso - um item gerenciável disponível por meio do Azure. Exemplos de recursos incluem máquinas virtuais, contas de armazenamento, aplicativos Web, bancos de dados e redes virtuais. Grupos de recursos, subscrições, grupos de gestão e etiquetas também são exemplos de recursos.
* grupo de recursos – Um contêiner que contém recursos relacionados a uma solução do Azure. Os grupos de recursos incluem os recursos que você deseja gerenciar como um grupo. Decida quais recursos pertencem a qual grupo de recursos com base no que é melhor para sua organização.
* provedor de recursos – um serviço que fornece recursos do Azure. Por exemplo, Microsoft.Compute é um provedor de recursos comum que fornece recursos de máquinas virtuais. Microsoft.Storage também é um provedor de recursos comum.
* sintaxe declarativa - Uma sintaxe que permite afirmar "Aqui está o projeto que quero criar" sem ter que escrever uma série de comandos de programação para criá-lo. Modelos ARM e arquivos Bicep são exemplos de sintaxe declarativa. Nestes ficheiros, pode definir as propriedades da infraestrutura a implantar no Azure.
* Modelo ARM - Um arquivo JavaScript Object Notation (JSON) que define um ou mais recursos a serem implantados em um grupo de recursos, assinatura, grupo de gerenciamento ou locatário. Use modelos para implantar recursos de maneira consistente repetidamente. Consulte Visão geral da implantação do modelo.
* Arquivo Bicep – Um arquivo que implanta recursos do Azure de forma declarativa. Bicep é uma linguagem projetada para fornecer a melhor experiência de autoria para soluções de infraestrutura como código no Azure. Consulte Visão geral do bíceps.

# Registro de Contêiner do Azure (ACR) -Azure Container Registry

[https://learn.microsoft.com/en-us/azure/container-registry/](https://learn.microsoft.com/en-us/azure/container-registry/)

O Registo de Contentores do Azure permite-lhe construir, armazenar e gerir imagens e artefactos de contentores num registo privado para todos os tipos de implementações de contentores.

# Instâncias de Contêiner do Azure (ACI) -Azure Container Instances

[https://learn.microsoft.com/en-us/azure/container-instances/](https://learn.microsoft.com/en-us/azure/container-instances/)

## Grupos de contêineres - Container groups

[https://learn.microsoft.com/zh-cn/azure/container-instances/container-instances-container-groups?source=recommendations](https://learn.microsoft.com/zh-cn/azure/container-instances/container-instances-container-groups?source=recommendations)

Um grupo de contêineres é uma coleção de contêineres organizados no mesmo host. Os contêineres em um grupo de contêineres compartilham ciclo de vida, recursos, rede local e volumes de armazenamento. É semelhante ao conceito de Pod no Kubernetes.

# Plataforma de identidade - Identity Platform

[https://learn.microsoft.com/zh-cn/entra/identity-platform/v2-overview](https://learn.microsoft.com/zh-cn/entra/identity-platform/v2-overview)

A Plataforma de Identidade do Azure é um conjunto de serviços de autenticação e autorização fornecidos pelo Azure para a construção de soluções seguras de autenticação e controle de acesso na nuvem. Ele fornece uma variedade de ferramentas de autenticação e gerenciamento de identidade para atender às necessidades de segurança de desenvolvedores e organizações.

Azure Active Directory (Azure AD): O Azure AD é o núcleo dos serviços de autenticação e autorização do Azure. É um serviço de identidade em nuvem para gerenciar e proteger informações de identidade, suportando modelos de implantação multilocatário, monolocatário e híbrido.

ADAL é a abreviatura de Biblioteca de Autenticação do Azure Active Directory. É um conjunto de bibliotecas para implementação de autenticação em aplicações, projetadas especificamente para integração com Azure Active Directory (Azure AD). ADAL fornece bibliotecas clientes que os desenvolvedores podem usar em uma variedade de plataformas e linguagens de programação para autenticar e obter tokens de acesso em seus aplicativos.

## Registre um aplicativo

"Registrar um aplicativo" significa registrar um aplicativo no Azure Active Directory (Azure AD). Este processo envolve a criação de uma identidade para a aplicação para que esta possa integrar-se com o Azure AD e obter as credenciais de autenticação e autorização necessárias. Registar a sua aplicação no Azure AD é um passo crítico para ligar a sua aplicação ao Azure AD e obter acesso aos recursos.

[https://learn.microsoft.com/en-us/entra/identity-platform/application-model](https://learn.microsoft.com/en-us/entra/identity-platform/application-model)

Para que o provedor de identidade saiba que um usuário tem acesso a um aplicativo específico, tanto o usuário quanto o aplicativo devem estar registrados no provedor de identidade. Ao registrar um aplicativo com o Microsoft Entra ID, você precisa fornecer a configuração de identidade do aplicativo para que ele possa ser integrado à plataforma de identidade da Microsoft.

## Diretores de serviço

Na AWS, os conceitos correspondentes aos princípios de serviço no Azure são principalmente usuários IAM e funções IAM.

[https://learn.microsoft.com/zh-cn/entra/identity-platform/app-objects-and-service-principals?tabs=browser](https://learn.microsoft.com/zh-cn/entra/identity-platform/app-objects-and-service-principals?tabs=browser)

No Azure Ative Directory (Azure AD), um Diretor de Serviço é uma identidade de segurança usada para representar uma aplicação em cenários de autenticação não interativos. É a identidade de um aplicativo (ou serviço) no Azure AD que permite que o aplicativo seja autenticado e autorizado com recursos do Azure sem o envolvimento direto do usuário.

Ao registar/atualizar uma aplicação, tanto o objeto de aplicação como o objeto principal de serviço correspondente são criados/atualizados para o inquilino. O objeto de aplicativo define a configuração de identidade do aplicativo globalmente (em todos os locatários aos quais o aplicativo associado recebeu acesso) e pode ser usado como modelo para derivar seu objeto principal de serviço correspondente para uso local em tempo de execução (em locatário específico).

# Microsoft Graph

O Microsoft Graph é um ponto de extremidade de API unificado para um conjunto de serviços do Microsoft 365 que permite aos desenvolvedores acessar e interagir com vários serviços e dados no Microsoft 365 de maneira consistente. O Microsoft Graph fornece acesso a recursos como usuários, organizações, emails, calendários, arquivos, tarefas e suporte para muitos outros serviços do Microsoft 365.

# Azure Key Vault

Azure Key Vault é um serviço gerenciado no Microsoft Azure para armazenar e gerenciar com segurança informações confidenciais, como senhas, chaves, certificados e muito mais. O Azure Key Vault fornece uma maneira segura para aplicativos e serviços acessarem esses dados confidenciais sem armazená-los diretamente. Isso ajuda a melhorar a segurança e reduz o risco de uso indevido e vazamento de informações confidenciais.

# Gerenciamento de API do Azure - Azure API Management

O Azure API Management é um serviço gerenciado fornecido pelo Microsoft Azure para simplificar e gerenciar centralmente a criação, publicação, manutenção e proteção de APIs. Através do API Management, os desenvolvedores podem criar, implantar e monitorar APIs com mais facilidade e garantir sua disponibilidade, segurança e escalabilidade.

Aqui estão alguns dos principais recursos e capacidades do Azure API Management:

Criação e design de API: forneça ferramentas de design de API que possam definir a estrutura da API, os formatos de solicitação e resposta e realizar o controle de versão da API.

Liberação e gerenciamento de APIs: gerencie o ciclo de vida das APIs, incluindo criação, lançamento, controle de versão e descontinuação. Várias versões de APIs podem ser publicadas simultaneamente e metadados detalhados são fornecidos para cada API.

Segurança e Autorização: Fornece recursos de controle de acesso e autenticação para a API. Suporta protocolos padrão de autenticação e autorização, como OAuth e JWT. As políticas de acesso para APIs podem ser definidas para garantir que apenas aplicativos e usuários autorizados possam acessar a API.

Desempenho e escalabilidade: fornece recursos de desempenho e escalabilidade, como cache, limitação de corrente e balanceamento de carga, para garantir que a API possa lidar com alto tráfego e solicitações em grande escala.

Análise e monitoramento: fornece recursos de monitoramento, análise e relatórios em tempo real para entender o uso, o desempenho e os problemas da API. Pode integrar ferramentas como Azure Monitor e Application Insights.

Portal do desenvolvedor: fornece um portal do desenvolvedor que permite que os desenvolvedores se registrem, aprendam sobre a API, obtenham tokens de acesso, visualizem a documentação e testem.

Transformação e integração de API: oferece suporte à transformação de solicitações e respostas no gerenciamento de API, incluindo mapeamento, reescrita e transcodificação. Pode ser integrado com Azure Functions, Logic Apps e outros serviços.

Controle de versão de API: Fornece funcionalidade de controle de versão, permitindo suporte para múltiplas versões de API ao mesmo tempo, garantindo compatibilidade retroativa com clientes existentes.

Suporte a padrões abertos: Suporta padrões de API abertos, como OpenAPI (Swagger) e WSDL para integração e interação mais fáceis.

O Gerenciamento de API do Azure é parte integrante da criação e do gerenciamento de aplicativos modernos, especialmente em arquiteturas de microsserviços, desenvolvimento nativo da nuvem e integração de API em diversas plataformas. Ao usar o API Management, as organizações podem controlar e otimizar melhor seu ecossistema de API.

# Azure Event Grid

Na AWS, a contrapartida de serviço do Azure Event Grid é o Amazon EventBridge

[https://learn.microsoft.com/en-us/azure/event-grid/overview](https://learn.microsoft.com/en-us/azure/event-grid/overview)

Azure Event Grid é um serviço de processamento de eventos na plataforma de nuvem Azure que é usado para simplificar e unificar a forma como os eventos são processados. Ele fornece um sistema de eventos extensível baseado em modelo de publicação/assinatura que permite que vários serviços do Azure, serviços de terceiros e aplicativos personalizados publiquem, processem e assinem eventos à medida que eles ocorrem.

## Filtragem de tipo de evento -Event type filtering

[https://learn.microsoft.com/en-us/azure/event-grid/namespace-event-filtering](https://learn.microsoft.com/en-us/azure/event-grid/namespace-event-filtering)

Por padrão, todos os tipos de eventos da origem do evento são enviados ao terminal. Você pode decidir enviar apenas determinados tipos de eventos para o endpoint. Por exemplo, você pode receber notificações sobre atualizações de recursos, mas não sobre outras operações, como exclusões. Nesse caso, filtre pelo tipo de evento Microsoft.Resources.ResourceWriteSuccess. Forneça uma matriz contendo tipos de eventos ou especifique All para obter todos os tipos de eventos para a origem do evento.

## domínio de evento

[https://learn.microsoft.com/zh-cn/azure/event-grid/event-domains?tabs=event-grid-event-schema](https://learn.microsoft.com/zh-cn/azure/event-grid/event-domains?tabs=event-grid-event-schema)

[](https://github.com/rumia-san/az-204-notes/blob/master/note.md#azure-event-hubs)

# Azure Event Hubs

Na AWS, a contrapartida de serviço do Azure Event Hubs é o Amazon Kinesis.

[https://learn.microsoft.com/zh-cn/azure/event-hubs/event-hubs-features](https://learn.microsoft.com/zh-cn/azure/event-hubs/event-hubs-features)

O Azure Event Hubs é uma plataforma de streaming de dados em grande escala e em tempo real para ingestão e processamento de grandes quantidades de dados de eventos. É um serviço gerenciado no Azure que é particularmente útil para a construção de aplicativos de processamento de eventos em tempo real em grande escala e alto rendimento.

## partição - partition


Nos Hubs de Eventos do Azure, "Partição" é um conceito chave. As partições são a unidade básica do fluxo de dados dos Event Hubs e são usadas para alcançar o dimensionamento horizontal e melhorar a simultaneidade. Cada Hub de Eventos pode ter várias partições e cada partição é um fluxo de eventos ordenado e independente.

## capturar - capture


Usando a captura de Hubs de Eventos, você pode capturar automaticamente dados de streaming do hub de eventos e salvá-los em uma conta de armazenamento de Blobs selecionada ou em uma conta de armazenamento do Azure Data Lake. Você pode habilitar a captura no portal do Azure e especificar um tamanho máximo e um intervalo de tempo para realizar a captura. Utilizando a captura de Event Hubs, os utilizadores podem especificar a sua própria conta e contentor de armazenamento Azure Blob ou conta de armazenamento Azure Data Lake (uma das quais é usada para armazenar os dados capturados). Os dados capturados são gravados no formato Apache Avro.

# Barramento de serviço do Azure - Azure Service Bus


O Azure Service Bus é um serviço de mensagens nativo da nuvem fornecido pelo Azure para comunicação assíncrona confiável em aplicativos distribuídos. Ele oferece suporte a vários modos de mensagens, incluindo Filas e Tópicos, para entregar mensagens entre aplicativos, serviços e sistemas.

Na AWS, os serviços que correspondem ao Azure Service Bus são Amazon Simple Queue Service (SQS) e Amazon Simple Notification Service (SNS).

## Comparativo


A Azure Event Grid e o Azure Service Bus são dois serviços de processamento de eventos diferentes e têm algumas diferenças significativas no design e na utilização. Aqui estão suas principais diferenças:

Modelo de publicação/assinatura versus comunicação ponto a ponto:

Grade de Eventos do Azure: fornece um modelo de publicação/assinatura onde as fontes de eventos podem publicar eventos e os assinantes podem optar por assinar tipos de eventos de interesse. Oferece suporte a uma ampla variedade de serviços do Azure, serviços de terceiros e aplicativos personalizados como fontes de eventos. Azure Service Bus: Inclui dois modelos: fila e tópico. A fila utiliza um modelo de comunicação ponto a ponto, em que cada mensagem só pode ser processada por um receptor. Os tópicos usam um modelo de publicação/assinatura para oferecer suporte a vários assinantes que assinam mensagens de forma independente. Tipos e estrutura de eventos:

Grade de Eventos do Azure: Muito adequada para lidar com cenários com tipos de eventos relativamente simples, como alterações de recursos, alterações de status do sistema, etc. Os eventos podem ser quaisquer objetos JSON. Azure Service Bus: Mais adequado para processar mensagens estruturadas e lógica de negócios complexa. As mensagens podem estar em formato XML, JSON ou binário. Método de tratamento de eventos:

Grade de Eventos do Azure: o processamento de eventos é assíncrono e oferece suporte a WebHook, Azure Functions, aplicativos lógicos, etc. Barramento de Serviço do Azure: dá suporte à recepção síncrona de mensagens e ao processamento assíncrono de mensagens, como por meio de funções de processamento de mensagens (Manipulador de Mensagens). Serviços alvo:

Grade de Eventos do Azure: usada principalmente em cenários nativos da nuvem, oferece suporte a uma ampla gama de integração de serviços do Azure e também pode ser integrada a aplicativos personalizados e serviços de terceiros. Barramento de Serviço do Azure: adequado para vários cenários de integração empresarial e comunicação de aplicativos e pode ser integrado a aplicativos de diferentes pilhas de tecnologia. Período de atraso e retenção:

Grade de Eventos do Azure: fornece entrega de eventos de baixa latência sem período de retenção explícito para eventos. Barramento de serviço do Azure: oferece menor latência e suporta a configuração do período de retenção de mensagens. As mensagens são retidas na fila por um tempo limitado. Ambiente alvo:

Grade de Eventos do Azure: para criar aplicativos e arquiteturas de microsserviços modernos e orientados a eventos. Barramento de Serviço do Azure: adequado para integração empresarial tradicional, enfileiramento de mensagens e cenários de comunicação confiáveis. A escolha de utilizar a Azure Event Grid ou o Azure Service Bus depende das suas necessidades específicas e cenários de utilização. Se precisar de lidar com um grande número de eventos simples e construir um sistema fracamente acoplado, considere usar a Azure Event Grid. Se precisar de mais padrões de mensagens e processamento estruturado de mensagens, você poderá escolher o Azure Service Bus.

# Armazenamento de filas do Azure - Azure Queue Storage


[https://learn.microsoft.com/zh-cn/azure/storage/queues/storage-queues-introduction](https://learn.microsoft.com/zh-cn/azure/storage/queues/storage-queues-introduction)

O Azure Queue Storage é um serviço que pode armazenar grandes quantidades de mensagens. As mensagens podem ser acessadas de qualquer lugar do mundo por meio de chamadas autenticadas usando HTTP ou HTTPS. O tamanho da mensagem da fila pode ser de até 64 KB. Uma fila pode conter milhões de mensagens, até ao limite de capacidade total da conta de armazenamento. As filas são frequentemente usadas para criar um backlog de trabalho a ser processado de forma assíncrona, como no estilo arquitetônico Web-Queue-Worker.

Na AWS, a contrapartida de serviço do Azure Queue Storage é o Amazon Simple Queue Service (SQS). O Amazon SQS é um serviço gerenciado de enfileiramento de mensagens que permite mensagens assíncronas e confiáveis entre componentes distribuídos e microsserviços.

Formato de URL: a fila pode ser endereçada usando o seguinte formato de URL:

https://.queue.core.windows.net/

Uma fila no diagrama pode ser acessada usando o seguinte URL:

[https://myaccount.queue.core.windows.net/images-to-download](https://myaccount.queue.core.windows.net/images-to-download)

Conta de armazenamento: todo o acesso ao Armazenamento do Azure é feito através de uma conta de armazenamento. Para obter informações sobre a capacidade da conta de armazenamento, consulte Metas de escalabilidade e desempenho para contas de armazenamento padrão.

Fila: uma fila contém um grupo de mensagens. Os nomes das filas devem estar todos em letras minúsculas. Para obter informações sobre filas nomeadas, consulte Filas nomeadas e metadados.

Mensagens: O tamanho máximo de uma mensagem (independentemente do formato) é 64 KB. Nas versões anteriores a 29/07/2017, o tempo máximo de sobrevivência permitido era de 7 dias. Em 29/07/2017 ou posterior, o tempo máximo de vida pode ser qualquer número positivo ou -1 (o que significa que a mensagem não expirará). Se este parâmetro for omitido, o tempo de vida padrão será de 7 dias.

## Comparativo


O Azure Queue Storage e o Azure Service Bus Queue são dois serviços diferentes do Azure que suportam a comunicação assíncrona em sistemas distribuídos. Eles têm algumas diferenças importantes, principalmente relacionadas a cenários de uso, recursos e preços.

Cenário de uso: Armazenamento de Filas do Azure:

Adequado para cenários de mensagens simples, especialmente em microsserviços e sistemas distribuídos. Fornece uma fila de mensagens leve, adequada para comunicação de mensagens simples, como processamento assíncrono de tarefas, componentes desacoplados, etc. Fornece funções básicas de fila sem envolver lógica complexa de processamento de mensagens. Fila do Barramento de Serviço do Azure:

Adequado para cenários de mensagens mais complexos, especialmente em aplicações de nível empresarial e sistemas heterogêneos. Fornece recursos avançados de mensagens, incluindo suporte para transações, filtragem de mensagens, assinaturas de vários caminhos e muito mais. Fornece recursos mais avançados de processamento e roteamento de mensagens para aplicativos que exigem mais controle e confiabilidade. Recursos: Armazenamento de filas do Azure:

Fornece funções básicas de fila de mensagens, incluindo operações de enfileiramento e desenfileiramento de mensagens. Simples e leve, adequado para enfileiramento rápido de tarefas e passagem simples de mensagens. Fila do Barramento de Serviço do Azure:

Fornece recursos avançados de mensagens, como suporte a transações, filtragem de mensagens, entrega programada, etc. Suporta assinatura de vários caminhos e pode realizar diferentes roteamentos e processamentos com base no conteúdo da mensagem. Possui mecanismos de mensagens e roteamento mais complexos. Preços: Armazenamento de Filas do Azure:

Modelo de precificação baseado no volume de armazenamento e número de transações. Fila do Barramento de Serviço do Azure:

Oferece recursos mais avançados e, portanto, é relativamente mais caro. Modelo de preços baseado no número de mensagens entregues e no uso de outros recursos premium. Em geral, a escolha de utilizar o Azure Queue Storage ou o Azure Service Bus Queue depende dos cenários e requisitos específicos da aplicação. Se você precisar apenas de funções simples de fila de mensagens e não tiver requisitos especiais para recursos avançados, poderá escolher o Azure Queue Storage. Se precisar de funcionalidades mais avançadas e de maior controlo, bem como de requisitos mais elevados de fiabilidade e transacionalidade, pode escolher a Fila do Barramento de Serviço do Azure.

# Comparação entre Plano de Serviço (Service Plan) e Plano de Consumo  (Consumption Plan)


O Plano de Serviço de Aplicativo do Azure e o Plano de Consumo para Funções do Azure são dois tipos de planos de serviço do Azure para hospedagem de aplicativos, mas apresentam algumas diferenças em finalidade e recursos.

Plano de serviço de aplicativo:

Finalidade: Usado principalmente para hospedar vários tipos de aplicativos, como aplicativos da web, aplicativos API, aplicativos móveis, etc. Funcionalidades: Requer pré-configuração e pagamento de determinados recursos computacionais, incluindo o número e tamanho das instâncias de máquinas virtuais. É adequado para aplicações com boa previsão de requisitos de recursos. Você pode optar por cobrar por tempo ou por instância de contêiner de aplicação. Elasticidade: O número de instâncias pode ser ampliado ou reduzido manualmente e os recursos computacionais podem ser ajustados de acordo com as necessidades reais. Plano de Consumo:

Objetivo: usado principalmente em Azure Functions, adequado para tarefas de computação de curta duração e orientadas a eventos, como processamento de mensagens de fila, gatilhos cronometrados, etc. Características: É um modelo de computação serverless que não requer configuração prévia de instâncias de máquinas virtuais e é cobrado de acordo com o código efetivamente executado e o consumo de recursos. Lide automaticamente com o dimensionamento elástico e aloque recursos dinamicamente de acordo com a carga. Elasticidade: Totalmente gerenciados automaticamente pelo Azure, os recursos computacionais são alocados e liberados dinamicamente de acordo com a carga real, sem intervenção manual. Resumindo, o Plano de Serviço de Aplicativo é adequado para aplicativos de longa execução com requisitos de recursos relativamente estáveis, enquanto o Plano de Consumo é adequado para tarefas de computação que não precisam ser executadas o tempo todo e processar eventos sob demanda, e são mais elásticos e custosos. -eficaz.

[https://learn.microsoft.com/en-us/azure/azure-functions/functions-scale](https://learn.microsoft.com/en-us/azure/azure-functions/functions-scale)

# Change feed

O Change Feed do Azure Cosmos DB é um recurso que rastreia e captura alterações em documentos em uma coleção do Cosmos DB. O Change Feed registra as operações de criação e atualização de documentos na coleção, armazena essas alterações em ordem cronológica e os clientes podem usar o Change Feed para obter alterações de dados de forma incremental.

Os principais recursos e usos incluem:

Alterações incrementais: O Change Feed registra as alterações no documento e as armazena em ordem cronológica, permitindo ao cliente obter facilmente as alterações ocorridas desde a última consulta.

Processamento em tempo real: pode ser usado para construir aplicativos de processamento em tempo real para monitorar e responder a alterações nos dados do banco de dados.

Notificação assíncrona: as alterações são transmitidas de forma assíncrona ao cliente, e o cliente pode processar essas alterações por meio do SDK do Cosmos DB ou dos gatilhos do Azure Functions.

Implementar vários cenários: adequado para implementar arquitetura orientada a eventos, como notificar outros serviços sobre alterações de dados em microsserviços.

O uso do Change Feed pode ajudar os desenvolvedores a rastrear e processar alterações de dados no banco de dados com mais facilidade, criando assim aplicativos com reconhecimento de tempo real.

# Diversos


o conjunto de contêineres de configuração az webapp é definir a imagem

Após a criação do cofre de chaves, a política de acesso deve ser definida

Plano de Consumo:

Modelo de cobrança: o plano de consumo é um modelo de computação sem servidor onde você paga com base nos recursos consumidos durante a execução da função.

Plano de serviço de aplicativo:

Modelo de cobrança: os planos de serviço de aplicativo são um modelo de hospedagem mais tradicional, onde você paga com base nos recursos alocados da máquina virtual, independentemente do uso real.

É uma prática comum adicionar o ID do cliente do usuário conectado ao CorrelationContext em um aplicativo Web para garantir que todas as operações em todo o sistema estejam associadas ao contexto do usuário correspondente. Isso ajuda a manter a consistência contextual ao depurar e analisar operações entre sistemas.

No Azure, "Autenticação Básica" geralmente se refere a um mecanismo de autenticação simples no qual as credenciais do usuário (nome de usuário e senha) são enviadas ao servidor de maneira codificada em Base64. Embora este método não seja seguro em trânsito, pois as credenciais podem ser interceptadas e decodificadas com relativa facilidade, ele ainda é amplamente utilizado em alguns casos.

Para recursos do Azure (como contas de armazenamento, aplicações Web, etc.), a Autenticação Básica normalmente envolve a inclusão de um nome de utilizador e palavra-passe codificados em Base64 no cabeçalho de Autorização do pedido HTTP. Por exemplo, um cabeçalho de solicitação HTTP pode ter esta aparência:

makefile Copiar código Autorização: QWxhZGRpbjpPcGVuU2VzYW1l básico Neste exemplo, "QWxhZGRpbjpPcGVuU2VzYW1l" é a codificação Base64 do nome de usuário e senha "Aladdin:OpenSesame".

Note-se que, devido a questões de segurança, o Azure já não recomenda a utilização da Autenticação Básica em muitos serviços e, em vez disso, defende a utilização de métodos de autenticação mais seguros, como a Autenticação baseada em Token. Em aplicações web, o Azure Ative Directory (AAD) é frequentemente utilizado para autenticação e autorização em vez da Autenticação Básica.
