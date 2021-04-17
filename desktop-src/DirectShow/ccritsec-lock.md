---
description: El método lock bloquea el objeto de sección crítica.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Método CCritSec. Lock (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681267"
---
# <a name="ccritseclock-method"></a><span data-ttu-id="67fd0-103">CCritSec. Lock (método)</span><span class="sxs-lookup"><span data-stu-id="67fd0-103">CCritSec.Lock method</span></span>

<span data-ttu-id="67fd0-104">El método **Lock** bloquea el objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="67fd0-104">The **Lock** method locks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="67fd0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67fd0-105">Syntax</span></span>


```C++
void Lock();
```



## <a name="parameters"></a><span data-ttu-id="67fd0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67fd0-106">Parameters</span></span>

<span data-ttu-id="67fd0-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="67fd0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67fd0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67fd0-108">Return value</span></span>

<span data-ttu-id="67fd0-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="67fd0-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="67fd0-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67fd0-110">Remarks</span></span>

<span data-ttu-id="67fd0-111">Este método llama a la función [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) .</span><span class="sxs-lookup"><span data-stu-id="67fd0-111">This method calls the [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) function.</span></span>

<span data-ttu-id="67fd0-112">Llame a la función miembro [**CCritSec:: Unlock**](ccritsec-unlock.md) para desbloquear la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="67fd0-112">Call the [**CCritSec::Unlock**](ccritsec-unlock.md) member function to unlock the critical section.</span></span> <span data-ttu-id="67fd0-113">Puede realizar varias llamadas al método **Lock** en el mismo subproceso. Asegúrese de llamar a **Unlock** un número de veces correspondiente.</span><span class="sxs-lookup"><span data-stu-id="67fd0-113">You can make multiple calls to the **Lock** method on the same thread; be sure to call **Unlock** a corresponding number of times.</span></span>

<span data-ttu-id="67fd0-114">Si el objeto ya está bloqueado por otro subproceso, el método **CCritSec:: Lock** se bloquea hasta que se libera el objeto o hasta que se produce una excepción de interbloqueo posible.</span><span class="sxs-lookup"><span data-stu-id="67fd0-114">If the object is already locked by another thread, the **CCritSec::Lock** method blocks until the object is released, or until a possible-deadlock exception occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="67fd0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67fd0-115">Requirements</span></span>



| <span data-ttu-id="67fd0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="67fd0-116">Requirement</span></span> | <span data-ttu-id="67fd0-117">Value</span><span class="sxs-lookup"><span data-stu-id="67fd0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67fd0-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67fd0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="67fd0-119"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67fd0-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="67fd0-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67fd0-120">Library</span></span><br/> | <dl> <span data-ttu-id="67fd0-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="67fd0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67fd0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="67fd0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67fd0-123">**Clase CCritSec**</span><span class="sxs-lookup"><span data-stu-id="67fd0-123">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

