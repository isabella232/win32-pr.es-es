---
description: El método IsSpecialSample determina si los datos en cola son un mensaje de control.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Método COutputQueue. IsSpecialSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670599"
---
# <a name="coutputqueueisspecialsample-method"></a><span data-ttu-id="01f0d-103">COutputQueue. IsSpecialSample, método</span><span class="sxs-lookup"><span data-stu-id="01f0d-103">COutputQueue.IsSpecialSample method</span></span>

<span data-ttu-id="01f0d-104">El `IsSpecialSample` método determina si los datos en cola son un mensaje de control.</span><span class="sxs-lookup"><span data-stu-id="01f0d-104">The `IsSpecialSample` method determines whether queued data is a control message.</span></span>

## <a name="syntax"></a><span data-ttu-id="01f0d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01f0d-105">Syntax</span></span>


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="01f0d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="01f0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f0d-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="01f0d-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="01f0d-108">Puntero a un elemento de la cola.</span><span class="sxs-lookup"><span data-stu-id="01f0d-108">Pointer to an item in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f0d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01f0d-109">Return value</span></span>

<span data-ttu-id="01f0d-110">Devuelve **true** si *pSample* es un mensaje de control o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="01f0d-110">Returns **TRUE** if *pSample* is a control message, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="01f0d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01f0d-111">Remarks</span></span>

<span data-ttu-id="01f0d-112">El método [**COutputQueue:: QueueSample**](coutputqueue-queuesample.md) puede recibir mensajes de control además de ejemplos de medios.</span><span class="sxs-lookup"><span data-stu-id="01f0d-112">The [**COutputQueue::QueueSample**](coutputqueue-queuesample.md) method can receive control messages in addition to media samples.</span></span> <span data-ttu-id="01f0d-113">Un mensaje de control es una constante definida (convertida en un \_ tipo Long PTR) que indica al subproceso que realice una acción.</span><span class="sxs-lookup"><span data-stu-id="01f0d-113">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform an action.</span></span> <span data-ttu-id="01f0d-114">Los mensajes de control no contienen datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="01f0d-114">Control messages do not contain media data.</span></span> <span data-ttu-id="01f0d-115">Para obtener más información, vea **COutputQueue:: QueueSample**.</span><span class="sxs-lookup"><span data-stu-id="01f0d-115">For more information, see **COutputQueue::QueueSample**.</span></span>

## <a name="requirements"></a><span data-ttu-id="01f0d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01f0d-116">Requirements</span></span>



| <span data-ttu-id="01f0d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="01f0d-117">Requirement</span></span> | <span data-ttu-id="01f0d-118">Value</span><span class="sxs-lookup"><span data-stu-id="01f0d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f0d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01f0d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="01f0d-120"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01f0d-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01f0d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01f0d-121">Library</span></span><br/> | <dl> <span data-ttu-id="01f0d-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="01f0d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01f0d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="01f0d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f0d-124">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="01f0d-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




