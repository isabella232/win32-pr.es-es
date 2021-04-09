---
description: La operación Hold permite que una sola dirección controle varias sesiones de comunicación.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Contener
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908281"
---
# <a name="hold"></a><span data-ttu-id="261cd-103">Contener</span><span class="sxs-lookup"><span data-stu-id="261cd-103">Hold</span></span>

<span data-ttu-id="261cd-104">La operación Hold permite que una sola dirección controle varias sesiones de comunicación.</span><span class="sxs-lookup"><span data-stu-id="261cd-104">The hold operation allows a single address to handle multiple communications sessions.</span></span> <span data-ttu-id="261cd-105">La colocación de una sesión en un disco duro de retención libera la línea o la dirección del usuario para realizar otras llamadas.</span><span class="sxs-lookup"><span data-stu-id="261cd-105">Placing a session on a hard hold frees the user's line/address to make other calls.</span></span> <span data-ttu-id="261cd-106">Normalmente, una llamada en retención no se puede transferir ni incluir en una llamada de conferencia, pero sí una llamada de consulta.</span><span class="sxs-lookup"><span data-stu-id="261cd-106">A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can.</span></span> <span data-ttu-id="261cd-107">Las llamadas de consulta se inician mediante operaciones de [Conferencia](conference-ovr.md) o [transferencia](transfer-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="261cd-107">Consultation calls are initiated using [conference](conference-ovr.md) or [transfer](transfer-ovr.md) operations.</span></span>

<span data-ttu-id="261cd-108">Una vez que se ha colocado correctamente una llamada en espera, el estado de la llamada normalmente realiza la transición al estado de suspensión.</span><span class="sxs-lookup"><span data-stu-id="261cd-108">After a call has been successfully placed on hold, the call state typically transitions to the onhold state.</span></span> <span data-ttu-id="261cd-109">Mientras una llamada está en espera, la aplicación puede recibir mensajes sobre los cambios de estado de la llamada retenida.</span><span class="sxs-lookup"><span data-stu-id="261cd-109">While a call is on hold, the application can receive messages about state changes of the held call.</span></span> <span data-ttu-id="261cd-110">Por ejemplo, si la parte que contiene se cuelga, el estado de la llamada puede pasar a desconectado.</span><span class="sxs-lookup"><span data-stu-id="261cd-110">For example, if the held party hangs up, the call state can transition to disconnected.</span></span>

<span data-ttu-id="261cd-111">En una situación de puente, es posible que la operación de retención no coloque realmente la llamada en espera.</span><span class="sxs-lookup"><span data-stu-id="261cd-111">In a bridged situation, the hold operation may not actually place the call on hold.</span></span> <span data-ttu-id="261cd-112">El estado de otras estaciones de la llamada puede regir (por ejemplo, si se intenta "mantener" una llamada cuando no se pueden participar otras estaciones). en su lugar, la llamada solo se puede cambiar al estado inactivo mientras permanezca conectado en otras estaciones.</span><span class="sxs-lookup"><span data-stu-id="261cd-112">The status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call can simply be changed to the inactive state while it remains connected at other stations.</span></span>

<span data-ttu-id="261cd-113">No todos los proveedores de servicios admiten el uso de esta operación.</span><span class="sxs-lookup"><span data-stu-id="261cd-113">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="261cd-114">**TAPI 2. x:** Vea [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span><span class="sxs-lookup"><span data-stu-id="261cd-114">**TAPI 2.x:** See [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span></span>

<span data-ttu-id="261cd-115">**TAPI 3. x:** Vea [**ITBasicCallControl:: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span><span class="sxs-lookup"><span data-stu-id="261cd-115">**TAPI 3.x:** See [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span></span>

 

 
