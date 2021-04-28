---
description: 'Método CDynamicOutputPin.DeliverBeginFlush: el método DeliverBeginFlush solicita el pin de entrada conectado para iniciar una operación de vaciado.'
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Método CDynamicOutputPin.DeliverBeginFlush (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4158a3d6191325e8b647e4551133952d623f795
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099323"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="e7030-103">Método CDynamicOutputPin.DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="e7030-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="e7030-104">El `DeliverBeginFlush` método solicita el pin de entrada conectado para iniciar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="e7030-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7030-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7030-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="e7030-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7030-106">Parameters</span></span>

<span data-ttu-id="e7030-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e7030-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7030-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7030-108">Return value</span></span>

<span data-ttu-id="e7030-109">Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="e7030-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7030-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e7030-110">Remarks</span></span>

<span data-ttu-id="e7030-111">Este método invalida el [**método CBaseOutputPin::D eliverBeginFlush.**](cbaseoutputpin-deliverbeginflush.md)</span><span class="sxs-lookup"><span data-stu-id="e7030-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="e7030-112">Establece el evento [**CDynamicOutputPin::m \_ hStopEvent.**](cdynamicoutputpin-m-hstopevent.md)</span><span class="sxs-lookup"><span data-stu-id="e7030-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7030-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7030-113">Requirements</span></span>



| <span data-ttu-id="e7030-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7030-114">Requirement</span></span> | <span data-ttu-id="e7030-115">Value</span><span class="sxs-lookup"><span data-stu-id="e7030-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7030-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7030-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e7030-117"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7030-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e7030-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7030-118">Library</span></span><br/> | <dl> <span data-ttu-id="e7030-119"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e7030-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7030-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e7030-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7030-121">**CDynamicOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="e7030-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




