---
title: Autorización de servicio
description: Una aplicación puede implementar la autorización personalizada para los mensajes entrantes en un host de servicio.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Servicios Web de autorización de servicios para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149732"
---
# <a name="service-authorization"></a><span data-ttu-id="dbab4-106">Autorización de servicio</span><span class="sxs-lookup"><span data-stu-id="dbab4-106">Service Authorization</span></span>

<span data-ttu-id="dbab4-107">Una aplicación puede implementar la autorización personalizada para los mensajes entrantes en un host de servicio.</span><span class="sxs-lookup"><span data-stu-id="dbab4-107">An application can implement custom authorization for incoming messages on a service host .</span></span>


<span data-ttu-id="dbab4-108">Un host de servicio recibe una [**devolución de \_ \_ \_ llamada de seguridad del servicio WS del servicio**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) de devolución de llamada de seguridad como parte del punto de [**\_ \_ conexión de servicio WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) que se pasa a la función [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) .</span><span class="sxs-lookup"><span data-stu-id="dbab4-108">A service host receives a security callback [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) as part of the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) which is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function.</span></span> <span data-ttu-id="dbab4-109">Esta devolución de llamada se invoca cuando se recibe el [ \_ mensaje de WS](ws-message.md) .</span><span class="sxs-lookup"><span data-stu-id="dbab4-109">This callback is invoked when the [WS\_MESSAGE](ws-message.md) is received.</span></span>

<span data-ttu-id="dbab4-110">La aplicación puede basarse en esta devolución de llamada para implementar la autorización personalizada para los mensajes entrantes en el host del servicio.</span><span class="sxs-lookup"><span data-stu-id="dbab4-110">The application can rely on this callback to implement custom authorization for incoming messages on the service host.</span></span> <span data-ttu-id="dbab4-111">Si se produce un error en la autorización, la función de devolución de llamada de seguridad devuelve un error HR y el host del servicio anula el canal.</span><span class="sxs-lookup"><span data-stu-id="dbab4-111">If the authorization fails the security callback function returns a failure HR, and the service host aborts the channel.</span></span>

<span data-ttu-id="dbab4-112">Vea el ejemplo de nombre de usuario sobre SSL, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), para obtener una implementación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="dbab4-112">See the user name over SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), for an example implementation.</span></span>

 

 




