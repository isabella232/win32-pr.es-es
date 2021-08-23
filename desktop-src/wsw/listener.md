---
title: Agente de escucha
description: El cliente usa un agente de escucha para aceptar un canal entrante de un servicio.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Servicios web de escucha para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26a2f9951dedefd5fb686de7935a76ce3b6ef24dcea140d5414b713e89ad1f1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026383"
---
# <a name="listener"></a>Agente de escucha

El cliente usa un agente de escucha para aceptar un canal [entrante](channel.md) de un servicio.

Para crear un listner, especifique el tipo de canal como [](binding.md) un valor de enumeración [**\_ WS CHANNEL \_ TYPE,**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) la información de enlace y la [dirección URL](url.md) en la que se va a escuchar.


Para empezar a escuchar en la dirección URL, llame a la [**función WsOpenListener.**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)

Para aceptar las comunicaciones entrantes, llame a [**WsAcceptChannel.**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)

Para cancelar la E/S pendiente de un agente de escucha, llame a [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).

Para obtener información sobre las transiciones de estado de un agente de escucha, vea la [**enumeración \_ LISTENER STATE \_ de WS.**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Las devoluciones de llamada siguientes forman parte del agente de escucha:

-   [**WS \_ ABORT \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**WS \_ CLOSE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ FOR \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ CREATE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**WS \_ FREE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**WS \_ OPEN \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**WS \_ RESET \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**WS \_ SET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

Las enumeraciones siguientes forman parte del agente de escucha:

-   [**WS \_ IP \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**ID. DE \_ PROPIEDAD DEL AGENTE DE ESCUCHA \_ \_ DE WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**ESTADO DEL AGENTE \_ DE ESCUCHA DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Las siguientes funciones forman parte del agente de escucha:

-   [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**WsCloseListener**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**WsFreeListener**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**WsGetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**WsResetListener**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**WsSetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

El siguiente identificador forma parte del agente de escucha:

-   [AGENTE DE ESCUCHA DE WS \_](ws-listener.md)

Las estructuras siguientes forman parte del agente de escucha:

-   [**DEVOLUCIONES DE LLAMADA \_ DE AGENTE DE ESCUCHA PERSONALIZADO DE \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**SUBCADENAS DEL AGENTE DE USUARIO NO \_ \_ \_ \_ PERMITIDOS**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**NOMBRES DE HOST DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**PROPIEDADES DEL AGENTE DE ESCUCHA DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**WS \_ LISTENER \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




