---
description: El método GetMediaType recupera un tipo de medio preferido.
ms.assetid: 85605885-adb5-4f13-91af-48bf74684eca
title: 'CSourceStream. GetMediaType (método) (Source. h): parámetro pMediaType'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8306da8451d4af7da8ce4f4c7d4d3f6fd367e1ec
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389188"
---
# <a name="csourcestreamgetmediatype-method-sourceh"></a><span data-ttu-id="63a05-103">CSourceStream. GetMediaType (método) (Source. h)</span><span class="sxs-lookup"><span data-stu-id="63a05-103">CSourceStream.GetMediaType method (Source.h)</span></span>

<span data-ttu-id="63a05-104">El `GetMediaType` método recupera un tipo de medio preferido.</span><span class="sxs-lookup"><span data-stu-id="63a05-104">The `GetMediaType` method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a05-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63a05-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="63a05-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63a05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a05-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="63a05-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="63a05-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="63a05-108">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a05-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63a05-109">Return value</span></span>

<span data-ttu-id="63a05-110">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="63a05-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="63a05-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="63a05-111">Return code</span></span>                                                                                            | <span data-ttu-id="63a05-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="63a05-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="63a05-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="63a05-113"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="63a05-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="63a05-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="63a05-115"><dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt></span><span class="sxs-lookup"><span data-stu-id="63a05-115"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="63a05-116">Índice fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="63a05-116">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="63a05-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="63a05-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="63a05-118">Índice inferior a cero.</span><span class="sxs-lookup"><span data-stu-id="63a05-118">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="63a05-119"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="63a05-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="63a05-120">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="63a05-120">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="63a05-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63a05-121">Remarks</span></span>

<span data-ttu-id="63a05-122">Hay dos versiones de este método.</span><span class="sxs-lookup"><span data-stu-id="63a05-122">There are two versions of this method.</span></span> <span data-ttu-id="63a05-123">Una versión invalida el método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) y toma un valor de índice como parámetro.</span><span class="sxs-lookup"><span data-stu-id="63a05-123">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="63a05-124">La otra versión está diseñada para recuperar un tipo de medio único, por lo que carece del parámetro de índice.</span><span class="sxs-lookup"><span data-stu-id="63a05-124">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="63a05-125">El método de un solo parámetro devuelve E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="63a05-125">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="63a05-126">El método de dos parámetros comprueba que el parámetro *iPosition* es cero y, a continuación, llama a la versión de un solo parámetro.</span><span class="sxs-lookup"><span data-stu-id="63a05-126">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="63a05-127">En función del número de tipos de medios que admita el PIN, debe invalidar uno de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="63a05-127">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="63a05-128">Si el PIN admite exactamente un tipo de medio, invalide la versión de un solo parámetro.</span><span class="sxs-lookup"><span data-stu-id="63a05-128">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="63a05-129">Rellene el tipo de medio que admite el PIN.</span><span class="sxs-lookup"><span data-stu-id="63a05-129">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="63a05-130">Si el PIN admite más de un tipo de medio, invalide la versión de dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="63a05-130">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="63a05-131">También invalide el método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="63a05-131">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="63a05-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63a05-132">Requirements</span></span>



| <span data-ttu-id="63a05-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="63a05-133">Requirement</span></span> | <span data-ttu-id="63a05-134">Value</span><span class="sxs-lookup"><span data-stu-id="63a05-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a05-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63a05-135">Header</span></span><br/>  | <dl> <span data-ttu-id="63a05-136"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63a05-136"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="63a05-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63a05-137">Library</span></span><br/> | <dl> <span data-ttu-id="63a05-138"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="63a05-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a05-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="63a05-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a05-140">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="63a05-140">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




