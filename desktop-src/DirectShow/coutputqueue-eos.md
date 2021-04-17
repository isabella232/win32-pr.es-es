---
description: El método EOS entrega una llamada de final de secuencia al pin de entrada.
ms.assetid: 65e8db14-6ca8-4c4f-8bd8-2442f743499e
title: Método COutputQueue. EOS (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab05d4ab3f2620c11bd62d566be851e16b28cecd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680582"
---
# <a name="coutputqueueeos-method"></a><span data-ttu-id="d87f7-103">COutputQueue. EOS, método</span><span class="sxs-lookup"><span data-stu-id="d87f7-103">COutputQueue.EOS method</span></span>

<span data-ttu-id="d87f7-104">El `EOS` método entrega una llamada de final de secuencia al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="d87f7-104">The `EOS` method delivers an end-of-stream call to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d87f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d87f7-105">Syntax</span></span>


```C++
void EOS();
```



## <a name="parameters"></a><span data-ttu-id="d87f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d87f7-106">Parameters</span></span>

<span data-ttu-id="d87f7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d87f7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d87f7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d87f7-108">Return value</span></span>

<span data-ttu-id="d87f7-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d87f7-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d87f7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d87f7-110">Remarks</span></span>

<span data-ttu-id="d87f7-111">Si el objeto utiliza un subproceso, pone en cola un mensaje de control de paquetes de EOS \_ .</span><span class="sxs-lookup"><span data-stu-id="d87f7-111">If the object is using a thread, it queues an EOS\_PACKET control message.</span></span> <span data-ttu-id="d87f7-112">El subproceso entrega cualquier ejemplo pendiente y llama al método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d87f7-112">The thread delivers any pending samples and calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

<span data-ttu-id="d87f7-113">Si el objeto no utiliza un subproceso, llama al método [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) para proporcionar cualquier ejemplo pendiente.</span><span class="sxs-lookup"><span data-stu-id="d87f7-113">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="d87f7-114">A continuación, llama a **IPin:: EndOfStream** en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d87f7-114">Then it calls **IPin::EndOfStream** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d87f7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d87f7-115">Requirements</span></span>



| <span data-ttu-id="d87f7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d87f7-116">Requirement</span></span> | <span data-ttu-id="d87f7-117">Value</span><span class="sxs-lookup"><span data-stu-id="d87f7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d87f7-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d87f7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d87f7-119"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d87f7-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d87f7-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d87f7-120">Library</span></span><br/> | <dl> <span data-ttu-id="d87f7-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d87f7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d87f7-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d87f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d87f7-123">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="d87f7-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




