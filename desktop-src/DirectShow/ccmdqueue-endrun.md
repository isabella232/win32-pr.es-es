---
description: El método EndRun cambia al modo detenido o en pausa.
ms.assetid: 2c41262c-a809-4f3b-898c-02c0891dc6f8
title: Método CCmdQueue. EndRun (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.EndRun
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367ef026402ff191ceb04657c21d6f3bd11ebe73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660171"
---
# <a name="ccmdqueueendrun-method"></a><span data-ttu-id="5b2a2-103">CCmdQueue. EndRun, método</span><span class="sxs-lookup"><span data-stu-id="5b2a2-103">CCmdQueue.EndRun method</span></span>

<span data-ttu-id="5b2a2-104">El `EndRun` método cambia al modo detenido o en pausa.</span><span class="sxs-lookup"><span data-stu-id="5b2a2-104">The `EndRun` method switches to the stopped or paused mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b2a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b2a2-105">Syntax</span></span>


```C++
virtual HRESULT EndRun();
```



## <a name="parameters"></a><span data-ttu-id="5b2a2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b2a2-106">Parameters</span></span>

<span data-ttu-id="5b2a2-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5b2a2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b2a2-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b2a2-108">Return value</span></span>

<span data-ttu-id="5b2a2-109">Devuelve un valor **HRESULT** que depende de la implementación de.</span><span class="sxs-lookup"><span data-stu-id="5b2a2-109">Returns an **HRESULT** value that depends on the implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b2a2-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b2a2-110">Remarks</span></span>

<span data-ttu-id="5b2a2-111">No se conoce la asignación de tiempo entre la hora de la secuencia y el tiempo de presentación después de llamar a esta función miembro.</span><span class="sxs-lookup"><span data-stu-id="5b2a2-111">Time mapping between stream time and presentation time is not known after this member function has been called.</span></span> <span data-ttu-id="5b2a2-112">Llame a la función miembro [**CCmdQueue:: Run**](ccmdqueue-run.md) para llevar a cabo esta asignación.</span><span class="sxs-lookup"><span data-stu-id="5b2a2-112">Call the [**CCmdQueue::Run**](ccmdqueue-run.md) member function to carry out this mapping.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b2a2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b2a2-113">Requirements</span></span>



| <span data-ttu-id="5b2a2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b2a2-114">Requirement</span></span> | <span data-ttu-id="5b2a2-115">Value</span><span class="sxs-lookup"><span data-stu-id="5b2a2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2a2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b2a2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="5b2a2-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b2a2-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b2a2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b2a2-118">Library</span></span><br/> | <dl> <span data-ttu-id="5b2a2-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5b2a2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b2a2-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b2a2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2a2-121">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="5b2a2-121">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




