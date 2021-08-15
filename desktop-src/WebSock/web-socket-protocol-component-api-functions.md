---
title: Funciones de la API del componente de protocolo WebSocket
description: La API del componente de protocolo WebSocket define estas funciones.
ms.assetid: B833D18D-286C-4D32-A9C7-D5D5806EC306
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d88a4ef8eb9caa0e409d0ded60b6dffd2717dc74d1b2cdddeb08ee6d9de08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330343"
---
# <a name="websocket-protocol-component-api-functions"></a>Funciones de la API del componente de protocolo WebSocket

La API del componente de protocolo WebSocket define estas funciones.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                             | Descripción                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WebSocketAbortHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketaborthandle)<br/>                   | anula un identificador de sesión de WebSocket creado por [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) o [**WebSocketCreateServerHandle.**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle)<br/>   |
| [**WebSocketBeginClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginclienthandshake)<br/> | comienza el protocolo de enlace del lado cliente.<br/>                                                                                                                                                                |
| [**WebSocketBeginServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketbeginserverhandshake)<br/> | comienza el protocolo de enlace del lado servidor.<br/>                                                                                                                                                                |
| [**WebSocketCompleteAction**](/windows/desktop/api/Websocket/nf-websocket-websocketcompleteaction)<br/>             | completa una acción iniciada por [**WebSocketGetAction**](/windows/desktop/api/websocket/nf-websocket-websocketgetaction).<br/>                                                                                                             |
| [**WebSocketCreateClientHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateclienthandle)<br/>     | crea un identificador de sesión de WebSocket del lado cliente.<br/>                                                                                                                                                  |
| [**WebSocketCreateServerHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketcreateserverhandle)<br/>     | crea un identificador de sesión de WebSocket del lado servidor.<br/>                                                                                                                                                  |
| [**WebSocketDeleteHandle**](/windows/desktop/api/Websocket/nf-websocket-websocketdeletehandle)<br/>                 | elimina un identificador de sesión de WebSocket creado por [**WebSocketCreateClientHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateclienthandle) o [**WebSocketCreateServerHandle**](/windows/desktop/api/websocket/nf-websocket-websocketcreateserverhandle).<br/>  |
| [**WebSocketEndClientHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendclienthandshake)<br/>     | completa el protocolo de enlace del lado cliente.<br/>                                                                                                                                                             |
| [**WebSocketEndServerHandshake**](/windows/desktop/api/Websocket/nf-websocket-websocketendserverhandshake)<br/>     | completa el protocolo de enlace del lado servidor.<br/>                                                                                                                                                             |
| [**WebSocketGetAction**](/windows/desktop/api/Websocket/nf-websocket-websocketgetaction)<br/>                       | devuelve una acción de una llamada a [**WebSocketSend,**](/windows/desktop/api/websocket/nf-websocket-websocketsend) [**WebSocketReceive**](/windows/desktop/api/websocket/nf-websocket-websocketreceive) [**o WebSocketCompleteAction**](/windows/desktop/api/websocket/nf-websocket-websocketcompleteaction).<br/> |
| [**WebSocketGetGlobalProperty**](/windows/desktop/api/Websocket/nf-websocket-websocketgetglobalproperty)<br/>       | obtiene una única propiedad WebSocket.<br/>                                                                                                                                                                |
| [**WebSocketReceive**](/windows/desktop/api/Websocket/nf-websocket-websocketreceive)<br/>                           | agrega una operación de recepción a la cola de operaciones del componente de protocolo.<br/>                                                                                                                              |
| [**WebSocketSend**](/windows/desktop/api/Websocket/nf-websocket-websocketsend)<br/>                                 | agrega una operación de envío a la cola de la operación de componente de protocolo.<br/>                                                                                                                                 |



 

 

