---
description: En este tema se describe cómo una aplicación se conecta a un grupo del mismo nivel mediante las API de agrupación del mismo nivel.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: Cómo conectarse a un grupo del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3f41342573742e634a6e7ebce283188f3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667427"
---
# <a name="how-to-connect-to-a-peer-group"></a>Cómo conectarse a un grupo del mismo nivel

En este tema se describe cómo una aplicación se conecta a un grupo del mismo nivel mediante las API de agrupación del mismo nivel.

## <a name="joining-a-peer-group"></a>Unirse a un grupo del mismo nivel

Para unirse a un grupo del mismo nivel, llame a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), pasando el nombre de identidad del elemento del mismo nivel y la invitación (y un nombre de nube PNRP opcional, si el nombre de la nube en la invitación es ambiguo).

Si se realiza correctamente, [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) devuelve un identificador al grupo del mismo nivel.

Si el elemento del mismo nivel ha unido previamente el grupo del mismo nivel y, a continuación, ha cerrado el identificador, se debe volver a abrir el grupo del mismo nivel llamando a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) y pasando el nombre del grupo del mismo nivel. Esta llamada devuelve un nuevo identificador de grupo del mismo nivel.

Una vez que el grupo del mismo nivel se ha unido correctamente, el elemento del mismo nivel puede conectarse directamente al grupo del mismo nivel y comenzar a interactuar llamando a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect). Después de la conexión, se considera que el elemento del mismo nivel está "en línea".

Si una aplicación no va a interactuar con el grupo en el momento, puede permanecer sin conexión. Si decide participar directamente en el grupo del mismo nivel en una instancia posterior, una llamada subsiguiente a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) lo pondrá en línea. Una vez que un elemento del mismo nivel se une al grupo del mismo nivel, se debe conectar al menos una vez antes de poder publicar registros en el grupo del mismo nivel.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Abrir un grupo del mismo nivel sin conexión (sin conexión)

A menudo, puede que desee que una aplicación se conecte a un grupo del mismo nivel, pero no la participe directamente, la recepción y publicación de actualizaciones de registros, pero no el envío ni la recepción de mensajes de datos. Una aplicación se encuentra en este estado "sin conexión" inmediatamente después de que se haya llamado a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) .

Una aplicación sin conexión puede conectarse en cualquier momento llamando a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect). Una vez conectado, un grupo del mismo nivel no puede desconectarse hasta que todas las demás aplicaciones asociadas a esta identidad y que comparten este grupo también tengan conexiones cerradas con él.

Un grupo del mismo nivel es un recurso compartido, con el mismo grupo del mismo nivel disponible para varias aplicaciones. Si hay más de una aplicación para la misma identidad y usuario de Windows que usa el mismo grupo del mismo nivel, también comparten la misma base de datos y las mismas conexiones subyacentes (vecinos y directos). Si una de estas aplicaciones llama a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), todas las demás aplicaciones de esta identidad o usuario que participa en el grupo también se conectan al grupo. Si una aplicación agrega un registro mientras el grupo está sin conexión, otras aplicaciones también podrán verlo. Como resultado, una aplicación debe estar lista para conectarse en cualquier momento.

## <a name="connecting-to-a-peer-group-online"></a>Conexión a un grupo del mismo nivel (en línea)

Para empezar a participar en un grupo, llame a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) después de crear, unirse o abrir el grupo. En este estado, las conexiones directas se pueden abrir con otros elementos del mismo nivel que participan en el mismo grupo mediante una llamada a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection).

Para detectar si se ha producido un error en un intento de conexión, Regístrese para el \_ evento error de conexión de eventos de grupo del mismo nivel \_ \_ \_ . Este evento se desencadena si la infraestructura de agrupación no puede encontrar otro miembro al que conectarse o si se produce un error en la conexión antes de que se sincronice la base de datos del grupo y no se puede establecer otra conexión.

Aunque es posible que varias aplicaciones que se ejecutan en el mismo nivel y que participan en el mismo grupo con la misma identidad del mismo nivel estén sin conexión, una llamada a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) por parte de cualquiera de las aplicaciones produce la conexión de todas las aplicaciones.

Además, si una aplicación del mismo nivel se ha conectado al grupo, las demás aplicaciones que llaman a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) también se conectan de inmediato. Si una aplicación llama a [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), el identificador se cierra solo para esa aplicación. Por lo tanto, una llamada subsiguiente a **PeerGroupOpen** por parte de la aplicación devuelve un nuevo identificador de grupo y la aplicación se pone en línea inmediatamente si cualquier otra aplicación que participa en el mismo grupo sigue conectada.

## <a name="sending-and-receiving-data"></a>Envío y recepción de datos

Para enviar y recibir datos entre nodos de miembros específicos del grupo, se deben establecer conexiones directas con los miembros con los que pretende interactuar. Establecer una conexión directa es una llamada asincrónica a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), pasando el identificador de un grupo conectado y la identidad del elemento del mismo nivel dentro del grupo al que desea conectarse. Este método devolverá un identificador de conexión. Si la llamada se realiza correctamente, \_ \_ \_ \_ se genera un evento de conexión directa de evento de grupo del mismo nivel en el elemento del mismo nivel, validando el identificador de conexión.

Para recibir conexiones directas de otros equipos del mismo nivel en línea, Regístrese para el evento de conexión directa de evento de grupo del mismo nivel \_ \_ \_ \_ con una llamada a [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent).

Una vez que se ha establecido correctamente una conexión directa, la aplicación puede empezar a enviar datos con llamadas a [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata), pasando el identificador de conexión válido. El orden de las transmisiones de datos de varias partes se controla mediante **PeerGroupSendData**. Sin embargo, las aplicaciones deben implementar una pila de protocolos adecuada para controlar los datos opacos devueltos por esta llamada API.

Para recibir datos a través de una conexión directa, la aplicación debe registrarse para el evento de datos de entrada de evento de grupo del mismo nivel \_ \_ \_ \_ con [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). El controlador de eventos es responsable de obtener y ordenar los datos opacos y pasarlos a la aplicación. Estos datos se obtienen dentro del controlador de eventos mediante una llamada a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) con el identificador de los eventos registrados.

Una conexión directa se cierra llamando a [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) y pasando el identificador de conexión obtenido por una llamada anterior a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) o recibido en los datos de evento para \_ la \_ conexión directa del grupo de eventos del mismo nivel \_ \_ .

 

 



