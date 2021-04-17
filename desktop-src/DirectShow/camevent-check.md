---
description: El método check comprueba si el evento está establecido, sin bloqueos.
ms.assetid: b8e55798-fd8e-4442-bc35-08887d8a3129
title: Método CAMEvent. check (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Check
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a112d1b9484acb4d7e9cc2992b8dee629f40e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670373"
---
# <a name="cameventcheck-method"></a><span data-ttu-id="01753-103">CAMEvent. check (método)</span><span class="sxs-lookup"><span data-stu-id="01753-103">CAMEvent.Check method</span></span>

<span data-ttu-id="01753-104">El `Check` método comprueba si el evento está establecido, sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="01753-104">The `Check` method checks whether the event is set, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="01753-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01753-105">Syntax</span></span>


```C++
BOOL Check();
```



## <a name="parameters"></a><span data-ttu-id="01753-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01753-106">Parameters</span></span>

<span data-ttu-id="01753-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="01753-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="01753-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01753-108">Remarks</span></span>

<span data-ttu-id="01753-109">Devuelve **true** si se establece el evento o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01753-109">Returns **TRUE** if the event is set, or **FALSE** otherwise.</span></span> <span data-ttu-id="01753-110">Este método llama al método [**CAMEvent:: wait**](camevent-wait.md) con un tiempo de espera de cero.</span><span class="sxs-lookup"><span data-stu-id="01753-110">This method calls the [**CAMEvent::Wait**](camevent-wait.md) method with a time-out of zero.</span></span> <span data-ttu-id="01753-111">Si el objeto es un evento de restablecimiento automático, este método restablece el evento.</span><span class="sxs-lookup"><span data-stu-id="01753-111">If the object is an auto-reset event, this method resets the event.</span></span>

## <a name="requirements"></a><span data-ttu-id="01753-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01753-112">Requirements</span></span>



| <span data-ttu-id="01753-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="01753-113">Requirement</span></span> | <span data-ttu-id="01753-114">Value</span><span class="sxs-lookup"><span data-stu-id="01753-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01753-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01753-115">Header</span></span><br/>  | <dl> <span data-ttu-id="01753-116"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01753-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="01753-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01753-117">Library</span></span><br/> | <dl> <span data-ttu-id="01753-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="01753-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01753-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="01753-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01753-120">**Clase CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="01753-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




