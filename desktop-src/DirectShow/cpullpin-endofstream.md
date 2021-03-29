---
description: Se llama al método EndOfStream después de que el objeto entregue el último ejemplo. La clase derivada debe implementar este método.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Método CPullPin. EndOfStream (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680834"
---
# <a name="cpullpinendofstream-method"></a><span data-ttu-id="58ae0-104">CPullPin. EndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="58ae0-104">CPullPin.EndOfStream method</span></span>

<span data-ttu-id="58ae0-105">`EndOfStream`Se llama al método después de que el objeto entregue el último ejemplo.</span><span class="sxs-lookup"><span data-stu-id="58ae0-105">The `EndOfStream` method is called after the object delivers the last sample.</span></span> <span data-ttu-id="58ae0-106">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="58ae0-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="58ae0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58ae0-107">Syntax</span></span>


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a><span data-ttu-id="58ae0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58ae0-108">Parameters</span></span>

<span data-ttu-id="58ae0-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="58ae0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58ae0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58ae0-110">Return value</span></span>

<span data-ttu-id="58ae0-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="58ae0-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58ae0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58ae0-112">Remarks</span></span>

<span data-ttu-id="58ae0-113">Use este método para llamar a [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en cada pin de entrada de nivel inferior que reciba datos de este objeto.</span><span class="sxs-lookup"><span data-stu-id="58ae0-113">Use this method to call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="58ae0-114">Si los anclajes de salida del filtro se derivan de [**CBaseOutputPin**](cbaseoutputpin.md), llame al método [**eliverendofstream de CBaseOutputPin::D**](cbaseoutputpin-deliverendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="58ae0-114">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ae0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58ae0-115">Requirements</span></span>



| <span data-ttu-id="58ae0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ae0-116">Requirement</span></span> | <span data-ttu-id="58ae0-117">Value</span><span class="sxs-lookup"><span data-stu-id="58ae0-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58ae0-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58ae0-118">Header</span></span><br/>  | <dl> <span data-ttu-id="58ae0-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ae0-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="58ae0-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58ae0-120">Library</span></span><br/> | <dl> <span data-ttu-id="58ae0-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="58ae0-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ae0-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="58ae0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ae0-123">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="58ae0-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




