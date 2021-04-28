---
description: 'Método CTransInPlaceOutputPin.PeekAllocator: el método PeekAllocator devuelve un puntero al asignador del pin. El método no incrementa el recuento de referencias en la interfaz .'
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Método CTransInPlaceOutputPin.PeekAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084603"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="6d071-104">CTransInPlaceOutputPin.PeekAllocator (método)</span><span class="sxs-lookup"><span data-stu-id="6d071-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="6d071-105">El `PeekAllocator` método devuelve un puntero al asignador del pin.</span><span class="sxs-lookup"><span data-stu-id="6d071-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="6d071-106">El método no incrementa el recuento de referencias en la interfaz .</span><span class="sxs-lookup"><span data-stu-id="6d071-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d071-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d071-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="6d071-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d071-108">Parameters</span></span>

<span data-ttu-id="6d071-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6d071-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d071-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d071-110">Return value</span></span>

<span data-ttu-id="6d071-111">Devuelve la variable [**miembro CBaseOutputPin::m \_ pAllocator.**](cbaseoutputpin-m-pallocator.md)</span><span class="sxs-lookup"><span data-stu-id="6d071-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d071-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d071-112">Requirements</span></span>



| <span data-ttu-id="6d071-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d071-113">Requirement</span></span> | <span data-ttu-id="6d071-114">Value</span><span class="sxs-lookup"><span data-stu-id="6d071-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d071-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d071-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6d071-116"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d071-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6d071-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d071-117">Library</span></span><br/> | <dl> <span data-ttu-id="6d071-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6d071-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d071-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6d071-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d071-120">**CTransInPlaceOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="6d071-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




