---
description: 'Método CTransformFilter.GetMediaType: el método GetMediaType recupera un tipo de medio preferido para el pin de salida.'
ms.assetid: 9a1b123b-aa8a-4bf0-a926-466ded24e506
title: Método CTransformFilter.GetMediaType (Transfrm.h)
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
ms.openlocfilehash: 6415b8e3d8ae4e292b7e2592b123120927081ea8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095123"
---
# <a name="ctransformfiltergetmediatype-method"></a><span data-ttu-id="c7470-103">Método CTransformFilter.GetMediaType</span><span class="sxs-lookup"><span data-stu-id="c7470-103">CTransformFilter.GetMediaType method</span></span>

<span data-ttu-id="c7470-104">El `GetMediaType` método recupera un tipo de medio preferido para el pin de salida.</span><span class="sxs-lookup"><span data-stu-id="c7470-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7470-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7470-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c7470-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7470-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7470-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="c7470-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="c7470-108">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="c7470-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="c7470-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="c7470-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="c7470-110">Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c7470-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7470-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7470-111">Return value</span></span>

<span data-ttu-id="c7470-112">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c7470-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c7470-113">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c7470-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c7470-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c7470-114">Return code</span></span>                                                                                            | <span data-ttu-id="c7470-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7470-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c7470-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7470-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="c7470-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c7470-117">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="c7470-118"><dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="c7470-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="c7470-119">Índice fuera del intervalo.</span><span class="sxs-lookup"><span data-stu-id="c7470-119">Index out of range.</span></span><br/>   |
| <dl> <span data-ttu-id="c7470-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c7470-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="c7470-121">Índice menor que cero.</span><span class="sxs-lookup"><span data-stu-id="c7470-121">Index less than zero.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7470-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c7470-122">Remarks</span></span>

<span data-ttu-id="c7470-123">El método [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) del pin de salida llama a este método.</span><span class="sxs-lookup"><span data-stu-id="c7470-123">The output pin's [**CTransformOutputPin::GetMediaType**](ctransformoutputpin-getmediatype.md) method calls this method.</span></span> <span data-ttu-id="c7470-124">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="c7470-124">The derived class must implement this method.</span></span> <span data-ttu-id="c7470-125">Para obtener más información, [**vea CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="c7470-125">For more information, see [**CBasePin::GetMediaType**](cbasepin-getmediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7470-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7470-126">Requirements</span></span>



| <span data-ttu-id="c7470-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7470-127">Requirement</span></span> | <span data-ttu-id="c7470-128">Value</span><span class="sxs-lookup"><span data-stu-id="c7470-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7470-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7470-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c7470-130"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c7470-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c7470-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7470-131">Library</span></span><br/> | <dl> <span data-ttu-id="c7470-132"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c7470-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7470-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c7470-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7470-134">**CTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="c7470-134">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




