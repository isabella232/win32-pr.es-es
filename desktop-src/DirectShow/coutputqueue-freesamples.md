---
description: El método FreeSamples libera todos los ejemplos pendientes.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: Método COutputQueue. FreeSamples (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70d0680d2a1a3ac020be84f244e1cc02bb6efad0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671214"
---
# <a name="coutputqueuefreesamples-method"></a><span data-ttu-id="75b0b-103">COutputQueue. FreeSamples, método</span><span class="sxs-lookup"><span data-stu-id="75b0b-103">COutputQueue.FreeSamples method</span></span>

<span data-ttu-id="75b0b-104">El `FreeSamples` método libera todas las muestras pendientes.</span><span class="sxs-lookup"><span data-stu-id="75b0b-104">The `FreeSamples` method frees all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b0b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75b0b-105">Syntax</span></span>


```C++
void FreeSamples();
```



## <a name="parameters"></a><span data-ttu-id="75b0b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75b0b-106">Parameters</span></span>

<span data-ttu-id="75b0b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="75b0b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75b0b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75b0b-108">Return value</span></span>

<span data-ttu-id="75b0b-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="75b0b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75b0b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75b0b-110">Remarks</span></span>

<span data-ttu-id="75b0b-111">Este método quita cualquier ejemplo pendiente de la cola y de la matriz de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="75b0b-111">This method removes any pending samples from the queue and from the sample array.</span></span>

## <a name="requirements"></a><span data-ttu-id="75b0b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75b0b-112">Requirements</span></span>



| <span data-ttu-id="75b0b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="75b0b-113">Requirement</span></span> | <span data-ttu-id="75b0b-114">Value</span><span class="sxs-lookup"><span data-stu-id="75b0b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b0b-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75b0b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="75b0b-116"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75b0b-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="75b0b-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75b0b-117">Library</span></span><br/> | <dl> <span data-ttu-id="75b0b-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="75b0b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75b0b-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="75b0b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75b0b-120">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="75b0b-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




