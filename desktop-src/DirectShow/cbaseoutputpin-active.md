---
description: El método activo notifica al pin que el filtro está activo ahora.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Método CBaseOutputPin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 249cddac4027fa434996b1118cc692937b686a83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660801"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="6a4dd-103">CBaseOutputPin. Active (método)</span><span class="sxs-lookup"><span data-stu-id="6a4dd-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="6a4dd-104">El `Active` método notifica al pin que el filtro está activo ahora.</span><span class="sxs-lookup"><span data-stu-id="6a4dd-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a4dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a4dd-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="6a4dd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a4dd-106">Parameters</span></span>

<span data-ttu-id="6a4dd-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6a4dd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a4dd-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a4dd-108">Return value</span></span>

<span data-ttu-id="6a4dd-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a4dd-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6a4dd-110">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6a4dd-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="6a4dd-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6a4dd-111">Return code</span></span>                                                                                          | <span data-ttu-id="6a4dd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="6a4dd-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6a4dd-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4dd-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="6a4dd-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6a4dd-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="6a4dd-115"><dt>**VFW \_ E \_ no \_ asignador**</dt></span><span class="sxs-lookup"><span data-stu-id="6a4dd-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="6a4dd-116">No hay ningún asignador disponible.</span><span class="sxs-lookup"><span data-stu-id="6a4dd-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a4dd-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a4dd-117">Remarks</span></span>

<span data-ttu-id="6a4dd-118">Este método invalida el método [**CBasePin:: Active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="6a4dd-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="6a4dd-119">Llama al método [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) en el asignador para asignar memoria para los búferes.</span><span class="sxs-lookup"><span data-stu-id="6a4dd-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="6a4dd-120">Si invalida este método, llame al método de la clase base desde el método de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="6a4dd-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a4dd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a4dd-121">Requirements</span></span>



| <span data-ttu-id="6a4dd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a4dd-122">Requirement</span></span> | <span data-ttu-id="6a4dd-123">Value</span><span class="sxs-lookup"><span data-stu-id="6a4dd-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a4dd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a4dd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6a4dd-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4dd-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6a4dd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a4dd-126">Library</span></span><br/> | <dl> <span data-ttu-id="6a4dd-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6a4dd-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a4dd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a4dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a4dd-129">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="6a4dd-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




