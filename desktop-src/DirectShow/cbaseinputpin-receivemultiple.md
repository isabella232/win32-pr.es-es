---
description: 'El método ReceiveMultiple recibe una matriz de ejemplos. Este método implementa el método IMemInputPin:: ReceiveMultiple.'
ms.assetid: 21e757c7-f623-4ccb-8e37-512ee4dd7aa7
title: Método CBaseInputPin. ReceiveMultiple (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5725b7d8b70c8f7c61eb44231812997a903ba41a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671711"
---
# <a name="cbaseinputpinreceivemultiple-method"></a><span data-ttu-id="defda-104">CBaseInputPin. ReceiveMultiple, método</span><span class="sxs-lookup"><span data-stu-id="defda-104">CBaseInputPin.ReceiveMultiple method</span></span>

<span data-ttu-id="defda-105">El `ReceiveMultiple` método recibe una matriz de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="defda-105">The `ReceiveMultiple` method receives an array of samples.</span></span> <span data-ttu-id="defda-106">Este método implementa el método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="defda-106">This method implements the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="defda-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="defda-107">Syntax</span></span>


```C++
HRESULT ReceiveMultiple(
   IMediaSample **pSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="defda-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="defda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="defda-109">*pSamples*</span><span class="sxs-lookup"><span data-stu-id="defda-109">*pSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="defda-110">Dirección de una matriz de punteros [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) , de tamaño *nSamples*.</span><span class="sxs-lookup"><span data-stu-id="defda-110">Address of an array of [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers, of size *nSamples*.</span></span>

</dd> <dt>

<span data-ttu-id="defda-111">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="defda-111">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="defda-112">Número de muestras que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="defda-112">Number of samples to process.</span></span>

</dd> <dt>

<span data-ttu-id="defda-113">*nSamplesProcessed*</span><span class="sxs-lookup"><span data-stu-id="defda-113">*nSamplesProcessed*</span></span> 
</dt> <dd>

<span data-ttu-id="defda-114">Puntero a una variable que recibe el número de muestras que se procesaron.</span><span class="sxs-lookup"><span data-stu-id="defda-114">Pointer to a variable that receives the number of samples that were processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="defda-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="defda-115">Return value</span></span>

<span data-ttu-id="defda-116">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="defda-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="defda-117">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="defda-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="defda-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="defda-118">Return code</span></span>                                                                                             | <span data-ttu-id="defda-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="defda-119">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="defda-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="defda-120"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="defda-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="defda-121">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="defda-122"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="defda-122"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="defda-123">El PIN se está vaciando actualmente; se rechazó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="defda-123">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="defda-124"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="defda-124"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="defda-125">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="defda-125">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="defda-126"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="defda-126"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="defda-127">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="defda-127">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="defda-128"><dt>**\_error de \_ tiempo de ejecución de VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="defda-128"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="defda-129">Se produjo un error en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="defda-129">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="defda-130"><dt>**Estado de VFW \_ E \_ incorrecto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="defda-130"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="defda-131">El PIN está detenido.</span><span class="sxs-lookup"><span data-stu-id="defda-131">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="defda-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="defda-132">Remarks</span></span>

<span data-ttu-id="defda-133">Este método se comporta como el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) , pero recibe una matriz de ejemplos.</span><span class="sxs-lookup"><span data-stu-id="defda-133">This method behaves like the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method, but receives an array of samples.</span></span> <span data-ttu-id="defda-134">En la clase base, el método recorre en bucle la matriz y llama a **Receive** con cada ejemplo.</span><span class="sxs-lookup"><span data-stu-id="defda-134">In the base class, the method loops through the array and calls **Receive** with each sample.</span></span> <span data-ttu-id="defda-135">Invalide esta función si el filtro puede procesar lotes de muestras de forma más eficaz que procesarlos de uno en uno.</span><span class="sxs-lookup"><span data-stu-id="defda-135">Override this function if your filter can process batches of samples more efficiently than processing them one at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="defda-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="defda-136">Requirements</span></span>



| <span data-ttu-id="defda-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="defda-137">Requirement</span></span> | <span data-ttu-id="defda-138">Value</span><span class="sxs-lookup"><span data-stu-id="defda-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="defda-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="defda-139">Header</span></span><br/>  | <dl> <span data-ttu-id="defda-140"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="defda-140"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="defda-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="defda-141">Library</span></span><br/> | <dl> <span data-ttu-id="defda-142"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="defda-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="defda-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="defda-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="defda-144">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="defda-144">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




