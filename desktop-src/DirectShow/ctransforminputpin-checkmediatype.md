---
description: El método CheckMediaType determina si el PIN acepta un tipo de medio específico.
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: Método CTransformInputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6841370795a3131cdbcc95a3bab160be2011c600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680343"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="1e77e-103">CTransformInputPin. CheckMediaType, método</span><span class="sxs-lookup"><span data-stu-id="1e77e-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="1e77e-104">El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="1e77e-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e77e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e77e-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="1e77e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e77e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e77e-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="1e77e-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="1e77e-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="1e77e-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e77e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e77e-109">Return value</span></span>

<span data-ttu-id="1e77e-110">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e77e-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e77e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e77e-111">Remarks</span></span>

<span data-ttu-id="1e77e-112">Este método implementa el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtual puro.</span><span class="sxs-lookup"><span data-stu-id="1e77e-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="1e77e-113">Llama al método [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) del filtro, que también es virtual puro.</span><span class="sxs-lookup"><span data-stu-id="1e77e-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="1e77e-114">La clase derivada del filtro debe implementar **CheckInputType** para determinar si un tipo de entrada determinado es aceptable.</span><span class="sxs-lookup"><span data-stu-id="1e77e-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="1e77e-115">Si el PIN de salida del filtro está conectado, este método también llama al método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) del filtro para determinar si el tipo de entrada es compatible con el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="1e77e-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="1e77e-116">El método **CheckTransform** es también virtual puro.</span><span class="sxs-lookup"><span data-stu-id="1e77e-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e77e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e77e-117">Requirements</span></span>



| <span data-ttu-id="1e77e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e77e-118">Requirement</span></span> | <span data-ttu-id="1e77e-119">Value</span><span class="sxs-lookup"><span data-stu-id="1e77e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e77e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e77e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1e77e-121"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e77e-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1e77e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e77e-122">Library</span></span><br/> | <dl> <span data-ttu-id="1e77e-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1e77e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




