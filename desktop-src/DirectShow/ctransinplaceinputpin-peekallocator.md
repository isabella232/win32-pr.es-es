---
description: El método PeekAllocator devuelve un puntero al asignador del PIN. El método no incrementa el recuento de referencias en la interfaz.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Método CTransInPlaceInputPin. PeekAllocator (TRANSip. h)
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
ms.openlocfilehash: 22358dd776a0536cfbae819ec7cace02dd1775a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679253"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="0f191-104">CTransInPlaceInputPin. PeekAllocator, método</span><span class="sxs-lookup"><span data-stu-id="0f191-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="0f191-105">El `PeekAllocator` método devuelve un puntero al asignador del PIN.</span><span class="sxs-lookup"><span data-stu-id="0f191-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="0f191-106">El método no incrementa el recuento de referencias en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="0f191-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f191-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f191-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="0f191-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f191-108">Parameters</span></span>

<span data-ttu-id="0f191-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0f191-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f191-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f191-110">Return value</span></span>

<span data-ttu-id="0f191-111">Devuelve la variable miembro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="0f191-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f191-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f191-112">Requirements</span></span>



| <span data-ttu-id="0f191-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f191-113">Requirement</span></span> | <span data-ttu-id="0f191-114">Value</span><span class="sxs-lookup"><span data-stu-id="0f191-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f191-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f191-115">Header</span></span><br/>  | <dl> <span data-ttu-id="0f191-116"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0f191-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0f191-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f191-117">Library</span></span><br/> | <dl> <span data-ttu-id="0f191-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0f191-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f191-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f191-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f191-120">**Clase CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="0f191-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




