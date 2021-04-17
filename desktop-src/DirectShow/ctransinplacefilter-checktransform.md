---
description: 'El método CheckTransform comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida. Este método invalida el método CTransformFilter:: CheckTransform.'
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: Método CTransInPlaceFilter. CheckTransform (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681105"
---
# <a name="ctransinplacefilterchecktransform-method"></a><span data-ttu-id="ef02a-104">CTransInPlaceFilter. CheckTransform, método</span><span class="sxs-lookup"><span data-stu-id="ef02a-104">CTransInPlaceFilter.CheckTransform method</span></span>

<span data-ttu-id="ef02a-105">El `CheckTransform` método comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="ef02a-105">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span> <span data-ttu-id="ef02a-106">Este método invalida el método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="ef02a-106">This method overrides the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef02a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef02a-107">Syntax</span></span>


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a><span data-ttu-id="ef02a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef02a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef02a-109">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="ef02a-109">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="ef02a-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ef02a-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="ef02a-111">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="ef02a-111">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="ef02a-112">Puntero a un objeto **CMediaType** que especifica el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="ef02a-112">Pointer to a **CMediaType** object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef02a-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef02a-113">Return value</span></span>

<span data-ttu-id="ef02a-114">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ef02a-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef02a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef02a-115">Remarks</span></span>

<span data-ttu-id="ef02a-116">El filtro **CTransInPlace** nunca llama a `CheckTransform` .</span><span class="sxs-lookup"><span data-stu-id="ef02a-116">The **CTransInPlace** filter never calls `CheckTransform`.</span></span> <span data-ttu-id="ef02a-117">En su lugar, todas las conexiones de PIN usan [**CTransformFilter:: CheckInputType**](ctransformfilter-checkinputtype.md) para comprobar el tipo de medio, con la suposición de que los tipos de entrada y salida siempre coinciden.</span><span class="sxs-lookup"><span data-stu-id="ef02a-117">Instead, all pin connection use [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) to check the media type, with the assumption that the input and output types always match.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef02a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef02a-118">Requirements</span></span>



| <span data-ttu-id="ef02a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef02a-119">Requirement</span></span> | <span data-ttu-id="ef02a-120">Value</span><span class="sxs-lookup"><span data-stu-id="ef02a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef02a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef02a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ef02a-122"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef02a-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ef02a-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef02a-123">Library</span></span><br/> | <dl> <span data-ttu-id="ef02a-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ef02a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef02a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef02a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef02a-126">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="ef02a-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




