# Instrucciones de la actividad
## Toma como base la API REST pública de Pokémon: https://pokeapi.co/ para transformarla en una API GraphQL funcional.
### Requisitos:
1. Implementa un servidor GraphQL que permita consultar la información básica de los Pokémon utilizando el endpoint REST https://pokeapi.co/api/v2/pokemon/{id} o https://pokeapi.co/api/v2/pokemon/{name}.
2. Agrega resolvers encadenados para obtener detalles adicionales del Pokémon, como las habilidades (abilities) o los movimientos (moves), accediendo a las URLs proporcionadas en la respuesta REST.
3. Asegúrate de que sea posible consultar:
Un Pokémon por su ID o nombre.
La lista de habilidades del Pokémon.
Los movimientos aprendidos por el Pokémon.
Por ejemplo, una consulta como esta debería ser posible:

```
query {
  pokemon(name: "pikachu") {
    id
    name
    abilities {
      name
      effect
    }
    moves {
      name
      power
    }
  }
}
```
