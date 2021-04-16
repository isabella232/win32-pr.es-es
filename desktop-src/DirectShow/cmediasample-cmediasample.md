---
description: Método de constructor.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Constructor CMediaSample. CMediaSample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679297"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="19f3f-103">Constructor CMediaSample. CMediaSample</span><span class="sxs-lookup"><span data-stu-id="19f3f-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="19f3f-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="19f3f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19f3f-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="19f3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19f3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f3f-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="19f3f-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="19f3f-108">ignorado.</span><span class="sxs-lookup"><span data-stu-id="19f3f-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="19f3f-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="19f3f-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="19f3f-110">Puntero al objeto [**CBaseAllocator**](cbaseallocator.md) que creó este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="19f3f-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="19f3f-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="19f3f-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="19f3f-112">ignorado.</span><span class="sxs-lookup"><span data-stu-id="19f3f-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="19f3f-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="19f3f-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="19f3f-114">Puntero a un búfer de memoria asignado por el autor de la llamada, de *longitud* de tamaño.</span><span class="sxs-lookup"><span data-stu-id="19f3f-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="19f3f-115">*length*</span><span class="sxs-lookup"><span data-stu-id="19f3f-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="19f3f-116">Longitud del búfer de memoria.</span><span class="sxs-lookup"><span data-stu-id="19f3f-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19f3f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19f3f-117">Remarks</span></span>

<span data-ttu-id="19f3f-118">La clase base no modifica el valor **HRESULT** que se pasa en el parámetro *PHR* .</span><span class="sxs-lookup"><span data-stu-id="19f3f-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="19f3f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19f3f-119">Requirements</span></span>



| <span data-ttu-id="19f3f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="19f3f-120">Requirement</span></span> | <span data-ttu-id="19f3f-121">Value</span><span class="sxs-lookup"><span data-stu-id="19f3f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19f3f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19f3f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="19f3f-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19f3f-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="19f3f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19f3f-124">Library</span></span><br/> | <dl> <span data-ttu-id="19f3f-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="19f3f-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19f3f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="19f3f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f3f-127">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="19f3f-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




