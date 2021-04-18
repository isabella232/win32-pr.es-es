---
description: Método de destructor.
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: CCritSec. ~ CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21029e2d53fd03ded2be4faa98e8b3e27681600c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680754"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="2fd0c-103">CCritSec. ~ CCritSec (destructor)</span><span class="sxs-lookup"><span data-stu-id="2fd0c-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="2fd0c-104">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="2fd0c-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd0c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fd0c-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="2fd0c-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fd0c-106">Remarks</span></span>

<span data-ttu-id="2fd0c-107">Este método llama a la función [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) para eliminar la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="2fd0c-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd0c-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fd0c-108">Requirements</span></span>



| <span data-ttu-id="2fd0c-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd0c-109">Requirement</span></span> | <span data-ttu-id="2fd0c-110">Value</span><span class="sxs-lookup"><span data-stu-id="2fd0c-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd0c-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2fd0c-111">Header</span></span><br/>  | <dl> <span data-ttu-id="2fd0c-112"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2fd0c-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2fd0c-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fd0c-113">Library</span></span><br/> | <dl> <span data-ttu-id="2fd0c-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2fd0c-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fd0c-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fd0c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd0c-116">**Clase CCritSec**</span><span class="sxs-lookup"><span data-stu-id="2fd0c-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

