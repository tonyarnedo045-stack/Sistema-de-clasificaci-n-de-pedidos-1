Integrantes 
°Tony JuniorArnedo Alvarez
°Keli alejandra Velez Cardona
Entrega 1

Curso logica de programacion

descripcion del problema

Una tienda en línea necesita un sistema que permita clasificar los pedidos según ciertas reglas de negocio para determinar:
La categoría de despacho
El costo de envío
Un mensaje final al cliente
El sistema debe evaluar condiciones relacionadas con el monto del pedido, tipo de cliente, cantidad de ítems y ciudad destino.

Modelo IPO

| Variable      | Tipo C# | Descripción                              |
| ------------- | ------- | ---------------------------------------- |
| monto         | decimal | Valor total del pedido en pesos          |
| ciudad        | string  | Ciudad destino ("interior" o "exterior") |
| tipoCliente   | string  | Tipo de cliente ("nuevo" o "recurrente") |
| cantidadItems | int     | Número de productos en el pedido         |

Las Reglas con las que operara el negocio=
Si el monto ≥ 150000 Y el cliente es recurrente → Envío Gratis.
Si la cantidadItems ≥ 5 O el monto ≥ 300000 → Envío Express.
En cualquier otro caso → Envío Estándar.
Si la ciudad es "exterior" → Se adiciona un costo extra al envío.

| Variable   | Tipo C# | Descripción                    |
| ---------- | ------- | ------------------------------ |
| categoria  | string  | Tipo de despacho asignado      |
| costoEnvio | decimal | Valor final del envío          |
| mensaje    | string  | Mensaje informativo al cliente |

Tabla De Variables

| Nombre        | Tipo    | Propósito                                |
| ------------- | ------- | ---------------------------------------- |
| monto         | decimal | Almacena el valor del pedido             |
| ciudad        | string  | Determina si aplica recargo por exterior |
| tipoCliente   | string  | Determina si puede tener envío gratis    |
| cantidadItems | int     | Evalúa si aplica envío express           |
| categoria     | string  | Guarda el tipo de despacho               |
| costoEnvio    | decimal | Calcula el valor final del envío         |

CASOS DE PRUEBA
Entrada:
monto = 200000
tipoCliente = recurrente
cantidadItems = 3
ciudad = interior

El resultado que se espera que de es=
categoria de envio: gratis
Costo de envío: $0

Segundo Caso

Entrada:
monto = 300000
tipoCliente = nuevo
cantidadItems = 2
ciudad = exterior

El resultado que se espera que de es=
Categoría: Envío Express
Costo base: 20000
Recargo exterior: 15000
Total: 35000


