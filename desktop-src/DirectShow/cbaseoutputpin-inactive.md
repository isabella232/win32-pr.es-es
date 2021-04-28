---
description: 'Método CBaseOutputPin.Inactive: el método Inactivo notifica al pin que el filtro ya no está activo.'
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: Método CBaseOutputPin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc4901bba7f1e34d49ff5bafb7b291544157bd9c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096143"
---
# <a name="cbaseoutputpininactive-method"></a><span data-ttu-id="7e91c-103">CBaseOutputPin.Inactive (método)</span><span class="sxs-lookup"><span data-stu-id="7e91c-103">CBaseOutputPin.Inactive method</span></span>

<span data-ttu-id="7e91c-104">El `Inactive` método notifica al pin que el filtro ya no está activo.</span><span class="sxs-lookup"><span data-stu-id="7e91c-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e91c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e91c-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="7e91c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e91c-106">Parameters</span></span>

<span data-ttu-id="7e91c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7e91c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7e91c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e91c-108">Return value</span></span>

<span data-ttu-id="7e91c-109">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7e91c-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7e91c-110">Los valores posibles incluyen los enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7e91c-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="7e91c-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7e91c-111">Return code</span></span>                                                                                          | <span data-ttu-id="7e91c-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e91c-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7e91c-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7e91c-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="7e91c-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7e91c-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="7e91c-115"><dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt></span><span class="sxs-lookup"><span data-stu-id="7e91c-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="7e91c-116">No hay ningún asignador de memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="7e91c-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7e91c-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7e91c-117">Remarks</span></span>

<span data-ttu-id="7e91c-118">Este método invalida el [**método CBasePin::Inactive.**](cbasepin-inactive.md)</span><span class="sxs-lookup"><span data-stu-id="7e91c-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="7e91c-119">Llama al [**método IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) para desasignar el asignador de memoria.</span><span class="sxs-lookup"><span data-stu-id="7e91c-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="7e91c-120">Si invalida este método, llame al método de clase base desde el método de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="7e91c-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e91c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e91c-121">Requirements</span></span>



| <span data-ttu-id="7e91c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e91c-122">Requirement</span></span> | <span data-ttu-id="7e91c-123">Value</span><span class="sxs-lookup"><span data-stu-id="7e91c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e91c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e91c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7e91c-125"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e91c-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7e91c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e91c-126">Library</span></span><br/> | <dl> <span data-ttu-id="7e91c-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7e91c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e91c-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7e91c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e91c-129">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="7e91c-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




