---
description: El método Set señala el evento.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Método CAMEvent. set (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671424"
---
# <a name="cameventset-method"></a><span data-ttu-id="7607e-103">CAMEvent. set (método)</span><span class="sxs-lookup"><span data-stu-id="7607e-103">CAMEvent.Set method</span></span>

<span data-ttu-id="7607e-104">El `Set` método señala el evento.</span><span class="sxs-lookup"><span data-stu-id="7607e-104">The `Set` method signals the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="7607e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7607e-105">Syntax</span></span>


```C++
void Set();
```



## <a name="parameters"></a><span data-ttu-id="7607e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7607e-106">Parameters</span></span>

<span data-ttu-id="7607e-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7607e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7607e-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7607e-108">Return value</span></span>

<span data-ttu-id="7607e-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7607e-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7607e-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7607e-110">Remarks</span></span>

<span data-ttu-id="7607e-111">El comportamiento depende de si el objeto es un evento de restablecimiento automático o un evento de restablecimiento manual:</span><span class="sxs-lookup"><span data-stu-id="7607e-111">The behavior depends on whether the object is an auto-reset event or a manual-reset event:</span></span>

-   <span data-ttu-id="7607e-112">**Restablecimiento automático**: Si algún subproceso está esperando en este evento, se libera un subproceso y se restablece el evento.</span><span class="sxs-lookup"><span data-stu-id="7607e-112">**Auto-reset**: If any threads are waiting on this event, one thread is released and the event is reset.</span></span> <span data-ttu-id="7607e-113">Si no hay ningún subproceso esperando en este evento, el evento permanece señalado.</span><span class="sxs-lookup"><span data-stu-id="7607e-113">If no threads are waiting on this event, the event remains signaled.</span></span>
-   <span data-ttu-id="7607e-114">**Restablecimiento manual**: se liberan todos los subprocesos que esperan en este evento.</span><span class="sxs-lookup"><span data-stu-id="7607e-114">**Manual-reset**: All the threads waiting on this event are released.</span></span> <span data-ttu-id="7607e-115">El evento permanece señalado.</span><span class="sxs-lookup"><span data-stu-id="7607e-115">The event remains signaled.</span></span>

## <a name="requirements"></a><span data-ttu-id="7607e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7607e-116">Requirements</span></span>



| <span data-ttu-id="7607e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7607e-117">Requirement</span></span> | <span data-ttu-id="7607e-118">Value</span><span class="sxs-lookup"><span data-stu-id="7607e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7607e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7607e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7607e-120"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7607e-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7607e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7607e-121">Library</span></span><br/> | <dl> <span data-ttu-id="7607e-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7607e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7607e-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="7607e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7607e-124">**Clase CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="7607e-124">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




