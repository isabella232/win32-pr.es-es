---
description: El método DecideBufferSize establece los requisitos de búfer del terminal de salida.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Método CTransformFilter. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660709"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="bcbb0-103">CTransformFilter. DecideBufferSize, método</span><span class="sxs-lookup"><span data-stu-id="bcbb0-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="bcbb0-104">El `DecideBufferSize` método establece los requisitos de búfer del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbb0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcbb0-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="bcbb0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcbb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcbb0-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="bcbb0-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="bcbb0-108">Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) en el asignador del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="bcbb0-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="bcbb0-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="bcbb0-110">Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del PIN de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcbb0-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcbb0-111">Return value</span></span>

<span data-ttu-id="bcbb0-112">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bcbb0-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcbb0-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcbb0-113">Remarks</span></span>

<span data-ttu-id="bcbb0-114">El método [**CTransformOutputPin::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) del PIN de salida llama a este método.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="bcbb0-115">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="bcbb0-115">The derived class must implement this method.</span></span> <span data-ttu-id="bcbb0-116">Para obtener más información, vea [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="bcbb0-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbb0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcbb0-117">Requirements</span></span>



| <span data-ttu-id="bcbb0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcbb0-118">Requirement</span></span> | <span data-ttu-id="bcbb0-119">Value</span><span class="sxs-lookup"><span data-stu-id="bcbb0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbb0-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcbb0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="bcbb0-121"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcbb0-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bcbb0-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bcbb0-122">Library</span></span><br/> | <dl> <span data-ttu-id="bcbb0-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bcbb0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcbb0-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcbb0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbb0-125">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="bcbb0-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




