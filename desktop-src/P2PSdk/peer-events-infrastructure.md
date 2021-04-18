---
description: La infraestructura del mismo nivel usa eventos para notificar a las aplicaciones de los cambios que se han producido en una red del mismo nivel, por ejemplo, un nodo que se agrega o se quita de un gráfico.
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: Infraestructura de eventos del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6347ad6a7dd0cf2fae4a0aa623bfda48ab0aa9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667403"
---
# <a name="peer-events-infrastructure"></a>Infraestructura de eventos del mismo nivel

La infraestructura del mismo nivel usa eventos para notificar a las aplicaciones de los cambios que se han producido en una red del mismo nivel, por ejemplo, un nodo que se agrega o se quita de un gráfico. Las infraestructuras de gráficos del mismo nivel y de agrupación del mismo nivel usan la infraestructura de eventos del mismo nivel.

## <a name="receiving-peer-event-notification"></a>Recepción de la notificación de eventos del mismo nivel

Un elemento del mismo nivel puede registrarse para recibir notificaciones cuando cambia un atributo de un gráfico o un grupo, o cuando se produce un evento del mismo nivel específico. Una aplicación del mismo nivel llama a la función [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) o [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) y pasa un identificador de evento a la infraestructura del mismo nivel, que se crea antes mediante una llamada a [**CreateEvent**](graphing-reference-links.md). La infraestructura del mismo nivel usa el identificador para indicar a una aplicación que se ha producido un evento del mismo nivel.

La aplicación también pasa una serie de estructuras de registro de [**\_ eventos de grafos del mismo \_ \_ nivel**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) o de [**\_ registro de \_ eventos \_ de grupo del mismo**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) nivel que indican a la infraestructura del mismo nivel los eventos específicos del mismo nivel para los que la aplicación solicita la notificación. La aplicación también debe especificar exactamente el número de estructuras que se pasan.

## <a name="peer-graphing-events"></a>Eventos de gráficos del mismo nivel

Una aplicación de gráficos del mismo nivel puede registrarse para recibir notificaciones de 9 eventos de grafos del mismo nivel. Cada nombre de evento está precedido por **un \_ \_ \_ evento de grafo del mismo nivel**, por ejemplo, el **Estado del grafo del mismo nivel \_ \_ \_ ha cambiado**. A menos que se indique lo contrario, la información sobre un cambio se recupera mediante [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata).

-   **Del mismo nivel \_ El \_ Estado del evento de gráfico \_ \_ cambiado** indica que se ha cambiado el estado de un gráfico; por ejemplo, un nodo se ha sincronizado con un grafo.
-   **Del mismo nivel \_ \_ \_ \_ Cambiar propiedad de evento de gráfico** indica que se ha cambiado una propiedad de un gráfico o un grupo; por ejemplo, el nombre descriptivo de un gráfico ha cambiado.
    > [!Note]  
    > La aplicación debe llamar a [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) para obtener la información modificada.

     

-   **Del mismo nivel \_ El \_ registro de eventos de gráfico \_ \_ cambiado** indica que se ha cambiado un registro, por ejemplo, se elimina un registro.
-   **Del mismo nivel \_ La \_ \_ \_ conexión directa de eventos de gráfico** indica que se ha cambiado una conexión directa; por ejemplo, un nodo se ha conectado.
-   **Del mismo nivel \_ La \_ \_ \_ conexión de vecino del evento de gráfico** indica que se ha cambiado una conexión a un nodo vecino; por ejemplo, un nodo se ha conectado.
-   **Del mismo nivel \_ Los \_ \_ \_ datos entrantes del evento de gráfico** indican que los datos se han recibido de una conexión directa o de vecino.
-   **Del mismo nivel \_ La \_ conexión de eventos de gráfico \_ \_ requerida** indica que la infraestructura de gráficos requiere una nueva conexión.
    > [!Note]  
    > Una llamada a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) se conecta a un nuevo nodo. Una llamada a [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) no devuelve datos.

     

-   **Del mismo nivel \_ El \_ nodo de eventos de gráfico \_ \_ cambiado** indica que se ha cambiado la información de presencia del nodo, por ejemplo, una dirección IP ha cambiado.
-   **Del mismo nivel \_ El \_ evento de gráfico \_ sincronizado** indica que un tipo de registro específico está sincronizado.

Una vez que una aplicación recibe la notificación de que se ha producido un evento del mismo nivel, la aplicación llama a [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)y pasa el identificador de evento del mismo nivel devuelto por [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent). La infraestructura del mismo nivel devuelve un puntero a una estructura de [**\_ datos de \_ evento \_ de grafo del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) que contiene los datos solicitados. Se debe llamar a esta función hasta que no se devuelvan **\_ \_ \_ \_ datos del evento** .

Después de que una aplicación no requiera una notificación de eventos del mismo nivel, la aplicación llama a [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)y pasa el identificador de evento del mismo nivel devuelto por [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) cuando se registra la aplicación.

## <a name="handling-graph-connection-referrals"></a>Control de referencias de conexión de grafos

Cuando se llama a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) , se notifica al elemento del mismo nivel de conexión que se ha realizado correctamente o se ha producido un error a través del evento de **conexión de \_ \_ \_ vecino \_ del evento del elemento del mismo nivel** asincrónico Si se produjo un error en la conexión debido a un problema de red específico (por ejemplo, un firewall mal configurado), se genera el evento de **conexión de vecino del evento del grafo del mismo nivel \_ \_ \_ \_** , con el estado de conexión establecido en **\_ conexión \_ del mismo nivel**.

Sin embargo, cuando un elemento del mismo nivel recibe una referencia cuando intenta conectarse a un nodo ocupado, **la \_ \_ conexión del \_ vecino \_ del evento del grafo del mismo nivel** se genera en el elemento del mismo nivel que se conecta, con el estado de conexión establecido en **conexión del mismo nivel \_ \_**. Se puede hacer referencia al elemento de conexión del mismo nivel a otro nodo que se encuentra ocupado y puede enviar una referencia, y el mismo evento y estado se generan en el elemento del mismo nivel de conexión. Esta cadena de referencias que provocan **\_ \_ errores de conexión del mismo nivel** puede continuar hasta que se agote el número máximo de intentos de conexión. El elemento del mismo nivel no tiene un mecanismo para determinar la diferencia entre un intento de conexión completa y la referencia de la conexión.

Para solucionar este problema, los desarrolladores deben considerar el uso de los eventos de cambio de estado del grafo del mismo nivel para determinar si el intento de conexión correcta. Si el evento no se recibe en un período de tiempo determinado, la aplicación puede suponer que se está haciendo referencia al mismo nivel de conexión y que la aplicación del mismo nivel debe considerar el intento de conexión.

## <a name="peer-grouping-events"></a>Eventos de agrupación del mismo nivel

Una aplicación de agrupación del mismo nivel puede registrarse para recibir notificaciones de 8 eventos del mismo nivel. Cada nombre de evento está precedido por **un \_ \_ \_ evento de grupo del mismo nivel**; por ejemplo, el **Estado del evento de grupo del mismo nivel \_ \_ \_ \_ ha cambiado**. A menos que se indique lo contrario, la información sobre un cambio se recupera mediante [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata).

-   **Del mismo nivel \_ El \_ Estado del evento de grupo \_ \_ cambiado** indica que el estado del grupo ha cambiado. Hay dos valores de estado posibles: **\_ escuchando el \_ estado \_ del grupo del mismo nivel**, lo que indica que el grupo no tiene ninguna conexión y está esperando nuevos miembros, y el estado del **Grupo del mismo nivel \_ \_ \_ tiene conexiones**, lo que indica que el grupo tiene al menos una conexión. Este valor de estado se puede obtener llamando a [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) después de que se genere este evento.
-   **Del mismo nivel \_ Propiedad de evento de grupo \_ \_ \_ cambiada** indica que el creador del grupo ha cambiado o actualizado las propiedades del grupo.
-   **Del mismo nivel \_ El \_ registro de eventos de grupo \_ \_ cambiado** indica que se ha realizado una operación de registro. Este evento se desencadena cuando un elemento del mismo nivel que participa en el grupo publica, actualiza o elimina un registro. Por ejemplo, este evento se genera cuando una aplicación de chat envía un mensaje de chat.
-   **Del mismo nivel \_ Miembro de evento de grupo \_ \_ \_ cambiado** indica que ha cambiado el estado de un miembro dentro del grupo. Los cambios de estado incluyen:
    -   **Del mismo nivel \_ MIEMBRO \_ conectado**. Un elemento del mismo nivel se ha conectado al grupo.
    -   **Del mismo nivel \_ MIEMBRO \_ desconectado**. Un elemento del mismo nivel se ha desconectado del grupo.
    -   **Del mismo nivel \_ MIEMBRO \_ Unido**. Se ha publicado una nueva información de pertenencia para un elemento del mismo nivel.
    -   **Del mismo nivel \_ MIEMBRO \_ actualizado**. Un elemento del mismo nivel se ha actualizado con información nueva, como una nueva dirección IP.
-   **Del mismo nivel \_ \_conexión de \_ vecino \_ del evento de grupo**. Los pares que participarán en las conexiones de vecinos dentro del grupo deben registrarse para este evento. Tenga en cuenta que el registro para este evento no permite que el elemento del mismo nivel reciba datos; el registro de este evento solo garantiza la notificación cuando se recibe una solicitud de conexión de vecino.
-   **Del mismo nivel \_ \_ \_ \_ conexión directa de eventos de grupo**. Los pares que participarán en las conexiones directas dentro del grupo deben registrarse para este evento. Tenga en cuenta que el registro para este evento no permite que el elemento del mismo nivel reciba datos; el registro de este evento solo garantiza la notificación cuando se recibe una solicitud de conexión directa.
-   **Del mismo nivel \_ \_datos de \_ entrada \_ de eventos de grupo**. Los equipos del mismo nivel que recibirán datos a través de un vecino o conexión directa deben registrarse para este evento. Cuando se genera este evento, los datos opacos transmitidos por el otro elemento del mismo nivel de participación se pueden obtener llamando a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Tenga en cuenta que para recibir este evento, el elemento del mismo nivel debe haberse registrado previamente para la conexión **directa de eventos de grupo del mismo \_ \_ \_ \_ nivel** o la **conexión de vecino del evento de \_ Grupo del \_ \_ \_ mismo** nivel.
-   **Del mismo nivel \_ \_error de \_ conexión \_ de eventos de grupo**. Se produjo un error en la conexión por algún motivo. No se proporcionan datos cuando se genera este evento y no se debe llamar a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) .

Una vez que una aplicación recibe la notificación de que se ha producido un evento del mismo nivel (con excepción del **error de conexión de eventos de grupo del mismo nivel \_ \_ \_ \_**), la aplicación llama a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)y pasa el identificador de evento del mismo nivel devuelto por [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). La infraestructura del mismo nivel devuelve un puntero a una estructura de [**\_ datos de \_ eventos \_ de grupo del mismo nivel**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) que contiene los datos solicitados. Se debe llamar a esta función hasta que no se devuelvan **\_ \_ \_ \_ datos del evento** . Cuando una aplicación ya no requiere notificación para un evento del mismo nivel, se debe realizar una llamada a [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent), pasando el identificador de evento del mismo nivel devuelto por **PeerGroupRegisterEvent** cuando la aplicación se registra para el evento determinado.

## <a name="example-of-registering-for-peer-graphing-events"></a>Ejemplo de registro de eventos de gráficos del mismo nivel

En el ejemplo de código siguiente se muestra cómo registrar con los eventos de gráficos del mismo nivel.


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



 

 



