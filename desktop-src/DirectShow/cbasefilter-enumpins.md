---
description: 'El método EnumPins enumera los pin de este filtro. Este método implementa el método IBaseFilter:: EnumPins.'
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: Método CBaseFilter. EnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660963"
---
# <a name="cbasefilterenumpins-method"></a><span data-ttu-id="5da7f-104">CBaseFilter. EnumPins, método</span><span class="sxs-lookup"><span data-stu-id="5da7f-104">CBaseFilter.EnumPins method</span></span>

<span data-ttu-id="5da7f-105">El `EnumPins` método enumera los pin de este filtro.</span><span class="sxs-lookup"><span data-stu-id="5da7f-105">The `EnumPins` method enumerates the pins on this filter.</span></span> <span data-ttu-id="5da7f-106">Este método implementa el método [**IBaseFilter:: EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) .</span><span class="sxs-lookup"><span data-stu-id="5da7f-106">This method implements the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5da7f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5da7f-107">Syntax</span></span>


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="5da7f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5da7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5da7f-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="5da7f-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="5da7f-110">Dirección de una variable que recibe un puntero a la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="5da7f-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5da7f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5da7f-111">Return value</span></span>

<span data-ttu-id="5da7f-112">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5da7f-112">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="5da7f-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5da7f-113">Return code</span></span>                                                                                   | <span data-ttu-id="5da7f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="5da7f-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="5da7f-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="5da7f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5da7f-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="5da7f-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="5da7f-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5da7f-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5da7f-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="5da7f-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="5da7f-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="5da7f-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="5da7f-120">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="5da7f-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5da7f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5da7f-121">Remarks</span></span>

<span data-ttu-id="5da7f-122">Este método crea una instancia de la clase base [**CEnumPins**](cenumpins.md) y devuelve un puntero a ese objeto, de tipo **IEnumPins**.</span><span class="sxs-lookup"><span data-stu-id="5da7f-122">This method creates an instance of the [**CEnumPins**](cenumpins.md) base class, and returns a pointer to that object, of type **IEnumPins**.</span></span> <span data-ttu-id="5da7f-123">La clase **CEnumPins** llama al método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) del filtro para enumerar los PIN del filtro.</span><span class="sxs-lookup"><span data-stu-id="5da7f-123">The **CEnumPins** class calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to enumerate the pins on the filter.</span></span>

<span data-ttu-id="5da7f-124">Si este método se ejecuta correctamente, la interfaz **IEnumPins** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="5da7f-124">If this method succeeds, the **IEnumPins** interface has an outstanding reference count.</span></span> <span data-ttu-id="5da7f-125">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="5da7f-125">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5da7f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5da7f-126">Requirements</span></span>



| <span data-ttu-id="5da7f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5da7f-127">Requirement</span></span> | <span data-ttu-id="5da7f-128">Value</span><span class="sxs-lookup"><span data-stu-id="5da7f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5da7f-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5da7f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5da7f-130"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5da7f-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5da7f-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5da7f-131">Library</span></span><br/> | <dl> <span data-ttu-id="5da7f-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5da7f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5da7f-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="5da7f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5da7f-134">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="5da7f-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




