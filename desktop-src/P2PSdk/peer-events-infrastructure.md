---
description: La infraestructura del mismo nivel usa eventos para notificar a las aplicaciones los cambios que se han producido dentro de una red del mismo nivel, por ejemplo, un nodo que se agrega o quita de un gráfico.
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: Infraestructura de eventos del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6347ad6a7dd0cf2fae4a0aa623bfda48ab0aa9f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161070"
---
# <a name="peer-events-infrastructure"></a>Infraestructura de eventos del mismo nivel

La infraestructura del mismo nivel usa eventos para notificar a las aplicaciones los cambios que se han producido dentro de una red del mismo nivel, por ejemplo, un nodo que se agrega o quita de un gráfico. Las infraestructuras peer graphing y peer grouping usan la infraestructura de eventos del mismo nivel.

## <a name="receiving-peer-event-notification"></a>Recepción de notificaciones de eventos del mismo nivel

Un elemento del mismo nivel puede registrarse para recibir una notificación cuando cambia un atributo de un grafo o grupo, o se produce un evento del mismo nivel específico. Una aplicación del mismo nivel llama a la [**función PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) o [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) y pasa un identificador de evento a la infraestructura del mismo nivel, que se creó anteriormente mediante una llamada a [**CreateEvent**](graphing-reference-links.md). La infraestructura del mismo nivel usa el identificador para indicar a una aplicación que se ha producido un evento del mismo nivel.

La aplicación también pasa una serie de estructuras [**PEER \_ GRAPH EVENT \_ \_ REGISTRATION**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) o [**PEER GROUP EVENT \_ \_ \_ REGISTRATION**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) que indican a la infraestructura del mismo nivel los eventos del mismo nivel específicos para los que la aplicación solicita notificación. La aplicación también debe especificar exactamente cuántas estructuras se pasan.

## <a name="peer-graphing-events"></a>Eventos de grafos del mismo nivel

Una aplicación de Peer Graphing puede registrarse para recibir la notificación de 9 eventos de grafo del mismo nivel. Cada nombre de evento va precedido de **PEER \_ GRAPH \_ \_ EVENT**, por ejemplo, PEER GRAPH STATUS **\_ \_ \_ CHANGED**. A menos que se indique lo contrario, la información sobre un cambio se recupera mediante [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata).

-   **PEER \_ GRAPH \_ EVENT \_ STATUS \_ CHANGED** indica que se ha cambiado el estado de un gráfico; por ejemplo, un nodo se ha sincronizado con un gráfico.
-   **PEER \_ GRAPH \_ EVENT \_ PROPERTY \_ CHANGED** indica que se ha cambiado una propiedad de un grafo o grupo, por ejemplo, el nombre descriptivo de un gráfico ha cambiado.
    > [!Note]  
    > La aplicación debe llamar [**a PeerGraphGetProperties para**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) obtener la información modificada.

     

-   **PEER \_ GRAPH \_ EVENT \_ RECORD \_ CHANGED** indica que se cambia un registro, por ejemplo, se elimina un registro.
-   **PEER \_ GRAPH \_ EVENT \_ DIRECT \_ CONNECTION** indica que se ha cambiado una conexión directa, por ejemplo, que un nodo se ha conectado.
-   **PEER \_ GRAPH \_ EVENT \_ NEIGHBOR \_ CONNECTION** indica que se ha cambiado una conexión a un nodo vecino; por ejemplo, un nodo se ha conectado.
-   **PEER \_ GRAPH \_ EVENT \_ INCOMING DATA \_ indica** que se han recibido datos de una conexión directa o de un vecino.
-   **PEER \_ GRAPH \_ EVENT \_ CONNECTION \_ REQUIRED** indica que la infraestructura de grafos requiere una nueva conexión.
    > [!Note]  
    > Una llamada a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) se conecta a un nuevo nodo. Una llamada a [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) no devuelve datos.

     

-   **PEER \_ GRAPH \_ EVENT \_ NODE \_ CHANGED** indica que se ha cambiado la información de presencia del nodo, por ejemplo, una dirección IP.
-   **PEER \_ GRAPH \_ EVENT \_ SYNCHRONIZED** indica que se sincroniza un tipo de registro específico.

Una vez que una aplicación recibe la notificación de que se ha producido un evento del mismo nivel, la aplicación llama a [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)y pasa el identificador de evento del mismo nivel devuelto por [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent). La infraestructura del mismo nivel devuelve un puntero a una estructura [**\_ PEER GRAPH EVENT \_ \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) que contiene los datos solicitados. Se debe llamar a esta función hasta que **se devuelva PEER S NO EVENT \_ \_ \_ \_ DATA.**

Una vez que una aplicación no requiere una notificación de eventos del mismo nivel, la aplicación llama a [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)y pasa el identificador de evento del mismo nivel devuelto por [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) cuando se registró la aplicación.

## <a name="handling-graph-connection-referrals"></a>Control de Graph referencias de conexión

Cuando [**se llama a PeerGraphConnect,**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) se notifica al mismo nivel que se conecta si se ha correcto o no a través del evento asincrónico PEER GRAPH EVENT NEIGHBOR **\_ \_ \_ \_ CONNECTION.** Si se ha producido un error en la conexión debido a problemas de red específicos (por ejemplo, un firewall mal configurado), se genera el evento **PEER GRAPH EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION,** con el estado de conexión establecido en **PEER CONNECTION \_ \_ FAILED**.

Sin embargo, cuando un nodo del mismo nivel recibe una referencia cuando intenta conectarse a un nodo ocupado, se genera la CONEXIÓN DE VECINO DE EVENTO **\_ \_ \_ DE \_** GRAFO DEL MISMO NIVEL en el punto de conexión, con el estado de conexión establecido en CONEXIÓN DEL MISMO NIVEL CON **ERROR. \_ \_** El punto de conexión se puede hacer referencia a otro nodo que está ocupado y puede enviar una referencia, y el mismo evento y estado se genera en el mismo nodo del mismo nivel que se conecta. Esta cadena de referencias que produce el estado de evento **PEER \_ CONNECTION \_ FAILED** puede continuar hasta que se haya agotado el número máximo de intentos de conexión. El par no tiene un mecanismo para determinar la diferencia entre un intento de conexión completo y la referencia de conexión.

Para solucionar este problema, los desarrolladores deben considerar la posibilidad de usar los eventos de cambio de estado del grafo del mismo nivel para determinar si se ha intentado realizar la conexión. Si el evento no se recibe dentro de un período de tiempo específico, la aplicación puede suponer que se hace referencia al punto de conexión y que la aplicación del mismo nivel debe considerar que el intento de conexión es un error.

## <a name="peer-grouping-events"></a>Eventos de agrupación del mismo nivel

Una aplicación de agrupación del mismo nivel puede registrarse para recibir la notificación de 8 eventos del mismo nivel. Cada nombre de evento va precedido de **PEER \_ GROUP \_ EVENT; \_** por ejemplo, PEER GROUP EVENT STATUS **\_ \_ \_ \_ CHANGED**. A menos que se indique lo contrario, la información sobre un cambio se recupera mediante [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata).

-   **PEER \_ GROUP \_ EVENT \_ STATUS \_ CHANGED** indica que el estado del grupo ha cambiado. Hay dos valores de estado posibles: **PEER \_ GROUP STATUS \_ \_ LISTENING**, que indica que el grupo no tiene conexiones y está esperando nuevos miembros; y **PEER GROUP STATUS HAS \_ \_ \_ CONNECTIONS**, que indica que el grupo tiene al menos una conexión. Este valor de estado se puede obtener mediante una llamada [**a PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) después de que se genera este evento.
-   **PEER \_ GROUP \_ EVENT \_ PROPERTY \_ CHANGED** indica que el creador del grupo ha cambiado o actualizado las propiedades del grupo.
-   **PEER \_ GROUP \_ EVENT \_ RECORD \_ CHANGED** indica que se ha realizado una operación de registro. Este evento se genera cuando un par que participa en el grupo publica, actualiza o elimina un registro. Por ejemplo, este evento se genera cuando una aplicación de chat envía un mensaje de chat.
-   **PEER \_ GROUP \_ EVENT \_ MEMBER \_ CHANGED** indica que el estado de un miembro dentro del grupo ha cambiado. Los cambios de estado incluyen:
    -   **PEER \_ MIEMBRO \_ CONECTADO.** Un par se ha conectado al grupo.
    -   **PEER \_ MIEMBRO \_ DESCONECTADO.** Un par se ha desconectado del grupo.
    -   **PEER \_ MIEMBRO \_ UNIDO** A . Se ha publicado nueva información de pertenencia para un par.
    -   **PEER \_ MIEMBRO \_ ACTUALIZADO.** Un par se ha actualizado con nueva información, como una nueva dirección IP.
-   **PEER \_ GROUP \_ EVENT \_ NEIGHBOR \_ CONNECTION**. Los compañeros que participarán en conexiones de vecino dentro del grupo deben registrarse para este evento. Tenga en cuenta que el registro para este evento no permite que el mismo nivel reciba datos; El registro de este evento solo garantiza la notificación cuando se recibe una solicitud para una conexión de vecino.
-   **PEER \_ GROUP \_ EVENT \_ DIRECT \_ CONNECTION**. Los compañeros que participarán en conexiones directas dentro del grupo deben registrarse para este evento. Tenga en cuenta que el registro para este evento no permite que el mismo nivel reciba datos; El registro de este evento solo garantiza la notificación cuando se recibe una solicitud de conexión directa.
-   **PEER \_ AGRUPAR \_ DATOS \_ ENTRANTES DE \_ EVENTOS**. Los usuarios del mismo nivel que recibirán datos a través de una conexión directa o vecino deben registrarse para este evento. Cuando se genera este evento, los datos opacos transmitidos por el otro elemento del mismo nivel participante se pueden obtener llamando a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Tenga en cuenta que para recibir este evento, el mismo nivel debe haber registrado previamente para **PEER GROUP EVENT DIRECT \_ \_ \_ \_ CONNECTION** o **PEER GROUP EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION**.
-   **PEER \_ ERROR EN \_ LA CONEXIÓN DE EVENTOS DE \_ \_ GRUPO.** Error de conexión por algún motivo. No se proporciona ningún dato cuando se genera este evento y no se debe llamar a [**PeerGroupGetEventData.**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)

Una vez que una aplicación recibe la notificación de que se ha producido un evento del mismo nivel (excepto PEER **\_ GROUP EVENT CONNECTION \_ \_ \_ FAILED),** la aplicación llama a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)y pasa el identificador de evento del mismo nivel devuelto por [**PeerGroupRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) La infraestructura del mismo nivel devuelve un puntero a una [**estructura PEER GROUP EVENT \_ \_ \_ DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) que contiene los datos solicitados. Se debe llamar a esta función hasta que **se devuelva PEER S NO EVENT \_ \_ \_ \_ DATA.** Cuando una aplicación ya no requiere notificación para un evento del mismo nivel, se debe realizar una llamada a [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent), pasando el identificador de evento del mismo nivel devuelto por **PeerGroupRegisterEvent** cuando la aplicación se registró para el evento determinado.

## <a name="example-of-registering-for-peer-graphing-events"></a>Ejemplo de registro para eventos de grafos del mismo nivel

En el ejemplo de código siguiente se muestra cómo registrarse con los eventos de Peer Graphing.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it can be called for only
//           the events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents()
{
    HPEEREVENT  g_hPeerEvent = NULL;        // The one PeerEvent handle
    HANDLE      g_hEvent = NULL;            // Handle signaled by Graphing when we have an event
    HRESULT hr = S_OK;
    PEER_GRAPH_EVENT_REGISTRATION regs[] = {
        { PEER_GRAPH_EVENT_RECORD_CHANGED, 0 },
        { PEER_GRAPH_EVENT_NODE_CHANGED,   0 },
        { PEER_GRAPH_EVENT_STATUS_CHANGED, 0 },
        { PEER_GRAPH_EVENT_DIRECT_CONNECTION, 0 },
        { PEER_GRAPH_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        wprintf(L"CreateEvent call failed.\n");
        hr = E_OUTOFMEMORY;
    }
    else
    {
        hr = PeerGraphRegisterEvent(g_hGraph, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
        if (FAILED(hr))
        {
           wprintf(L"PeerGraphRegisterEvent call failed.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            wprintf(L"Could not set up event callback.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    return hr;
}
```



 

 



