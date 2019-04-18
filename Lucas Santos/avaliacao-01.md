Capitulo 1 Conceitos Básicos

1)Quais os dois principais objetivos dos sistemas operacionais?
R:Um sistema operacional visa abstrair o acesso e gerenciar os recursos de hardware,
provendo aos aplicativos um ambiente de execução abstrato, no qual o acesso aos
recursos se faz através de interfaces simples, independentes das características e
detalhes de baixo nível, e no qual os conflitos no uso do hardware são minimizados.
2)Por que a abstração de recursos é importante para os desenvolvedores de
aplicações? Ela tem utilidade para os desenvolvedores do próprio sistema
operacional?
R:Por prover interfaces de acesso aos dispositivos, tornar os aplicativos independentes
do hardware e definir interfaces de acesso homogêneas para dispositivos com tecnologia
distintas.
3)A gerência de atividades permite compartilhar o processador, executando mais
de uma aplicação ao mesmo tempo. Identifique as principais vantagens trazidas
por essa funcionalidade e os desafios a resolver para implementá-la.
R:Executando os aplicativos simultaneamente em velocidade adequada, gerando filas de
acesso para que não ocorram conflitos entre processos. O principal desafio ao se
implantar essa solução é impedir que os recursos do sistema sejam utilizados por um só
usuário.
4)O que caracteriza um sistema operacional de tempo real? Quais as duas
classificações de sistemas operacionais de tempo real e suas diferenças?
R:Seu tempo de resposta é conhecido no melhor e pior caso de operação. É classificado
emsoft real-time systems e hard real-time systems. No soft-real-time systems, a perda
de prazo implica na degradação do serviço prestado, e no hard real-time systems, a
perda de prazo pode causar graves consequências.
5)O que diferencia o núcleo do restante do sistema operacional?
R:É o coração do Sistema Operacional, responsável por todo gerenciamento dos demais
recursos utilizados pelas aplicações, além de implementar as abstrações utilizadas pelos
aplicativos.
6)Seria possível construir um sistema operacional seguro usando um processador
que não tenha níveis de privilégio? Por quê?
R:Não porque uma aplicação poderá interferir nas áreas de memória de outras
aplicações ou do núcleo. Sem os privilégios uma aplicação pode acessar a placa de rede
para enviar ou receber dados.
7)O processador Pentium possui dois bits para definir o nível de privilégio,
resultando em 4 níveis distintos. A maioria dos sistemas operacionais para esse
processador usa somente os níveis extremos (0 e 3, ou 002 e 112). Haveria alguma
utilidade para os níveis intermediários?
R:Sim, Se houvesse de processamento entre os níveis.8)Quais as diferenças entre interrupções, exceções e traps?
R:Interrupções são eventos causados por dispositivos externos ao processador, exceções
são eventos causados pelo próprio processador e traps são eventos causados por
softwares.
9)Quais as implicações de mascarar interrupções? O que pode ocorrer se o
processador ignorar interrupções por muito tempo? O que poderia ser feito para
evitar o mascaramento de interrupções?
R:O processador perde tempo para varrer todos os dispositivos do sistema para verificar
se há eventos a serem tratados ou não.
10)O comando em linguagem C fopen é uma chamada de sistema ou uma função
de biblioteca? Por quê?
R: É uma chamada de biblioteca, pois a linguagem C não possui nenhum comando de
entrada/saída, todas as operações de entrada/saída ocorrem mediante chamadas as
funções da biblioteca C.
11)Monte uma tabela com os benefícios e deficiências mais significativos das
principais arquiteturas de sistemas operacionais.
R:
Sistemas monolíticos:
Vantagem: desempenho.
Desvantagem: robustez e velocidade de desenvolvimento.
Sistemas em camadas:
Vantagem: domínio das redes de computadores.
Desvantagem: demora no pedido da aplicação, prejudicando o desempenho do sistema.
Sistemas micronúcleos:
Vantagem: robustez e flexibilidade.
Desvantagem: custo associado às trocas de mensagens muito elevado.
Máquinas Virtuais:
Vantagem: evita a construção de novas aplicações ou adapta as já existentes.
Desvantagem: custo adicional de execução dos processos na máquina virtual em
comparação com a máquina real.
12)Relacione as afirmações aos respectivos tipos de sistemas operacionais:
distribuído(D), multiusuário (M), desktop (K), servidor (S), embarcado (E) ou de
tempo real(T):
[D]Deve ter um comportamento temporal previsível, com prazos de resposta claramente
definidos.
[M]Sistema operacional usado por uma empresa para executar seu banco de dados
corporativo.
[E] São tipicamente usados em telefones celulares e sistemas eletrônicos dedicados.
[S]Neste tipo de sistema, a localização física dos recursos do sistema computacional é
transparente para os usuários.[D]Todos os recursos do sistema têm proprietários e existem regras controlando o
acesso aos mesmos pelos usuários.
[T]A gerência de energia é muito importante neste tipo de sistema.
[K]Sistema que prioriza a gerência da interface gráfica e a interação com o usuário.
[M]Construído para gerenciar de forma eficiente grandes volumes de recursos.
[T]O MacOS X é um exemplo típico deste tipo de sistema.
[E]São sistemas operacionais compactos, construídos para executar aplicações
específicas sobre plataformas com poucos recursos.
13)A operação em modo usuário permite ao processador executar somente parte
das instruções disponíveis em seu conjunto de instruções. Quais das seguintes
operações não deveriam ser permitidas em nível usuário? Por quê?
(a)Ler uma porta de entrada/saída
(b)Efetuar uma divisão inteira
(c)Escrever um valor em uma posição de memória
(d)Ajustar o valor do relógio do hardware
(e)Ler o valor dos registradores do processador
(f)Mascarar uma ou mais interrupções
R: C,E e F, pois as seguintes operações lidam diretamente com o hardwere
modificando-o sendo isso no nível de administrador.
14)Considerando um processo em um sistema operacional com proteção de
memória entre o núcleo e as aplicações, indique quais das seguintes ações do
processo teriam de ser realizadas através de chamadas de sistema, justificando
suas respostas:
(a)Ler o relógio de tempo real do hardware.
(b)Enviar um pacote através da rede.
(c)Calcular uma exponenciação.
(d)Preencher uma área de memória do processo com zeros.
(e)Remover um arquivo do disco.
R: d e e, pois, ambas lidam diretamente com o hardware.
15)Coloque na ordem correta as ações abaixo, que ocorrem durante a execução da
função printf("Hello world") por um processo (observe que nem todas as ações
indicadas fazem parte da sequência).
[5]A rotina de tratamento da interrupção de software é ativada dentro do núcleo.
[9]A função printf finaliza sua execução e devolve o controle ao código do processo.
[1]A função de biblioteca printf recebe e processa os parâmetros de entrada (a string
“Hello world”).
[4]A função de biblioteca printf prepara os registradores para solicitar a chamada de
sistema write().
[8]O disco rígido gera uma interrupção indicando a conclusão da operação.
[2]O escalonador escolhe o processo mais prioritário para execução.
[7]Uma interrupção de software é acionada.
[3]O processo chama a função printf da biblioteca C.[6]A operação de escrita no terminal é efetuada ou agendada pela rotina de tratamento
da interrupção.
[10]O controle volta para a função printf em modo usuário.
16)Considere as afirmações a seguir, relativas aos diversos tipos de sistemas
operacionais:
I. Em um sistema operacional de tempo real, a rapidez de resposta é menos importante
que a previsibilidade do tempo de resposta.
II. Um sistema operacional multiusuários associa um proprietário a cada recurso do
sistema e gerencia as permissões de acesso a esses recursos.
III. Nos sistemas operacionais de rede a localização dos recursos é transparente para os
usuários.
IV. Um sistema operacional de tempo real deve priorizar as tarefas que interagem com o
usuário.
V. Um sistema operacional embarcado é projetado para operar em hardware com
poucos recursos. Indique a alternativa correta:
(a)As afirmações II e III estão corretas.
(b)Apenas a afirmação V está correta.
(c)As afirmações III e IV estão erradas.
(d)As afirmações III, IV e V estão erradas.
(e)Todas as afirmações estão erradas.
Justifique as afirmações julgadas erradas (Assim: VII está errada porque ...):
R:(c) As afirmações III e IV estão erradas.
III está errado pois é uma característica de sistemas distribuídos e não de rede;
IV está errado pois é uma característica de sistemas desktop e não de tempo real.
17)Considere as afirmações a seguir, relativas às diversas arquiteturas de sistemas
operacionais:
I. Uma máquina virtual de sistema é construída para suportar uma aplicação escrita em
uma linguagem de programação específica, como Java.
II. Um hipervisor convidado executa sobre um sistema operacional hospedeiro.
III. Em um sistema operacional micronúcleo, os diversos componentes do sistema
são construídos como módulos interconectados executando dentro do núcleo.
IV. Núcleos monolíticos são muito utilizados devido à sua robustez e facilidade de
manutenção.
V. Em um sistema operacional micronúcleos, as chamadas de sistema são
implementadas através de trocas de mensagens.
Indique a alternativa correta:
(a) Todas as afirmações estão erradas.
(b)As afirmações II e III estão corretas.
(c)As afirmações II e IV estão erradas.
(d)Apenas a afirmação V está correta.
(e)As afirmações II e V estão corretas.
Justifique as afirmações julgadas erradas (Assim: VII está errada porque ...):R:(e) As afirmações II e V estão corretas.
I está errada pois uma máquina virtual de sistema é construída para suportar sistemas
operacionais convidados completos;
III está errada pois isso ocorre em sistemas monolíticos e não micronúcleos;
IV está errada pois sistemas monolíticos não tem uma manutenção fácil e sim
complexa.
18)O utilitário strace do UNIX permite observar a sequência de chamadas de
sistema efetuadas por uma aplicação. Em um terminal UNIX, execute strace date
para descobrir quais os arquivos abertos pela execução do utilitário date (que
indica a data e hora correntes). Por que o utilitário date precisa fazer chamadas de
sistema?
R: Para o carregamento de bibliotecas compartilhadas, mapeamento da memória e -- no
final do rastreio -- a emissão das informações sobre a data para a saída padrão.
19)O utilitário ltrace do UNIX permite observar a sequência de chamadas de
biblioteca efetuadas por uma aplicação. Em um terminal UNIX, execute ltrace date
para descobrir as funções de biblioteca chamadas pela execução do utilitário date
(que indica a data e hora correntes). Pode ser observada alguma relação entre as
chamadas de biblioteca e as chamadas de sistema observadas no item anterior?
R:É possível observar que a função date executa as funções do processador sem utilizar
bibliotecas.
