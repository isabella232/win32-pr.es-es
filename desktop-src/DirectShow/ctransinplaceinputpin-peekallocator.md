---
description: 'Método CTransInPlaceInputPin.PeekAllocator: el método PeekAllocator devuelve un puntero al asignador del pin. El método no incrementa el recuento de referencias en la interfaz .'
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Método CTransInPlaceInputPin.PeekAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7a5f7cb0fbe754890b1d7930bb54c6fca47afa5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084673"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="e497e-104">Método CTransInPlaceInputPin.PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="e497e-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="e497e-105">El `PeekAllocator` método devuelve un puntero al asignador del pin.</span><span class="sxs-lookup"><span data-stu-id="e497e-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="e497e-106">El método no incrementa el recuento de referencias en la interfaz .</span><span class="sxs-lookup"><span data-stu-id="e497e-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e497e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e497e-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="e497e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e497e-108">Parameters</span></span>

<span data-ttu-id="e497e-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e497e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e497e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e497e-110">Return value</span></span>

<span data-ttu-id="e497e-111">Devuelve la variable [**miembro CBaseInputPin::m \_ pAllocator.**](cbaseinputpin-m-pallocator.md)</span><span class="sxs-lookup"><span data-stu-id="e497e-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="e497e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e497e-112">Requirements</span></span>



| <span data-ttu-id="e497e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e497e-113">Requirement</span></span> | <span data-ttu-id="e497e-114">Value</span><span class="sxs-lookup"><span data-stu-id="e497e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e497e-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e497e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e497e-116"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e497e-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e497e-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e497e-117">Library</span></span><br/> | <dl> <span data-ttu-id="e497e-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e497e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e497e-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e497e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e497e-120">**CTransInPlaceInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="e497e-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




