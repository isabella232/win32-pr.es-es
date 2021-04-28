---
description: 'Método CTransInPlaceFilter.GetMediaType: el método GetMediaType recupera un tipo de medio preferido para el pin de salida.'
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: Método CTransInPlaceFilter.GetMediaType (Transip.h)
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
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094813"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="fb055-103">Método CTransInPlaceFilter.GetMediaType</span><span class="sxs-lookup"><span data-stu-id="fb055-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="fb055-104">El `GetMediaType` método recupera un tipo de medio preferido para el pin de salida.</span><span class="sxs-lookup"><span data-stu-id="fb055-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb055-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb055-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="fb055-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb055-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb055-107">*iPosition*</span><span class="sxs-lookup"><span data-stu-id="fb055-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="fb055-108">Valor de índice de base cero.</span><span class="sxs-lookup"><span data-stu-id="fb055-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="fb055-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="fb055-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="fb055-110">Puntero a un [**objeto CMediaType**](cmediatype.md) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="fb055-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb055-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb055-111">Return value</span></span>

<span data-ttu-id="fb055-112">Devuelve E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fb055-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb055-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb055-113">Remarks</span></span>

<span data-ttu-id="fb055-114">Este método invalida el [**método CTransformFilter::GetMediaType.**](ctransformfilter-getmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="fb055-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="fb055-115">En la **clase CTransInPlaceFilter,** cada pin llama al pin conectado opuesto para enumerar los tipos de medios preferidos.</span><span class="sxs-lookup"><span data-stu-id="fb055-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="fb055-116">El pin de entrada llama al pin de entrada del filtro de bajada y el pin de salida llama al pin de salida del filtro ascendente.</span><span class="sxs-lookup"><span data-stu-id="fb055-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="fb055-117">Por lo tanto, nunca se llama `GetMediaType` al método del filtro.</span><span class="sxs-lookup"><span data-stu-id="fb055-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb055-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb055-118">Requirements</span></span>



| <span data-ttu-id="fb055-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb055-119">Requirement</span></span> | <span data-ttu-id="fb055-120">Value</span><span class="sxs-lookup"><span data-stu-id="fb055-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb055-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb055-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fb055-122"><dt>Transip.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb055-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb055-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb055-123">Library</span></span><br/> | <dl> <span data-ttu-id="fb055-124"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fb055-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb055-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fb055-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb055-126">**CTransInPlaceFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="fb055-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




