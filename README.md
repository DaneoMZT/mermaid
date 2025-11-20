flowchart LR
    subgraph Catálogo
        UC1[Ver catálogo]
        UC2[Ver detalle de producto]
    end

    subgraph Carrito_y_Pedidos
        UC3[Añadir al carrito]
        UC4[Ver/Modificar carrito]
        UC5[Iniciar Checkout]
        UC6[Confirmar pedido]
    end

    subgraph Usuarios
        UC7[Registrarse]
        UC8[Iniciar sesión]
        UC9[Ver perfil]
    end

    subgraph Contacto_y_Solicitudes
        UC10[Enviar solicitud]
        UC11[Responder solicitud]
    end

    subgraph Ofertas_y_Valoraciones
        UC12[Ver ofertas]
        UC13[Aplicar oferta]
        UC14[Publicar valoración]
    end

    Cliente((Cliente)) --> UC1
    Cliente --> UC2
    Cliente --> UC3
    Cliente --> UC4
    Cliente --> UC5
    Cliente --> UC6
    Cliente --> UC7
    Cliente --> UC8
    Cliente --> UC9
    Cliente --> UC10
    Cliente --> UC12
    Cliente --> UC14

    Administrador((Administrador)) --> UC11
    Administrador --> UC12
    Administrador --> UC1
    Administrador --> UC2

    Pasarela((Pasarela de Pago)) --> UC6
