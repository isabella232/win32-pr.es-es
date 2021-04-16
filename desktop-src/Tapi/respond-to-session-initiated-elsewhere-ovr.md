---
description: Cuando llega una nueva sesión de comunicaciones, las aplicaciones TAPI que registraron interés en la dirección y el tipo de medio se enviarán a una notificación de eventos.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Responder a la sesión iniciada en otro lugar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678561"
---
# <a name="respond-to-session-initiated-elsewhere"></a><span data-ttu-id="55776-103">Responder a la sesión iniciada en otro lugar</span><span class="sxs-lookup"><span data-stu-id="55776-103">Respond to Session Initiated Elsewhere</span></span>

<span data-ttu-id="55776-104">Cuando llega una nueva sesión de comunicaciones, las aplicaciones TAPI que registraron interés en la [Dirección](address-ovr.md) y el [tipo de medio](media-type-ovr.md) se enviarán a una [notificación de eventos](event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="55776-104">When a new communications session arrives, TAPI applications that registered an interest in the [address](address-ovr.md) and [media type](media-type-ovr.md) will be sent an [event notification](event-notification.md).</span></span> <span data-ttu-id="55776-105">Solo se ofrecerá a una aplicación [privilegios](privilege-ovr.md) de propiedad a través de la sesión.</span><span class="sxs-lookup"><span data-stu-id="55776-105">Only one application will be offered ownership [privileges](privilege-ovr.md) over the session.</span></span> <span data-ttu-id="55776-106">Esta aplicación no puede rechazar la sesión.</span><span class="sxs-lookup"><span data-stu-id="55776-106">This application cannot refuse the session.</span></span>

<span data-ttu-id="55776-107">El estado de la llamada inicial de una sesión entrante es ofrecer.</span><span class="sxs-lookup"><span data-stu-id="55776-107">The initial call state of an incoming session is offering.</span></span> <span data-ttu-id="55776-108">Mientras la llamada está en el estado de la oferta, una aplicación puede obtener información como el modo de portador y el motivo de la llamada, si los proveedores de servicios proporcionan esta información y está disponible.</span><span class="sxs-lookup"><span data-stu-id="55776-108">While the call is in the offering state, an application can obtain information such as bearer mode and call reason, if the service providers supplied this information and it is available.</span></span> <span data-ttu-id="55776-109">Es posible que parte de la información de llamada no esté disponible de inmediato, como el identificador del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="55776-109">Some call information may not be available immediately, such as caller ID.</span></span>

<span data-ttu-id="55776-110">Hay seis respuestas básicas a una sesión ofrecida: [responder](answer-ovr.md), [Aceptar](accept-ovr.md), [entregar](handoffs-ovr.md), [quitar](drop-ovr.md), [reenviar](forward-ovr.md)y [redirigir](redirect-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="55776-110">There are six basic responses to an offered session: [answer](answer-ovr.md), [accept](accept-ovr.md), [handoff](handoffs-ovr.md), [drop](drop-ovr.md), [forward](forward-ovr.md), and [redirect](redirect-ovr.md).</span></span> <span data-ttu-id="55776-111">Dependiendo del proveedor de servicios, es posible que el conjunto completo de estas operaciones no esté disponible.</span><span class="sxs-lookup"><span data-stu-id="55776-111">Depending on the service provider, the full set of these operations may not be available.</span></span>

 

 



