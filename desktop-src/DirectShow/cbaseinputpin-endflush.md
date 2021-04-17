---
description: 'El método EndFlush finaliza una operación de vaciado. Implementa el método IPin:: EndFlush.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Método CBaseInputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660345"
---
# <a name="cbaseinputpinendflush-method"></a><span data-ttu-id="02417-104">CBaseInputPin. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="02417-104">CBaseInputPin.EndFlush method</span></span>

<span data-ttu-id="02417-105">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="02417-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="02417-106">Implementa el método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="02417-106">Implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="02417-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02417-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="02417-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02417-108">Parameters</span></span>

<span data-ttu-id="02417-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="02417-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02417-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02417-110">Return value</span></span>

<span data-ttu-id="02417-111">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="02417-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="02417-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02417-112">Remarks</span></span>

<span data-ttu-id="02417-113">Este método establece la marca [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) en **true**, lo que permite que el método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) acepte ejemplos.</span><span class="sxs-lookup"><span data-stu-id="02417-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which enables the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to accept samples.</span></span>

<span data-ttu-id="02417-114">La clase derivada debe invalidar este método y realizar los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="02417-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="02417-115">Libere los datos almacenados en búfer y espere a que se descarten todas las muestras en cola.</span><span class="sxs-lookup"><span data-stu-id="02417-115">Free any buffered data and wait for all queued samples to be discarded.</span></span>
2.  <span data-ttu-id="02417-116">Borre cualquier notificación de [**EC \_ completa**](ec-complete.md) pendiente.</span><span class="sxs-lookup"><span data-stu-id="02417-116">Clear any pending [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>
3.  <span data-ttu-id="02417-117">Llame al método de la clase base.</span><span class="sxs-lookup"><span data-stu-id="02417-117">Call the base class method.</span></span>
4.  <span data-ttu-id="02417-118">Llame a [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en las clavijas de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="02417-118">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on downstream input pins.</span></span> <span data-ttu-id="02417-119">Si el PIN no ha entregado todavía ningún ejemplo de multimedia en el nivel inferior, puede omitir este paso.</span><span class="sxs-lookup"><span data-stu-id="02417-119">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="02417-120">Si los pin de salida derivan de la clase [**CBaseOutputPin**](cbaseoutputpin.md) , puede llamar al método [**eliverendflush de CBaseOutputPin::D**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="02417-120">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="02417-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02417-121">Requirements</span></span>



| <span data-ttu-id="02417-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="02417-122">Requirement</span></span> | <span data-ttu-id="02417-123">Value</span><span class="sxs-lookup"><span data-stu-id="02417-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02417-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02417-124">Header</span></span><br/>  | <dl> <span data-ttu-id="02417-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02417-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="02417-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02417-126">Library</span></span><br/> | <dl> <span data-ttu-id="02417-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="02417-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02417-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="02417-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02417-129">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="02417-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




