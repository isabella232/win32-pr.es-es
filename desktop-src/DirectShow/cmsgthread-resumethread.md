---
description: 'Usa la función ResumeThread de Microsoft Win32 para continuar con la operación del subproceso de trabajo después de una llamada anterior a la función miembro CMsgThread:: SuspendThread.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Método CMsgThread. ResumeThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681175"
---
# <a name="cmsgthreadresumethread-method"></a><span data-ttu-id="502f3-103">CMsgThread. ResumeThread (método)</span><span class="sxs-lookup"><span data-stu-id="502f3-103">CMsgThread.ResumeThread method</span></span>

<span data-ttu-id="502f3-104">Usa la función **ResumeThread** de Microsoft Win32 para continuar con la operación del subproceso de trabajo después de una llamada anterior a la función miembro [**CMsgThread:: SuspendThread**](cmsgthread-suspendthread.md) .</span><span class="sxs-lookup"><span data-stu-id="502f3-104">Uses the Microsoft Win32 **ResumeThread** function to continue the operation of the worker thread after a previous call to the [**CMsgThread::SuspendThread**](cmsgthread-suspendthread.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="502f3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="502f3-105">Syntax</span></span>


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a><span data-ttu-id="502f3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="502f3-106">Parameters</span></span>

<span data-ttu-id="502f3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="502f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="502f3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="502f3-108">Return value</span></span>

<span data-ttu-id="502f3-109">Si la función miembro se ejecuta correctamente, el valor devuelto es el recuento de suspensión anterior del subproceso.</span><span class="sxs-lookup"><span data-stu-id="502f3-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="502f3-110">Si se produce un error en la función miembro, el valor devuelto es 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="502f3-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="502f3-111">Para obtener información de error extendida, llame a la función **GetLastError** de Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="502f3-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="502f3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="502f3-112">Requirements</span></span>



| <span data-ttu-id="502f3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="502f3-113">Requirement</span></span> | <span data-ttu-id="502f3-114">Value</span><span class="sxs-lookup"><span data-stu-id="502f3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="502f3-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="502f3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="502f3-116"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="502f3-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="502f3-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="502f3-117">Library</span></span><br/> | <dl> <span data-ttu-id="502f3-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="502f3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="502f3-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="502f3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="502f3-120">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="502f3-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




