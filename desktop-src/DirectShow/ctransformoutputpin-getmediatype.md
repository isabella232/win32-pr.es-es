---
description: 'Método CTransformOutputPin.GetMediaType: el método GetMediaType recupera un tipo de medio preferido, por valor de índice.'
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: Método CTransformOutputPin.GetMediaType (Transfrm.h)
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
ms.openlocfilehash: 1dd0bf38f2fa3be0e077f2509001680bbfc84e15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094903"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="6df68-103">Método CTransformOutputPin.GetMediaType</span><span class="sxs-lookup"><span data-stu-id="6df68-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="6df68-104">El `GetMediaType` método recupera un tipo de medio preferido, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="6df68-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df68-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6df68-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="6df68-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6df68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df68-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="6df68-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="6df68-108">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="6df68-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="6df68-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="6df68-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="6df68-110">Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6df68-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df68-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6df68-111">Return value</span></span>

<span data-ttu-id="6df68-112">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="6df68-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6df68-113">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6df68-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6df68-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6df68-114">Return code</span></span>                                                                                            | <span data-ttu-id="6df68-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6df68-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="6df68-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6df68-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="6df68-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="6df68-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="6df68-118"><dt>**VFW \_ S \_ NO \_ MORE \_ ITEMS**</dt></span><span class="sxs-lookup"><span data-stu-id="6df68-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="6df68-119">Índice fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="6df68-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6df68-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6df68-120">Remarks</span></span>

<span data-ttu-id="6df68-121">Este método invalida el [**método CBasePin::GetMediaType.**](cbasepin-getmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="6df68-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="6df68-122">Si el pin de entrada del filtro no está conectado, el método devuelve VFW \_ S \_ NO MORE \_ \_ ITEMS.</span><span class="sxs-lookup"><span data-stu-id="6df68-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="6df68-123">De lo contrario, llama al método [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) del filtro para recuperar el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6df68-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="6df68-124">El **método CTransformFilter::GetMediaType** es virtual puro; La clase derivada del filtro debe invalidarla.</span><span class="sxs-lookup"><span data-stu-id="6df68-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df68-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6df68-125">Requirements</span></span>



| <span data-ttu-id="6df68-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6df68-126">Requirement</span></span> | <span data-ttu-id="6df68-127">Value</span><span class="sxs-lookup"><span data-stu-id="6df68-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df68-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6df68-128">Header</span></span><br/>  | <dl> <span data-ttu-id="6df68-129"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6df68-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6df68-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6df68-130">Library</span></span><br/> | <dl> <span data-ttu-id="6df68-131"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6df68-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




