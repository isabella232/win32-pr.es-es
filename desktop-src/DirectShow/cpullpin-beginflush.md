---
description: El método BeginFlush informa al filtro propietario de vaciar los filtros de nivel inferior. La clase derivada debe implementar este método.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Método CPullPin. BeginFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680276"
---
# <a name="cpullpinbeginflush-method"></a><span data-ttu-id="f8ce1-104">CPullPin. BeginFlush, método</span><span class="sxs-lookup"><span data-stu-id="f8ce1-104">CPullPin.BeginFlush method</span></span>

<span data-ttu-id="f8ce1-105">El `BeginFlush` método informa al filtro propietario de vaciar los filtros de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="f8ce1-105">The `BeginFlush` method informs the owning filter to flush the downstream filters.</span></span> <span data-ttu-id="f8ce1-106">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="f8ce1-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ce1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8ce1-107">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="f8ce1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8ce1-108">Parameters</span></span>

<span data-ttu-id="f8ce1-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f8ce1-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8ce1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8ce1-110">Return value</span></span>

<span data-ttu-id="f8ce1-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8ce1-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8ce1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f8ce1-112">Remarks</span></span>

<span data-ttu-id="f8ce1-113">El método [**CPullPin:: Seek**](cpullpin-seek.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="f8ce1-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="f8ce1-114">Implemente este método para llamar al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en cada pin de entrada de nivel inferior que reciba datos de este objeto.</span><span class="sxs-lookup"><span data-stu-id="f8ce1-114">Implement this method to call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="f8ce1-115">Si los anclajes de salida del filtro se derivan de [**CBaseOutputPin**](cbaseoutputpin.md), llame al método [**eliverbeginflush de CBaseOutputPin::D**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="f8ce1-115">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>

<span data-ttu-id="f8ce1-116">Este diseño permite que el filtro busque el flujo simplemente mediante una llamada a **Seek** en el objeto **CPullPin** .</span><span class="sxs-lookup"><span data-stu-id="f8ce1-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ce1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8ce1-117">Requirements</span></span>



| <span data-ttu-id="f8ce1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8ce1-118">Requirement</span></span> | <span data-ttu-id="f8ce1-119">Value</span><span class="sxs-lookup"><span data-stu-id="f8ce1-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ce1-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8ce1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f8ce1-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ce1-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="f8ce1-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8ce1-122">Library</span></span><br/> | <dl> <span data-ttu-id="f8ce1-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f8ce1-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8ce1-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8ce1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ce1-125">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="f8ce1-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




