---
title: Duración del contexto de operación y subprocesamiento
description: La duración del contexto de la operación, representada por un \_ \_ identificador de contexto de operación de WS, determina la duración de las propiedades que contiene.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Duración del contexto de operación y servicios Web de subprocesos para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ea27b0b1dc41ccd029df7d726fe92631adc1ee4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797308"
---
# <a name="operation-context-lifetime-and-threading"></a><span data-ttu-id="b383d-106">Duración del contexto de operación y subprocesamiento</span><span class="sxs-lookup"><span data-stu-id="b383d-106">Operation Context Lifetime and Threading</span></span>

<span data-ttu-id="b383d-107">La duración del contexto de la operación, representada por un identificador de [ \_ \_ contexto de operación de WS](ws-operation-context.md) , determina la duración de las propiedades que contiene.</span><span class="sxs-lookup"><span data-stu-id="b383d-107">The lifetime of the operation context, represented by a [WS\_OPERATION\_CONTEXT](ws-operation-context.md) handle, determines the lifetime of the properties it contains.</span></span> <span data-ttu-id="b383d-108">Por lo tanto, solo se debe usar un contexto dentro de la duración de la [operación de servicio](service-operation.md) o la devolución de llamada a la que se proporciona.</span><span class="sxs-lookup"><span data-stu-id="b383d-108">Therefore, a context should only be used within the lifetime of the [service operation](service-operation.md) or the callback to which its provided.</span></span> <span data-ttu-id="b383d-109">La duración de una llamada sincrónica es la ejecución de la propia función.</span><span class="sxs-lookup"><span data-stu-id="b383d-109">The lifetime of a synchronous call is the execution of function itself.</span></span> <span data-ttu-id="b383d-110">Para una llamada asincrónica, la duración finaliza una vez completada la llamada asincrónica.</span><span class="sxs-lookup"><span data-stu-id="b383d-110">For an asynchronous call the lifetime ends once the asynchronous call is completed.</span></span> <span data-ttu-id="b383d-111">El modelo de servicio no proporciona ninguna garantía sobre el contexto una vez completada la llamada.</span><span class="sxs-lookup"><span data-stu-id="b383d-111">The Service Model gives no guarantees about the context once the call is completed.</span></span> <span data-ttu-id="b383d-112">El comportamiento que se basa en el contexto de la operación o en cualquiera de sus propiedades más allá de su duración es indefinido.</span><span class="sxs-lookup"><span data-stu-id="b383d-112">The behavior of relying on operation context or any of its properties beyond its lifetime is undefined.</span></span>


<span data-ttu-id="b383d-113">Vea también el ejemplo de calculadora basado en sesión, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="b383d-113">See also, the session based calculator example, [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).</span></span>

## <a name="threading-model"></a><span data-ttu-id="b383d-114">Modelo de subprocesos</span><span class="sxs-lookup"><span data-stu-id="b383d-114">Threading Model</span></span>

<span data-ttu-id="b383d-115">El contexto de la operación admite el subprocesamiento libre, pero esto es cierto en el propio contexto de la operación y no se aplica a ninguna de las propiedades que contiene.</span><span class="sxs-lookup"><span data-stu-id="b383d-115">The operation context supports free threading, however this is true of the operation context itself and does not apply to any of the properties it contains.</span></span>

<span data-ttu-id="b383d-116">Al registrar una devolución de llamada de cancelación para una operación de servicio a través de la función [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) , tenga en cuenta que el primer registro se realizará correctamente. sin embargo, se producirá un error al establecer la devolución de llamada de cancelación varias veces.</span><span class="sxs-lookup"><span data-stu-id="b383d-116">When you register a cancel callback for a service operation through the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function, note that the first registration will succeed; setting the cancel callback multiple times, however, will fail.</span></span>

 

 




