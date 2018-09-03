# ConsumientoApiRuby
A pedido de un colega que buscaba como consumir una api de manera simple y eficaz en Ruby creo este repositorio.

Comenzamos instalando la gema HTTParty
```
    gem install HTTParty
    # o en caso de rails copiamos en el gemfile lo siguiente y ejecutamos bundle install
    gem 'httparty' 
```

# Ejemplo API SBIF
```
    url = 'https://api.sbif.cl/api-sbifv3/recursos_api/dolar?apikey=tuapikeyaca&formato=json'
    response = HTTParty.get(url, :verify => false )
    $dolar  = response.parsed_response["Dolares"][0]["Valor"].to_f
```
