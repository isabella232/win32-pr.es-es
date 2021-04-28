---
description: 'Método CTransInPlaceInputPin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: Método CTransInPlaceInputPin.CheckMediaType (Transip.h)
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
ms.openlocfilehash: 5de3cec87d740db42824b0d7abf1ee4bfc6aeecb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094803"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="a3f4b-103">Método CTransInPlaceInputPin.CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="a3f4b-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="a3f4b-104">El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3f4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3f4b-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="a3f4b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3f4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3f4b-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="a3f4b-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a3f4b-108">Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3f4b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3f4b-109">Return value</span></span>

<span data-ttu-id="a3f4b-110">Devuelve S \_ OK si el tipo de medio propuesto es aceptable.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="a3f4b-111">De lo contrario, devuelve S \_ FALSE o un código de error.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3f4b-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a3f4b-112">Remarks</span></span>

<span data-ttu-id="a3f4b-113">Este método invalida el [**método CTransformInputPin::CheckMediaType.**](ctransforminputpin-checkmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="a3f4b-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="a3f4b-114">Llama al método [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="a3f4b-115">Si el pin de salida está conectado, este método también llama al método [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el pin de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="a3f4b-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f4b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3f4b-116">Requirements</span></span>



| <span data-ttu-id="a3f4b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3f4b-117">Requirement</span></span> | <span data-ttu-id="a3f4b-118">Value</span><span class="sxs-lookup"><span data-stu-id="a3f4b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f4b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3f4b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a3f4b-120"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4b-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a3f4b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3f4b-121">Library</span></span><br/> | <dl> <span data-ttu-id="a3f4b-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a3f4b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f4b-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a3f4b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f4b-124">**CTransInPlaceInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="a3f4b-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




