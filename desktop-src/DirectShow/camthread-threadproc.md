---
description: El método ThreadProc es el procedimiento de subproceso.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Método CAMThread. ThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660983"
---
# <a name="camthreadthreadproc-method"></a><span data-ttu-id="2e933-103">CAMThread. ThreadProc (método)</span><span class="sxs-lookup"><span data-stu-id="2e933-103">CAMThread.ThreadProc method</span></span>

<span data-ttu-id="2e933-104">El `ThreadProc` método es el procedimiento de subproceso.</span><span class="sxs-lookup"><span data-stu-id="2e933-104">The `ThreadProc` method is the thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e933-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e933-105">Syntax</span></span>


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a><span data-ttu-id="2e933-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e933-106">Parameters</span></span>

<span data-ttu-id="2e933-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2e933-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2e933-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e933-108">Return value</span></span>

<span data-ttu-id="2e933-109">Devuelve un valor **DWORD** cuyo significado está definido por la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="2e933-109">Returns a **DWORD** value whose meaning is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e933-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e933-110">Remarks</span></span>

<span data-ttu-id="2e933-111">Este es un método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="2e933-111">This is a pure virtual method.</span></span> <span data-ttu-id="2e933-112">Implemente este método en la clase derivada para proporcionar un procedimiento de subproceso.</span><span class="sxs-lookup"><span data-stu-id="2e933-112">Implement this method in your derived class to supply a thread procedure.</span></span> <span data-ttu-id="2e933-113">Cuando el método [**CAMThread:: Create**](camthread-create.md) crea un subproceso, proporciona la dirección del método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) , que a su vez llama al método ThreadProc.</span><span class="sxs-lookup"><span data-stu-id="2e933-113">When the [**CAMThread::Create**](camthread-create.md) method creates a thread, it gives the address of the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method, which in turn calls your ThreadProc method.</span></span>

<span data-ttu-id="2e933-114">Normalmente, el método ThreadProc entrará en un bucle que recupera las solicitudes (llamando a los métodos [**CAMThread:: GetRequest**](camthread-getrequest.md) o [**CAMThread:: CheckRequest**](camthread-checkrequest.md) ) y procesa los datos.</span><span class="sxs-lookup"><span data-stu-id="2e933-114">Typically, your ThreadProc method will enter a loop that retrieves requests (by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods) and processes data.</span></span>

<span data-ttu-id="2e933-115">Cuando este método finaliza, el subproceso se cierra.</span><span class="sxs-lookup"><span data-stu-id="2e933-115">When this method returns, the thread exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e933-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e933-116">Requirements</span></span>



| <span data-ttu-id="2e933-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e933-117">Requirement</span></span> | <span data-ttu-id="2e933-118">Value</span><span class="sxs-lookup"><span data-stu-id="2e933-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e933-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e933-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2e933-120"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e933-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2e933-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e933-121">Library</span></span><br/> | <dl> <span data-ttu-id="2e933-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2e933-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e933-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e933-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e933-124">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="2e933-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




