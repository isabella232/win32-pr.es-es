---
description: El método GetMediaType recupera un tipo de medio preferido, por valor de índice.
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Método CTransformOutputPin. GetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680744"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="132b2-103">CTransformOutputPin. GetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="132b2-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="132b2-104">El `GetMediaType` método recupera un tipo de medio preferido, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="132b2-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="132b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="132b2-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="132b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="132b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="132b2-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="132b2-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="132b2-108">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="132b2-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="132b2-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="132b2-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="132b2-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="132b2-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="132b2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="132b2-111">Return value</span></span>

<span data-ttu-id="132b2-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="132b2-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="132b2-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="132b2-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="132b2-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="132b2-114">Return code</span></span>                                                                                            | <span data-ttu-id="132b2-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="132b2-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="132b2-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="132b2-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="132b2-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="132b2-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="132b2-118"><dt>**VFW \_ S \_ no hay \_ más \_ elementos**</dt></span><span class="sxs-lookup"><span data-stu-id="132b2-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="132b2-119">Índice fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="132b2-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="132b2-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="132b2-120">Remarks</span></span>

<span data-ttu-id="132b2-121">Este método invalida el método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="132b2-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="132b2-122">Si el PIN de entrada del filtro no está conectado, el método devuelve VFW \_ s \_ no hay \_ más \_ elementos.</span><span class="sxs-lookup"><span data-stu-id="132b2-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="132b2-123">De lo contrario, llama al método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) del filtro para recuperar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="132b2-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="132b2-124">El método **CTransformFilter:: GetMediaType** es virtual puro; la clase derivada del filtro debe reemplazarla.</span><span class="sxs-lookup"><span data-stu-id="132b2-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="132b2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="132b2-125">Requirements</span></span>



| <span data-ttu-id="132b2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="132b2-126">Requirement</span></span> | <span data-ttu-id="132b2-127">Value</span><span class="sxs-lookup"><span data-stu-id="132b2-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="132b2-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="132b2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="132b2-129"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="132b2-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="132b2-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="132b2-130">Library</span></span><br/> | <dl> <span data-ttu-id="132b2-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="132b2-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




