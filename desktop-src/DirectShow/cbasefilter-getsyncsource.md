---
description: 'El método GetSyncSource recupera el reloj de referencia que usa el filtro. Este método implementa el método IMediaFilter:: GetSyncSource.'
ms.assetid: b8c95838-bd6e-41c5-b3ab-71ebb33136f0
title: Método CBaseFilter. GetSyncSource (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetSyncSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 64f2d46ded16384e53e5281632bc0a064021f673
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661081"
---
# <a name="cbasefiltergetsyncsource-method"></a><span data-ttu-id="198d4-104">CBaseFilter. GetSyncSource, método</span><span class="sxs-lookup"><span data-stu-id="198d4-104">CBaseFilter.GetSyncSource method</span></span>

<span data-ttu-id="198d4-105">El `GetSyncSource` método recupera el reloj de referencia que usa el filtro.</span><span class="sxs-lookup"><span data-stu-id="198d4-105">The `GetSyncSource` method retrieves the reference clock that the filter is using.</span></span> <span data-ttu-id="198d4-106">Este método implementa el método [**IMediaFilter:: GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) .</span><span class="sxs-lookup"><span data-stu-id="198d4-106">This method implements the [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="198d4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="198d4-107">Syntax</span></span>


```C++
HRESULT GetSyncSource(
   IReferenceClock **pClock
);
```



## <a name="parameters"></a><span data-ttu-id="198d4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="198d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="198d4-109">*pClock*</span><span class="sxs-lookup"><span data-stu-id="198d4-109">*pClock*</span></span> 
</dt> <dd>

<span data-ttu-id="198d4-110">Dirección de una variable que recibe un puntero a la interfaz [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) del reloj.</span><span class="sxs-lookup"><span data-stu-id="198d4-110">Address of a variable that receives a pointer to the clock's [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="198d4-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="198d4-111">Return value</span></span>

<span data-ttu-id="198d4-112">Devuelve el \_ puntero S o E \_ .</span><span class="sxs-lookup"><span data-stu-id="198d4-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="remarks"></a><span data-ttu-id="198d4-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="198d4-113">Remarks</span></span>

<span data-ttu-id="198d4-114">Si el filtro no usa un reloj de referencia, *\* pClock* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="198d4-114">If the filter is not using a reference clock, *\*pClock* is set to **NULL**.</span></span> <span data-ttu-id="198d4-115">Cuando el método devuelve un valor, si *\* pClock* no es **null**, la interfaz **IReferenceClock** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="198d4-115">When the method returns, if *\*pClock* is non-**NULL**, the **IReferenceClock** interface has an outstanding reference count.</span></span> <span data-ttu-id="198d4-116">Asegúrese de liberarlo cuando haya terminado.</span><span class="sxs-lookup"><span data-stu-id="198d4-116">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="198d4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="198d4-117">Requirements</span></span>



| <span data-ttu-id="198d4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="198d4-118">Requirement</span></span> | <span data-ttu-id="198d4-119">Value</span><span class="sxs-lookup"><span data-stu-id="198d4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="198d4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="198d4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="198d4-121"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="198d4-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="198d4-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="198d4-122">Library</span></span><br/> | <dl> <span data-ttu-id="198d4-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="198d4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="198d4-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="198d4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="198d4-125">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="198d4-125">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




