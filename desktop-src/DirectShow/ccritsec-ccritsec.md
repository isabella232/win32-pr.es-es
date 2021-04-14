---
description: Método de constructor.
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Constructor CCritSec. CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6baeadace7c1f8d8d3ad5dee1ff5c9dace1c6907
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661403"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="345e5-103">Constructor CCritSec. CCritSec</span><span class="sxs-lookup"><span data-stu-id="345e5-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="345e5-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="345e5-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="345e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="345e5-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="345e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="345e5-106">Parameters</span></span>

<span data-ttu-id="345e5-107">Este constructor no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="345e5-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="345e5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="345e5-108">Remarks</span></span>

<span data-ttu-id="345e5-109">Este método llama a la función [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) para inicializar la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="345e5-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="345e5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="345e5-110">Requirements</span></span>



| <span data-ttu-id="345e5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="345e5-111">Requirement</span></span> | <span data-ttu-id="345e5-112">Value</span><span class="sxs-lookup"><span data-stu-id="345e5-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="345e5-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="345e5-113">Header</span></span><br/>  | <dl> <span data-ttu-id="345e5-114"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="345e5-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="345e5-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="345e5-115">Library</span></span><br/> | <dl> <span data-ttu-id="345e5-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="345e5-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="345e5-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="345e5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345e5-118">**Clase CCritSec**</span><span class="sxs-lookup"><span data-stu-id="345e5-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

