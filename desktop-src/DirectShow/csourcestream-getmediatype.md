---
description: El método GetMediaType recupera un tipo de medio preferido. Este método usa los parámetros *iPosition* y *pMediaType* .
ms.assetid: c5c5f498-a9a3-4ce7-8cf5-941397aa649d
title: 'CSourceStream. GetMediaType (método) (Source. h): parámetros iPosition y pMediaType'
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
ms.openlocfilehash: 9d8936f08b952af069812859736a6a13ea9c0e4e
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187942"
---
# <a name="csourcestreamgetmediatype-method-sourceh---iposition-and-pmediatype-parameters"></a><span data-ttu-id="79f9d-104">CSourceStream. GetMediaType (método) (Source. h): parámetros iPosition y pMediaType</span><span class="sxs-lookup"><span data-stu-id="79f9d-104">CSourceStream.GetMediaType method (Source.h) - iPosition and pMediaType parameters</span></span>

<span data-ttu-id="79f9d-105">El método **GetMediaType** recupera un tipo de medio preferido.</span><span class="sxs-lookup"><span data-stu-id="79f9d-105">The **GetMediaType** method retrieves a preferred media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f9d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79f9d-106">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="79f9d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79f9d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f9d-108">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="79f9d-108">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="79f9d-109">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="79f9d-109">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="79f9d-110">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="79f9d-110">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="79f9d-111">Puntero a un objeto [**CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="79f9d-111">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f9d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79f9d-112">Return value</span></span>

<span data-ttu-id="79f9d-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="79f9d-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="79f9d-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="79f9d-114">Return code</span></span>                                                                                            | <span data-ttu-id="79f9d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="79f9d-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="79f9d-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="79f9d-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="79f9d-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="79f9d-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="79f9d-118"><dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt></span><span class="sxs-lookup"><span data-stu-id="79f9d-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="79f9d-119">Índice fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="79f9d-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="79f9d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="79f9d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="79f9d-121">Índice inferior a cero.</span><span class="sxs-lookup"><span data-stu-id="79f9d-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="79f9d-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="79f9d-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="79f9d-123">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="79f9d-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="79f9d-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="79f9d-124">Remarks</span></span>

<span data-ttu-id="79f9d-125">Hay dos versiones de este método.</span><span class="sxs-lookup"><span data-stu-id="79f9d-125">There are two versions of this method.</span></span> <span data-ttu-id="79f9d-126">Una versión invalida el método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) y toma un valor de índice como parámetro.</span><span class="sxs-lookup"><span data-stu-id="79f9d-126">One version overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method and takes an index value as a parameter.</span></span> <span data-ttu-id="79f9d-127">La otra versión está diseñada para recuperar un tipo de medio único, por lo que carece del parámetro de índice.</span><span class="sxs-lookup"><span data-stu-id="79f9d-127">The other version is designed to retrieve a single media type, so it lacks the index parameter.</span></span>

<span data-ttu-id="79f9d-128">El método de un solo parámetro devuelve E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="79f9d-128">The single-parameter method returns E\_UNEXPECTED.</span></span> <span data-ttu-id="79f9d-129">El método de dos parámetros comprueba que el parámetro *iPosition* es cero y, a continuación, llama a la versión de un solo parámetro.</span><span class="sxs-lookup"><span data-stu-id="79f9d-129">The two-parameter method verifies that the *iPosition* parameter is zero and then calls the single-parameter version.</span></span> <span data-ttu-id="79f9d-130">En función del número de tipos de medios que admita el PIN, debe invalidar uno de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="79f9d-130">Depending on the number of media types the pin supports, you must override one of these methods:</span></span>

-   <span data-ttu-id="79f9d-131">Si el PIN admite exactamente un tipo de medio, invalide la versión de un solo parámetro.</span><span class="sxs-lookup"><span data-stu-id="79f9d-131">If the pin supports exactly one media type, override the single-parameter version.</span></span> <span data-ttu-id="79f9d-132">Rellene el tipo de medio que admite el PIN.</span><span class="sxs-lookup"><span data-stu-id="79f9d-132">Fill in the media type that the pin supports.</span></span>
-   <span data-ttu-id="79f9d-133">Si el PIN admite más de un tipo de medio, invalide la versión de dos parámetros.</span><span class="sxs-lookup"><span data-stu-id="79f9d-133">If the pin supports more than one media type, override the two-parameter version.</span></span> <span data-ttu-id="79f9d-134">También invalide el método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="79f9d-134">Also override the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="79f9d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79f9d-135">Requirements</span></span>



| <span data-ttu-id="79f9d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="79f9d-136">Requirement</span></span> | <span data-ttu-id="79f9d-137">Value</span><span class="sxs-lookup"><span data-stu-id="79f9d-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79f9d-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79f9d-138">Header</span></span>  | <span data-ttu-id="79f9d-139">Source. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="79f9d-139">Source.h (include Streams.h)</span></span>                                                                                    |
| <span data-ttu-id="79f9d-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79f9d-140">Library</span></span> | <span data-ttu-id="79f9d-141">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="79f9d-141">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="79f9d-142">Consulte también</span><span class="sxs-lookup"><span data-stu-id="79f9d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f9d-143">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="79f9d-143">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




