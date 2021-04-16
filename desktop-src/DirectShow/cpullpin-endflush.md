---
description: El método EndFlush informa al filtro propietario de que finalice una operación de vaciado. La clase derivada debe implementar este método.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Método CPullPin. EndFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671387"
---
# <a name="cpullpinendflush-method"></a><span data-ttu-id="0f320-104">CPullPin. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="0f320-104">CPullPin.EndFlush method</span></span>

<span data-ttu-id="0f320-105">El `EndFlush` método informa al filtro propietario de que finalice una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="0f320-105">The `EndFlush` method informs the owning filter to end a flush operation.</span></span> <span data-ttu-id="0f320-106">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="0f320-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f320-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f320-107">Syntax</span></span>


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a><span data-ttu-id="0f320-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f320-108">Parameters</span></span>

<span data-ttu-id="0f320-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0f320-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f320-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f320-110">Return value</span></span>

<span data-ttu-id="0f320-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f320-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f320-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f320-112">Remarks</span></span>

<span data-ttu-id="0f320-113">El método [**CPullPin:: Seek**](cpullpin-seek.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="0f320-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="0f320-114">Implemente este método para llamar al método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en cada pin de entrada de nivel inferior que reciba datos de este objeto.</span><span class="sxs-lookup"><span data-stu-id="0f320-114">Implement this method to call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="0f320-115">Si los anclajes de salida del filtro se derivan de **CBaseOutputPin**, llame al método **eliverendflush de CBaseOutputPin::D** .</span><span class="sxs-lookup"><span data-stu-id="0f320-115">If your filter's output pin(s) derive from **CBaseOutputPin**, call the **CBaseOutputPin::DeliverEndFlush** method.</span></span>

<span data-ttu-id="0f320-116">Este diseño permite que el filtro busque el flujo simplemente mediante una llamada a **Seek** en el objeto **CPullPin** .</span><span class="sxs-lookup"><span data-stu-id="0f320-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f320-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f320-117">Requirements</span></span>



| <span data-ttu-id="0f320-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f320-118">Requirement</span></span> | <span data-ttu-id="0f320-119">Value</span><span class="sxs-lookup"><span data-stu-id="0f320-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f320-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f320-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0f320-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f320-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="0f320-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f320-122">Library</span></span><br/> | <dl> <span data-ttu-id="0f320-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0f320-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f320-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f320-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f320-125">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="0f320-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




