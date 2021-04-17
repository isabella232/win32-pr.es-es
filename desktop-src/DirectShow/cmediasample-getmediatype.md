---
description: 'El método GetMediaType recupera el tipo de medio, si el tipo de medio es distinto del ejemplo anterior. Este método implementa el método IMediaSample:: GetMediaType.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Método CMediaSample. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670665"
---
# <a name="cmediasamplegetmediatype-method"></a><span data-ttu-id="80e74-104">CMediaSample. GetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="80e74-104">CMediaSample.GetMediaType method</span></span>

<span data-ttu-id="80e74-105">El `GetMediaType` método recupera el tipo de medio si el tipo de medio es distinto del ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="80e74-105">The `GetMediaType` method retrieves the media type, if the media type differs from the previous sample.</span></span> <span data-ttu-id="80e74-106">Este método implementa el método [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="80e74-106">This method implements the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e74-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80e74-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="80e74-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80e74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e74-109">*ppMediaType*</span><span class="sxs-lookup"><span data-stu-id="80e74-109">*ppMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="80e74-110">Dirección de una variable que recibe un puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="80e74-110">Address of a variable that receives a pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="80e74-111">Si el tipo de medio no ha cambiado en el ejemplo anterior, *\* ppMediaType* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="80e74-111">If the media type has not changed from the previous sample, *\*ppMediaType* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e74-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80e74-112">Return value</span></span>

<span data-ttu-id="80e74-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="80e74-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="80e74-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="80e74-114">Return code</span></span>                                                                                   | <span data-ttu-id="80e74-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="80e74-115">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="80e74-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="80e74-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="80e74-117">El tipo de medio no ha cambiado en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="80e74-117">The media type has not changed from the previous sample.</span></span><br/> |
| <dl> <span data-ttu-id="80e74-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="80e74-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="80e74-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="80e74-119">Success.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="80e74-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="80e74-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="80e74-121">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="80e74-121">Insufficient memory.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="80e74-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80e74-122">Remarks</span></span>

<span data-ttu-id="80e74-123">Cuando haya terminado con el tipo de medio, libere el bloque de memoria mediante una llamada a la función de la utilidad [**DeleteMediaType**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="80e74-123">When you are done with the media type, free the memory block by calling the [**DeleteMediaType**](deletemediatype.md) utility function.</span></span>

<span data-ttu-id="80e74-124">La variable miembro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="80e74-124">The [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable specifies the media type.</span></span> <span data-ttu-id="80e74-125">La variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica si el tipo de medio ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="80e74-125">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the media type has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="80e74-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80e74-126">Requirements</span></span>



| <span data-ttu-id="80e74-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e74-127">Requirement</span></span> | <span data-ttu-id="80e74-128">Value</span><span class="sxs-lookup"><span data-stu-id="80e74-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e74-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80e74-129">Header</span></span><br/>  | <dl> <span data-ttu-id="80e74-130"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80e74-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="80e74-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80e74-131">Library</span></span><br/> | <dl> <span data-ttu-id="80e74-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="80e74-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80e74-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="80e74-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e74-134">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="80e74-134">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




