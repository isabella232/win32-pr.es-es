---
description: La clase CAMEvent es un contenedor para los eventos de restablecimiento manual y de restablecimiento automático.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: Clase CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670692"
---
# <a name="camevent-class"></a><span data-ttu-id="8b787-103">Clase CAMEvent</span><span class="sxs-lookup"><span data-stu-id="8b787-103">CAMEvent class</span></span>

![jerarquía de clases camevent](images/util06.png)

<span data-ttu-id="8b787-105">La clase **CAMEvent** es un contenedor para los eventos de restablecimiento manual y de restablecimiento automático.</span><span class="sxs-lookup"><span data-stu-id="8b787-105">The **CAMEvent** class is a wrapper for manual-reset and auto-reset events.</span></span>

<span data-ttu-id="8b787-106">Esta clase proporciona una manera cómoda de administrar eventos, en lugar de llamar a funciones como [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)y [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span><span class="sxs-lookup"><span data-stu-id="8b787-106">This class provides a convenient way to manage events, rather than calling functions such as [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), and [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).</span></span>



| <span data-ttu-id="8b787-107">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="8b787-107">Protected Member Variables</span></span>                          | <span data-ttu-id="8b787-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b787-108">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="8b787-109">**m \_ hEvent**</span><span class="sxs-lookup"><span data-stu-id="8b787-109">**m\_hEvent**</span></span>](camevent-m-hevent.md)              | <span data-ttu-id="8b787-110">Identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="8b787-110">Event handle.</span></span>                                                   |
| <span data-ttu-id="8b787-111">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="8b787-111">Public Methods</span></span>                                      | <span data-ttu-id="8b787-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b787-112">Description</span></span>                                                     |
| [<span data-ttu-id="8b787-113">**CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="8b787-113">**CAMEvent**</span></span>](camevent-camevent.md)               | <span data-ttu-id="8b787-114">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="8b787-114">Constructor method.</span></span>                                             |
| [<span data-ttu-id="8b787-115">**~ CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="8b787-115">**~CAMEvent**</span></span>](camevent--camevent.md)             | <span data-ttu-id="8b787-116">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="8b787-116">Destructor method.</span></span>                                              |
| [<span data-ttu-id="8b787-117">**de Azure Functions**</span><span class="sxs-lookup"><span data-stu-id="8b787-117">**Check**</span></span>](camevent-check.md)                     | <span data-ttu-id="8b787-118">Comprueba si el evento está establecido, sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="8b787-118">Checks whether the event is set, without blocking.</span></span>              |
| [<span data-ttu-id="8b787-119">**Reset**</span><span class="sxs-lookup"><span data-stu-id="8b787-119">**Reset**</span></span>](camevent-reset.md)                     | <span data-ttu-id="8b787-120">Establece el estado del evento en no señalado.</span><span class="sxs-lookup"><span data-stu-id="8b787-120">Sets the state of the event to nonsignaled.</span></span>                     |
| [<span data-ttu-id="8b787-121">**Conjunto**</span><span class="sxs-lookup"><span data-stu-id="8b787-121">**Set**</span></span>](camevent-set.md)                         | <span data-ttu-id="8b787-122">Señala el evento.</span><span class="sxs-lookup"><span data-stu-id="8b787-122">Signals the event.</span></span>                                              |
| [<span data-ttu-id="8b787-123">**Esperar**</span><span class="sxs-lookup"><span data-stu-id="8b787-123">**Wait**</span></span>](camevent-wait.md)                       | <span data-ttu-id="8b787-124">Se bloquea hasta que se señale el evento o hasta que se agote el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="8b787-124">Blocks until the event is signaled, or until a time-out occurs.</span></span> |
| <span data-ttu-id="8b787-125">Operadores</span><span class="sxs-lookup"><span data-stu-id="8b787-125">Operators</span></span>                                           | <span data-ttu-id="8b787-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b787-126">Description</span></span>                                                     |
| [<span data-ttu-id="8b787-127">**IDENTIFICADOR de operador**</span><span class="sxs-lookup"><span data-stu-id="8b787-127">**operator HANDLE**</span></span>](camevent-operator-handle.md) | <span data-ttu-id="8b787-128">Recupera el identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="8b787-128">Retrieves the event handle.</span></span>                                     |



 

## <a name="requirements"></a><span data-ttu-id="8b787-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b787-129">Requirements</span></span>



| <span data-ttu-id="8b787-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b787-130">Requirement</span></span> | <span data-ttu-id="8b787-131">Value</span><span class="sxs-lookup"><span data-stu-id="8b787-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b787-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b787-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8b787-133"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b787-133"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8b787-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b787-134">Library</span></span><br/> | <dl> <span data-ttu-id="8b787-135"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8b787-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

