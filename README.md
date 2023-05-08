#WebserviceBuscarCep <br>
Buscar o endereço através do webservice retornando um XML e sendo convertido ao modelo CEP:<br>
<br>
modelo CEP<br>
&nbsp;&nbsp;&nbsp;String cep, logadouro, bairro, cidade, uf, ibge, ddd, siafi;<br>
&nbsp;&nbsp;&nbsp;boolean cepValido;<br>
<br>
Webservice = (Via Cep [http://viacep.com.br/])<br>
Retorno caso encontrado;<br>
<*xmlcep*><br>
&nbsp;&nbsp;&nbsp;<*cep*>**00000-000**<*/cep*><br>
&nbsp;&nbsp;&nbsp;<*logradouro*>**Rua Projetada**<*/logradouro*><br>
&nbsp;&nbsp;&nbsp;<*complemento/*><br>
&nbsp;&nbsp;&nbsp;<*bairro*>**Bairro**<*/bairro*><br>
&nbsp;&nbsp;&nbsp;<*localidade*>**Cidade**<*/localidade*><br>
&nbsp;&nbsp;&nbsp;<*uf*>**UF**<*/uf*><br>
&nbsp;&nbsp;&nbsp;<*ibge*>**cod ibge**<*/ibge*><br>
&nbsp;&nbsp;&nbsp;<*gia/*><br>
&nbsp;&nbsp;&nbsp;<*ddd*>**dd**<*/ddd*><br>
&nbsp;&nbsp;&nbsp;<*siafi*>**0000**<*/siafi*><br>
<*/xmlcep*><br>
<br>
Retorno caso NÂO encontrado;<br>
<*xmlcep*><br>
&nbsp;&nbsp;&nbsp;<*erro*>**true**<*/erro*><br>
<*/xmlcep*><br>
<br>
<br>
Caso deseje buscar por outro webservice, há possibilidade, contudo deve-se atentar ao retorno e parametros.<br>
<br>
Webservice = {Republica Virtual(testado) [http://cep.republicavirtual.com.br/]}<br>
Retorno caso encontrado;<br>
<*webservicecep*><br>
&nbsp;&nbsp;&nbsp;<*debug*>**- nao encontrado via search_db cep unico -** <*/debug*><br>
&nbsp;&nbsp;&nbsp;<*resultado*>**1**<*/resultado*><br>
&nbsp;&nbsp;&nbsp;<*resultado_txt*>**sucesso - cep completo**<*/resultado_txt*><br>
&nbsp;&nbsp;&nbsp;<*uf*>**UF**<*/uf*><br>
&nbsp;&nbsp;&nbsp;<*cidade*>**Cidade**<*/cidade*><br>
&nbsp;&nbsp;&nbsp;<*bairro*>**Bairro**<*/bairro*><br>
&nbsp;&nbsp;&nbsp;<*tipo_logradouro*>**Rua**<*/tipo_logradouro*><br>
&nbsp;&nbsp;&nbsp;<*logradouro*>**Projetada**<*/logradouro*><br>
<*/webservicecep*><br>
<br>
Retorno caso NÃO encontrado;<br>
<*webservicecep*><br>
&nbsp;&nbsp;&nbsp;<*debug*> **- nao encontrado via search_db cep unico -** <*/debug*><br>
&nbsp;&nbsp;&nbsp;<*resultado*>**0**<*/resultado*><br>
&nbsp;&nbsp;&nbsp;<*resultado_txt*>**sucesso - cep não encontrado**<*/resultado_txt*><br>
&nbsp;&nbsp;&nbsp;<*/uf*><br>
&nbsp;&nbsp;&nbsp;<*/cidade*><br>
&nbsp;&nbsp;&nbsp;<*/bairro*><br>
&nbsp;&nbsp;&nbsp;<*/tipo_logradouro*><br>
&nbsp;&nbsp;&nbsp;<*/logradouro*><br>
<*/webservicecep*>
