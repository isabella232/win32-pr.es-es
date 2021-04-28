---
description: 'Método CTransInPlaceOutputPin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: Método CTransInPlaceOutputPin.CheckMediaType (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66cd29758e0b2d63db88db8b998cc79ec12efdd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094723"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="62cde-103">Método CTransInPlaceOutputPin.CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="62cde-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="62cde-104">El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="62cde-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="62cde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62cde-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="62cde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="62cde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62cde-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="62cde-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="62cde-108">Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="62cde-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62cde-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="62cde-109">Return value</span></span>

<span data-ttu-id="62cde-110">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="62cde-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="62cde-111">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="62cde-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="62cde-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="62cde-112">Return code</span></span>                                                                                                | <span data-ttu-id="62cde-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="62cde-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="62cde-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="62cde-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="62cde-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="62cde-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="62cde-116"><dt>**TIPO E VFW \_ \_ NO \_ \_ ACEPTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="62cde-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="62cde-117">Tipo de medio no aceptado.</span><span class="sxs-lookup"><span data-stu-id="62cde-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62cde-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="62cde-118">Remarks</span></span>

<span data-ttu-id="62cde-119">Este método invalida el [**método CTransformOutputPin::CheckMediaType.**](ctransformoutputpin-checkmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="62cde-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="62cde-120">Si el filtro ya está transmitiendo y usa dos asignadores, este método rechaza los cambios de formato.</span><span class="sxs-lookup"><span data-stu-id="62cde-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="62cde-121">De lo contrario, este método llama al método [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) del filtro para comprobar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="62cde-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="62cde-122">Si el pin de entrada está conectado, también llama al método [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) en el pin de salida ascendente.</span><span class="sxs-lookup"><span data-stu-id="62cde-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="62cde-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62cde-123">Requirements</span></span>



| <span data-ttu-id="62cde-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="62cde-124">Requirement</span></span> | <span data-ttu-id="62cde-125">Value</span><span class="sxs-lookup"><span data-stu-id="62cde-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62cde-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="62cde-126">Header</span></span><br/>  | <dl> <span data-ttu-id="62cde-127"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="62cde-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62cde-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62cde-128">Library</span></span><br/> | <dl> <span data-ttu-id="62cde-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="62cde-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62cde-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="62cde-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62cde-131">**CTransInPlaceOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="62cde-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




