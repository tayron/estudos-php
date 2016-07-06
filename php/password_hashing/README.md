# Password Hashing

Gerar hash de senha é uma das considerações mais básicas de segurança que deve ser 
feita ao projetar qualquer aplicativo que aceita senhas dos usuários. Sem gerar hash, 
todas as senhas armazenadas em seu banco de dados da aplicação podem ser roubadas, 
e então imediatamente usada para comprometer não só a sua aplicação, mas também as 
contas de seus usuários em outros serviços, se eles não usarem senhas únicas.

Aplicando um algoritmo de hash para a senha de seus usuários antes de armazenar em 
seu banco de dados, dificulta um atacande determinar a senha original, enquanto 
ainda é possível de comparar o hash resultante para a senha original no futuro.

É importante observar, entretanto, que hash de senhas só protege de comprometer 
em seu armazenameto de dados, mas não necessariamente protege de serem interceptadas 
por um código malicioso injetado em sua própria aplicação.

# Por que são comuns funções de hash tais como md5() e sha1() inadequados para senhas?

Algoritmos de hash como MD5, SHA1 e SHA256 são projetados para serem muito rápidos e eficientes. 
Com técnicas modernas e equipamento de informática, tornou-se trivial de "força bruta" a saída desses algoritmos, a fim de determinar a entrada original.

Por causa da rapidez com que um computador moderno pode "inverter" esses algoritmos de hash, 
muitos profissionais de segurança sugerem fortemente contra a sua utilização para hash da senha.

PHP 5.5 fornece uma API de hash de senha nativo (Password Hashing) que lida de forma 
segura tanto gerando hash e verificando senhas de forma segura.


```php
$str = "A 'quote' is <b>bold</b>";

// Outputs: A 'quote' is &lt;b&gt;bold&lt;/b&gt;
echo htmlentities($str);

$new = htmlspecialchars("<a href='test'>Test</a>", ENT_QUOTES);
echo $new; // &lt;a href=&#039;test&#039;&gt;Test&lt;/a&gt;    
```


Referência: 
* http://codigofonte.uol.com.br/artigos/utilizando-php-para-validar-dados-passados-pelo-usuario
* http://www.php.net/manual/pt_BR/ref.filter.php
* http://php.net/manual/pt_BR/function.filter-input.php
* http://php.net/manual/pt_BR/function.htmlentities.php
* http://php.net/manual/pt_BR/function.htmlspecialchars.php


