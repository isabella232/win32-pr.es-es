---
description: 'El método siguiente recupera un número especificado de tipos de medios. Este método implementa el método IEnumMediaTypes:: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Método CEnumMediaTypes. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660868"
---
# <a name="cenummediatypesnext-method"></a><span data-ttu-id="ab3bd-104">CEnumMediaTypes. Next (método)</span><span class="sxs-lookup"><span data-stu-id="ab3bd-104">CEnumMediaTypes.Next method</span></span>

<span data-ttu-id="ab3bd-105">El `Next` método recupera un número especificado de tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-105">The `Next` method retrieves a specified number of media types.</span></span> <span data-ttu-id="ab3bd-106">Este método implementa el método [**IEnumMediaTypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .</span><span class="sxs-lookup"><span data-stu-id="ab3bd-106">This method implements the [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab3bd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab3bd-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="ab3bd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab3bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab3bd-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="ab3bd-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="ab3bd-110">Número de tipos de medios que se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-110">Number of media types to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ab3bd-111">*ppMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="ab3bd-111">*ppMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="ab3bd-112">Matriz de punteros a estructuras de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , de tamaño *cPins*.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-112">Array of pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures, of size *cPins*.</span></span>

</dd> <dt>

<span data-ttu-id="ab3bd-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="ab3bd-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="ab3bd-114">Puntero a una variable que recibe el número de tipos de medios que devuelve el método.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-114">Pointer to a variable that receives the number of media types the method returned.</span></span> <span data-ttu-id="ab3bd-115">Puede ser **null** si *cMediaTypes* es 1.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-115">Can be **NULL** if *cMediaTypes* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab3bd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab3bd-116">Return value</span></span>

<span data-ttu-id="ab3bd-117">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ab3bd-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ab3bd-118">Return code</span></span>                                                                                                | <span data-ttu-id="ab3bd-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab3bd-119">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab3bd-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3bd-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="ab3bd-121">No recuperó tantos tipos de medios como se solicitó.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-121">Did not retrieve as many media types as requested.</span></span><br/>                       |
| <dl> <span data-ttu-id="ab3bd-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3bd-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="ab3bd-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-123">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="ab3bd-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3bd-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="ab3bd-125">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-125">Invalid argument.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ab3bd-126"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3bd-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="ab3bd-127">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ab3bd-127">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="ab3bd-128"><dt>**\_ \_ enumeración de VFW E no \_ \_ \_ sincronizada**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3bd-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="ab3bd-129">El estado del PIN ha cambiado y ahora es incoherente con el enumerador.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-129">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab3bd-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab3bd-130">Remarks</span></span>

<span data-ttu-id="ab3bd-131">Si el método se ejecuta correctamente, la matriz especificada por *ppMediaTypes* contiene punteros a \_ estructuras de tipo de medio am \_ .</span><span class="sxs-lookup"><span data-stu-id="ab3bd-131">If the method succeeds, the array specified by *ppMediaTypes* contains pointers to AM\_MEDIA\_TYPE structures.</span></span> <span data-ttu-id="ab3bd-132">El número de estructuras es igual a *\* pcFetched*.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-132">The number of structures is equal to *\*pcFetched*.</span></span> <span data-ttu-id="ab3bd-133">Libere cada tipo de medio mediante una llamada a la función [**DeleteMediaType**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="ab3bd-133">Free each media type by calling the [**DeleteMediaType**](deletemediatype.md) function.</span></span>

<span data-ttu-id="ab3bd-134">Este método llama al método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) del PIN para recuperar los tipos de medios.</span><span class="sxs-lookup"><span data-stu-id="ab3bd-134">This method calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to retrieve the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab3bd-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab3bd-135">Requirements</span></span>



| <span data-ttu-id="ab3bd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab3bd-136">Requirement</span></span> | <span data-ttu-id="ab3bd-137">Value</span><span class="sxs-lookup"><span data-stu-id="ab3bd-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3bd-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab3bd-138">Header</span></span><br/>  | <dl> <span data-ttu-id="ab3bd-139"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab3bd-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ab3bd-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab3bd-140">Library</span></span><br/> | <dl> <span data-ttu-id="ab3bd-141"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab3bd-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab3bd-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab3bd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab3bd-143">**Clase CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="ab3bd-143">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




