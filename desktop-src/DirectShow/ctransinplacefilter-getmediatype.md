---
description: El método GetMediaType recupera un tipo de medio preferido para el PIN de salida.
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Método CTransInPlaceFilter. GetMediaType (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2347e0466a7df848e0f0b2bccec325eedfefc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679290"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="d0310-103">CTransInPlaceFilter. GetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="d0310-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="d0310-104">El `GetMediaType` método recupera un tipo de medio preferido para el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="d0310-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0310-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0310-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="d0310-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0310-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0310-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="d0310-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="d0310-108">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="d0310-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="d0310-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="d0310-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="d0310-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="d0310-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0310-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0310-111">Return value</span></span>

<span data-ttu-id="d0310-112">Devuelve E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="d0310-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0310-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0310-113">Remarks</span></span>

<span data-ttu-id="d0310-114">Este método invalida el método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="d0310-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="d0310-115">En la clase **CTransInPlaceFilter** , cada pin llama al pin conectado opuesto para enumerar los tipos de medios preferidos.</span><span class="sxs-lookup"><span data-stu-id="d0310-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="d0310-116">El PIN de entrada llama al pin de entrada del filtro de bajada y el PIN de salida llama al pin de salida del filtro de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="d0310-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="d0310-117">Por lo tanto, `GetMediaType` nunca se llama al método del filtro.</span><span class="sxs-lookup"><span data-stu-id="d0310-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0310-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0310-118">Requirements</span></span>



| <span data-ttu-id="d0310-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0310-119">Requirement</span></span> | <span data-ttu-id="d0310-120">Value</span><span class="sxs-lookup"><span data-stu-id="d0310-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0310-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0310-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d0310-122"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0310-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0310-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0310-123">Library</span></span><br/> | <dl> <span data-ttu-id="d0310-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d0310-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0310-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0310-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0310-126">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="d0310-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




