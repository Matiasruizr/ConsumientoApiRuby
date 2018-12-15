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

# Ejemplo API de spotify
Referencias
https://developer.spotify.com/documentation/web-api/reference/

Wrapper para facilitar proceso:
https://github.com/guilhermesad/rspotify



# Ejemplo API de Wordpress
    @url = 'https://www.turismoraido.cl/wp-json/wp/v2/posts'
    @response = HTTParty.get(@url, :verify => false )

    @post = @response.parsed_response

    <% @post.each do |p| %>          
        <h2><%= p['title']["rendered"] %>></h2>
        <p> <%= p['excerpt']["rendered"] %></p>
    <% end %>
    
