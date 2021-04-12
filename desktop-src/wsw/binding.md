---
title: enlace del canal
description: Los enlaces especifican el protocolo de conexión y el comportamiento local de un canal.
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Enlazar servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723a729b87dc26849dbd1f84038805c5e47a0ea4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357227"
---
# <a name="channel-binding"></a><span data-ttu-id="de30d-106">enlace del canal</span><span class="sxs-lookup"><span data-stu-id="de30d-106">Channel Binding</span></span>

<span data-ttu-id="de30d-107">Los enlaces especifican el protocolo de conexión y el comportamiento local de un canal.</span><span class="sxs-lookup"><span data-stu-id="de30d-107">Bindings specify the wire protocol and local behavior for a channel.</span></span> <span data-ttu-id="de30d-108">Los enlaces se componen de los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="de30d-108">Bindings are made up of the following components:</span></span>

-   <span data-ttu-id="de30d-109">Un [**\_ \_ enlace de canal de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), que identifica el protocolo de transferencia que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="de30d-109">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), which identifies the transfer protocol to use.</span></span>
-   <span data-ttu-id="de30d-110">Una [**\_ \_ Descripción de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), que especifica cómo proteger el canal.</span><span class="sxs-lookup"><span data-stu-id="de30d-110">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), which specifies how to secure the channel.</span></span>
-   <span data-ttu-id="de30d-111">Una [**\_ \_ propiedad Set WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, que especifica una configuración adicional opcional (vea también ID. de [**\_ propiedad de canal \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span><span class="sxs-lookup"><span data-stu-id="de30d-111">A set [**WS\_CHANNEL\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, which specify additional optional settings (see also [**WS\_CHANNEL\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).</span></span>

 

 




