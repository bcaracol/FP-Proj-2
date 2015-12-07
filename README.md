# FP-Proj-2

################
# ADT Coordinate
################

quadrado do tabuleiro
linha, coluna
linha de 1 a n
coluna de 1 a n

imutável
dois inteiros

cria_coordenada(l, c) : int × int → coordenada
	⁃	l,c inteiros positivos acima de 1
	⁃	coordenada (1 : c)
	⁃	check argumentos
	⁃	ValueError cria_coordenada: argumentos invalidos

coordenada_linha : coordenada → inteiro

coordenada_coluna : coordenada → inteiro

e_coordenada : universal → lógico

coordenadas_iguais : coordenada × coordenada → lógico

coordenada_para_cadeia : coordenada → cad. caracteres
	⁃	“(l : c)”

### Questões:
—— têm todas de check o input? eg. coordenada para cadeia e coordenadas iguais
—— o cria_coordenada tem de receber c e l? ou pode ser col e lin
—— o tabuleiro tem de ser quadrado?
—— trocar ands por alls e ors por anys?



################
# ADT Tabuleiro
################

•  representar um tabuleiro de Picross (uma grelha de n × n células);
•  aceder a cada uma das células do tabuleiro;
•  modificar o conteúdo de cada uma das células.

especificação linhas colunas = dois tuplos de tuplos de inteiros, em que o primeiro corresponde à especificação das linhas e o segundo à especificação das colunas.

cria_tabuleiro(t): tuplo → tabuleiro
	⁃	t = especificação linhas colunas
	⁃	vazio, todas as células a 0
	⁃	return tabuleiro
	⁃	verificar  argumentos: ValueError ’cria_tabuleiro: argumentos invalidos’

tabuleiro_dimensoes(t): tabuleiro → tuplo 
	⁃	return tuplo com dois elementos, nº linhas e nº colunas

tabuleiro_especificacoes(t): tabuleiro → tuplo 
	⁃	return tuplo de especificações

tabuleiro_celula(t, c): tabuleiro × coordenada → {0, 1, 2} 
	⁃	return estado da célula 
	⁃	vazia,  0
	⁃	em branco, 1
	⁃	 preenchida, 2
	⁃	verificar argumentos para o tabuleiro em causa,  ValueError  ’tabuleiro_celula: argumentos invalidos’ 

tabuleiro_preenche_celula(t, c, i): tabuleiro × coordenada × {0, 1, 2} → tabuleiro
	⁃	modifica o tabuleiro t, preenchendo a célula referente à coordenada c com o elemento 
	⁃	return o tabuleiro modificado
	⁃	verificar argumentos, ValueError ’tabuleiro_preenche_celula: argumentos invalidos’


### Questões:
—— cria_tabuleiro tem de verificar o argumento, mas tem de verificar se o tuplo é composto por tuplos de length n e de inteiros? ou basta chegar se é um tuplo com length 2?
