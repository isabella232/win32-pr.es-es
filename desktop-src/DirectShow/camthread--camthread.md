---
description: Método de destructor.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: CAMThread. ~ CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660735"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="c07f6-103">CAMThread. ~ CAMThread (destructor)</span><span class="sxs-lookup"><span data-stu-id="c07f6-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="c07f6-104">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="c07f6-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c07f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c07f6-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="c07f6-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c07f6-106">Remarks</span></span>

<span data-ttu-id="c07f6-107">El destructor llama al método [**CAMThread:: Close**](camthread-close.md) , que espera a que se cierre el subproceso.</span><span class="sxs-lookup"><span data-stu-id="c07f6-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="c07f6-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c07f6-108">Requirements</span></span>



| <span data-ttu-id="c07f6-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="c07f6-109">Requirement</span></span> | <span data-ttu-id="c07f6-110">Value</span><span class="sxs-lookup"><span data-stu-id="c07f6-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c07f6-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c07f6-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c07f6-112"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c07f6-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c07f6-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c07f6-113">Library</span></span><br/> | <dl> <span data-ttu-id="c07f6-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c07f6-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c07f6-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="c07f6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c07f6-116">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="c07f6-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




