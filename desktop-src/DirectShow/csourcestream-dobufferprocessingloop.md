---
description: El método DoBufferProcessingLoop genera datos multimedia y los entrega al pin de entrada de nivel inferior.
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: CSourceStream. DoBufferProcessingLoop (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 809694cacf0c30acf88ddf7d14c7f5ea1f654436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690547"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a><span data-ttu-id="bdeb9-103">CSourceStream. DoBufferProcessingLoop, método</span><span class="sxs-lookup"><span data-stu-id="bdeb9-103">CSourceStream.DoBufferProcessingLoop method</span></span>

<span data-ttu-id="bdeb9-104">El `DoBufferProcessingLoop` método genera datos multimedia y los entrega al pin de entrada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-104">The `DoBufferProcessingLoop` method generates media data and delivers it to the downstream input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdeb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdeb9-105">Syntax</span></span>


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a><span data-ttu-id="bdeb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bdeb9-106">Parameters</span></span>

<span data-ttu-id="bdeb9-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bdeb9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bdeb9-108">Return value</span></span>

<span data-ttu-id="bdeb9-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bdeb9-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bdeb9-110">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="bdeb9-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bdeb9-111">Return code</span></span>                                                                             | <span data-ttu-id="bdeb9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdeb9-112">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bdeb9-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="bdeb9-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="bdeb9-114">El subproceso ha recibido una solicitud de detención.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-114">Thread received a stop request.</span></span><br/>                              |
| <dl> <span data-ttu-id="bdeb9-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bdeb9-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="bdeb9-116">La secuencia finalizó o el filtro descendente no acepta ejemplos.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-116">Stream ended, or downstream filter is not accepting samples.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdeb9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdeb9-117">Remarks</span></span>

<span data-ttu-id="bdeb9-118">Este método implementa el bucle principal que procesa los datos y los entrega hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-118">This method implements the main loop that processes data and delivers it downstream.</span></span> <span data-ttu-id="bdeb9-119">Cada vez a través del bucle, el método recupera un ejemplo de medio vacío del asignador.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-119">Each time through the loop, the method retrieves an empty media sample from the allocator.</span></span> <span data-ttu-id="bdeb9-120">Pasa el ejemplo al método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="bdeb9-120">It passes the sample to the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method.</span></span> <span data-ttu-id="bdeb9-121">El método **FillBuffer** , que la clase derivada debe implementar, genera datos multimedia y los coloca en el búfer de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-121">The **FillBuffer** method, which the derived class must implement, generates media data and places it in the sample buffer.</span></span>

<span data-ttu-id="bdeb9-122">El bucle finaliza cuando se produce cualquiera de las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="bdeb9-122">The loop ends when any of the following occurs:</span></span>

-   <span data-ttu-id="bdeb9-123">El método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN de entrada rechaza un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-123">The input pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method rejects a sample.</span></span>
-   <span data-ttu-id="bdeb9-124">El método **FillBuffer** devuelve S \_ false, que indica el final de la secuencia o devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-124">The **FillBuffer** method returns S\_FALSE, indicating the end of the stream, or returns an error code.</span></span>
-   <span data-ttu-id="bdeb9-125">El subproceso recibe una solicitud [**CSourceStream:: Stop**](csourcestream-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="bdeb9-125">The thread receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span>

<span data-ttu-id="bdeb9-126">El `DoBufferProcessingLoop` método controla la notificación de final de secuencia.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-126">The `DoBufferProcessingLoop` method handles the end-of-stream notification.</span></span> <span data-ttu-id="bdeb9-127">Si se produce un error, envía un [**evento \_ ERRORABORT de EC**](ec-errorabort.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="bdeb9-127">If an error occurs, it sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the filter graph manager.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdeb9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdeb9-128">Requirements</span></span>



| <span data-ttu-id="bdeb9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdeb9-129">Requirement</span></span> | <span data-ttu-id="bdeb9-130">Value</span><span class="sxs-lookup"><span data-stu-id="bdeb9-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdeb9-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdeb9-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bdeb9-132"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdeb9-132"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bdeb9-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdeb9-133">Library</span></span><br/> | <dl> <span data-ttu-id="bdeb9-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bdeb9-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdeb9-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdeb9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdeb9-136">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="bdeb9-136">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




