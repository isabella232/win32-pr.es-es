---
description: 'Método CTransformFilter.DecideBufferSize: el método DecideBufferSize establece los requisitos de búfer del pin de salida.'
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Método CTransformFilter.DecideBufferSize (Transfrm.h)
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
ms.openlocfilehash: f3276170f1256bba41aa075b0e5f06fb7becbcd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095153"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="a002f-103">Método CTransformFilter.DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="a002f-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="a002f-104">El `DecideBufferSize` método establece los requisitos de búfer del pin de salida.</span><span class="sxs-lookup"><span data-stu-id="a002f-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="a002f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a002f-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a002f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a002f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a002f-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="a002f-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="a002f-108">Puntero a la [**interfaz IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) en el asignador de la patilla de salida.</span><span class="sxs-lookup"><span data-stu-id="a002f-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="a002f-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="a002f-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="a002f-110">Puntero a una [**estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del pin de entrada de bajada.</span><span class="sxs-lookup"><span data-stu-id="a002f-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a002f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a002f-111">Return value</span></span>

<span data-ttu-id="a002f-112">Devuelve S \_ OK u otro valor **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a002f-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a002f-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a002f-113">Remarks</span></span>

<span data-ttu-id="a002f-114">El método [**CTransformOutputPin::D ecideBufferSize**](ctransformoutputpin-decidebuffersize.md) del pin de salida llama a este método.</span><span class="sxs-lookup"><span data-stu-id="a002f-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="a002f-115">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="a002f-115">The derived class must implement this method.</span></span> <span data-ttu-id="a002f-116">Para obtener más información, [**vea CBaseOutputPin::D ecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="a002f-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a002f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a002f-117">Requirements</span></span>



| <span data-ttu-id="a002f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a002f-118">Requirement</span></span> | <span data-ttu-id="a002f-119">Value</span><span class="sxs-lookup"><span data-stu-id="a002f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a002f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a002f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="a002f-121"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a002f-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a002f-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a002f-122">Library</span></span><br/> | <dl> <span data-ttu-id="a002f-123"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a002f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a002f-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a002f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a002f-125">**CTransformFilter (clase)**</span><span class="sxs-lookup"><span data-stu-id="a002f-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




