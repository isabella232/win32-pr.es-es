---
description: Diagramas de vistas de tráfico de red para un bloqueo oportunista de nivel 1, un bloqueo oportunista por lotes y un bloqueo oportunista de filtro.
ms.assetid: 78830113-b18e-40c7-8ec4-8896dbc58030
title: Ejemplos de bloqueos oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8b8a0c5b04897ddc2fc8f2e3bdec20f2fdb02d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069880"
---
# <a name="opportunistic-lock-examples"></a>Ejemplos de bloqueos oportunistas

En los ejemplos siguientes se muestran los movimientos de datos y mensajes SMB a medida que se realizan bloqueos oportunistas y se rotan. Tenga en cuenta que los clientes pueden almacenar en caché datos de atributos de archivo, así como datos de archivo.

Tenga en cuenta también que estos ejemplos se basan en situaciones en las que las aplicaciones cliente solicitan bloqueos oportunistas desde servidores remotos. El redirector de red y el servidor remoto inician automáticamente estos procesos: no hay ninguna participación directa por parte de la aplicación cliente o las aplicaciones. Los procesos descritos en estos ejemplos se pueden generalizar en situaciones en las que las aplicaciones cliente locales solicitan directamente bloqueos oportunistas desde el sistema de archivos local, con la excepción de que no interviene ningún intercambio de datos a través de la red.

## <a name="level-1-opportunistic-lock"></a>Bloqueo oportunista de nivel 1

En el diagrama siguiente se muestra una vista del tráfico de red de un bloqueo oportunista de nivel 1 en un archivo. Las flechas indican la dirección del movimiento de datos, si las hay.



| Evento | Cliente X                                          | Servidor                                   | Cliente Y                                          |
|-------|---------------------------------------------------|------------------------------------------|---------------------------------------------------|
| 1     | Abre el archivo, solicita el bloqueo de nivel 1 ==>          |                                          |                                                   |
| 2     |                                                   | <== Concesión de bloqueo oportunista de nivel 1 |                                                   |
| 3     | Realiza operaciones de lectura, escritura y otras operaciones ==> |                                          |                                                   |
| 4     |                                                   |                                          | <== Solicitudes para abrir el archivo                      |
| 5     |                                                   | <== Interrumpe el bloqueo oportunista         |                                                   |
| 6     | Descarta los datos de lectura adelantada                          |                                          |                                                   |
| 7     | Escribe datos ==>                                |                                          |                                                   |
| 8     | Envía el mensaje "close" o "done" ==>            |                                          |                                                   |
| 9     |                                                   | Oks open operation ==>              |                                                   |
| 10    | Realiza operaciones de lectura, escritura y otras operaciones ==> |                                          | <== Realiza operaciones de lectura, escritura y otras operaciones |



 

En el evento 1, el cliente X abre un archivo y, como parte de la operación de apertura, solicita un bloqueo oportunista de nivel 1 en el archivo. En el caso 2, el servidor concede el bloqueo de nivel 1 porque ningún otro cliente tiene el archivo abierto. El cliente continúa con el acceso al archivo de la manera habitual en el evento 3.

En el caso 4, el cliente Y intenta abrir el archivo y solicita un bloqueo oportunista. El servidor ve que el cliente X tiene el archivo abierto. El servidor omite la solicitud de Y mientras el cliente X vacía los datos de escritura y abandona su caché de lectura para el archivo.

El servidor fuerza a X a limpiar mediante el envío a X de un mensaje SMB que rompa el bloqueo oportunista, evento 5. El cliente X descarta "en modo silencioso" los datos de lectura adelantada; en otras palabras, este proceso no genera tráfico de red. En el evento 7, el cliente X escribe los datos de escritura almacenados en caché en el servidor. Cuando el cliente X ha terminado de escribir datos almacenados en caché en el servidor, el cliente X envía un mensaje "cerrar" o "listo" al servidor, evento 8.

Una vez que se ha notificado al servidor que el cliente X ha terminado de vaciar su caché de escritura en el servidor o que ha cerrado el archivo, el servidor puede abrir el archivo para el cliente Y, en el evento 9. Dado que el servidor ahora tiene dos clientes con el mismo archivo abierto, no concede un bloqueo oportunista a ninguno de los dos. Ambos clientes proceden a leer del archivo y uno o ninguno escribe en el archivo.

## <a name="batch-opportunistic-lock"></a>Bloqueo oportunista por lotes

En el diagrama siguiente se muestra una vista del tráfico de red de un bloqueo oportunista por lotes. Las flechas indican la dirección del movimiento de datos, si las hay.



| Evento | Cliente X                               | Servidor                                 | Cliente Y                                          |
|-------|----------------------------------------|----------------------------------------|---------------------------------------------------|
| 1     | Abre el archivo, solicita el bloqueo por lotes ==> |                                        |                                                   |
| 2     |                                        | <== Concede bloqueo oportunista por lotes |                                                   |
| 3     | Lee el archivo ==>                      |                                        |                                                   |
| 4     |                                        | <== Envía datos                      |                                                   |
| 5     | Cierra el archivo.                            |                                        |                                                   |
| 6     | Abre el archivo.                             |                                        |                                                   |
| 7     | Búsqueda de datos                      |                                        |                                                   |
| 8     | Lee datos ==>                      |                                        |                                                   |
| 9     |                                        | <== Envía datos                      |                                                   |
| 10    | Cierra el archivo.                            |                                        |                                                   |
| 11    |                                        |                                        | <== Abre el archivo                                 |
| 12    |                                        | <== Interrumpe el bloqueo oportunista       |                                                   |
| 13    | Cierra el archivo ==>                     |                                        |                                                   |
| 14    |                                        | Oks open operation ==>            |                                                   |
| 15    |                                        |                                        | <== Realiza operaciones de lectura, escritura y otras operaciones |



 

En el bloqueo oportunista por lotes, el cliente X abre un archivo, evento 1, y el servidor concede al cliente X un bloqueo por lotes en el evento 2. El cliente X intenta leer datos, evento 3, al que el servidor responde con datos, evento 4.

El evento 5 muestra el bloqueo oportunista por lotes en el trabajo. La aplicación del cliente X cierra el archivo. Sin embargo, el redirector de red filtra la operación de cierre y no transmite un mensaje de cierre, por lo que realiza un cierre "silencioso". El redirector de red puede hacerlo porque el cliente X es el único propietario del archivo. Más adelante, en el evento 6, la aplicación vuelve a abrir el archivo. De nuevo, no hay ningún flujo de datos a través de la red. En lo que respecta al servidor, este cliente ha tenido el archivo abierto desde el evento 2.

Los eventos 7, 8 y 9 muestran el curso habitual del tráfico de red. En el evento 10, se produce otro cierre silencioso.

En el evento 11, el cliente Y intenta abrir el archivo. La vista del servidor del archivo es que el cliente X lo tiene abierto, aunque la aplicación del cliente X lo haya cerrado. Por lo tanto, el servidor envía un mensaje que separa el bloqueo oportunista al cliente X. El cliente X envía ahora el mensaje de cierre a través de la red, evento 13. El evento 14 sigue cuando el servidor abre el archivo para el cliente Y. La aplicación en el cliente X ha cerrado el archivo, por lo que no realiza más transferencias hacia o desde el servidor para ese archivo. El cliente Y comienza las transferencias de datos como de costumbre en el evento 15.

Entre el momento en que se concede al cliente X el bloqueo en el archivo en el evento 2 y el cierre final en el evento 13, los datos de archivo que el cliente ha almacenado en caché son válidos, a pesar de las operaciones de apertura y cierre de la aplicación que interviene. Sin embargo, una vez que se ha roto el bloqueo oportunista, los datos almacenados en caché no se pueden considerar válidos.

## <a name="filter-opportunistic-lock"></a>Filtrar bloqueo oportunista

En el diagrama siguiente se muestra una vista del tráfico de red de un bloqueo oportunista de filtro. Las flechas indican la dirección del movimiento de datos, si las hay.



| Evento | Cliente X                                | Servidor                   | Cliente Y                    |
|-------|-----------------------------------------|--------------------------|-----------------------------|
| 1     | Abre el archivo sin derechos de acceso ==> |                          |                             |
| 2     |                                         | <== Abre el archivo    |                             |
| 3     | Requests filter lock==>              |                          |                             |
| 4     |                                         | <== Concesión de bloqueo       |                             |
| 5     | Abre el archivo para leer ==>           |                          |                             |
| 6     |                                         | <== Vuelve a abrir el archivo  |                             |
| 7     | Lee datos mediante el identificador de lectura ==> |                          |                             |
| 8     |                                         | <== Envía datos        |                             |
| 9     |                                         | <== Envía datos        |                             |
| 10    |                                         | <== Envía datos        |                             |
| 11    |                                         |                          | <== Abre el archivo       |
| 12    |                                         | Abre el archivo ==>    |                             |
| 13    |                                         |                          | <== Bloqueo de filtro de solicitudes |
| 14    |                                         | Deniega el filtro lock==> |                             |
| 15    |                                         |                          | <== Lee datos           |
| 16    |                                         | Envía datos ==>        |                             |
| 17    | Lee datos (almacenados en caché)                     |                          |                             |
| 18    | Cierra el archivo ==>                      |                          |                             |
| 19    |                                         |                          | <== Cierra el archivo          |



 

En el bloqueo oportunista del filtro, el cliente X abre un archivo, el evento 1, y el servidor responde en el evento 2. A continuación, el cliente solicita un bloqueo oportunista de filtro en el evento 3, seguido del servidor que concede el bloqueo oportunista en el evento 4. A continuación, el cliente X vuelve a abrir el archivo para leerlo en el evento 5, al que el servidor responde en el evento 6. A continuación, el cliente intenta leer los datos, a los que el servidor responde con datos, evento 8.

El evento 9 muestra el bloqueo oportunista del filtro en el trabajo. El servidor lee delante del cliente y envía los datos a través de la red, aunque el cliente no los haya solicitado. El cliente almacena en caché los datos. En el caso 10, el servidor también prevé una solicitud futura de datos y envía otra parte del archivo para que el cliente la almacena en caché.

En el evento 11 y 12, otro cliente, Y, abre el archivo. El cliente Y también solicita un bloqueo oportunista de filtro. En el caso 14, el servidor lo deniega. En el evento 15, el cliente Y solicita datos, que el servidor envía en el evento 16. Nada de esto afecta al cliente X. En cualquier momento, otro cliente puede abrir este archivo para el acceso de lectura. Ningún otro cliente afecta al bloqueo de filtro del cliente X.

El evento 17 muestra el cliente X leyendo datos. Sin embargo, dado que el servidor ya ha enviado los datos y el cliente los ha almacenado en caché, no hay tráfico que cruce la red.

En este ejemplo, el cliente X nunca intenta leer todos los datos del archivo, por lo que la lectura adelantada indicada por los eventos 9 y 10 es "desperdiciada"; es decir, los datos nunca se usan realmente. Se trata de una pérdida aceptable porque la lectura adelantada ha puesto en marcha la aplicación.

En el evento 18, el cliente X cierra el archivo. El redirector de red del cliente abandona los datos almacenados en caché. El servidor cierra el archivo.

 

 



