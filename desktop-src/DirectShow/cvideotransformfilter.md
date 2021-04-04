---
description: La clase CVideoTransformFilter está diseñada principalmente como una clase base para los filtros de descompresor de AVI.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Clase CVideoTransformFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906865"
---
# <a name="cvideotransformfilter-class"></a><span data-ttu-id="2c453-103">Clase CVideoTransformFilter</span><span class="sxs-lookup"><span data-stu-id="2c453-103">CVideoTransformFilter class</span></span>

![jerarquía de clases cvideotransformfilter](images/vtsip01.png)

<span data-ttu-id="2c453-105">La `CVideoTransformFilter` clase está diseñada principalmente como una clase base para los filtros de descompresor de AVI.</span><span class="sxs-lookup"><span data-stu-id="2c453-105">The `CVideoTransformFilter` class is designed primarily as a base class for AVI decompressor filters.</span></span> <span data-ttu-id="2c453-106">Esta clase agrega compatibilidad para el control de calidad a la clase [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="2c453-106">This class adds support for quality control to the [**CTransformFilter**](ctransformfilter.md) class.</span></span> <span data-ttu-id="2c453-107">El método **Receive** del filtro puede decidir quitar fotogramas, en función de los mensajes de calidad del representador y las medidas de rendimiento que el filtro recopila mientras se transmite por secuencias.</span><span class="sxs-lookup"><span data-stu-id="2c453-107">The filter's **Receive** method can decide to drop frames, based on quality messages from the renderer and performance measurements that the filter collects while it is streaming.</span></span>

<span data-ttu-id="2c453-108">Si el filtro quita un fotograma, sigue colocando fotogramas hasta que llega al siguiente fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="2c453-108">If the filter drops a frame, it continues to drop frames until it reaches the next key frame.</span></span> <span data-ttu-id="2c453-109">En el caso de las secuencias MPEG, el filtro no distingue entre fotogramas B y fotogramas P.</span><span class="sxs-lookup"><span data-stu-id="2c453-109">For MPEG streams, the filter does not distinguish between B frames and P frames.</span></span>



| <span data-ttu-id="2c453-110">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="2c453-110">Protected Member Variables</span></span>                                                      | <span data-ttu-id="2c453-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c453-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c453-112">**m \_ bQualityChanged**</span><span class="sxs-lookup"><span data-stu-id="2c453-112">**m\_bQualityChanged**</span></span>](cvideotransformfilter-m-bqualitychanged.md)           | <span data-ttu-id="2c453-113">Indica si el filtro ha quitado fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2c453-113">Indicates whether the filter has dropped frames.</span></span>                                               |
| [<span data-ttu-id="2c453-114">**m \_ bSkipping**</span><span class="sxs-lookup"><span data-stu-id="2c453-114">**m\_bSkipping**</span></span>](cvideotransformfilter-m-bskipping.md)                       | <span data-ttu-id="2c453-115">Indica si el filtro está quitando actualmente fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2c453-115">Indicates whether the filter is currently dropping frames.</span></span>                                     |
| [<span data-ttu-id="2c453-116">**m \_ itrAvgDecode**</span><span class="sxs-lookup"><span data-stu-id="2c453-116">**m\_itrAvgDecode**</span></span>](cvideotransformfilter-m-itravgdecode.md)                 | <span data-ttu-id="2c453-117">Promedio de tiempo que ha tardado en descodificar un marco.</span><span class="sxs-lookup"><span data-stu-id="2c453-117">Average length of time it has taken to decode a frame.</span></span>                                         |
| [<span data-ttu-id="2c453-118">**m \_ itrLate**</span><span class="sxs-lookup"><span data-stu-id="2c453-118">**m\_itrLate**</span></span>](cvideotransformfilter-m-itrlate.md)                           | <span data-ttu-id="2c453-119">Indica el nivel de finalización de las muestras en el representador.</span><span class="sxs-lookup"><span data-stu-id="2c453-119">Indicates how late the samples are arriving at the renderer.</span></span>                                   |
| [<span data-ttu-id="2c453-120">**m \_ nFramesSinceKeyFrame**</span><span class="sxs-lookup"><span data-stu-id="2c453-120">**m\_nFramesSinceKeyFrame**</span></span>](cvideotransformfilter-m-nframessincekeyframe.md) | <span data-ttu-id="2c453-121">Número de fotogramas que ha recibido el filtro desde el último fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="2c453-121">The number of frames that the filter has received since the last key frame.</span></span>                    |
| [<span data-ttu-id="2c453-122">**m \_ nKeyFramePeriod**</span><span class="sxs-lookup"><span data-stu-id="2c453-122">**m\_nKeyFramePeriod**</span></span>](cvideotransformfilter-m-nkeyframeperiod.md)           | <span data-ttu-id="2c453-123">El intervalo observado más grande entre fotogramas clave.</span><span class="sxs-lookup"><span data-stu-id="2c453-123">The largest observed interval between key frames.</span></span>                                              |
| [<span data-ttu-id="2c453-124">**m \_ nWaitForKey**</span><span class="sxs-lookup"><span data-stu-id="2c453-124">**m\_nWaitForKey**</span></span>](cvideotransformfilter-m-nwaitforkey.md)                   | <span data-ttu-id="2c453-125">Número máximo actual de fotogramas Delta que se van a quitar.</span><span class="sxs-lookup"><span data-stu-id="2c453-125">The current maximum number of delta frames to drop.</span></span>                                            |
| [<span data-ttu-id="2c453-126">**m \_ tDecodeStart**</span><span class="sxs-lookup"><span data-stu-id="2c453-126">**m\_tDecodeStart**</span></span>](cvideotransformfilter-m-tdecodestart.md)                 | <span data-ttu-id="2c453-127">Período de tiempo que se tardó en descodificar el ejemplo más reciente.</span><span class="sxs-lookup"><span data-stu-id="2c453-127">Length of time that it took to decode the most recent sample.</span></span>                                  |
| <span data-ttu-id="2c453-128">Métodos protegidos</span><span class="sxs-lookup"><span data-stu-id="2c453-128">Protected Methods</span></span>                                                               | <span data-ttu-id="2c453-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c453-129">Description</span></span>                                                                                    |
| [<span data-ttu-id="2c453-130">**AbortPlayback**</span><span class="sxs-lookup"><span data-stu-id="2c453-130">**AbortPlayback**</span></span>](cvideotransformfilter-abortplayback.md)                    | <span data-ttu-id="2c453-131">Se usa para indicar un error de streaming.</span><span class="sxs-lookup"><span data-stu-id="2c453-131">Used to signal a streaming error.</span></span>                                                              |
| [<span data-ttu-id="2c453-132">**AlterQuality**</span><span class="sxs-lookup"><span data-stu-id="2c453-132">**AlterQuality**</span></span>](cvideotransformfilter-alterquality.md)                      | <span data-ttu-id="2c453-133">Notifica al filtro que se ha solicitado un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="2c453-133">Notifies the filter that a quality change is requested.</span></span>                                        |
| [<span data-ttu-id="2c453-134">**Aparecen**</span><span class="sxs-lookup"><span data-stu-id="2c453-134">**Receive**</span></span>](cvideotransformfilter-receive.md)                                | <span data-ttu-id="2c453-135">Recibe un ejemplo multimedia, lo procesa y entrega un ejemplo de salida al filtro de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="2c453-135">Receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> |
| [<span data-ttu-id="2c453-136">**ShouldSkipFrame**</span><span class="sxs-lookup"><span data-stu-id="2c453-136">**ShouldSkipFrame**</span></span>](cvideotransformfilter-shouldskipframe.md)                | <span data-ttu-id="2c453-137">Determina si el filtro debe quitar un ejemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="2c453-137">Determines whether the filter should drop a specified sample.</span></span>                                  |
| [<span data-ttu-id="2c453-138">**StartStreaming**</span><span class="sxs-lookup"><span data-stu-id="2c453-138">**StartStreaming**</span></span>](cvideotransformfilter-startstreaming.md)                  | <span data-ttu-id="2c453-139">Se le llama cuando el filtro cambia al estado de pausa.</span><span class="sxs-lookup"><span data-stu-id="2c453-139">Called when the filter switches to the paused state.</span></span>                                           |
| <span data-ttu-id="2c453-140">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="2c453-140">Public Methods</span></span>                                                                  | <span data-ttu-id="2c453-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c453-141">Description</span></span>                                                                                    |
| [<span data-ttu-id="2c453-142">**CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="2c453-142">**CVideoTransformFilter**</span></span>](cvideotransformfilter-cvideotransformfilter.md)    | <span data-ttu-id="2c453-143">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="2c453-143">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="2c453-144">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="2c453-144">**EndFlush**</span></span>](cvideotransformfilter-endflush.md)                              | <span data-ttu-id="2c453-145">Finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="2c453-145">Ends a flush operation.</span></span>                                                                        |



 

 

 



