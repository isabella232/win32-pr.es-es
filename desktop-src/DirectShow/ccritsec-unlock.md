---
description: El método Unlock desbloquea el objeto de sección crítica.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: Método CCritSec. Unlock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660872"
---
# <a name="ccritsecunlock-method"></a><span data-ttu-id="13cb3-103">CCritSec. Unlock (método)</span><span class="sxs-lookup"><span data-stu-id="13cb3-103">CCritSec.Unlock method</span></span>

<span data-ttu-id="13cb3-104">El método **Unlock** desbloquea el objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="13cb3-104">The **Unlock** method unlocks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="13cb3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13cb3-105">Syntax</span></span>


```C++
void Unlock();
```



## <a name="parameters"></a><span data-ttu-id="13cb3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13cb3-106">Parameters</span></span>

<span data-ttu-id="13cb3-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="13cb3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13cb3-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13cb3-108">Return value</span></span>

<span data-ttu-id="13cb3-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="13cb3-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13cb3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13cb3-110">Remarks</span></span>

<span data-ttu-id="13cb3-111">Este método llama a la función [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="13cb3-111">This method calls the [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) function.</span></span> <span data-ttu-id="13cb3-112">Llame a este método una vez por cada llamada al método [**CCritSec:: Lock**](ccritsec-lock.md) .</span><span class="sxs-lookup"><span data-stu-id="13cb3-112">Call this method once for each call to the [**CCritSec::Lock**](ccritsec-lock.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="13cb3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13cb3-113">Requirements</span></span>



| <span data-ttu-id="13cb3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="13cb3-114">Requirement</span></span> | <span data-ttu-id="13cb3-115">Value</span><span class="sxs-lookup"><span data-stu-id="13cb3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13cb3-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13cb3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="13cb3-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13cb3-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="13cb3-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13cb3-118">Library</span></span><br/> | <dl> <span data-ttu-id="13cb3-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="13cb3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13cb3-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="13cb3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13cb3-121">**Clase CCritSec**</span><span class="sxs-lookup"><span data-stu-id="13cb3-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

