---
description: 'Método CDynamicOutputPin.DeliverEndFlush: el método DeliverEndFlush solicita el pin de entrada conectado para finalizar una operación de vaciado.'
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: Método CDynamicOutputPin.DeliverEndFlush (Amfilter.h)
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
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095713"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="a4036-103">Método CDynamicOutputPin.DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="a4036-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="a4036-104">El `DeliverEndFlush` método solicita el pin de entrada conectado para finalizar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="a4036-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4036-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4036-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="a4036-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4036-106">Parameters</span></span>

<span data-ttu-id="a4036-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a4036-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4036-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4036-108">Return value</span></span>

<span data-ttu-id="a4036-109">Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="a4036-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4036-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a4036-110">Remarks</span></span>

<span data-ttu-id="a4036-111">Este método invalida el [**método CBaseOutputPin::D eliverEndFlush.**](cbaseoutputpin-deliverendflush.md)</span><span class="sxs-lookup"><span data-stu-id="a4036-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="a4036-112">Restablece el evento [**CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md)</span><span class="sxs-lookup"><span data-stu-id="a4036-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4036-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4036-113">Requirements</span></span>



| <span data-ttu-id="a4036-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4036-114">Requirement</span></span> | <span data-ttu-id="a4036-115">Value</span><span class="sxs-lookup"><span data-stu-id="a4036-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4036-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a4036-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a4036-117"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4036-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a4036-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4036-118">Library</span></span><br/> | <dl> <span data-ttu-id="a4036-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a4036-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4036-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a4036-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4036-121">**CDynamicOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="a4036-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




