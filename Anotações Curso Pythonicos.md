#    **Anotações do Curso Pythonicos - Papo Binário**

0. ## Comandos Gerais
 
    * _raw_input(text)_: usado para receber uma entrada de valores até receber <Enter> para sair;
    * _"%s %d %f.2 %r" %(string, integer, float[with tow decimal numbers])_;
    * _in_: usado para saber se um elemento está em uma lista, tupla ou dicionário.

1. ## Aula 10 - Listas

 	* Posso ter vários valores de tipos diferentes em uma lista;
 	* Adicionar um elemento a uma lista: _list.append(elemento)_;
 	* Removendo um elemento de uma lista: _del list[index]_    **OU** _list.remove(elemento)_;
 	* Para copiar listas: _list.copy()_;
    * _for valor in list_: Passa os valores dentro de _lista_ para a veriável _valor_;
    * _list.index(valor)_: retorna o index de _valor_ na lista;
    * _list.insert(posição, valor)_: adiciona _valor_ à lista na posição _posição_;
    * _list1.extend(elemento)_, adiciona _elemento_ no final de _list1_, adicionando elemento por elemento;
    * _list.pop(index)_, remove o elemento no _index_;
    * _list.sort()_: ordena a lista;
    * _list.reverse()_: reverte a lista;
    * _list.count(elemento)_: conta quantas aparições o _elemento_ tem na lista tem.


    1. ### Slices

 		* Para usar **slices**, faça: _list[início:final]_;
 		* Para ir até o fim sem saber o tamanho, usar: _list[:]_;

    2. ### Concatenação

 		* _list1 + list2_;
 		* _list    * 3_;

2. ## Aula 11 - Trabalhando com Listas

    * Múltiplas atribuições: _var1,var2,var3 = list_. **var1 = list[0]**, **var2 = list[1]** e **var3 = list[2]**;

3. ## Aula 12 - Tuplas

    * Tuplas são imutáveis;
    * _tuple = ()_ ou _tuple = tuple()_;
    * Para criar tuplas de um valor só: _tuple = (elemento,)_;
    * Pode fazer: _tuple = list(tuple)_, ou o contrário também.

4. ## Aula 13 - Dicionários

    * _dict = dict()_ ou _dict = {}_;
    * Estrutura: _dict{index1:value1,index2:value2,...}_;
    * Não são ordenados;
    * Se tenho dois dicionários, com o mesmo conteúdo mas com ordenação diferente, eles são iguais;
    * Para adicionar, basta: _dict[new index] = new value_;
    * Para remover: _del dict[index]_;
    * _dict[keys] = indexes_, _dict[values] = values_, _dict[items] = indexes and values_;
    * _dict.get(index, valueNotFound)_: identifica se existe um valor com index _index_ no dicionário, se não existir, retorna o valor _valueNotFound_;
    * _dict.setDefault(index, defaultValue)_: anexa no dicionário um valor padrão para o index.

5. ## Aula 14 - Strings

	* _"string" in String_, identifica se há uma ocorrência da string _string_ dentro da outra string _String_;

	1. ### Utilidades

		* _upper()_ :arrow_right: deixa todas as letras maiúsculas;
		* _lower()_ :arrow_right: deixa todas as letras minúsculas;
		* _isupper()_ :arrow_right: retorna _True_ se todas as letras forem maiúsculas;
		* _islower()_ :arrow_right: retorna _True_ se todas as letras forem minúsculas;
		* _isalpha()_ :arrow_right: retorna _True_ se tiver apenas letras (sem espaços em branco);
		* _isalnum()_ :arrow_right: retorna _True_ se tiver letras e/ou números (sem espaços em branco);
		* _'number'.isdecimal()_ :arrow_right: retorna _True_ se tiver apenas números (sem espaços em branco. O 'u' significa unicode, para que ele recoheça o número em unicode);
		* _isspace()_ :arrow_right: retorna _True_ se tiver apenas tabulações, espaços em branco ou quebras de linha;
		* _istitle()_ :arrow_right: retorna _True_ se tiver a primeira letra de cada palavra maiúscula apenas.

	2. ### Mais Utilidades

		* _startswith(string)_;
		* _endswith(string)_;
		* _join(string)_ :arrow_right: concatena as strings;
		* _split(separator)_;
		* _strip(), rstrip() e lstrip()_ :arrow_right: remove espaços em branco das extremidades da string;
		* _replace(oldValue, newValue)_.

6. ## Aula 15 - Funções

	1. ### Tratando Exceções

		* Usar _try e except_.

7. ## Aula 16 - Módulos

	* Utilizar o _pip_;
	* _pip install request_, _pip install --upgrade request_ ou _pip install -r dependencias.txt_;
	* _pip uninstall request_;
	* _pip list_ ou _pip list --outdated_;

8. ## Aula 17 - Trabalhando com o módulo OS - *Para fazer ações no OS*

	* Concatenando paths :arrow_right: _os.path.join(path, path, path)_;
	* Diretório atual :arrow_right: _os.getcwd()_;
	* Mudar de diretório :arrow_right: _os.chdir(path)_;
	* Criar pastas :arrow_right: _os.makedirs(path)_;
	* Retorna path absoluto :arrow_right: _os.path.abspath()_;

9. ## Aula 18 - Lendo Arquivos

	* _file = open(filename)_;

10. ## Aula 19 - Escrevendo Arquivos

	* _w_ :arrow_right: escrita;
	* _a_ :arrow_right: adição;
	* _r_ :arrow_right: leitura;
	* _b_ :arrow_right: binário;

	1. ### Sobrescrevendo um arquivo

		* _open(filename, 'w')_ :arrow_right: _f.write(content)_;

	2. ### Adicionando conteúdo a um arquivo

		* _open(filename, 'a')_ :arrow_right: _f.write(content)_;

	3. ### Salvando um binário

		* _import requests
			url = 'http://downloads.sourceforge.net/gnuwin32/wget-1.11.4-1-setup.exe'
			r = requests.get(url)
			f = open('saida.exe','ab')
			f.write(r.content)
			f.close()__

11. ## Aula 20 - Organizando Arquivos

	1. ### Copiando Arquivos
		
		* _import shutil (shell utilities)_;
		* _shutil.copy(pathOrigin/filename, pathDestiny)_ (mesmo nome);
		* _shutil.copy(pathOrigin/filename, pathDestiny/newFilename)_ (nome diferente);

	2. ### Sobrescrevendo ou movendo arquivos

		* _shutil.move(pathOrigin/filename, pathDestiny/newFilename)_;
		* _shtutil.move(pathOrigin/filename, pathOrigin)_;

	3. ### Apagando arquivos e pastas

		* _os.unlink(path)_ :arrow_right: apaga arquivos;
		* _os.rmdir(path)_ :arrow_right: apaga diretório vazio;
		* _shutil.rmtree(path)_ :arrow_right: apaga diretórios e todos seus arquivos e subdiretórios.

12. ## Aula 21 - Arquivos Zipados

* **Comandos:**

	* Lendo arquivos

		> _import zipfile_ 

		> _zipado =  zipfile.ZipFila(arquivo zipado existente)_

		> _zipado.namelist()_

		> _infos = zipado.getinfo(arquivo)_

		> _infos.file_size_

		> _infos.compress_size_

		> _zipado.close()_

	* Extraindo todos os arquivos

		> _zipado.extractall()_

		> _zipado.extract(filename)_

		> _zipado.extract(filename, path)_

		> _zipado.close()_

	* Criando arquivo zip e adicionando

		> _zipback = zipfile.ZipFile(zipfilename.zip, 'w')_

		> _zipback.write(filename)_

		> _zipback.close()_

13. ## Aula 22 - Subprocess

* Executar códigos de OS dentro do código python.
* **Comandos:**

	* _subprocess.call()_

		> _import subprocess_

		> _a = subprocess.call('ls')_

		> a

		> Retorna 0 caso sucesso e 1 caso erro

	* _subprocess.check_call()_

		> _a = subprocess.check_call(value)_

		> Retorna erro caso o valor não seja 0

	* Argumentos

		> _shell_: utiliza a shell para executar o comando\
		> _stdin_: redireciona a entrada\
		> _stdout:_ redireciona a saída\
		> _stderr_: redireciona o erro