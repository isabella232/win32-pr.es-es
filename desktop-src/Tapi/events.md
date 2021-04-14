---
description: Los eventos son una parte fundamental del control de llamadas en TAPI 3. El control de eventos incluye cuatro fases.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Eventos (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545454"
---
# <a name="events-telephony-api"></a><span data-ttu-id="c31e4-104">Eventos (API de telefonía)</span><span class="sxs-lookup"><span data-stu-id="c31e4-104">Events (Telephony API)</span></span>

<span data-ttu-id="c31e4-105">Los eventos son una parte fundamental del control de llamadas en TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="c31e4-105">Events are a crucial part of call handling under TAPI 3.</span></span> <span data-ttu-id="c31e4-106">El control de eventos incluye cuatro fases.</span><span class="sxs-lookup"><span data-stu-id="c31e4-106">Event handling includes four stages.</span></span>

<span data-ttu-id="c31e4-107">**Para registrarse y habilitar la recepción de eventos**</span><span class="sxs-lookup"><span data-stu-id="c31e4-107">**To register for and enable the reception of events**</span></span>

1.  <span data-ttu-id="c31e4-108">Implemente el método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) .</span><span class="sxs-lookup"><span data-stu-id="c31e4-108">Implement the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method.</span></span> <span data-ttu-id="c31e4-109">(TAPI llama a este método cuando se produce un evento). Normalmente, esta implementación no hace más que **AddRef** el puntero de interfaz **IDispatch** y, a continuación, se envía al bombeo de mensajes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c31e4-109">(TAPI calls this method when an event occurs.) Typically, this implementation does no more than **AddRef** the **IDispatch** interface pointer, then post to the application's message pump.</span></span>
2.  <span data-ttu-id="c31e4-110">Registre la interfaz de salida de [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) con las interfaces estándar de com [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) e [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) y pase el método [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) a un puntero a [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span><span class="sxs-lookup"><span data-stu-id="c31e4-110">Register the [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) outgoing interface using the COM standard [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) and [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) interfaces, and pass the [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) method a pointer to [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).</span></span>
3.  <span data-ttu-id="c31e4-111">Llame al método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) para indicar a TAPI los eventos que controlará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c31e4-111">Call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method to tell TAPI which events the application will handle.</span></span> <span data-ttu-id="c31e4-112">El filtro de eventos consta de **o** Ed miembros de la enumeración de [**\_ eventos TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .</span><span class="sxs-lookup"><span data-stu-id="c31e4-112">The event filter consists of **OR** ed members of the [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) enumeration.</span></span>
    > [!Note]  
    > <span data-ttu-id="c31e4-113">Debe llamar al método **ITTAPI::p UT \_ EventFilter** para establecer la máscara del filtro de eventos y habilitar la recepción de eventos.</span><span class="sxs-lookup"><span data-stu-id="c31e4-113">You must call the **ITTAPI::put\_EventFilter** method to set the event filter mask and enable reception of events.</span></span> <span data-ttu-id="c31e4-114">Si no llama a **ITTAPI::p UT \_ EventFilter**, la aplicación no recibirá ningún evento.</span><span class="sxs-lookup"><span data-stu-id="c31e4-114">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span>

     

<span data-ttu-id="c31e4-115">También debe llamar al método [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) para cada objeto de dirección en el que la aplicación controlará las llamadas.</span><span class="sxs-lookup"><span data-stu-id="c31e4-115">You must also call the [**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) method for each address object on which the application will handle calls.</span></span>

<span data-ttu-id="c31e4-116">Vea [interfaces de eventos](./event-interfaces.md) para obtener una lista de todas las interfaces de eventos.</span><span class="sxs-lookup"><span data-stu-id="c31e4-116">See [Event Interfaces](./event-interfaces.md) for a list of all event interfaces.</span></span> <span data-ttu-id="c31e4-117">Consulte [registrar eventos](register-events.md) para ver ejemplos de código que ilustran el proceso de registro y [recibir una llamada](receive-a-call.md) para obtener un ejemplo de código que muestra un uso de los eventos.</span><span class="sxs-lookup"><span data-stu-id="c31e4-117">See [Register Events](register-events.md) for code examples that illustrate the registration process and [Receive a Call](receive-a-call.md) for a code example that shows one use of events.</span></span>

 

 
