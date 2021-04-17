---
description: El método Inactive notifica al pin que el filtro ya no está activo.
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Método CBaseInputPin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52bf7efa352e8a73d562c61c3833a051ee860d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660342"
---
# <a name="cbaseinputpininactive-method"></a><span data-ttu-id="4bd47-103">CBaseInputPin. Inactive (método)</span><span class="sxs-lookup"><span data-stu-id="4bd47-103">CBaseInputPin.Inactive method</span></span>

<span data-ttu-id="4bd47-104">El `Inactive` método notifica al pin que el filtro ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="4bd47-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bd47-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bd47-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="4bd47-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4bd47-106">Parameters</span></span>

<span data-ttu-id="4bd47-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4bd47-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4bd47-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bd47-108">Return value</span></span>

<span data-ttu-id="4bd47-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4bd47-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4bd47-110">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4bd47-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="4bd47-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4bd47-111">Return code</span></span>                                                                                          | <span data-ttu-id="4bd47-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bd47-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4bd47-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4bd47-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="4bd47-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4bd47-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="4bd47-115"><dt>**VFW \_ E \_ no \_ asignador**</dt></span><span class="sxs-lookup"><span data-stu-id="4bd47-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="4bd47-116">No hay ningún asignador de memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="4bd47-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4bd47-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bd47-117">Remarks</span></span>

<span data-ttu-id="4bd47-118">Este método invalida el método [**CBasePin:: Inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="4bd47-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="4bd47-119">Llama al método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) para desasignar el asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="4bd47-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="4bd47-120">Si invalida este método, llame al método de la clase base desde el método de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="4bd47-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bd47-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bd47-121">Requirements</span></span>



| <span data-ttu-id="4bd47-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bd47-122">Requirement</span></span> | <span data-ttu-id="4bd47-123">Value</span><span class="sxs-lookup"><span data-stu-id="4bd47-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bd47-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4bd47-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4bd47-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4bd47-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4bd47-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4bd47-126">Library</span></span><br/> | <dl> <span data-ttu-id="4bd47-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4bd47-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bd47-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bd47-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bd47-129">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="4bd47-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




