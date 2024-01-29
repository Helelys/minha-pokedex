# Requisição HTTP 

## URL: https://pokeapi.co/api/v2/pokemon

Usar "?" no final da URL é uma Querry String, ou um
buscador de identificação por string. Usado para filtrar 
por texto.

Exemplo: https://pokeapi.co/api/v2/pokemon?type=grass

E pode ser concatenado com o símbolo "&"
Exemplo: https://pokeapi.co/api/v2/pokemon?type=grass&name=i

Com isso, ele buscará todos os pokémons do tipo grama e
que comecem com a letra i

Offset diz quantas páginas se passarão.

E limite diz quantos elementos aparecerão.

## Link do IP: https://pokeapi.co/

Também pode ser usado o ip em números.

## request method: GET | POST | PUT | DELETE

### request headers

configuração
accept-language: 
*lista de linguagens*

credenciais de autentificação (authorization)

content-type: aplication/json

Body {
    "name": "teste"
}

### response headers


__________________________________

### Fetch error

    try {

    } catch (error) {

    } finally {
        
    }

    ou

    const offset = 0;
const limit = 10;
const url = `https://pokeapi.co/api/v2/pokemon/?offset=${offset}&limit=${limit}`

fetch(url)
    .then(function (response) {
        return response.json()
    })
    .then(function (jsonBody) {
        console.log(jsonBody)
    })
    .catch(function (error) {
    console.error(error)
    }) 
    .finally(function () {
        console.log('Concluído')
    })

