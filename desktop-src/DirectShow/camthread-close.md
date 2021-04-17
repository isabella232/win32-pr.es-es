---
description: El método Close espera a que se cierre el subproceso y, a continuación, libera sus recursos.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Método CAMThread. Close (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690768"
---
# <a name="camthreadclose-method"></a><span data-ttu-id="d1b41-103">CAMThread. Close (método)</span><span class="sxs-lookup"><span data-stu-id="d1b41-103">CAMThread.Close method</span></span>

<span data-ttu-id="d1b41-104">El `Close` método espera a que se cierre el subproceso y, a continuación, libera sus recursos.</span><span class="sxs-lookup"><span data-stu-id="d1b41-104">The `Close` method waits for the thread to exit, then releases its resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1b41-105">Syntax</span></span>


```C++
void Close();
```



## <a name="parameters"></a><span data-ttu-id="d1b41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1b41-106">Parameters</span></span>

<span data-ttu-id="d1b41-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d1b41-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d1b41-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1b41-108">Return value</span></span>

<span data-ttu-id="d1b41-109">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d1b41-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b41-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1b41-110">Remarks</span></span>

<span data-ttu-id="d1b41-111">Antes de llamar a este método, debe proporcionar una manera de salir del subproceso.</span><span class="sxs-lookup"><span data-stu-id="d1b41-111">Before calling this method, you must provide a way for the thread to exit.</span></span> <span data-ttu-id="d1b41-112">Por ejemplo, en el método [**CAMThread:: ThreadProc**](camthread-threadproc.md) , defina una solicitud que indique al subproceso que salga.</span><span class="sxs-lookup"><span data-stu-id="d1b41-112">For example, in your [**CAMThread::ThreadProc**](camthread-threadproc.md) method, define a request that signals the thread to exit.</span></span> <span data-ttu-id="d1b41-113">A continuación, llame al método [**CAMThread:: CallWorker**](camthread-callworker.md) con ese valor.</span><span class="sxs-lookup"><span data-stu-id="d1b41-113">Then call the [**CAMThread::CallWorker**](camthread-callworker.md) method with that value.</span></span>

<span data-ttu-id="d1b41-114">El método de destructor [**~ CAMThread**](camthread--camthread.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="d1b41-114">The [**~ CAMThread**](camthread--camthread.md) destructor method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b41-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1b41-115">Requirements</span></span>



| <span data-ttu-id="d1b41-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b41-116">Requirement</span></span> | <span data-ttu-id="d1b41-117">Value</span><span class="sxs-lookup"><span data-stu-id="d1b41-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b41-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1b41-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d1b41-119"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b41-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d1b41-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1b41-120">Library</span></span><br/> | <dl> <span data-ttu-id="d1b41-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b41-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b41-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1b41-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b41-123">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="d1b41-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




