classDiagram
    class Usuario {
        +String nome
        +String email
        -String senha
        +autenticar() bool
    }

    class Pedido {
        +int id
        +Date dataCriacao
        +String status
        +calcularTotal() float
    }

    class ItemPedido {
        +int quantidade
        +float precoUnitario
    }

    Usuario "1" -- "0..*" Pedido : realiza
    Pedido "1" *-- "1..*" ItemPedido : contem

<!--
Símbolos de Visibilidade:

    +: Público (public)

    -: Privado (private)

    #: Protegido (protected)

Símbolos de Relacionamento Comuns:

    --: Associação simples (ex: Usuario realiza Pedido).

    *--: Composição (se o Pedido for destruído, os itens dele deixam de existir).

    o--: Agregação (relação onde as partes podem existir de forma independente).

    <|--: Herança (orientação a objetos).

-->