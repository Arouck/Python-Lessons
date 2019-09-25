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

 		* Para usar    **slices**, faça: _list[início:final]_;
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
