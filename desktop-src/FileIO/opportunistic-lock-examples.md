---
description: Diagramas de vistas de tráfico de red para un bloqueo oportunista de nivel 1, un bloqueo oportunista de lotes y un bloqueo oportunista de filtro.
ms.assetid: 78830113-b18e-40c7-8ec4-8896dbc58030
title: Ejemplos de bloqueos oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8b8a0c5b04897ddc2fc8f2e3bdec20f2fdb02d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545710"
---
# <a name="opportunistic-lock-examples"></a>Ejemplos de bloqueos oportunistas

En los ejemplos siguientes se muestran datos y movimientos de mensajes SMB, ya que se realizan bloqueos oportunistas y se rompen. Tenga en cuenta que los clientes pueden almacenar en caché datos de atributos de archivos, así como datos de archivos.

Tenga en cuenta también que estos ejemplos se basan en situaciones en las que las aplicaciones cliente solicitan bloqueos oportunistas desde servidores remotos. Estos procesos los inicia automáticamente el redirector de red y el servidor remoto; no hay ninguna implicación directa por parte de la aplicación o aplicaciones cliente. Los procesos descritos en estos ejemplos se pueden generalizar en situaciones en las que las aplicaciones cliente locales están solicitando directamente bloqueos oportunistas del sistema de archivos local, con la excepción de que no interviene el intercambio de datos a través de la red.

## <a name="level-1-opportunistic-lock"></a>Bloqueo oportunista de nivel 1

En el diagrama siguiente se muestra una vista de tráfico de red de un bloqueo oportunista de nivel 1 en un archivo. Las flechas indican la dirección del movimiento de datos, si existe.



| Evento | Cliente X                                          | Servidor                                   | Cliente Y                                          |
|-------|---------------------------------------------------|------------------------------------------|---------------------------------------------------|
| 1     | Abre el archivo, nivel de solicitudes 1 Lock = =>          |                                          |                                                   |
| 2     |                                                   | <= = concede un bloqueo oportunista de nivel 1 |                                                   |
| 3     | Realiza operaciones de lectura, escritura y otras = => |                                          |                                                   |
| 4     |                                                   |                                          | <= = solicitudes para abrir el archivo                      |
| 5     |                                                   | <= = interrumpe el bloqueo oportunista         |                                                   |
| 6     | Descarta los datos de lectura previa                          |                                          |                                                   |
| 7     | Escribe Data = =>                                |                                          |                                                   |
| 8     | Envía el mensaje "CLOSE" o "Done" = =>            |                                          |                                                   |
| 9     |                                                   | Correcto operación de apertura = =>              |                                                   |
| 10    | Realiza operaciones de lectura, escritura y otras = => |                                          | <= = realiza operaciones de lectura, escritura y otras. |



 

En el evento 1, el cliente X abre un archivo y, como parte de la operación de apertura, solicita un bloqueo oportunista de nivel 1 en el archivo. En el evento 2, el servidor concede el bloqueo de nivel 1 porque ningún otro cliente tiene abierto el archivo. El cliente continúa accediendo al archivo de la manera habitual en el evento 3.

En el evento 4, el cliente Y intenta abrir el archivo y solicita un bloqueo oportunista. El servidor ve que el cliente X tiene el archivo abierto. El servidor omite la solicitud de Y, mientras que el cliente X vacía los datos de escritura y abandona su caché de lectura para el archivo.

El servidor fuerza la limpieza de X mediante el envío de a X un mensaje SMB que interrumpa el bloqueo oportunista, el evento 5. El cliente X "silenciosamente" descarta cualquier dato de lectura previa; en otras palabras, este proceso no genera tráfico de red. En el evento 7, el cliente X escribe los datos escritos en caché en el servidor. Cuando el cliente X ha terminado de escribir los datos en caché en el servidor, el cliente X envía un mensaje "cerrar" o "listo" al servidor, evento 8.

Una vez que se ha notificado al servidor que el cliente X ha terminado de vaciar la memoria caché de escritura en el servidor o ha cerrado el archivo, el servidor puede abrir el archivo para el cliente Y, en el evento 9. Dado que ahora el servidor tiene dos clientes con el mismo archivo abierto, concede un bloqueo oportunista a ninguno. Ambos clientes continúan leyendo desde el archivo y uno o ninguno de los dos escribe en el archivo.

## <a name="batch-opportunistic-lock"></a>Bloqueo oportunista de Batch

En el diagrama siguiente se muestra una vista de tráfico de red de un bloqueo oportunista de batch. Las flechas indican la dirección del movimiento de datos, si existe.



| Evento | Cliente X                               | Servidor                                 | Cliente Y                                          |
|-------|----------------------------------------|----------------------------------------|---------------------------------------------------|
| 1     | Abre el archivo, requests batch Lock = => |                                        |                                                   |
| 2     |                                        | <= = concede el bloqueo oportunista de Batch |                                                   |
| 3     | Lee archivo = =>                      |                                        |                                                   |
| 4     |                                        | <= = envía datos                      |                                                   |
| 5     | Cierra el archivo                            |                                        |                                                   |
| 6     | Abre el archivo                             |                                        |                                                   |
| 7     | Busca datos                      |                                        |                                                   |
| 8     | Lee Data = =>                      |                                        |                                                   |
| 9     |                                        | <= = envía datos                      |                                                   |
| 10    | Cierra el archivo                            |                                        |                                                   |
| 11    |                                        |                                        | <= = abre el archivo                                 |
| 12    |                                        | <= = interrumpe el bloqueo oportunista       |                                                   |
| 13    | Cierra File = =>                     |                                        |                                                   |
| 14    |                                        | Correcto operación de apertura = =>            |                                                   |
| 15    |                                        |                                        | <= = realiza operaciones de lectura, escritura y otras. |



 

En el bloqueo oportunista de batch, el cliente X abre un archivo, el evento 1 y el servidor concede al cliente X un bloqueo por lotes en el evento 2. Client X intenta leer datos, evento 3, a los que el servidor responde con datos, evento 4.

El evento 5 muestra el bloqueo oportunista de batch en el trabajo. La aplicación en el cliente X cierra el archivo. Sin embargo, el redirector de red filtra la operación de cierre y no transmite un mensaje de cierre, con lo que se realiza un cierre "silencioso". El redirector de red puede hacer esto porque el cliente X tiene propiedad exclusiva del archivo. Más adelante, en el evento 6, la aplicación vuelve a abrir el archivo. De nuevo, ningún flujo de datos fluye a través de la red. En lo que respecta al servidor, este cliente ha tenido abierto el archivo desde el evento 2.

Los eventos 7, 8 y 9 muestran el curso habitual del tráfico de red. En el evento 10, se produce otro cierre silencioso.

En el evento 11, el cliente Y intenta abrir el archivo. La vista del archivo del servidor es que el cliente X lo tiene abierto, aunque la aplicación en el cliente X la ha cerrado. Por lo tanto, el servidor envía un mensaje que interrumpe el bloqueo oportunista al cliente X. Client X envía ahora el mensaje de cierre a través de la red, evento 13. El evento 14 sigue a medida que el servidor abre el archivo para el cliente Y. La aplicación en el cliente X ha cerrado el archivo, por lo que no realiza más transferencias hacia o desde el servidor para ese archivo. El cliente Y comienza las transferencias de datos como de costumbre en el evento 15.

Entre el momento en que el cliente X se le concede el bloqueo en el archivo en el evento 2 y el cierre final en el evento 13, los datos de archivos que el cliente ha almacenado en caché son válidos, a pesar de las operaciones de apertura y cierre de la aplicación que intervienen. Sin embargo, una vez interrumpido el bloqueo oportunista, los datos almacenados en caché no se pueden considerar válidos.

## <a name="filter-opportunistic-lock"></a>Filtrar bloqueo oportunista

En el diagrama siguiente se muestra una vista de tráfico de red de un bloqueo oportunista de filtro. Las flechas indican la dirección del movimiento de datos, si existe.



| Evento | Cliente X                                | Servidor                   | Cliente Y                    |
|-------|-----------------------------------------|--------------------------|-----------------------------|
| 1     | Abre el archivo sin derechos de acceso = => |                          |                             |
| 2     |                                         | <= = abre el archivo    |                             |
| 3     | Filtro de solicitudes Lock = =>              |                          |                             |
| 4     |                                         | <= = concede el bloqueo       |                             |
| 5     | Abre el archivo para lectura = =>           |                          |                             |
| 6     |                                         | <= = vuelve a abrir el archivo  |                             |
| 7     | Lee datos mediante el identificador de lectura = => |                          |                             |
| 8     |                                         | <= = envía datos        |                             |
| 9     |                                         | <= = envía datos        |                             |
| 10    |                                         | <= = envía datos        |                             |
| 11    |                                         |                          | <= = abre el archivo       |
| 12    |                                         | Abre el archivo = =>    |                             |
| 13    |                                         |                          | <= = bloqueo de filtrado de solicitudes |
| 14    |                                         | Deniega el bloqueo de filtro = => |                             |
| 15    |                                         |                          | <= = lee datos           |
| 16    |                                         | Envía Data = =>        |                             |
| 17    | Lee datos (almacenados en caché)                     |                          |                             |
| 18    | Cierra File = =>                      |                          |                             |
| 19    |                                         |                          | <= = cierra el archivo          |



 

En el bloqueo oportunista de filtro, el cliente X abre un archivo, el evento 1 y el servidor responde en el evento 2. Después, el cliente solicita un bloqueo oportunista de filtro en el evento 3, seguido del servidor que concede el bloqueo oportunista en el evento 4. El cliente X vuelve a abrir el archivo para leerlo en el evento 5, al que el servidor responde en el evento 6. Después, el cliente intenta leer los datos, a los que el servidor responde con datos, evento 8.

El evento 9 muestra el bloqueo oportunista de filtro en el trabajo. El servidor se lee por la delantera del cliente y envía los datos a través de la red, aunque el cliente no lo haya solicitado. El cliente almacena en caché los datos. En el evento 10, el servidor también anticipa una solicitud futura de datos y envía otra parte del archivo para que el cliente lo almacene en la memoria caché.

En el evento 11 y 12, otro cliente, Y, abre el archivo. El cliente Y también solicita un bloqueo oportunista de filtro. En el evento 14, el servidor lo deniega. En el evento 15, el cliente Y solicita los datos, que el servidor envía en el evento 16. Ninguno de esto afecta a Client X. En cualquier momento, otro cliente puede abrir este archivo para el acceso de lectura. Ningún otro cliente afecta al bloqueo del filtro del cliente X.

El evento 17 muestra los datos de lectura del cliente X. Sin embargo, dado que el servidor ya ha enviado los datos y el cliente los ha almacenado en la memoria caché, ningún tráfico cruza la red.

En este ejemplo, el cliente X nunca intenta leer todos los datos del archivo, por lo que la lectura anticipada indicada por los eventos 9 y 10 está "desperdiciada"; es decir, los datos nunca se utilizan realmente. Se trata de una pérdida aceptable porque la lectura previa sped la aplicación.

En el evento 18, el cliente X cierra el archivo. El redirector de red del cliente abandona los datos almacenados en caché. El servidor cierra el archivo.

 

 



