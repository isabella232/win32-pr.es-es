---
description: En este tema se describe cómo una aplicación se conecta a un grupo del mismo nivel mediante las API de agrupación del mismo nivel.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: Cómo Conectar a un grupo del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3f41342573742e634a6e7ebce283188f3ffd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069244"
---
# <a name="how-to-connect-to-a-peer-group"></a>Cómo Conectar a un grupo del mismo nivel

En este tema se describe cómo una aplicación se conecta a un grupo del mismo nivel mediante las API de agrupación del mismo nivel.

## <a name="joining-a-peer-group"></a>Unión a un grupo del mismo nivel

Para unirse a un grupo del mismo nivel, llame a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), pasando el nombre de identidad del mismo nivel y la invitación (y un nombre de nube PNRP opcional, si el nombre de la nube de la invitación es ambiguo).

Si se realiza [**correctamente, PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) devuelve un identificador al grupo del mismo nivel.

Si el mismo nivel se ha unido previamente al grupo del mismo nivel y, a continuación, ha cerrado el identificador, el grupo del mismo nivel debe volver a abrirse llamando a [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) y pasando el nombre del grupo del mismo nivel. Esta llamada devuelve un nuevo identificador de grupo del mismo nivel.

Una vez que el grupo del mismo nivel se ha unido correctamente, el mismo nivel puede conectarse directamente al grupo del mismo nivel y empezar a interactuar llamando a [**PeerGroupConnect.**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) Después de conectarse, se considera que el mismo nivel está "en línea".

Si una aplicación no interactúa con el grupo en ese momento, puede permanecer "sin conexión". Si decide participar directamente en el grupo del mismo nivel en una instancia posterior, una llamada posterior a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) lo pondrá en línea. Una vez que un mismo nivel se ha unido al grupo del mismo nivel, debe conectarse al menos una vez antes de poder publicar registros en el grupo del mismo nivel.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Abrir un grupo del mismo nivel sin conectarse (sin conexión)

A menudo, es posible que desee que una aplicación se conecte a un grupo del mismo nivel, pero no la participe directamente, recibiendo y publicando actualizaciones de registros, pero sin enviar ni recibir mensajes de datos. Una aplicación se encuentra en este estado "sin conexión" inmediatamente después de llamar a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen.**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)

Una aplicación sin conexión puede conectarse en cualquier momento llamando a [**PeerGroupConnect.**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) Una vez conectado, un grupo del mismo nivel no puede desconectarse hasta que todas las demás aplicaciones asociadas a esta identidad y compartir este grupo también tengan conexiones cerradas a él.

Un grupo del mismo nivel es un recurso compartido, con el mismo grupo del mismo nivel disponible para varias aplicaciones. Si más de una aplicación para la misma identidad y Windows usuario usa el mismo grupo del mismo nivel, también comparte la misma base de datos y conexiones subyacentes (vecino y directo). Si alguna de estas aplicaciones llama a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), todas las demás aplicaciones de esta identidad o usuario que participan en el grupo también se conectan al grupo. Si una aplicación agrega un registro mientras el grupo está sin conexión, otras aplicaciones también podrán verlo. Como resultado, una aplicación debe estar lista para estar en línea en cualquier momento.

## <a name="connecting-to-a-peer-group-online"></a>Conectarse a un grupo del mismo nivel (en línea)

Para empezar a participar en un grupo, llame a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) después de crear, unirse o abrir el grupo. En este estado, se pueden abrir conexiones directas con otros elementos del mismo nivel que participan en el mismo grupo llamando a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection).

Para detectar si se ha produce un error en un intento de conexión, regístrese para el evento PEER \_ GROUP \_ EVENT CONNECTION \_ \_ FAILED. Este evento se genera si la infraestructura de agrupación no encuentra otro miembro al que conectarse, o si se produce un error en la conexión antes de que se sincronice la base de datos de grupo y no se pueda establecer otra conexión.

Aunque varias aplicaciones que se ejecutan en el mismo nivel y participan en el mismo grupo con la misma identidad del mismo nivel pueden estar sin conexión, una llamada a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) por parte de cualquiera de las aplicaciones da lugar a que todas las aplicaciones se conecten.

Además, si una aplicación del mismo nivel se ha conectado al grupo, cualquier otra aplicación que llame a [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) también se conectará inmediatamente. Si una aplicación llama a [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), el identificador se cierra solo para esa aplicación. Por lo tanto, una llamada posterior a **PeerGroupOpen** por parte de la aplicación devuelve un nuevo identificador de grupo y la aplicación se conecta inmediatamente si cualquier otra aplicación que participa en el mismo grupo todavía está conectada.

## <a name="sending-and-receiving-data"></a>Envío y recepción de datos

Para enviar y recibir datos entre nodos miembros específicos del grupo, se deben establecer conexiones directas con los miembros con los que desea interactuar. Establecer una conexión directa es una llamada asincrónica a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), pasando el identificador de un grupo conectado, así como la identidad del mismo nivel dentro del grupo al que desea conectarse. Este método devolverá un identificador de conexión. Si la llamada se realiza correctamente, se genera un evento PEER GROUP EVENT DIRECT CONNECTION en el mismo \_ \_ \_ \_ nivel, validando el identificador de conexión.

Para recibir conexiones directas de otros elementos del mismo nivel en línea, regístrese para el evento PEER GROUP EVENT DIRECT CONNECTION con una llamada \_ \_ a \_ \_ [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent).

Una vez que se ha establecido correctamente una conexión directa, la aplicación puede empezar a enviar datos con llamadas a [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)y pasar el identificador de conexión válido. **PeerGroupSendData** controla el orden de las transmisiones de datos de varias partes. Sin embargo, las aplicaciones deben implementar una pila de protocolos adecuada para controlar los datos opacos devueltos por esta llamada API.

Para recibir datos a través de una conexión directa, la aplicación debe registrarse para el evento PEER \_ GROUP \_ EVENT \_ INCOMING DATA con \_ [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). El controlador de eventos es responsable de obtener y ordenar los datos opacos y de pasarlos a la aplicación. Estos datos se obtienen en el controlador de eventos llamando a [**PeerGroupGetEventData con**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) el identificador de los eventos registrados.

Una conexión directa se cierra llamando a [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) y pasando el identificador de conexión obtenido por una llamada anterior a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) o recibido en los datos de evento para PEER \_ EVENT GROUP DIRECT \_ \_ \_ CONNECTION.

 

 



