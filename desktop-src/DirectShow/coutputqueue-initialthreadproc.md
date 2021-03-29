---
description: 'El método InitialThreadProc llama al método COutputQueue:: ThreadProc cuando se crea el subproceso.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Inimétodo tialThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680886"
---
# <a name="coutputqueueinitialthreadproc-method"></a><span data-ttu-id="00a9d-103">COutputQueue.Inimétodo tialThreadProc</span><span class="sxs-lookup"><span data-stu-id="00a9d-103">COutputQueue.InitialThreadProc method</span></span>

<span data-ttu-id="00a9d-104">El `InitialThreadProc` método llama al método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) cuando se crea el subproceso.</span><span class="sxs-lookup"><span data-stu-id="00a9d-104">The `InitialThreadProc` method calls the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method when the thread is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a9d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00a9d-105">Syntax</span></span>


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="00a9d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00a9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a9d-107">*FV*</span><span class="sxs-lookup"><span data-stu-id="00a9d-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="00a9d-108">`this` puntero.</span><span class="sxs-lookup"><span data-stu-id="00a9d-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a9d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00a9d-109">Return value</span></span>

<span data-ttu-id="00a9d-110">Devuelve el valor devuelto por el método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="00a9d-110">Returns the value returned by the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a9d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00a9d-111">Remarks</span></span>

<span data-ttu-id="00a9d-112">Este método es el procedimiento de subproceso para el subproceso de trabajo del objeto.</span><span class="sxs-lookup"><span data-stu-id="00a9d-112">This method is the thread procedure for the object's worker thread.</span></span> <span data-ttu-id="00a9d-113">El puntero del objeto `this` es el parámetro Thread.</span><span class="sxs-lookup"><span data-stu-id="00a9d-113">The object's `this` pointer is the thread parameter.</span></span> <span data-ttu-id="00a9d-114">El método desreferencia este para llamar a **ThreadProc**.</span><span class="sxs-lookup"><span data-stu-id="00a9d-114">The method dereferences this to call **ThreadProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="00a9d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00a9d-115">Requirements</span></span>



| <span data-ttu-id="00a9d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a9d-116">Requirement</span></span> | <span data-ttu-id="00a9d-117">Value</span><span class="sxs-lookup"><span data-stu-id="00a9d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a9d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00a9d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="00a9d-119"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00a9d-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00a9d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00a9d-120">Library</span></span><br/> | <dl> <span data-ttu-id="00a9d-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="00a9d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a9d-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="00a9d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a9d-123">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="00a9d-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




