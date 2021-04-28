---
description: 'Método CBasePin.GetMediaType: el método GetMediaType recupera un tipo de medio preferido, por valor de índice.'
ms.assetid: 96f102b0-e2d1-49a1-84af-aa4622cae2a9
title: Método CBasePin.GetMediaType (Amfilter.h)
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
ms.openlocfilehash: 186f2eddbedf4eb0565a4ca66ff4ed7e5b080090
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099373"
---
# <a name="cbasepingetmediatype-method"></a><span data-ttu-id="7db94-103">Método CBasePin.GetMediaType</span><span class="sxs-lookup"><span data-stu-id="7db94-103">CBasePin.GetMediaType method</span></span>

<span data-ttu-id="7db94-104">El `GetMediaType` método recupera un tipo de medio preferido, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="7db94-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7db94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7db94-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="7db94-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7db94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7db94-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="7db94-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="7db94-108">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="7db94-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="7db94-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="7db94-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="7db94-110">Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="7db94-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7db94-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7db94-111">Return value</span></span>

<span data-ttu-id="7db94-112">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="7db94-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7db94-113">Los valores posibles incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7db94-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7db94-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7db94-114">Return code</span></span>                                                                                            | <span data-ttu-id="7db94-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="7db94-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7db94-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7db94-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="7db94-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7db94-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="7db94-118"><dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="7db94-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="7db94-119">Índice fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="7db94-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="7db94-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7db94-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="7db94-121">Índice menor que cero.</span><span class="sxs-lookup"><span data-stu-id="7db94-121">Index less than zero.</span></span><br/> |
| <dl> <span data-ttu-id="7db94-122"><dt>**E \_ UNEXPECTED**</dt></span><span class="sxs-lookup"><span data-stu-id="7db94-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="7db94-123">error inesperado.</span><span class="sxs-lookup"><span data-stu-id="7db94-123">Unexpected error.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="7db94-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7db94-124">Remarks</span></span>

<span data-ttu-id="7db94-125">En la lista de tipos de medios preferidos del pin, este método devuelve el tipo con un valor de índice *de iPosition*.</span><span class="sxs-lookup"><span data-stu-id="7db94-125">From the pin's list of preferred media types, this method returns the type with an index value of *iPosition*.</span></span> <span data-ttu-id="7db94-126">La [**clase CEnumMediaTypes**](cenummediatypes.md) llama a este método para enumerar los tipos de medios preferidos.</span><span class="sxs-lookup"><span data-stu-id="7db94-126">The [**CEnumMediaTypes**](cenummediatypes.md) class calls this method to enumerate preferred media types.</span></span>

<span data-ttu-id="7db94-127">La clase base devuelve E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="7db94-127">The base class returns E\_UNEXPECTED.</span></span> <span data-ttu-id="7db94-128">Invalide este método en la clase derivada.</span><span class="sxs-lookup"><span data-stu-id="7db94-128">Override this method in your derived class.</span></span>

## <a name="requirements"></a><span data-ttu-id="7db94-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7db94-129">Requirements</span></span>



| <span data-ttu-id="7db94-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7db94-130">Requirement</span></span> | <span data-ttu-id="7db94-131">Value</span><span class="sxs-lookup"><span data-stu-id="7db94-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db94-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7db94-132">Header</span></span><br/>  | <dl> <span data-ttu-id="7db94-133"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7db94-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7db94-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7db94-134">Library</span></span><br/> | <dl> <span data-ttu-id="7db94-135"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7db94-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7db94-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7db94-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7db94-137">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="7db94-137">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




