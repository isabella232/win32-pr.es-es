---
description: El método GetMediaType recupera un tipo de medio preferido para el PIN de salida.
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Método CTransformFilter. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba751e291a1ffa8e030be7e77cfd456956718baa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661051"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="9318b-103">CTransformFilter. GetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="9318b-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="9318b-104">El `GetMediaType` método recupera un tipo de medio preferido para el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="9318b-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="9318b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9318b-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="9318b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9318b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9318b-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="9318b-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="9318b-108">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="9318b-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="9318b-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="9318b-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="9318b-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="9318b-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9318b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9318b-111">Return value</span></span>

<span data-ttu-id="9318b-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9318b-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9318b-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="9318b-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="9318b-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9318b-114">Return code</span></span>                                                                                            | <span data-ttu-id="9318b-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9318b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9318b-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9318b-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="9318b-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9318b-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="9318b-118"><dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt></span><span class="sxs-lookup"><span data-stu-id="9318b-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="9318b-119">Índice fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="9318b-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="9318b-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9318b-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="9318b-121">Índice inferior a cero.</span><span class="sxs-lookup"><span data-stu-id="9318b-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9318b-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9318b-122">Remarks</span></span>

<span data-ttu-id="9318b-123">El método [**CTransformOutputPin:: GetMediaType**](ctransformoutputpin-getmediatype.md) del PIN de salida llama a este método.</span><span class="sxs-lookup"><span data-stu-id="9318b-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="9318b-124">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="9318b-124">The derived class must implement this method.</span></span> <span data-ttu-id="9318b-125">Para obtener más información, vea [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="9318b-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9318b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9318b-126">Requirements</span></span>



| <span data-ttu-id="9318b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9318b-127">Requirement</span></span> | <span data-ttu-id="9318b-128">Value</span><span class="sxs-lookup"><span data-stu-id="9318b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9318b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9318b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9318b-130"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9318b-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9318b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9318b-131">Library</span></span><br/> | <dl> <span data-ttu-id="9318b-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9318b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9318b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="9318b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9318b-134">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9318b-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




