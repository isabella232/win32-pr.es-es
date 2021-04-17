---
description: El método CheckMediaType determina si el PIN acepta un tipo de medio específico.
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Método CTransInPlaceInputPin. CheckMediaType (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22f271759bc0ade6b820aed2039bbc16a2cf4a31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660365"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="37124-103">CTransInPlaceInputPin. CheckMediaType, método</span><span class="sxs-lookup"><span data-stu-id="37124-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="37124-104">El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="37124-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="37124-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37124-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="37124-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37124-107">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="37124-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="37124-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="37124-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37124-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37124-109">Return value</span></span>

<span data-ttu-id="37124-110">Devuelve S \_ OK si el tipo de medio propuesto es aceptable.</span><span class="sxs-lookup"><span data-stu-id="37124-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="37124-111">De lo contrario, devuelve S \_ false o un código de error.</span><span class="sxs-lookup"><span data-stu-id="37124-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="37124-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37124-112">Remarks</span></span>

<span data-ttu-id="37124-113">Este método invalida el método [**CTransformInputPin:: CheckMediaType**](ctransforminputpin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="37124-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="37124-114">Llama al método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="37124-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="37124-115">Si el PIN de salida está conectado, este método también llama al método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="37124-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="37124-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37124-116">Requirements</span></span>



| <span data-ttu-id="37124-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="37124-117">Requirement</span></span> | <span data-ttu-id="37124-118">Value</span><span class="sxs-lookup"><span data-stu-id="37124-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37124-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37124-119">Header</span></span><br/>  | <dl> <span data-ttu-id="37124-120"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37124-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37124-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37124-121">Library</span></span><br/> | <dl> <span data-ttu-id="37124-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="37124-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37124-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="37124-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37124-124">**Clase CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="37124-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




