---
description: Evento que se señala cuando el PIN se bloquea correctamente o el usuario cancela un bloque pendiente.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Miembro CDynamicOutputPin:: m_hNotifyCallerPinBlockedEvent (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670507"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a><span data-ttu-id="5b7b0-103">Miembro hNotifyCallerPinBlockedEvent CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="5b7b0-103">CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent member</span></span>

<span data-ttu-id="5b7b0-104">Evento que se señala cuando el PIN se bloquea correctamente o el usuario cancela un bloque pendiente.</span><span class="sxs-lookup"><span data-stu-id="5b7b0-104">Event that is signaled when the pin successfully blocks, or the user cancels a pending block.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b7b0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b7b0-105">Syntax</span></span>


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a><span data-ttu-id="5b7b0-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b7b0-106">Remarks</span></span>

<span data-ttu-id="5b7b0-107">Antes de tener acceso a esta variable, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="5b7b0-107">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b7b0-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b7b0-108">Requirements</span></span>



| <span data-ttu-id="5b7b0-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b7b0-109">Requirement</span></span> | <span data-ttu-id="5b7b0-110">Value</span><span class="sxs-lookup"><span data-stu-id="5b7b0-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b7b0-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b7b0-111">Header</span></span><br/>  | <dl> <span data-ttu-id="5b7b0-112"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b7b0-112"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5b7b0-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b7b0-113">Library</span></span><br/> | <dl> <span data-ttu-id="5b7b0-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5b7b0-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b7b0-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b7b0-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b7b0-116">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="5b7b0-116">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




