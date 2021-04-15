---
title: Agente de escucha
description: El cliente utiliza un agente de escucha para aceptar un canal entrante de un servicio.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Servicios web del agente de escucha para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421644"
---
# <a name="listener"></a>Agente de escucha

El cliente utiliza un agente de escucha para aceptar un [canal](channel.md) entrante de un servicio.

Para crear un agente, debe especificar el tipo de canal como un valor de enumeración de [**\_ \_ tipo de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , la información de [enlace](binding.md) y la [dirección URL](url.md) en la que se va a escuchar.


Para empezar a escuchar en la dirección URL, llame a la función [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) .

Para aceptar las comunicaciones entrantes, llame a [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).

Para cancelar la e/s pendiente para un agente de escucha, llame a [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).

Para obtener información sobre las transiciones de estado de un agente de escucha, vea la enumeración de [**\_ \_ Estado de escucha de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .

Las siguientes devoluciones de llamada forman parte del agente de escucha:

-   [**\_devolución de \_ llamada de agente de escucha de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_devolución de \_ llamada de canal de aceptación de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_devolución de \_ llamada del agente de escucha de WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ Create \_ Channel \_ para \_ devolución de llamada del agente de escucha \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**\_devolución de \_ llamada de agente de escucha de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**\_devolución de \_ llamada de agente de escucha gratuito de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**\_devolución de \_ llamada de \_ propiedad de agente de escucha de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**\_devolución de \_ llamada de agente de escucha abierto WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**\_devolución de \_ llamada del agente de escucha de WS RESET \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**\_devolución de \_ llamada de \_ propiedad del agente de escucha de WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

Las enumeraciones siguientes forman parte del agente de escucha:

-   [**versión de WS \_ IP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**identificador de la propiedad del agente de escucha de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**\_Estado del agente de escucha de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

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

-   [agente de escucha de WS \_](ws-listener.md)

Las siguientes estructuras forman parte del agente de escucha:

-   [**\_devoluciones de llamada de agente de escucha personalizado de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**no se \_ permiten \_ \_ subcadenas de agente de usuario \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**\_nombres de host de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**\_propiedades del agente de escucha de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**\_propiedad del agente de escucha de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




