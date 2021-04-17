---
description: Método de constructor.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Constructor COutputQueue. COutputQueue (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de4d8fe0d0a7c3dcf90e67f80a939f6294cb3d5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680583"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="a76d6-103">Constructor COutputQueue. COutputQueue</span><span class="sxs-lookup"><span data-stu-id="a76d6-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="a76d6-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="a76d6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a76d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a76d6-105">Syntax</span></span>


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a><span data-ttu-id="a76d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a76d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a76d6-107">*pInputPin*</span><span class="sxs-lookup"><span data-stu-id="a76d6-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a76d6-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="a76d6-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="a76d6-109">El objeto proporcionará ejemplos a este pin.</span><span class="sxs-lookup"><span data-stu-id="a76d6-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="a76d6-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="a76d6-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a76d6-111">Puntero a un código de retorno **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a76d6-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="a76d6-112">Establezca el valor en es \_ correcto antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="a76d6-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="a76d6-113">En la devolución, *PHR* recibe un valor que indica si el método se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="a76d6-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="a76d6-114">*bAuto*</span><span class="sxs-lookup"><span data-stu-id="a76d6-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="a76d6-115">Marca que especifica si el objeto decide cuándo se debe crear una cola.</span><span class="sxs-lookup"><span data-stu-id="a76d6-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="a76d6-116">Si **es true**, el objeto crea una cola solo si el PIN de entrada puede bloquearse.</span><span class="sxs-lookup"><span data-stu-id="a76d6-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="a76d6-117">Si **es false**, el parámetro *bQueue* especifica si se va a crear una cola.</span><span class="sxs-lookup"><span data-stu-id="a76d6-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="a76d6-118">*bQueue*</span><span class="sxs-lookup"><span data-stu-id="a76d6-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="a76d6-119">Si *bAuto* es **true**, se omite este parámetro.</span><span class="sxs-lookup"><span data-stu-id="a76d6-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="a76d6-120">Si *bAuto* es **false**, esta marca especifica si se va a crear una cola.</span><span class="sxs-lookup"><span data-stu-id="a76d6-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="a76d6-121">*lBatchSize*</span><span class="sxs-lookup"><span data-stu-id="a76d6-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a76d6-122">Número máximo de muestras que se van a enviar en un lote.</span><span class="sxs-lookup"><span data-stu-id="a76d6-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="a76d6-123">*bBatchExact*</span><span class="sxs-lookup"><span data-stu-id="a76d6-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="a76d6-124">Marca que especifica si se van a utilizar tamaños de lote exactos.</span><span class="sxs-lookup"><span data-stu-id="a76d6-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="a76d6-125">Si **es true**, el objeto espera los ejemplos de *lBatchSize* antes de entregarlos al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="a76d6-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="a76d6-126">Si **es false**, el objeto proporciona ejemplos a medida que los recibe.</span><span class="sxs-lookup"><span data-stu-id="a76d6-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="a76d6-127">*lListSize*</span><span class="sxs-lookup"><span data-stu-id="a76d6-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a76d6-128">Tamaño de la memoria caché para la cola.</span><span class="sxs-lookup"><span data-stu-id="a76d6-128">Cache size for the queue.</span></span> <span data-ttu-id="a76d6-129">El valor predeterminado, DEFAULTCACHE, es una constante definida para la clase [**CBaseList**](cbaselist.md) .</span><span class="sxs-lookup"><span data-stu-id="a76d6-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="a76d6-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="a76d6-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="a76d6-131">Prioridad del subproceso que proporciona ejemplos.</span><span class="sxs-lookup"><span data-stu-id="a76d6-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a76d6-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a76d6-132">Remarks</span></span>

<span data-ttu-id="a76d6-133">Si *bAuto* es **true**, el objeto llama al método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) en el código PIN de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="a76d6-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="a76d6-134">Si **ReceiveCanBlock** devuelve S \_ correcto (lo que significa que el PIN podría bloquearse en las llamadas a [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) ), el objeto crea un subproceso para entregar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="a76d6-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="a76d6-135">De lo contrario, no crea un subproceso.</span><span class="sxs-lookup"><span data-stu-id="a76d6-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="a76d6-136">Si *bAuto* es **false**, el valor de *bQueue* determina si se va a crear un subproceso.</span><span class="sxs-lookup"><span data-stu-id="a76d6-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="a76d6-137">Si el objeto crea un subproceso, asigna el identificador de subproceso a la variable miembro [**COutputQueue:: m \_ hThread**](coutputqueue-m-hthread.md) .</span><span class="sxs-lookup"><span data-stu-id="a76d6-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="a76d6-138">El procedimiento de subproceso es [**COutputQueue:: InitialThreadProc**](coutputqueue-initialthreadproc.md)y el parámetro Thread es un puntero a este.</span><span class="sxs-lookup"><span data-stu-id="a76d6-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="a76d6-139">El objeto también crea una cola para contener ejemplos, que viene dado por la variable de miembro de [**\_ lista COutputQueue:: m**](coutputqueue-m-list.md) .</span><span class="sxs-lookup"><span data-stu-id="a76d6-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a76d6-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a76d6-140">Requirements</span></span>



| <span data-ttu-id="a76d6-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="a76d6-141">Requirement</span></span> | <span data-ttu-id="a76d6-142">Value</span><span class="sxs-lookup"><span data-stu-id="a76d6-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a76d6-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a76d6-143">Header</span></span><br/>  | <dl> <span data-ttu-id="a76d6-144"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a76d6-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a76d6-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a76d6-145">Library</span></span><br/> | <dl> <span data-ttu-id="a76d6-146"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a76d6-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a76d6-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="a76d6-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76d6-148">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="a76d6-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




