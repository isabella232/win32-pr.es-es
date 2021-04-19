---
description: El método EndOfStream notifica al filtro que no se esperan datos adicionales del PIN de entrada.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Método CTransformFilter. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660431"
---
# <a name="ctransformfilterendofstream-method"></a><span data-ttu-id="81525-103">CTransformFilter. EndOfStream, método</span><span class="sxs-lookup"><span data-stu-id="81525-103">CTransformFilter.EndOfStream method</span></span>

<span data-ttu-id="81525-104">El `EndOfStream` método notifica al filtro que no se esperan datos adicionales del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="81525-104">The `EndOfStream` method notifies the filter that no additional data is expected from the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="81525-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81525-105">Syntax</span></span>


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="81525-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81525-106">Parameters</span></span>

<span data-ttu-id="81525-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="81525-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81525-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81525-108">Return value</span></span>

<span data-ttu-id="81525-109">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81525-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="81525-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81525-110">Remarks</span></span>

<span data-ttu-id="81525-111">El método [**CTransformInputPin:: EndOfStream**](ctransforminputpin-endofstream.md) del PIN de entrada llama a este método.</span><span class="sxs-lookup"><span data-stu-id="81525-111">The input pin's [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) method calls this method.</span></span> <span data-ttu-id="81525-112">Este método entrega la notificación de final de secuencia de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="81525-112">This method delivers the end-of-stream notification downstream.</span></span> <span data-ttu-id="81525-113">Si la clase derivada utiliza un subproceso de trabajo para proporcionar ejemplos de medios, debe invalidar este método y poner en cola la notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="81525-113">If the derived class uses a worker thread to deliver media samples, it should override this method and queue the end-of-stream notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="81525-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81525-114">Requirements</span></span>



| <span data-ttu-id="81525-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="81525-115">Requirement</span></span> | <span data-ttu-id="81525-116">Value</span><span class="sxs-lookup"><span data-stu-id="81525-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81525-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81525-117">Header</span></span><br/>  | <dl> <span data-ttu-id="81525-118"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81525-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="81525-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81525-119">Library</span></span><br/> | <dl> <span data-ttu-id="81525-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="81525-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81525-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="81525-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81525-122">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="81525-122">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




