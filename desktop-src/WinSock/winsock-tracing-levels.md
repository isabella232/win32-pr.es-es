---
description: 'Más información sobre: Niveles de seguimiento de Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Niveles de seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e1dbc746b90d77353d19b381c8eceed82eceec0d878b347bb3aa309a0df939b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733155"
---
# <a name="winsock-tracing-levels"></a>Niveles de seguimiento de Winsock

## <a name="levels-of-winsock-tracing"></a>Niveles de seguimiento de Winsock

Hay dos niveles de registro posibles en el seguimiento de Winsock:

-   Information
-   Verbose

El nivel de información hace un seguimiento de los eventos de creación y cierre del socket, así como los errores que se producen en el socket.

El nivel detallado incluye los eventos de nivel de información y agrega seguimiento adicional para los eventos de envío y recepción. El registro detallado se usaría para detectar problemas de daños en el búfer, así como aplicaciones mal escritas.

La información o el nivel detallado se pueden usar con el seguimiento de eventos de winsock Network. El seguimiento de cambios del catálogo de Winsock solo admite el nivel de información.

## <a name="information-event-tracing"></a>Seguimiento de eventos de información

En la lista siguiente se detallan las operaciones de socket de eventos de red de Winsock de las que se hace un seguimiento en el nivel de información:

-   Creación de sockets

    Un evento se registra en la creación de sockets que se puede usar para realizar un seguimiento de la duración de un socket. Estos eventos también incluyen sockets creados mediante la aceptación de conexiones en un socket de escucha.

-   Bind

    La dirección IP local se registra para ayudar a correlacionar la información de seguimiento de Winsock con las llamadas de socket de una aplicación.

-   Conectar

    La dirección IP remota del socket conectado se registra para ayudar a correlacionar la información de seguimiento de Winsock con las llamadas de socket de una aplicación.

-   Winsock-initiated aborts and cancels (Anulaciones y cancelaciones iniciadas por Winsock)

    Cada vez que Winsock anula o cancela activamente una solicitud, se registra el evento.

-   Restablecimientos iniciados por transporte

    Cada vez que el transporte subyacente indica que se ha restablecido una conexión, se registra el evento.

-   Errores de envío y recepción

    Cada vez que se produce un error en una llamada de envío o recepción al transporte subyacente, se registra el evento.

-   Desconexión y cierre del socket

    Se registra un evento cuando se cierra un identificador de socket.

## <a name="verbose-event-tracing"></a>Seguimiento detallado de eventos

Todos los eventos de información se seguimienton en el nivel detallado. En la lista siguiente se detallan las operaciones adicionales de socket de eventos de red de Winsock de las que se hace un seguimiento en el nivel detallado:

-   Búferes de envío y recepción

    Los eventos se registran de direcciones de búfer de usuario y longitudes cuando se publican llamadas de envío y recepción en Winsock, así como tras la finalización de estas llamadas. Esto es útil para diagnosticar problemas de volver a usar el búfer, así como para el uso ineficaz de los búferes.

-   Opciones de socket

    Se registra un evento cuando una aplicación cambia determinados valores de opción de socket. Algunas de las opciones registradas incluyen SO \_ SNDBUF, SO \_ RCVBUF, SIO \_ ENABLE CIRCULAR \_ \_ QUEUEING y FIONBIO.

-   WSAPoll y seleccione

    Se registra un evento del uso de [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) por parte de una aplicación y se seleccionan llamadas que se pueden usar para buscar cuellos de botella de rendimiento. [](/windows/desktop/api/Winsock2/nf-winsock2-select)

-   Winsock-initiated aborts and cancels (Anulaciones y cancelaciones iniciadas por Winsock)

    Cada vez que Winsock anula o cancela activamente una solicitud, se registra el evento.

-   Máscara de eventos

    Se registra un evento de la máscara de eventos que registra una aplicación para usar la [**función WSAEventSelect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)

-   Datagrama

    Un evento se registra cada vez que llega un datagrama y no hay ningún espacio de búfer en el que copiarlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control del seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Detalles del seguimiento de cambios del catálogo de Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Detalles del seguimiento de eventos de Winsock Network](winsock-tracing-event-details.md)
</dt> </dl>

 

 
