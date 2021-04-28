---
description: 'Constructor CCritSec.CCritSec: método constructor.'
ms.assetid: e8e9138a-6c39-41de-a7f8-d9e9c4fe5ab6
title: Constructor CCritSec.CCritSec (Wxutil.h)
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
ms.openlocfilehash: de2b852ffc9a12622a4560ae834a3347b1e07552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119803"
---
# <a name="ccritsecccritsec-constructor"></a><span data-ttu-id="5537f-103">Constructor CCritSec.CCritSec</span><span class="sxs-lookup"><span data-stu-id="5537f-103">CCritSec.CCritSec constructor</span></span>

<span data-ttu-id="5537f-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="5537f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5537f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5537f-105">Syntax</span></span>


```C++
CCritSec();
```



## <a name="parameters"></a><span data-ttu-id="5537f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5537f-106">Parameters</span></span>

<span data-ttu-id="5537f-107">Este constructor no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5537f-107">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5537f-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5537f-108">Remarks</span></span>

<span data-ttu-id="5537f-109">Este método llama a [**la función InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) para inicializar la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="5537f-109">This method calls the [**InitializeCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-initializecriticalsection) function to initialize the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="5537f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5537f-110">Requirements</span></span>



| <span data-ttu-id="5537f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5537f-111">Requirement</span></span> | <span data-ttu-id="5537f-112">Value</span><span class="sxs-lookup"><span data-stu-id="5537f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5537f-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5537f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="5537f-114"><dt>Wxutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5537f-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="5537f-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5537f-115">Library</span></span><br/> | <dl> <span data-ttu-id="5537f-116"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5537f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5537f-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5537f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5537f-118">**CCritSec (clase)**</span><span class="sxs-lookup"><span data-stu-id="5537f-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

