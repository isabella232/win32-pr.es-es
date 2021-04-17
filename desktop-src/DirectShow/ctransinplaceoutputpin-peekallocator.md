---
description: El método PeekAllocator devuelve un puntero al asignador del PIN. El método no incrementa el recuento de referencias en la interfaz.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Método CTransInPlaceOutputPin. PeekAllocator (TRANSip. h)
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
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679239"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="c9b40-104">CTransInPlaceOutputPin. PeekAllocator, método</span><span class="sxs-lookup"><span data-stu-id="c9b40-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="c9b40-105">El `PeekAllocator` método devuelve un puntero al asignador del PIN.</span><span class="sxs-lookup"><span data-stu-id="c9b40-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="c9b40-106">El método no incrementa el recuento de referencias en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c9b40-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b40-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9b40-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="c9b40-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9b40-108">Parameters</span></span>

<span data-ttu-id="c9b40-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c9b40-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9b40-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9b40-110">Return value</span></span>

<span data-ttu-id="c9b40-111">Devuelve la variable miembro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="c9b40-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b40-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9b40-112">Requirements</span></span>



| <span data-ttu-id="c9b40-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9b40-113">Requirement</span></span> | <span data-ttu-id="c9b40-114">Value</span><span class="sxs-lookup"><span data-stu-id="c9b40-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b40-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9b40-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c9b40-116"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9b40-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9b40-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9b40-117">Library</span></span><br/> | <dl> <span data-ttu-id="c9b40-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c9b40-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9b40-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9b40-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b40-120">**Clase CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c9b40-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




