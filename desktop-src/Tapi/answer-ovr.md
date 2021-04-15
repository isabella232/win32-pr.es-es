---
description: La operación de respuesta es una respuesta típica de las aplicaciones a una sesión de comunicaciones ofrecida. Si se realiza correctamente, esta operación hace que una sesión pase al estado conectado.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Respuesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545654"
---
# <a name="answer"></a><span data-ttu-id="71368-104">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71368-104">Answer</span></span>

<span data-ttu-id="71368-105">La operación de respuesta es la respuesta típica de una aplicación a una sesión de comunicaciones ofrecida.</span><span class="sxs-lookup"><span data-stu-id="71368-105">The answer operation is an application's typical response to an offered communications session.</span></span> <span data-ttu-id="71368-106">Si se realiza correctamente, esta operación hace que una sesión pase al estado conectado.</span><span class="sxs-lookup"><span data-stu-id="71368-106">If successful, this operation causes a session to transition into the connected state.</span></span>

<span data-ttu-id="71368-107">En algunos entornos de telefonía (como RDSI), en los que la alerta de usuario es independiente de la oferta de llamada, la aplicación tiene la opción de [Aceptar](accept-ovr.md) una llamada antes de responder o rechazar ([quitar](drop-ovr.md)) o [redirigir](redirect-ovr.md) la llamada de *oferta* .</span><span class="sxs-lookup"><span data-stu-id="71368-107">In some telephony environments (like ISDN), where user alerting is separate from call offering, the application has the option to [accept](accept-ovr.md) a call prior to answering or to reject ([drop](drop-ovr.md)) or [redirect](redirect-ovr.md) the *offering* call.</span></span>

<span data-ttu-id="71368-108">Si se realiza una operación de respuesta para una nueva sesión cuando una sesión ya está activa, el efecto que tiene en la sesión activa existente depende de las capacidades del proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="71368-108">If an answer operation is performed for a new session when a session is already active, the effect this has on the existing active session depends on the service provider's capabilities.</span></span> <span data-ttu-id="71368-109">La primera llamada puede no verse afectada, se puede quitar automáticamente o puede colocarse automáticamente en espera.</span><span class="sxs-lookup"><span data-stu-id="71368-109">The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold.</span></span> <span data-ttu-id="71368-110">TAPI enviará las notificaciones de eventos adecuadas relativas a ambas llamadas.</span><span class="sxs-lookup"><span data-stu-id="71368-110">TAPI will send the appropriate event notifications concerning both calls.</span></span>

<span data-ttu-id="71368-111">En una situación de puente, si una llamada está conectada pero en el estado activo, se puede combinar con la operación de respuesta.</span><span class="sxs-lookup"><span data-stu-id="71368-111">In a bridged situation, if a call is connected but in the active state, it can be joined using the answer operation.</span></span>

<span data-ttu-id="71368-112">La aplicación tiene la opción de enviar información de usuario al usuario en el momento de la respuesta, si el proveedor de servicios lo admite.</span><span class="sxs-lookup"><span data-stu-id="71368-112">The application has the option to send user-user information at the time of the answer, if the service provider supports it.</span></span>

<span data-ttu-id="71368-113">**TAPI 2. x:** Vea [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="71368-113">**TAPI 2.x:** See [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="71368-114">**TAPI 3. x:** Vea [**ITBasicCallControl:: Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span><span class="sxs-lookup"><span data-stu-id="71368-114">**TAPI 3.x:** See [**ITBasicCallControl::Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span></span>

 

 
