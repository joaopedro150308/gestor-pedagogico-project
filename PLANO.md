# Este programa deve lançar as notas dos professores no site do SIAP

- Pesquisar o que é data-frame
- Pesquisar a relação de data-frame e o pandas
- Table board HTML
- Vídeo sobre converssão de planilhas para HTML: https://www.youtube.com/watch?v=IpQ-o6dhUDM

- Formato superficial do sitema preesnte em: https://portaleduca.educacao.go.gov.br/suporte_ti/siap-perfil-professor/

    - Ideia de Funcionalidade do programa:
    O programa deve contar com uma GUI, e deverá acessar e interagir com o SIAP através do Selenium.
    O professor deve ser capaz de fornecer os seus dados para que eles sejam utilizados pelo selenium




### Módulo 1.0 - Dados para localizar o formulario a preencher

- O programa preencisa dos seguintes dados para identificar a tabela a ser preenchida:
    - Composição de Ensino, Série, Turno, Turma, Disciplina e Bimestre
    - Estes são filtros necessários para localizar o formulário desejado
    - Em seguida é necessário clicar em listar, e depois selecionar o formulário de a cordo com a etapa avaliativa

### Módulo 1.1 - Etapa avaliativa alvo
- O professor também deve indicar qual das etapas avaliativas será preenchida. Sendo uma entre:
    - 1. Ciclo1 – Bloco 1
    - 2. Ciclo2 – Bloco 1
    - 3. Ciclo2 – Simulado

- Ao selecionar a etapa desejada, é necessário clicar em visualizar, para só então ter acesso à planilha da avaliação




### Módulo 2 - Planilha de avaliação

- Informações presentes no site: https://portaleduca.educacao.go.gov.br/suporte_ti/siap-perfil-professor/

- A tabela segue o seguinte layout:

    # Nome dos alunos
    - A primeira coluna recebe o nome dos alunos, juntamente com um índice númerico, no seguinte formato: 1 - Ana Carolina (numero '-' Nome)

    # Presença 1 e 2 chamada
    - A 2 e 3 coluna são designadas à presença na primeira chamada, enquanto a 4 e 5 coluna são designadas à presença na segunda chamada
    - Caso a presença na primeria chamada seja positiva, a segunda chamada é desativada.
    - Caso o aluno não tenha sido presente em nenhuma das chamdas o preenchimento das questões deste aluno é bloqueado.

    # Intervalo de questões do teste
    - A partir da 6 coluna existe um intervalo onde as colunas deste são questões, que são representadas por elementos CheckBox, podendo receber verdadeiro ou flaso.
    - O tamanho do intervalo pode variar de acordo com o número de questões de cada disciplina

    # Informações sobre o acerto do aluno
    - Por fim, as ultimas duas colunas são responsáveis por obrigar as seguintes informações, respectivamente: Quantidade de acertos e Porcentagem de acertos.