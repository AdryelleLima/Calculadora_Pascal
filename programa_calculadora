Program Caulculadora;
	Type calculo = record
		v1:integer;
		v2:integer;
		acao:char;
	end;
	
	{FUNÇÕES MATEMATICAS PARA REALIZAR CALCULO}
	function Somar(v1,v2:integer): integer;
		begin
			Somar:= v1 + v2;
		end;
			
	function Subtrair(v1,v2:integer): integer;
		begin
			Subtrair:= v1 - v2;
		end;
			
	function Multiplicar(v1,v2:integer): integer;
		begin
			Multiplicar:= v1 * v2;
		end;
			
	function Dividir(v1,v2:integer): real;
		begin
			if v2 <> 0 then	
			 Dividir:= v1 / v2
			else
				Dividir:= 0;
		end;	
	
	{PROCEDIMENTO DE INTERFACE}
			
	function menu: char;
	var
		opcao:char;
		begin
			repeat
				writeln('==================');
				writeln('    CALCULADORA   ');
				writeln('==================');
				writeln('[+]. Somar');
				writeln('[-]. Subtrair');
				writeln('[*]. Multiplicar');
				writeln('[/]. Dividir');
				writeln('[0]. Sair');
				
				readln(opcao);
			until opcao in ['+','-','*','/','0'];
			
			menu:= opcao;
		end;
		
	procedure LerValor(var valores: calculo);
		begin
			writeln('digite o primeiro valor: ');
			readln(valores.v1);
			writeln('digite o segundo valor: ');	
			readln(valores.v2);
		end;
			
	procedure Inicio;
		var
			opcao: char;
			operacao: calculo;
		begin
			opcao:=menu;
			while(opcao <> '0') do
				begin
					LerValor(operacao);
					
					case(opcao)of
						('+'): 
							writeln('Resultado= ',Somar(operacao.v1, operacao.v2));
						('-'):
								writeln('Resultado= ',Subtrair(operacao.v1, operacao.v2));
						('*'):
								writeln('Resultado= ',Multiplicar(operacao.v1, operacao.v2));
						('/'):
							if operacao.v2 <> 0 then
								writeln('Resultado= ',Dividir(operacao.v1, operacao.v2):0:2)
							else
								writeln('erro: divisão por zero')
	      	end;
	      	writeln;
	        opcao:=menu;
	      end;
		end;
{BLOCO PRINCIPAL}
Begin
	 Inicio;
	 writeln('Programa encerrado');
End.
