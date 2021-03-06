M�dulo PagSeguro para OpenCart Vers�o v1.5.x
-------------------------------------------------------

Requisitos:
----------

A biblioteca PagSeguro em PHP necessita das seguintes depend�ncias para seu funcionamento:

- Standard PHP Library (SPL)

- Biblioteca cURL

- DOM extension

Instala��o
----------

1 - Descompacte o conte�do no diret�rio raiz de sua loja.

2 - Configure as op��es do m�dulo PagSeguro pelo painel de administra��o de sua loja navegando at� Extens�es -> Formas de Pagamento.

3 - No painel da sua conta no site do PagSeguro(menu � esquerda) navegue at� Prefer�ncias -> Frete, escolha o tipo de frete conforme a configura��o feita para o m�dulo.
	Se optou pelo frete calculado pela sua loja, marque 'Frete fixo'. Se optou pelo c�lculo de frete feito pelo PagSeguro, marque "Frete por peso" 

4 - Ainda neste menu, navegue at� Integra��es -> Notifica��o de Transa��o, marque "Ativado" e define a URL de notifica��es seguindo o padr�o:
	
	http://www.SUALOJA.com.br/index.php?route=payment/pagseguro/callback
	
	Substitui a parte 'SUALOJA' pelo nome de sua loja.
	
5 - Confira se a op��o "Pagamento Via API" esteja desativada.

6 - Confira se a op��o "Retorno autom�tico de dados" esteja desativada.

7 - Confira se as duas op��es (P�gina fixa de redirecionamento e P�gina de redirecionamento din�mico) no menu "P�gina de redirecionamento" estejam desativadas.
	
Notas
----------	

- Se optar pelo frete calculado pelo PagSeguro, o valor n�o constar� no total do pedido. O mesmo ser� informado no  hist�rico do pedido.
- H� limita��o de 60 caracteres para o e-mail do cliente, de acordo com a API do PagSeguro. Se ultrapass�-lo, um erro ser� gerado.
- H� limita��o de 50 caracteres para o nome do cliente. O m�dulo retira os caracteres que ultrapassarem esse limite.
- O m�dulo tenta separar o DDD do n�mero de telefone (a API tem campos separados para DDD e o n�mero do telefone em si), mas somente se o telefone do cliente tiver mais de 9 d�gitos.
Exemplos de formatos v�lidos s�o: (11)7777-0000, 11 7777 0000, 1177770000, etc. Se n�o obtiver sucesso, o PagSeguro pedir� o DDD e telefone para prosseguir com o pagamento.
- Os campos 'n�mero' e 'complemento' do endere�o de entrega exigidos pelo PagSeguro s�o enviados com nenhum dado porque o OpenCart n�o possui esses campos separados.
Assim o cliente dever� preench�-los para continuar com o pagamento.

----------------------------
D�vidas, sugest�es e avisos sobre bugs acessem o f�rum do OpenCart Brasil:
http://opencartbrasil.com.br/forum

Mantenedor:
J�lio C�sar Campos Guimar�es