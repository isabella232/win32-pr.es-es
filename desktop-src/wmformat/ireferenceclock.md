---
title: Interfaz IReferenceClock
description: La interfaz IReferenceClock proporciona acceso a un reloj externo. Esta interfaz se proporciona para permitir que todas las rutinas de representación se sincronicen con el mismo reloj. Esta interfaz se puede obtener de un objeto de lector.
ms.assetid: 1424fd74-d56c-4338-801f-319ef975169f
keywords:
- Interfaz IReferenceClock formato de Windows Media
- Interfaz IReferenceClock formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IReferenceClock
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72d17ef362aa5436fe98443d86dff5ae31212650
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105704965"
---
# <a name="ireferenceclock-interface"></a><span data-ttu-id="c6340-106">Interfaz IReferenceClock</span><span class="sxs-lookup"><span data-stu-id="c6340-106">IReferenceClock interface</span></span>

<span data-ttu-id="c6340-107">La interfaz **IReferenceClock** proporciona acceso a un reloj externo.</span><span class="sxs-lookup"><span data-stu-id="c6340-107">The **IReferenceClock** interface provides access to an external clock.</span></span> <span data-ttu-id="c6340-108">Esta interfaz se proporciona para permitir que todas las rutinas de representación se sincronicen con el mismo reloj.</span><span class="sxs-lookup"><span data-stu-id="c6340-108">This interface is provided to enable all rendering routines to be synchronized to the same clock.</span></span>

<span data-ttu-id="c6340-109">Esta interfaz se puede obtener de un objeto de lector.</span><span class="sxs-lookup"><span data-stu-id="c6340-109">This interface can be obtained from a reader object.</span></span>

## <a name="members"></a><span data-ttu-id="c6340-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c6340-110">Members</span></span>

<span data-ttu-id="c6340-111">La interfaz **IReferenceClock** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c6340-111">The **IReferenceClock** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c6340-112">**IReferenceClock** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c6340-112">**IReferenceClock** also has these types of members:</span></span>

-   [<span data-ttu-id="c6340-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6340-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c6340-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6340-114">Methods</span></span>

<span data-ttu-id="c6340-115">La interfaz **IReferenceClock** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="c6340-115">The **IReferenceClock** interface has these methods.</span></span>



| <span data-ttu-id="c6340-116">Método</span><span class="sxs-lookup"><span data-stu-id="c6340-116">Method</span></span>                                                   | <span data-ttu-id="c6340-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6340-117">Description</span></span>                                                               |
|:---------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="c6340-118">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="c6340-118">**AdvisePeriodic**</span></span>](ireferenceclock-adviseperiodic.md) | <span data-ttu-id="c6340-119">No implementado por este SDK.</span><span class="sxs-lookup"><span data-stu-id="c6340-119">Not implemented by this SDK.</span></span><br/>                                   |
| [<span data-ttu-id="c6340-120">**AdviseTime**</span><span class="sxs-lookup"><span data-stu-id="c6340-120">**AdviseTime**</span></span>](ireferenceclock-advisetime.md)         | <span data-ttu-id="c6340-121">Solicita una notificación asincrónica de que ha transcurrido una hora.</span><span class="sxs-lookup"><span data-stu-id="c6340-121">Requests an asynchronous notification that a time has elapsed.</span></span><br/> |
| [<span data-ttu-id="c6340-122">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="c6340-122">**GetTime**</span></span>](ireferenceclock-gettime.md)               | <span data-ttu-id="c6340-123">Recupera el tiempo de referencia actual.</span><span class="sxs-lookup"><span data-stu-id="c6340-123">Retrieves the current reference time.</span></span><br/>                          |
| [<span data-ttu-id="c6340-124">**No notificar**</span><span class="sxs-lookup"><span data-stu-id="c6340-124">**Unadvise**</span></span>](ireferenceclock-unadvise.md)             | <span data-ttu-id="c6340-125">Cancela una solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="c6340-125">Cancels a notification request.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="c6340-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6340-126">Remarks</span></span>

<span data-ttu-id="c6340-127">Para obtener información sobre otras interfaces que se pueden obtener con el método QueryInterface de esta interfaz, vea objeto Reader.</span><span class="sxs-lookup"><span data-stu-id="c6340-127">For information on other interfaces that can be obtained by using the QueryInterface method of this interface, see Reader Object.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6340-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6340-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6340-129">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="c6340-129">**Interfaces**</span></span>](interfaces.md)
</dt> </dl>

 

