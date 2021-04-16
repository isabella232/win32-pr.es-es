---
description: Usa la función SuspendThread de Microsoft Win32 para suspender el funcionamiento de un subproceso en ejecución.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Método CMsgThread. SuspendThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671724"
---
# <a name="cmsgthreadsuspendthread-method"></a><span data-ttu-id="f525a-103">CMsgThread. SuspendThread, método</span><span class="sxs-lookup"><span data-stu-id="f525a-103">CMsgThread.SuspendThread method</span></span>

<span data-ttu-id="f525a-104">Usa la función **SuspendThread** de Microsoft Win32 para suspender el funcionamiento de un subproceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="f525a-104">Uses the Microsoft Win32 **SuspendThread** function to suspend the operation of a running thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="f525a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f525a-105">Syntax</span></span>


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a><span data-ttu-id="f525a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f525a-106">Parameters</span></span>

<span data-ttu-id="f525a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f525a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f525a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f525a-108">Return value</span></span>

<span data-ttu-id="f525a-109">Si la función miembro se ejecuta correctamente, el valor devuelto es el recuento de suspensión anterior del subproceso.</span><span class="sxs-lookup"><span data-stu-id="f525a-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="f525a-110">Si se produce un error en la función miembro, el valor devuelto es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="f525a-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="f525a-111">Para obtener información de error extendida, llame a la función **GetLastError** de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="f525a-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="f525a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f525a-112">Remarks</span></span>

<span data-ttu-id="f525a-113">El subproceso de cliente llama a esta función miembro para suspender la operación del subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f525a-113">The client thread calls this member function to suspend the operation of the worker thread.</span></span> <span data-ttu-id="f525a-114">El subproceso de trabajo permanece suspendido y no se ejecutará hasta que se realice una llamada adicional a la función miembro [**CMsgThread:: ResumeThread**](cmsgthread-resumethread.md) .</span><span class="sxs-lookup"><span data-stu-id="f525a-114">The worker thread remains suspended and will not execute until an additional call to the [**CMsgThread::ResumeThread**](cmsgthread-resumethread.md) member function is made.</span></span>

## <a name="requirements"></a><span data-ttu-id="f525a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f525a-115">Requirements</span></span>



| <span data-ttu-id="f525a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f525a-116">Requirement</span></span> | <span data-ttu-id="f525a-117">Value</span><span class="sxs-lookup"><span data-stu-id="f525a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f525a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f525a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f525a-119"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f525a-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f525a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f525a-120">Library</span></span><br/> | <dl> <span data-ttu-id="f525a-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f525a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f525a-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f525a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f525a-123">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="f525a-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




