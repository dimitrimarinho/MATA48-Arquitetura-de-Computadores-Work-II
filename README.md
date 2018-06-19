# MATA48-Arquitetura-de-Computadores-Work-II

Link da especificação: https://www.moodle.ufba.br/pluginfile.php/560311/mod_resource/content/1/MATA48_TP2_2018_1.pdf

**Especificação**

1.Objetivo geral: 

estudo de pipelining através da execução de programas MIPS 32 bits no simulador WebSimple.

2.Objetivos específicos:

a. Execute  o  programa  abaixo  no  simulador  WebSimple.  Utilize  a configuração padrão para tempo monociclo (50 ns) e para pipeline (10 ns). Não utilize forwarding (deixe desmarcadas todas as opções MEM → EX,WB  →  EX,  WB  →  MEM.  Indique:  a)  as  dependências  de  dados existentes;  b)  a  quantidade  de  ciclos  ociosos  no  pipeline;  c)  o desempenho (speed up) obtido.

lw  $1, 0($1)
lw  $2, 4($0)
add $3, $1, $2
sw  $3, 12($0)
lw  $4, 8($0)
add $5, $1, $4
sw  $5, 
16($0)
add $1, $0, $3
sub $3, $2 $2
lw  $6, 8($0)
add $5, $6, $4
add $1, $6, $6

b. Modifique  o  exercício  anterior  para  considerar forwarding entre  os estágios MEM → EX. Indique novamente: a) as dependências de dados existentes;  b)  a  quantidade  de  ciclos  ociosos  no  pipeline;  c)  o desempenho (speed up) obtido.

c. Modifique  o  exercício  anterior  para  considerar forwarding entre  os estágios WB → EX. Indique novamente: a) as dependências de dados existentes;  b)  a  quantidade  de  ciclos  ociosos  no  pipeline;  c) o desempenho (speed up) obtido.

d. Modifique  o  exercício  anterior  para  considerar forwarding entre  os estágios WB → MEM. Indique novamente: a) as dependências de dados existentes;  b)  a  quantidade  de  ciclos  ociosos  no  pipeline;  c)  o desempenho (speed up) obtido.

e. Modifique o exercício anterior para considerar forwarding entre todos os estágios (MEM → EX, WB → EX, WB → MEM). Indique novamente: a) as dependências de dados existentes; b) a quantidade de ciclos ociosos no pipeline; c) o desempenho (speed up) obtido.

f. Comente  sobre  os  resultados  obtidos  em  cada  configuração.  Na  sua opinião,  faz  sentido  (seria  viável  tecnicamente) utilizar forwarding em todos os estágios (configuração da questão **e**)? Em caso negativo, qual das configurações de forwarding (questões **b** a **d**), na sua opinião, gera o melhor resultado? Por quê?

g. Escolha um dos trechos de código abaixo e o traduza para o MIPS 32 bits. Teste o programa traduzido com o simulador MARS (ou outro simulador MIPS) para garantir que o código está funcional. Após, insira os comandos MIPS  (segmento  .data)  no  simulador
WebSimple  e  repita  os  passos executados  nos  exercícios **a** a **e** (habilitando  as  diferentes  opções  de forwarding). Relate,  para  cada  opção  de  forwarding  simulada, i) as dependências de dados encontradas, ii) a quantidade de ciclos ociosos no pipeline e iii) o desempenho obtido com a habilitação de cada opção de forwarding.

**TRECHO 1**

for(i=0; i<20; i++) {
  scanf(“%d”,&x);
  vetor[i] = x;
  y = vetor[i] + x + i;
}

**TRECHO 2**

x = 10;
y = 0;
do {
  z = (x*2) + y;
  y--;
  scanf(“%d”,&x);
} while (x < 50);

**TRECHO 3**

scanf(“%d”, &x);
if (x < 10) && (x > 2) {
  z = x + 200;
  y = z * z;
}
else 
  z = x + 32;

3. O trabalho poderá ser realizado de forma individual ou em duplas.

**Data máxima de submissão: 03/07/2018**, 23h59m.

**Formato de submissão:**

1. arquivo zipado (.zip, .tar ou outro compactador) com todos os trechos de códigos-fonte (programas .asm) testados nos simuladores. **OBS.: não inserir arquivos executáveis.**

2. o arquivo zipado deve ter o seguinte nome: MATA48_ALUNO1.ext (ex. MATA48_BILLGATES.zip) ou MATA48_ALUNO1_ALUNO2.ext (ex.MATA
48_BILLGATES__STEVEJOBS.zip).

**Local de submissão:**

1. Link a ser disponibilizado na página da disciplina no Moodle.

**Critérios de correção:**

1. Cada programa totalmente correto vale 10.0 pontos.

2. Cada erro de sintaxe apontado pelo compilador será descontado em 0,5 ponto.

3. Programas  idênticos,  submetidos  por  grupos  diferentes,  serão  zerados,  por caracterizarem  plágio.  Por  “idênticos” serão  entendidos  os  programas  que tenham a mesma estrutura de variáveis (nomes, tipos etc) e sigam a mesma lógica (estrutura) de comandos; ou ainda qu e apresentem os mesmos erros de compilação  e/ou  execução,  considerada  a  estrutura  de  código apresentada. Serão usados programas comparadores e identificadores de plágio para esta aferição.

4. A nota final do trabalho será composta pela média aritmética das notas dos 3 programas entregues. **OBS.:** conforme Plano de Ensino (disponível no Moodle), o peso total do trabalho será de **30%** da primeira nota.

**Divulgação de resultados:**

1. Será feita até a data de **17/07/2018**, 23h59m, via Moodle.

**Resolução de dúvidas referentes ao trabalho:**

1.Acessar o fórum específico para o Trabalho Prático II no Moodle e inserir lá toda e qualquer pergunta pertinente ao trabalho. 

2. OBS.: preferencialmente, usar o fórum do Moodle em vez de e-mail para que toda a turma possa interagir e socializar dúvidas e dicas.
