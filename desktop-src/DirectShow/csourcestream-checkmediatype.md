---
description: 'El método CheckMediaType determina si el PIN acepta un tipo de medio específico. Este método implementa el método CBasePin:: CheckMediaType virtual puro.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: CSourceStream. CheckMediaType (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660723"
---
# <a name="csourcestreamcheckmediatype-method"></a><span data-ttu-id="a86f6-104">CSourceStream. CheckMediaType, método</span><span class="sxs-lookup"><span data-stu-id="a86f6-104">CSourceStream.CheckMediaType method</span></span>

<span data-ttu-id="a86f6-105">El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="a86f6-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="a86f6-106">Este método implementa el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtual puro.</span><span class="sxs-lookup"><span data-stu-id="a86f6-106">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a86f6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a86f6-107">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="a86f6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a86f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a86f6-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="a86f6-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="a86f6-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="a86f6-110">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a86f6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a86f6-111">Return value</span></span>

<span data-ttu-id="a86f6-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a86f6-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a86f6-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a86f6-113">Return code</span></span>                                                                            | <span data-ttu-id="a86f6-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a86f6-114">Description</span></span>                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a86f6-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="a86f6-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a86f6-116">Este pin es compatible con este tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a86f6-116">This pin supports this media type.</span></span><br/>        |
| <dl> <span data-ttu-id="a86f6-117"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="a86f6-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a86f6-118">El PIN no admite este tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a86f6-118">The pin does not support this media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a86f6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a86f6-119">Remarks</span></span>

<span data-ttu-id="a86f6-120">De forma predeterminada, el PIN admite un solo tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a86f6-120">By default, the pin supports a single media type.</span></span> <span data-ttu-id="a86f6-121">Este método recupera el tipo admitido mediante una llamada a la versión de un solo parámetro del método [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) y lo compara con el tipo propuesto.</span><span class="sxs-lookup"><span data-stu-id="a86f6-121">This method retrieves the supported type by calling the single-parameter version of the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method, and compares it to the proposed type.</span></span> <span data-ttu-id="a86f6-122">Si el PIN admite más de un tipo de medio, Invalide este método.</span><span class="sxs-lookup"><span data-stu-id="a86f6-122">If your pin supports more than one media type, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a86f6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a86f6-123">Requirements</span></span>



| <span data-ttu-id="a86f6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a86f6-124">Requirement</span></span> | <span data-ttu-id="a86f6-125">Value</span><span class="sxs-lookup"><span data-stu-id="a86f6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a86f6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a86f6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a86f6-127"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a86f6-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a86f6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a86f6-128">Library</span></span><br/> | <dl> <span data-ttu-id="a86f6-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a86f6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a86f6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a86f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a86f6-131">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="a86f6-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




