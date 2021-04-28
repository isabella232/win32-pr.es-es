---
description: 'Método CTransformOutputPin.DecideBufferSize: el método DecideBufferSize establece los requisitos del búfer.'
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Método CTransformOutputPin.DecideBufferSize (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084843"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="6ae2d-103">Método CTransformOutputPin.DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="6ae2d-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="6ae2d-104">El `DecideBufferSize` método establece los requisitos del búfer.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ae2d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ae2d-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="6ae2d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ae2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ae2d-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="6ae2d-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae2d-108">Puntero a la interfaz [**IMemAllocator del asignador.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)</span><span class="sxs-lookup"><span data-stu-id="6ae2d-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="6ae2d-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="6ae2d-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="6ae2d-110">Puntero a [**una estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ae2d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ae2d-111">Return value</span></span>

<span data-ttu-id="6ae2d-112">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="6ae2d-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ae2d-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6ae2d-113">Remarks</span></span>

<span data-ttu-id="6ae2d-114">Este método invalida el [**método CBaseOutputPin::D ecideBufferSize.**](cbaseoutputpin-decidebuffersize.md)</span><span class="sxs-lookup"><span data-stu-id="6ae2d-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="6ae2d-115">Llama al método [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) virtual puro del filtro, que la clase derivada del filtro debe implementar.</span><span class="sxs-lookup"><span data-stu-id="6ae2d-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ae2d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ae2d-116">Requirements</span></span>



| <span data-ttu-id="6ae2d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ae2d-117">Requirement</span></span> | <span data-ttu-id="6ae2d-118">Value</span><span class="sxs-lookup"><span data-stu-id="6ae2d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae2d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ae2d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6ae2d-120"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ae2d-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6ae2d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ae2d-121">Library</span></span><br/> | <dl> <span data-ttu-id="6ae2d-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6ae2d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




