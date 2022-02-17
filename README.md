
# Como configurar o ExpressionEngine para utilzar o serviço de cache da CloudFlare

Na CloudFlare, podemos utilizar até três regras gratuitamente, mas para nossa sorte o ExpressionEngine precisa apenas de duas.

Vamos a primeira regra:

Insira os dados abaixo no formulário, substituindo ```seusite.com``` pelo endereço do seu site:

```
*seusite.com/?ACT=*
```

Agora acrescente os parâmetros: 

- Verificação da integridade do navegador: Desativado,
- Always Online: Desativado, 
- Nível de cache: Ignorar,
- Desabilitar aplicativos, 
- Desabilitar desempenho
	
Feito isso, vamos criar a segunda regra:
	
```	
*seusite.com/admin.php*
```

Com os seguintes parâmetros:

- Always Online: Desativado, 
- Nível de cache: Ignorar, 
- Desabilitar aplicativos, 
- Desabilitar desempenho

Pronto! Seu site agora está utilizando os recursos de cache da CloudFlare, sem interferir no funcionamento do painel do ExpressionEngine!
