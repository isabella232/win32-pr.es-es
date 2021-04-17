---
description: En el ejemplo de código siguiente se muestra cómo controlar las nuevas notificaciones de llamada, como buscar o crear los terminales adecuados para representar el medio.
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: Recibir una llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a78ebf5b77569f8468a8b2c0a30217f4f7430e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688412"
---
# <a name="receive-a-call"></a><span data-ttu-id="bc982-103">Recibir una llamada</span><span class="sxs-lookup"><span data-stu-id="bc982-103">Receive a Call</span></span>

<span data-ttu-id="bc982-104">En el ejemplo de código siguiente se muestra cómo controlar las nuevas notificaciones de llamada, como buscar o crear los terminales adecuados para representar el medio.</span><span class="sxs-lookup"><span data-stu-id="bc982-104">The following code example demonstrates handling of new call notifications, such as finding or creating appropriate terminals to render the media.</span></span> <span data-ttu-id="bc982-105">Este ejemplo es una parte de la instrucción switch que una aplicación debe implementar para el control de eventos.</span><span class="sxs-lookup"><span data-stu-id="bc982-105">This example is a portion of the switch statement an application must implement for event handling.</span></span> <span data-ttu-id="bc982-106">El propio código puede estar incluido en la implementación de [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), o el método de **evento** puede publicar un mensaje en un subproceso de trabajo que contenga el modificador.</span><span class="sxs-lookup"><span data-stu-id="bc982-106">The code itself may be contained in the implementation of [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), or the **Event** method may post a message to a worker thread that contains the switch.</span></span>

<span data-ttu-id="bc982-107">Antes de usar este ejemplo de código, debe realizar las operaciones en [Initialize TAPI](initialize-tapi.md), [seleccionar una dirección](select-an-address.md)y [registrar eventos](register-events.md).</span><span class="sxs-lookup"><span data-stu-id="bc982-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md), [Select an Address](select-an-address.md), and [Register Events](register-events.md).</span></span>

<span data-ttu-id="bc982-108">Además, debe realizar las operaciones que se muestran en [seleccionar un terminal](select-a-terminal.md) después de la recuperación de los punteros de la interfaz [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) y [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) .</span><span class="sxs-lookup"><span data-stu-id="bc982-108">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the retrieval of the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) interface pointers.</span></span>

> [!Note]  
> <span data-ttu-id="bc982-109">Este ejemplo no tiene la comprobación de errores y las versiones adecuadas para el código de producción.</span><span class="sxs-lookup"><span data-stu-id="bc982-109">This example does not have the error checking and releases appropriate for production code.</span></span>

 

``` syntax
// pEvent is an IDispatch pointer for the ITCallNotificationEvent interface of the
// call object created by TAPI, and is passed into the event handler by TAPI. 

case TE_CALLNOTIFICATION:
{
    // Get the ITCallNotification interface.
    ITCallNotificationEvent * pNotify;
    hr = pEvent->QueryInterface( 
            IID_ITCallNotificationEvent, 
            (void **)&pNotify 
            );
    // If ( hr != S_OK ) process the error here. 
    
    // Get the ITCallInfo interface.
    ITCallInfo * pCallInfo;
    hr = pNotify->get_Call( &pCallInfo);
    // If ( hr != S_OK ) process the error here. 

    // Get the ITBasicCallControl interface.
    ITBasicCallControl * pBasicCall;
    hr = pCallInfo->QueryInterface(
            IID_ITBasicCallControl,
            (void**)&pBasicCall
            );
    // If ( hr != S_OK ) process the error here. 

    // Get the ITAddress interface.
    ITAddress * pAddress;
    hr = pCallInfo->get_Address( &pAddress );
    // If ( hr != S_OK ) process the error here. 

    // Create the required terminals for this call.
    {
        // See the Select a Terminal code example.
    }
    // Complete incoming call processing.
    hr = pBasicCall->Answer();
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a><span data-ttu-id="bc982-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc982-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc982-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="bc982-111">Events</span></span>](events.md)
</dt> <dt>

[<span data-ttu-id="bc982-112">**ITTAPIEventNotification**</span><span class="sxs-lookup"><span data-stu-id="bc982-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[<span data-ttu-id="bc982-113">**ITTAPI::RegisterCallNotifications**</span><span class="sxs-lookup"><span data-stu-id="bc982-113">**ITTAPI::RegisterCallNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[<span data-ttu-id="bc982-114">**ITCallNotificationEvent**</span><span class="sxs-lookup"><span data-stu-id="bc982-114">**ITCallNotificationEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[<span data-ttu-id="bc982-115">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="bc982-115">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="bc982-116">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="bc982-116">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="bc982-117">**ITTerminalSupport**</span><span class="sxs-lookup"><span data-stu-id="bc982-117">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
