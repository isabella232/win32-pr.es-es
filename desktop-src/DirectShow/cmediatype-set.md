---
description: El método CMediaType. set (mtype. h) establece el tipo de medio desde otro tipo de medio. El método usa el parámetro ' cmtype '.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Método CMediaType. set (mtype. h)-cmtype [Ref] parámetro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105670277"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a><span data-ttu-id="0331d-104">Método CMediaType. set (mtype. h)-cmtype [Ref] parámetro</span><span class="sxs-lookup"><span data-stu-id="0331d-104">CMediaType.Set method (Mtype.h) - cmtype [ref] parameter</span></span>

<span data-ttu-id="0331d-105">El `Set` método establece el tipo de medio desde otro tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="0331d-105">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0331d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0331d-106">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="0331d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0331d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0331d-108">*cmtype* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="0331d-108">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="0331d-109">Referencia a un objeto [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="0331d-109">Reference to a [**CMediaType**](cmediatype.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0331d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0331d-110">Return value</span></span>

<span data-ttu-id="0331d-111">Devuelve S \_ OK o E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0331d-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0331d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0331d-112">Remarks</span></span>

<span data-ttu-id="0331d-113">Este método copia todo el tipo de medio de *cmtype*.</span><span class="sxs-lookup"><span data-stu-id="0331d-113">This method copies the entire media type from *cmtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0331d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0331d-114">Requirements</span></span>

| <span data-ttu-id="0331d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0331d-115">Requirement</span></span>                   | <span data-ttu-id="0331d-116">Value</span><span class="sxs-lookup"><span data-stu-id="0331d-116">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0331d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0331d-117">Header</span></span>  | <span data-ttu-id="0331d-118">Mtype. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="0331d-118">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="0331d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0331d-119">Library</span></span> | <span data-ttu-id="0331d-120">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="0331d-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="0331d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0331d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0331d-122">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="0331d-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




