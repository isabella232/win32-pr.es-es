---
description: El método SendAnyway entrega cualquier ejemplo pendiente.
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: Método COutputQueue. SendAnyway (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678972"
---
# <a name="coutputqueuesendanyway-method"></a><span data-ttu-id="d9f22-103">COutputQueue. SendAnyway, método</span><span class="sxs-lookup"><span data-stu-id="d9f22-103">COutputQueue.SendAnyway method</span></span>

<span data-ttu-id="d9f22-104">El `SendAnyway` método entrega cualquier ejemplo pendiente.</span><span class="sxs-lookup"><span data-stu-id="d9f22-104">The `SendAnyway` method delivers any pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f22-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9f22-105">Syntax</span></span>


```C++
void SendAnyway();
```



## <a name="parameters"></a><span data-ttu-id="d9f22-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9f22-106">Parameters</span></span>

<span data-ttu-id="d9f22-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d9f22-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9f22-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9f22-108">Return value</span></span>

<span data-ttu-id="d9f22-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d9f22-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9f22-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9f22-110">Remarks</span></span>

<span data-ttu-id="d9f22-111">Si la variable miembro [**COutputQueue:: m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) es **true**, el objeto rellena la matriz [**COutputQueue:: m \_ ppSamples**](coutputqueue-m-ppsamples.md) antes de entregar un lote de muestras.</span><span class="sxs-lookup"><span data-stu-id="d9f22-111">If the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) member variable is **TRUE**, the object fills the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array before it delivers a batch of samples.</span></span> <span data-ttu-id="d9f22-112">Llame a este método para proporcionar un lote parcial.</span><span class="sxs-lookup"><span data-stu-id="d9f22-112">Call this method to deliver a partial batch.</span></span> <span data-ttu-id="d9f22-113">Por ejemplo, el método [**COutputQueue:: EOS**](coutputqueue-eos.md) llama `SendAnyway` a para serializar los mensajes de fin de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d9f22-113">For example, the [**COutputQueue::EOS**](coutputqueue-eos.md) method calls `SendAnyway` to serialize end-of-stream messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f22-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9f22-114">Requirements</span></span>



| <span data-ttu-id="d9f22-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9f22-115">Requirement</span></span> | <span data-ttu-id="d9f22-116">Value</span><span class="sxs-lookup"><span data-stu-id="d9f22-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f22-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9f22-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d9f22-118"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f22-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d9f22-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d9f22-119">Library</span></span><br/> | <dl> <span data-ttu-id="d9f22-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d9f22-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f22-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9f22-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f22-122">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="d9f22-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




