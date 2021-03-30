---
description: La operación de recogida permite a una aplicación responder a una sesión que se alerta en otra dirección. La aplicación identifica el destino de la recogida y se devuelve un identificador de sesión para la llamada de recogida.
ms.assetid: 3dfbb5c0-b533-403f-ad6c-b9e1b52ab47a
title: Diodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e033689ffccf6ba01ad06eb071514c1c37aaca03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816139"
---
# <a name="pickup"></a><span data-ttu-id="bd963-104">Diodo</span><span class="sxs-lookup"><span data-stu-id="bd963-104">Pickup</span></span>

<span data-ttu-id="bd963-105">La operación de recogida permite a una aplicación responder a una sesión que se alerta en otra dirección.</span><span class="sxs-lookup"><span data-stu-id="bd963-105">The pickup operation allows an application to answer a session that is alerting at another address.</span></span> <span data-ttu-id="bd963-106">La aplicación identifica el destino de la recogida y se devuelve un identificador de sesión para la llamada de recogida.</span><span class="sxs-lookup"><span data-stu-id="bd963-106">The application identifies the target of the pickup and is returned a session identifier for the picked-up call.</span></span>

<span data-ttu-id="bd963-107">Hay varias maneras de identificar el destino de la solicitud de recogida.</span><span class="sxs-lookup"><span data-stu-id="bd963-107">There are several ways to identify the target of the pickup request.</span></span> <span data-ttu-id="bd963-108">En primer lugar, la aplicación puede especificar la dirección de la entidad de alerta.</span><span class="sxs-lookup"><span data-stu-id="bd963-108">First, the application may specify the address of the alerting party.</span></span> <span data-ttu-id="bd963-109">En segundo lugar, si no se especifica ninguna dirección y el modificador lo permite, la aplicación puede seleccionar cualquier sesión de alertas en su grupo de recogida.</span><span class="sxs-lookup"><span data-stu-id="bd963-109">Second, if no address is specified and the switch allows it, the application can pick up any alerting session in its pickup group.</span></span> <span data-ttu-id="bd963-110">En tercer lugar, algunos modificadores permiten la recogida de una alerta de sesión en un grupo de recogida diferente si se especifica el identificador de grupo.</span><span class="sxs-lookup"><span data-stu-id="bd963-110">Third, some switches allow pickup of a session alerting in a different pickup group if the group identifier is specified.</span></span>

<span data-ttu-id="bd963-111">Algunos sistemas de teléfono clave admiten una *transferencia a través* de la capacidad de retención en las orientaciones de llamadas exclusivas de puente.</span><span class="sxs-lookup"><span data-stu-id="bd963-111">Some key telephone systems support a *transfer through hold* capability on bridged-exclusive call appearances.</span></span> <span data-ttu-id="bd963-112">En este esquema, un teléfono determinado posee una llamada exclusivamente cuando la llamada está activa, pero cuando la llamada está en espera, cualquier teléfono que tenga una apariencia de la línea puede recoger la llamada.</span><span class="sxs-lookup"><span data-stu-id="bd963-112">In this scheme, a particular phone owns a call exclusively when the call is active, but when the call is on hold, any phone that has an appearance of the line can pick up the call.</span></span>

<span data-ttu-id="bd963-113">**TAPI 2. x:** Una aplicación puede usar una operación de recogida con una dirección de destino **null** para este propósito, de forma similar a cómo se utiliza la función para recoger una llamada en espera en una línea analógica.</span><span class="sxs-lookup"><span data-stu-id="bd963-113">**TAPI 2.x:** An application can use a pickup operation with a **NULL** target address for this purpose, similar to how the function is used to pick up a call waiting call on an analog line.</span></span> <span data-ttu-id="bd963-114">LINEADDRFEATURE \_ PICKUPHELD indica la existencia de la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="bd963-114">LINEADDRFEATURE\_PICKUPHELD indicates the existence of the capability.</span></span>

<span data-ttu-id="bd963-115">Si LINEADDRCAPFLAGS \_ PICKUPCALLWAIT es **true**, se puede seleccionar una sesión para la que el usuario ha detectado de forma audible la señal de llamada en espera, pero para la que el proveedor de servicios no puede realizar la detección.</span><span class="sxs-lookup"><span data-stu-id="bd963-115">If LINEADDRCAPFLAGS\_PICKUPCALLWAIT is **TRUE**, a session can be picked up for which the user has audibly detected the call-waiting signal but for which the service provider is unable to perform the detection.</span></span> <span data-ttu-id="bd963-116">Esto proporciona al usuario un mecanismo para "responder" a una llamada en espera aunque el proveedor de servicios no pudiera detectar la señal de llamada en espera.</span><span class="sxs-lookup"><span data-stu-id="bd963-116">This gives the user a mechanism to "answer" a waiting call even though the service provider was unable to detect the call-waiting signal.</span></span> <span data-ttu-id="bd963-117">Tanto la dirección de destino como el ID. de grupo deben ser **null** para recoger una llamada de llamada en espera.</span><span class="sxs-lookup"><span data-stu-id="bd963-117">Both the destination address and the group ID must be **NULL** to pick up a call-waiting call.</span></span>

<span data-ttu-id="bd963-118">Cuando una sesión se ha recopilado correctamente, la aplicación recibe una notificación de cambio de estado con la [razón](reason-ovr.md) establecida en LINECALLREASON \_ pickup.</span><span class="sxs-lookup"><span data-stu-id="bd963-118">When a session has been picked up successfully, the application receives a state change notification with the [reason](reason-ovr.md) set to LINECALLREASON\_PICKUP.</span></span>

<span data-ttu-id="bd963-119">No todos los proveedores de servicios admiten el uso de esta operación.</span><span class="sxs-lookup"><span data-stu-id="bd963-119">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="bd963-120">**TAPI 2. x:** Vea [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span><span class="sxs-lookup"><span data-stu-id="bd963-120">**TAPI 2.x:** See [**linePickup**](/windows/win32/api/tapi/nf-tapi-linepickup).</span></span>

<span data-ttu-id="bd963-121">**TAPI 3. x:** Vea [**ITBasicCallControl::P ickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span><span class="sxs-lookup"><span data-stu-id="bd963-121">**TAPI 3.x:** See [**ITBasicCallControl::Pickup**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup).</span></span>

 

 
