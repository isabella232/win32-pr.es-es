---
description: 'El método siguiente recupera un número especificado de PIN en la secuencia de enumeración. Este método implementa el método IEnumPins:: Next.'
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: Método CEnumPins. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671154"
---
# <a name="cenumpinsnext-method"></a><span data-ttu-id="7ef8c-104">CEnumPins. Next (método)</span><span class="sxs-lookup"><span data-stu-id="7ef8c-104">CEnumPins.Next method</span></span>

<span data-ttu-id="7ef8c-105">El método siguiente recupera un número especificado de PIN en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-105">The Next method retrieves a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="7ef8c-106">Este método implementa el método [**IEnumPins:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) .</span><span class="sxs-lookup"><span data-stu-id="7ef8c-106">This method implements the [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ef8c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ef8c-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="7ef8c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ef8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ef8c-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="7ef8c-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef8c-110">Número de clavijas que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-110">Number of pins to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7ef8c-111">*ppPins*</span><span class="sxs-lookup"><span data-stu-id="7ef8c-111">*ppPins*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef8c-112">Matriz de tamaño *cPins* que se rellena con punteros [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="7ef8c-112">Array of size *cPins* that is filled with [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="7ef8c-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="7ef8c-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="7ef8c-114">Puntero a una variable que recibe el número de PIN recuperados.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-114">Pointer to a variable that receives the number of pins retrieved.</span></span> <span data-ttu-id="7ef8c-115">Puede ser **null** si *cPins* es 1.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-115">Can be **NULL** if *cPins* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ef8c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ef8c-116">Return value</span></span>

<span data-ttu-id="7ef8c-117">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="7ef8c-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7ef8c-118">Return code</span></span>                                                                                                | <span data-ttu-id="7ef8c-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ef8c-119">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ef8c-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7ef8c-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="7ef8c-121">No recuperó tantos PIN como se solicitó.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-121">Did not retrieve as many pins as requested.</span></span><br/>                                 |
| <dl> <span data-ttu-id="7ef8c-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7ef8c-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="7ef8c-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-123">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="7ef8c-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7ef8c-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="7ef8c-125">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-125">Invalid argument.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="7ef8c-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="7ef8c-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="7ef8c-127">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="7ef8c-127">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="7ef8c-128"><dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt></span><span class="sxs-lookup"><span data-stu-id="7ef8c-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="7ef8c-129">El estado del filtro ha cambiado y ahora es incoherente con el enumerador.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-129">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ef8c-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ef8c-130">Remarks</span></span>

<span data-ttu-id="7ef8c-131">Este método recupera punteros al número especificado de anclajes, empezando en la posición actual de la enumeración, y los coloca en la matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-131">This method retrieves pointers to the specified number of pins, starting at the current position in the enumeration, and places them in the specified array.</span></span>

<span data-ttu-id="7ef8c-132">Este método llama al método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) del filtro para recuperar los pin.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-132">This method calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to retrieve the pins.</span></span>

<span data-ttu-id="7ef8c-133">Si el método se ejecuta correctamente, todos los punteros de **IPin** tienen recuentos de referencias pendientes.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-133">If the method succeeds, the **IPin** pointers all have outstanding reference counts.</span></span> <span data-ttu-id="7ef8c-134">Asegúrese de liberarlos cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="7ef8c-134">Be sure to release them when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ef8c-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ef8c-135">Requirements</span></span>



| <span data-ttu-id="7ef8c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ef8c-136">Requirement</span></span> | <span data-ttu-id="7ef8c-137">Value</span><span class="sxs-lookup"><span data-stu-id="7ef8c-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef8c-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ef8c-138">Header</span></span><br/>  | <dl> <span data-ttu-id="7ef8c-139"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ef8c-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7ef8c-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ef8c-140">Library</span></span><br/> | <dl> <span data-ttu-id="7ef8c-141"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7ef8c-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ef8c-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ef8c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef8c-143">**Clase CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="7ef8c-143">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




