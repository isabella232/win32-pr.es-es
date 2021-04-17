---
description: El método DeliverEndFlush solicita que el PIN de entrada conectado finalice una operación de vaciado.
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Método CDynamicOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660185"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="fcb16-103">CDynamicOutputPin. DeliverEndFlush, método</span><span class="sxs-lookup"><span data-stu-id="fcb16-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="fcb16-104">El `DeliverEndFlush` método solicita el PIN de entrada conectado para finalizar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="fcb16-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcb16-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="fcb16-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcb16-106">Parameters</span></span>

<span data-ttu-id="fcb16-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fcb16-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fcb16-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcb16-108">Return value</span></span>

<span data-ttu-id="fcb16-109">Devuelve S \_ correcto si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="fcb16-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcb16-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fcb16-110">Remarks</span></span>

<span data-ttu-id="fcb16-111">Este método invalida el método [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb16-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="fcb16-112">Restablece el evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="fcb16-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb16-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcb16-113">Requirements</span></span>



| <span data-ttu-id="fcb16-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcb16-114">Requirement</span></span> | <span data-ttu-id="fcb16-115">Value</span><span class="sxs-lookup"><span data-stu-id="fcb16-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcb16-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcb16-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fcb16-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcb16-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fcb16-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcb16-118">Library</span></span><br/> | <dl> <span data-ttu-id="fcb16-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fcb16-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcb16-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="fcb16-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb16-121">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="fcb16-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




