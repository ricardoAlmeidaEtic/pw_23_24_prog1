- MAIN:
	- O main contem o display do menu principal do programa e contem também o processo de redirecionamento
	para todos os restantes processos existentes no programa, como a gestão e visualização das despesas.
	Para além disso este ficheiro importa e distribui as caracteristicas da gestão das despesas e envia as
	mesmas como argumentos para a secção de visualização, para tornar o sistema mais conciso em vez de
	obrigar a importação das despesas na secção da visualização.

- SRC:
	- RegistoDespesas:
		- O registoDespesas é um modelo que criei que centra em permitir ao utilizador Registar e Remover as
		despesas do mesmo, este modelo tem como caracteristas um mapa de despesas e um mapa de categorias.
		O mapa de categorias é definido por uma chave que é definida por um id único que consiste um número
		inteiro que incrementa a cada nova categoria registada, além este mesmo mapa aloca como valor o nome
		da categoria (ex. "Restauração","Têxtil","Automóvel"...)
		O mapa de despesas é definido por uma chave que também é definida por um id único que consiste um número
		inteiro que incrementa a cada nova despesa e essa mesma chave tem como valor um novo mapa que aloca as
		caracteristicas de cada despesa, sendo elas: o montante da despesa, o tipo da despesa, a categoria e uma
		breve descrição da despesa.
		
		O uso dos mapas em vez de modelos especificos por movimento advêm de uma manutenção mais fácil e de um
		uso de memória no sistema mais baixo, como o projeto não era de uma magnitude muito elevada, decidi
		assim usar os mapas para gerir as despesas.

	- VisualizacaoDespesas:
		- O visualizacaoDespesas é simplesmente um conjunto de funções que executam o display das despesas e
		categorias enviadas pelo main após serem executadas, este ficheiro contêm um menu especifico de seleção
		do display ("showMenu") com opções de imprimir por lista ("getDespesasCat") e o display de uma versão em
		gráfico ("getDespesasGraph") existe uma função que passa por todas as despesas e que verifica dentro de todas
		as despesas o montante máximo e mínimo para ajudar o display gráfico a poder ter um melhor ui para compreensão
		do Utilizador do sistema.