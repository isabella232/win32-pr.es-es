---
description: 'Más información acerca de: niveles de seguimiento de Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Niveles de seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716627"
---
# <a name="winsock-tracing-levels"></a>Niveles de seguimiento de Winsock

## <a name="levels-of-winsock-tracing"></a>Niveles de seguimiento de Winsock

Hay dos niveles de registro posibles en el seguimiento de Winsock:

-   Información
-   Verbose

El nivel de información realiza el seguimiento de los eventos de creación y cierre de socket, así como cualquier error que se produzca en el socket.

El nivel detallado incluye los eventos de nivel de información y agrega seguimiento adicional para los eventos de envío y recepción. El registro detallado se utilizaría para detectar problemas de daños en el búfer, así como aplicaciones mal escritas.

Se puede usar la información o el nivel detallado con el seguimiento de eventos de red Winsock. El seguimiento de cambios del catálogo Winsock solo admite el nivel de información.

## <a name="information-event-tracing"></a>Seguimiento de eventos de información

En la siguiente lista se detallan las operaciones de socket de eventos de red Winsock cuyo seguimiento se realiza en el nivel de información:

-   Creación de sockets

    Se ha registrado un evento en la creación de sockets que se puede usar para realizar un seguimiento de la duración de un socket. Estos eventos también incluyen sockets creados al aceptar conexiones en un socket de escucha.

-   Bind

    La dirección IP local se registra para ayudar a correlacionar la información de seguimiento de Winsock con las llamadas de socket de una aplicación.

-   Conectar

    La dirección IP remota del socket conectado se registra para ayudar a correlacionar la información de seguimiento de Winsock con las llamadas de socket de una aplicación.

-   Anulaciones y cancelaciones iniciadas por Winsock

    Cada vez que Winsock anula o cancela activamente una solicitud, se registra el evento.

-   Restablecimientos iniciados por transporte

    Cada vez que el transporte subyacente indica que se ha restablecido una conexión, se registra el evento.

-   Errores de envío y recepción

    Siempre que se produce un error en una llamada de envío o recepción al transporte subyacente, se registra el evento.

-   Desconectar socket y cerrar

    Se registra un evento cuando se cierra un identificador de socket.

## <a name="verbose-event-tracing"></a>Seguimiento detallado de eventos

Se realiza un seguimiento de todos los eventos de información en el nivel detallado. En la siguiente lista se detallan las operaciones adicionales de socket de eventos de red Winsock cuyo seguimiento se realiza en el nivel detallado:

-   Búferes de envío y recepción

    Los eventos se registran en las direcciones de búfer de usuario y las longitudes cuando las llamadas de envío y recepción se publican en Winsock, así como cuando se completan estas llamadas. Esto resulta útil para diagnosticar problemas de reutilización de búferes, así como un uso ineficaz de los búferes.

-   Opciones de socket

    Un evento se registra cuando una aplicación cambia determinados valores de opción de socket. Algunas de las opciones registradas incluyen \_ SNDBUF, por lo que \_ RCVBUF, SiO \_ habilitan la \_ \_ puesta en cola circular y FIONBIO.

-   WSAPoll y SELECT

    Se registra un evento del uso de [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) de una aplicación y se [**seleccionan**](/windows/desktop/api/Winsock2/nf-winsock2-select) llamadas que se pueden usar para encontrar cuellos de botella de rendimiento.

-   Anulaciones y cancelaciones iniciadas por Winsock

    Cada vez que Winsock anula o cancela activamente una solicitud, se registra el evento.

-   Máscara de eventos

    Se registra un evento de la máscara de eventos que una aplicación registra para usar la función [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .

-   Datagrama

    Se registra un evento cada vez que llega un datagrama y no hay espacio en el búfer en el que copiarlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Detalles de seguimiento de cambios de catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Detalles de seguimiento de eventos de red Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
