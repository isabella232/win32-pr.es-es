---
description: El método DecideBufferSize establece los requisitos de búfer.
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Método CTransformOutputPin. DecideBufferSize (Transfrm. h)
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
ms.openlocfilehash: dc17314887094b7f62a43f38dd406d0ac9039de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661005"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="1c4c1-103">CTransformOutputPin. DecideBufferSize, método</span><span class="sxs-lookup"><span data-stu-id="1c4c1-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="1c4c1-104">El `DecideBufferSize` método establece los requisitos de búfer.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c4c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c4c1-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="1c4c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c4c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c4c1-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="1c4c1-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="1c4c1-108">Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1c4c1-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="1c4c1-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="1c4c1-110">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c4c1-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c4c1-111">Return value</span></span>

<span data-ttu-id="1c4c1-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c4c1-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c4c1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c4c1-113">Remarks</span></span>

<span data-ttu-id="1c4c1-114">Este método invalida el método [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="1c4c1-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="1c4c1-115">Llama al método CTransformFilter virtual puro del filtro [**::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) , que debe implementar la clase derivada del filtro.</span><span class="sxs-lookup"><span data-stu-id="1c4c1-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c4c1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c4c1-116">Requirements</span></span>



| <span data-ttu-id="1c4c1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c4c1-117">Requirement</span></span> | <span data-ttu-id="1c4c1-118">Value</span><span class="sxs-lookup"><span data-stu-id="1c4c1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c4c1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c4c1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1c4c1-120"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c4c1-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1c4c1-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c4c1-121">Library</span></span><br/> | <dl> <span data-ttu-id="1c4c1-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1c4c1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




