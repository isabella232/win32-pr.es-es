---
description: Usa la función GetThreadPriority de Microsoft Win32 para recuperar la prioridad del subproceso de trabajo actual.
ms.assetid: a9db15cf-2c22-4c61-a817-20af5ade434b
title: Método CMsgThread. GetThreadPriority (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c9716b43ccc314ba487d982e0c1685960593f95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670607"
---
# <a name="cmsgthreadgetthreadpriority-method"></a><span data-ttu-id="72de8-103">CMsgThread. GetThreadPriority, método</span><span class="sxs-lookup"><span data-stu-id="72de8-103">CMsgThread.GetThreadPriority method</span></span>

<span data-ttu-id="72de8-104">Usa la función **GetThreadPriority** de Microsoft Win32 para recuperar la prioridad del subproceso de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="72de8-104">Uses the Microsoft Win32 **GetThreadPriority** function to retrieve the priority of the current worker thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="72de8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72de8-105">Syntax</span></span>


```C++
int GetThreadPriority();
```



## <a name="parameters"></a><span data-ttu-id="72de8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72de8-106">Parameters</span></span>

<span data-ttu-id="72de8-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="72de8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72de8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72de8-108">Return value</span></span>

<span data-ttu-id="72de8-109">Devuelve la prioridad del subproceso como un entero.</span><span class="sxs-lookup"><span data-stu-id="72de8-109">Returns the thread priority as an integer.</span></span>

## <a name="requirements"></a><span data-ttu-id="72de8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72de8-110">Requirements</span></span>



| <span data-ttu-id="72de8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="72de8-111">Requirement</span></span> | <span data-ttu-id="72de8-112">Value</span><span class="sxs-lookup"><span data-stu-id="72de8-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72de8-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72de8-113">Header</span></span><br/>  | <dl> <span data-ttu-id="72de8-114"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72de8-114"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72de8-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72de8-115">Library</span></span><br/> | <dl> <span data-ttu-id="72de8-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="72de8-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72de8-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="72de8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72de8-118">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="72de8-118">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




