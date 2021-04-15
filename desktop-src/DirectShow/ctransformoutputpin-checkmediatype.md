---
description: El método CheckMediaType determina si el PIN acepta un tipo de medio específico.
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Método CTransformOutputPin. CheckMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c2bc617a5ff56a8b82184700af85e2634960ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661313"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="c521d-103">CTransformOutputPin. CheckMediaType, método</span><span class="sxs-lookup"><span data-stu-id="c521d-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="c521d-104">El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="c521d-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c521d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c521d-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="c521d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c521d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c521d-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="c521d-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="c521d-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="c521d-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c521d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c521d-109">Return value</span></span>

<span data-ttu-id="c521d-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c521d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c521d-111">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="c521d-111">Possible values include the following.</span></span>



| <span data-ttu-id="c521d-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c521d-112">Return code</span></span>                                                                                  | <span data-ttu-id="c521d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="c521d-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="c521d-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c521d-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c521d-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c521d-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c521d-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c521d-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c521d-117">El PIN de entrada del filtro no está conectado.</span><span class="sxs-lookup"><span data-stu-id="c521d-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c521d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c521d-118">Remarks</span></span>

<span data-ttu-id="c521d-119">Este método implementa el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtual puro.</span><span class="sxs-lookup"><span data-stu-id="c521d-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="c521d-120">El método genera un error si el PIN de entrada del filtro no está conectado.</span><span class="sxs-lookup"><span data-stu-id="c521d-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="c521d-121">De lo contrario, llama al método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) del filtro, que también es virtual puro.</span><span class="sxs-lookup"><span data-stu-id="c521d-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="c521d-122">La clase derivada del filtro debe implementar **CheckTransform**, que determina si el tipo de medio de salida propuesto es compatible con el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="c521d-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c521d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c521d-123">Requirements</span></span>



| <span data-ttu-id="c521d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c521d-124">Requirement</span></span> | <span data-ttu-id="c521d-125">Value</span><span class="sxs-lookup"><span data-stu-id="c521d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c521d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c521d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c521d-127"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c521d-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c521d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c521d-128">Library</span></span><br/> | <dl> <span data-ttu-id="c521d-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c521d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




