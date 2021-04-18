---
description: El método allocator recupera un puntero al asignador de memoria.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Método CRendererInputPin. allocator (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670983"
---
# <a name="crendererinputpinallocator-method"></a><span data-ttu-id="49740-103">CRendererInputPin. allocator (método)</span><span class="sxs-lookup"><span data-stu-id="49740-103">CRendererInputPin.Allocator method</span></span>

<span data-ttu-id="49740-104">El `Allocator` método recupera un puntero al asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="49740-104">The `Allocator` method retrieves a pointer to the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="49740-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49740-105">Syntax</span></span>


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a><span data-ttu-id="49740-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49740-106">Parameters</span></span>

<span data-ttu-id="49740-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="49740-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49740-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49740-108">Return value</span></span>

<span data-ttu-id="49740-109">Devuelve un puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador o **null**.</span><span class="sxs-lookup"><span data-stu-id="49740-109">Returns a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="49740-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49740-110">Remarks</span></span>

<span data-ttu-id="49740-111">Este método devuelve la variable miembro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="49740-111">This method returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span> <span data-ttu-id="49740-112">El método no incrementa el recuento de referencias en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="49740-112">The method does not increment the reference count on the interface.</span></span> <span data-ttu-id="49740-113">Este método es estrictamente un método de descriptor de acceso.</span><span class="sxs-lookup"><span data-stu-id="49740-113">This method is strictly an accessor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="49740-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49740-114">Requirements</span></span>



| <span data-ttu-id="49740-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="49740-115">Requirement</span></span> | <span data-ttu-id="49740-116">Value</span><span class="sxs-lookup"><span data-stu-id="49740-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49740-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49740-117">Header</span></span><br/>  | <dl> <span data-ttu-id="49740-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49740-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="49740-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49740-119">Library</span></span><br/> | <dl> <span data-ttu-id="49740-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="49740-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49740-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="49740-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49740-122">**Clase CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="49740-122">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




