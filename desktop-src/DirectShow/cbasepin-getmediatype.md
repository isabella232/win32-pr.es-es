---
description: El método GetMediaType recupera un tipo de medio preferido, por valor de índice.
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Método CBasePin. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c54c5cd769a8efa0c720c7050cca45b00b8209e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671803"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="e4d03-103">CBasePin. GetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="e4d03-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="e4d03-104">El `GetMediaType` método recupera un tipo de medio preferido, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="e4d03-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d03-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4d03-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="e4d03-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4d03-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d03-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="e4d03-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d03-108">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="e4d03-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="e4d03-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="e4d03-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="e4d03-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="e4d03-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4d03-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4d03-111">Return value</span></span>

<span data-ttu-id="e4d03-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4d03-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e4d03-113">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e4d03-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="e4d03-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e4d03-114">Return code</span></span>                                                                                            | <span data-ttu-id="e4d03-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4d03-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e4d03-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d03-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="e4d03-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e4d03-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="e4d03-118"><dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d03-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="e4d03-119">Índice fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="e4d03-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="e4d03-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d03-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="e4d03-121">Índice inferior a cero.</span><span class="sxs-lookup"><span data-stu-id="e4d03-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="e4d03-122"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d03-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="e4d03-123">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="e4d03-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="e4d03-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e4d03-124">Remarks</span></span>

<span data-ttu-id="e4d03-125">En la lista de tipos de medios preferidos del PIN, este método devuelve el tipo con un valor de índice de *iPosition*.</span><span class="sxs-lookup"><span data-stu-id="e4d03-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="e4d03-126">La clase [**CEnumMediaTypes**](cenummediatypes.md) llama a este método para enumerar los tipos de medios preferidos.</span><span class="sxs-lookup"><span data-stu-id="e4d03-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="e4d03-127">La clase base devuelve E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="e4d03-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="e4d03-128">Invalide este método en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="e4d03-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d03-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4d03-129">Requirements</span></span>



| <span data-ttu-id="e4d03-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4d03-130">Requirement</span></span> | <span data-ttu-id="e4d03-131">Value</span><span class="sxs-lookup"><span data-stu-id="e4d03-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d03-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4d03-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e4d03-133"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4d03-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4d03-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4d03-134">Library</span></span><br/> | <dl> <span data-ttu-id="e4d03-135"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e4d03-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4d03-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4d03-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d03-137">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e4d03-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




