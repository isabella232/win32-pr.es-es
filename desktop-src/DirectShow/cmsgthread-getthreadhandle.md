---
description: Recupera el identificador del subproceso en el objeto CMsgThread.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Método CMsgThread. GetThreadHandle (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680347"
---
# <a name="cmsgthreadgetthreadhandle-method"></a><span data-ttu-id="04896-103">CMsgThread. GetThreadHandle, método</span><span class="sxs-lookup"><span data-stu-id="04896-103">CMsgThread.GetThreadHandle method</span></span>

<span data-ttu-id="04896-104">Recupera el identificador del subproceso en el objeto [**CMsgThread**](cmsgthread.md) .</span><span class="sxs-lookup"><span data-stu-id="04896-104">Retrieves the handle to the thread in the [**CMsgThread**](cmsgthread.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="04896-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04896-105">Syntax</span></span>


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a><span data-ttu-id="04896-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04896-106">Parameters</span></span>

<span data-ttu-id="04896-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="04896-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="04896-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04896-108">Return value</span></span>

<span data-ttu-id="04896-109">Devuelve el identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="04896-109">Returns the thread handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="04896-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="04896-110">Remarks</span></span>

<span data-ttu-id="04896-111">El identificador del subproceso se puede pasar a funciones de espera, como [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="04896-111">The thread handle can be passed to wait functions, such as [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span></span> <span data-ttu-id="04896-112">El identificador del subproceso se señala cuando el subproceso ha salido.</span><span class="sxs-lookup"><span data-stu-id="04896-112">The thread handle is signaled when the thread has exited.</span></span>

## <a name="requirements"></a><span data-ttu-id="04896-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04896-113">Requirements</span></span>



| <span data-ttu-id="04896-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="04896-114">Requirement</span></span> | <span data-ttu-id="04896-115">Value</span><span class="sxs-lookup"><span data-stu-id="04896-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04896-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04896-116">Header</span></span><br/>  | <dl> <span data-ttu-id="04896-117"><dt>Msgthrd. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04896-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="04896-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04896-118">Library</span></span><br/> | <dl> <span data-ttu-id="04896-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="04896-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04896-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="04896-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04896-121">**Clase CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="04896-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

