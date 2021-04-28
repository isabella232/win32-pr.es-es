---
description: 'Constructor COutputQueue.COutputQueue: método constructor.'
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Constructor COutputQueue.COutputQueue (Outputq.h)
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
ms.openlocfilehash: 17a795bf4ec33ec904b83f6621fc0bc4f43b4b15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095333"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="13f6f-103">Constructor COutputQueue.COutputQueue</span><span class="sxs-lookup"><span data-stu-id="13f6f-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="13f6f-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="13f6f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13f6f-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="13f6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13f6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f6f-107">*pInputPin*</span><span class="sxs-lookup"><span data-stu-id="13f6f-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="13f6f-108">Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="13f6f-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="13f6f-109">El objeto entregará ejemplos a este pin.</span><span class="sxs-lookup"><span data-stu-id="13f6f-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="13f6f-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="13f6f-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="13f6f-111">Puntero a un **código de retorno HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="13f6f-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="13f6f-112">Establezca el valor en S \_ OK antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="13f6f-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="13f6f-113">Al devolver, *phr* recibe un valor que indica el éxito o el error del método.</span><span class="sxs-lookup"><span data-stu-id="13f6f-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="13f6f-114">*bAuto*</span><span class="sxs-lookup"><span data-stu-id="13f6f-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="13f6f-115">Marca que especifica si el objeto decide cuándo crear una cola.</span><span class="sxs-lookup"><span data-stu-id="13f6f-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="13f6f-116">Si **es TRUE,** el objeto crea una cola solo si el pin de entrada puede bloquearse.</span><span class="sxs-lookup"><span data-stu-id="13f6f-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="13f6f-117">Si **es FALSE,** *el parámetro bQueue* especifica si se va a crear una cola.</span><span class="sxs-lookup"><span data-stu-id="13f6f-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="13f6f-118">*bQueue*</span><span class="sxs-lookup"><span data-stu-id="13f6f-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="13f6f-119">Si *bAuto* es **TRUE**, se omite este parámetro.</span><span class="sxs-lookup"><span data-stu-id="13f6f-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="13f6f-120">Si *bAuto* es **FALSE,** esta marca especifica si se va a crear una cola.</span><span class="sxs-lookup"><span data-stu-id="13f6f-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="13f6f-121">*lBatchSize*</span><span class="sxs-lookup"><span data-stu-id="13f6f-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="13f6f-122">Número máximo de muestras para entregar en un lote.</span><span class="sxs-lookup"><span data-stu-id="13f6f-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="13f6f-123">*bBatchExact*</span><span class="sxs-lookup"><span data-stu-id="13f6f-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="13f6f-124">Marca que especifica si se deben usar tamaños de lote exactos.</span><span class="sxs-lookup"><span data-stu-id="13f6f-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="13f6f-125">Si **es TRUE,** el objeto espera los ejemplos *de lBatchSize* antes de entregarlos al pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="13f6f-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="13f6f-126">Si **es FALSE,** el objeto entrega muestras a medida que las recibe.</span><span class="sxs-lookup"><span data-stu-id="13f6f-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="13f6f-127">*lListSize*</span><span class="sxs-lookup"><span data-stu-id="13f6f-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="13f6f-128">Tamaño de caché de la cola.</span><span class="sxs-lookup"><span data-stu-id="13f6f-128">Cache size for the queue.</span></span> <span data-ttu-id="13f6f-129">El valor predeterminado, DEFAULTCACHE, es una constante definida para la [**clase CBaseList.**](cbaselist.md)</span><span class="sxs-lookup"><span data-stu-id="13f6f-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="13f6f-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="13f6f-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="13f6f-131">Prioridad del subproceso que entrega ejemplos.</span><span class="sxs-lookup"><span data-stu-id="13f6f-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13f6f-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13f6f-132">Remarks</span></span>

<span data-ttu-id="13f6f-133">Si *bAuto* es **TRUE,** el objeto llama al método [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) en el pin de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="13f6f-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="13f6f-134">Si **ReceiveCanBlock devuelve** S OK (lo que significa que el pin podría bloquearse en \_ llamadas [**IMemInputPin::Receive),**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) el objeto crea un subproceso para entregar ejemplos.</span><span class="sxs-lookup"><span data-stu-id="13f6f-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="13f6f-135">De lo contrario, no crea un subproceso.</span><span class="sxs-lookup"><span data-stu-id="13f6f-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="13f6f-136">Si *bAuto* es **FALSE,** el valor de *bQueue* determina si se va a crear un subproceso.</span><span class="sxs-lookup"><span data-stu-id="13f6f-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="13f6f-137">Si el objeto crea un subproceso, asigna el identificador de subproceso a la variable miembro [**COutputQueue::m \_ hThread.**](coutputqueue-m-hthread.md)</span><span class="sxs-lookup"><span data-stu-id="13f6f-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="13f6f-138">El procedimiento del subproceso [**es COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md)y el parámetro thread es un puntero a esto.</span><span class="sxs-lookup"><span data-stu-id="13f6f-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="13f6f-139">El objeto también crea una cola para contener ejemplos, que se proporciona mediante la variable miembro [**COutputQueue::m \_ List.**](coutputqueue-m-list.md)</span><span class="sxs-lookup"><span data-stu-id="13f6f-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="13f6f-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13f6f-140">Requirements</span></span>



| <span data-ttu-id="13f6f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="13f6f-141">Requirement</span></span> | <span data-ttu-id="13f6f-142">Value</span><span class="sxs-lookup"><span data-stu-id="13f6f-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f6f-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13f6f-143">Header</span></span><br/>  | <dl> <span data-ttu-id="13f6f-144"><dt>Outputq.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="13f6f-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13f6f-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="13f6f-145">Library</span></span><br/> | <dl> <span data-ttu-id="13f6f-146"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="13f6f-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f6f-147">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13f6f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f6f-148">**COutputQueue (clase)**</span><span class="sxs-lookup"><span data-stu-id="13f6f-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




