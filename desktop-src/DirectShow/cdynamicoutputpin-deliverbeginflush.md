---
description: El método DeliverBeginFlush solicita la clavija de entrada conectada para iniciar una operación de vaciado.
ms.assetid: eafc3835-7696-480b-abc8-154938e19b15
title: Método CDynamicOutputPin. DeliverBeginFlush (Amfilter. h)
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
ms.openlocfilehash: 242394a327b63fcc901b08f572096bf2f42238b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670871"
---
# <a name="cdynamicoutputpindeliverbeginflush-method"></a><span data-ttu-id="cf943-103">CDynamicOutputPin. DeliverBeginFlush, método</span><span class="sxs-lookup"><span data-stu-id="cf943-103">CDynamicOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="cf943-104">El `DeliverBeginFlush` método solicita la clavija de entrada conectada para iniciar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="cf943-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf943-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf943-105">Syntax</span></span>


```C++
HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="cf943-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf943-106">Parameters</span></span>

<span data-ttu-id="cf943-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cf943-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf943-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf943-108">Return value</span></span>

<span data-ttu-id="cf943-109">Devuelve S \_ correcto si se realiza correctamente o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="cf943-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf943-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf943-110">Remarks</span></span>

<span data-ttu-id="cf943-111">Este método invalida el método [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="cf943-111">This method overrides the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span> <span data-ttu-id="cf943-112">Establece el evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="cf943-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf943-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf943-113">Requirements</span></span>



| <span data-ttu-id="cf943-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf943-114">Requirement</span></span> | <span data-ttu-id="cf943-115">Value</span><span class="sxs-lookup"><span data-stu-id="cf943-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf943-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf943-116">Header</span></span><br/>  | <dl> <span data-ttu-id="cf943-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf943-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cf943-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf943-118">Library</span></span><br/> | <dl> <span data-ttu-id="cf943-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cf943-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf943-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf943-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf943-121">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cf943-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




