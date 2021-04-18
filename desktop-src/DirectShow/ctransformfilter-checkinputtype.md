---
description: El método CheckInputType comprueba si un tipo de medio especificado es aceptable para la entrada.
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: Método CTransformFilter. CheckInputType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660301"
---
# <a name="ctransformfiltercheckinputtype-method"></a><span data-ttu-id="8f04d-103">CTransformFilter. CheckInputType, método</span><span class="sxs-lookup"><span data-stu-id="8f04d-103">CTransformFilter.CheckInputType method</span></span>

<span data-ttu-id="8f04d-104">El `CheckInputType` método comprueba si un tipo de medio especificado es aceptable para la entrada.</span><span class="sxs-lookup"><span data-stu-id="8f04d-104">The `CheckInputType` method checks whether a specified media type is acceptable for input.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f04d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f04d-105">Syntax</span></span>


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8f04d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f04d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f04d-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="8f04d-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="8f04d-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8f04d-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f04d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f04d-109">Return value</span></span>

<span data-ttu-id="8f04d-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f04d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8f04d-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8f04d-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8f04d-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8f04d-112">Return code</span></span>                                                                                                | <span data-ttu-id="8f04d-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f04d-113">Description</span></span>                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="8f04d-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8f04d-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="8f04d-115">El tipo de medio es aceptable.</span><span class="sxs-lookup"><span data-stu-id="8f04d-115">Media type is acceptable.</span></span><br/>     |
| <dl> <span data-ttu-id="8f04d-116"><dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt></span><span class="sxs-lookup"><span data-stu-id="8f04d-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="8f04d-117">El tipo de medio no es aceptable.</span><span class="sxs-lookup"><span data-stu-id="8f04d-117">Media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f04d-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f04d-118">Remarks</span></span>

<span data-ttu-id="8f04d-119">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="8f04d-119">The derived class must implement this method.</span></span> <span data-ttu-id="8f04d-120">Devuelve S \_ OK si el formato de entrada propuesto es aceptable o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8f04d-120">Return S\_OK if the proposed input format is acceptable, or an error code otherwise.</span></span>

<span data-ttu-id="8f04d-121">Este método no necesita comprobar si el formato de entrada es compatible con el formato de salida (si existe).</span><span class="sxs-lookup"><span data-stu-id="8f04d-121">This method does not need to verify that the input format is compatible with the output format (if any).</span></span> <span data-ttu-id="8f04d-122">El PIN de entrada comprueba que se llama al método [**CheckTransform**](ctransformfilter-checktransform.md) .</span><span class="sxs-lookup"><span data-stu-id="8f04d-122">The input pin verifies that by calling the [**CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f04d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f04d-123">Requirements</span></span>



| <span data-ttu-id="8f04d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f04d-124">Requirement</span></span> | <span data-ttu-id="8f04d-125">Value</span><span class="sxs-lookup"><span data-stu-id="8f04d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f04d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f04d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8f04d-127"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f04d-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8f04d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f04d-128">Library</span></span><br/> | <dl> <span data-ttu-id="8f04d-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8f04d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f04d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f04d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f04d-131">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="8f04d-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




