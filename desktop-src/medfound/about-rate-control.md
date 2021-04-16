---
description: Acerca del control tasa
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Acerca del control tasa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705564"
---
# <a name="about-rate-control"></a><span data-ttu-id="a4de7-103">Acerca del control tasa</span><span class="sxs-lookup"><span data-stu-id="a4de7-103">About Rate Control</span></span>

<span data-ttu-id="a4de7-104">En Media Foundation, la *velocidad* de reproducción se expresa como la relación entre la velocidad de reproducción actual y la velocidad de reproducción normal.</span><span class="sxs-lookup"><span data-stu-id="a4de7-104">In Media Foundation, the *playback rate* is expressed as the ratio of the current playback rate to the normal playback rate.</span></span> <span data-ttu-id="a4de7-105">Por ejemplo, una velocidad de 2,0 es dos veces la velocidad normal y 0,5 es la velocidad media normal.</span><span class="sxs-lookup"><span data-stu-id="a4de7-105">For example, a rate of 2.0 is twice normal speed, and 0.5 is half normal speed.</span></span> <span data-ttu-id="a4de7-106">Los valores negativos indican la reproducción inversa.</span><span class="sxs-lookup"><span data-stu-id="a4de7-106">Negative values indicate reverse playback.</span></span> <span data-ttu-id="a4de7-107">Una velocidad de reproducción de-2,0 se reproduce hacia atrás a lo largo de la secuencia dos veces la velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="a4de7-107">A playback rate of -2.0 plays backward through the stream at twice the normal speed.</span></span> <span data-ttu-id="a4de7-108">Una tasa de cero hace que se represente un fotograma; después, el reloj de la presentación no avanza.</span><span class="sxs-lookup"><span data-stu-id="a4de7-108">A rate of zero causes one frame to be rendered; after that, the presentation clock does not advance.</span></span> <span data-ttu-id="a4de7-109">Para obtener otro fotograma a la velocidad de cero, la aplicación debe buscar en una nueva posición.</span><span class="sxs-lookup"><span data-stu-id="a4de7-109">To get another frame at the rate of zero, the application must seek to a new position.</span></span>

<span data-ttu-id="a4de7-110">Las aplicaciones usan las siguientes interfaces para controlar la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a4de7-110">Applications use the following interfaces to control the playback rate.</span></span>

-   <span data-ttu-id="a4de7-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span><span class="sxs-lookup"><span data-stu-id="a4de7-111">[**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span></span> <span data-ttu-id="a4de7-112">Se usa para averiguar las velocidades de reproducción más rápidas y lentas posibles.</span><span class="sxs-lookup"><span data-stu-id="a4de7-112">Used to find out the fastest and slowest playback rates that are possible.</span></span>
-   <span data-ttu-id="a4de7-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span><span class="sxs-lookup"><span data-stu-id="a4de7-113">[**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="a4de7-114">Se usa para cambiar la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="a4de7-114">Used to change the playback rate.</span></span>

<span data-ttu-id="a4de7-115">Para obtener estas dos interfaces, llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) en la sesión multimedia.</span><span class="sxs-lookup"><span data-stu-id="a4de7-115">To get these two interfaces, call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the Media Session.</span></span> <span data-ttu-id="a4de7-116">El identificador del servicio es MF \_ rate \_ control \_ Service.</span><span class="sxs-lookup"><span data-stu-id="a4de7-116">The service identifier is MF\_RATE\_CONTROL\_SERVICE.</span></span>

<span data-ttu-id="a4de7-117">Con el servicio de control de tarifas, una aplicación puede implementar una reproducción rápida y directa.</span><span class="sxs-lookup"><span data-stu-id="a4de7-117">By using the rate control service, an application can implement fast forward and reverse playback.</span></span>

## <a name="thinning"></a><span data-ttu-id="a4de7-118">Simplificación</span><span class="sxs-lookup"><span data-stu-id="a4de7-118">Thinning</span></span>

<span data-ttu-id="a4de7-119">El *ligero* es cualquier proceso que reduzca el número de muestras de un flujo para reducir la velocidad de bits general.</span><span class="sxs-lookup"><span data-stu-id="a4de7-119">*Thinning* is any process that reduces the number of samples in a stream, to reduce the overall bit rate.</span></span> <span data-ttu-id="a4de7-120">En el caso de los vídeos, la reducción de los fotogramas Delta y la entrega solo de los fotogramas clave se logra con el ligero.</span><span class="sxs-lookup"><span data-stu-id="a4de7-120">For video, thinning is generally accomplished by dropping the delta frames and delivering only the key frames.</span></span> <span data-ttu-id="a4de7-121">A menudo, la canalización puede admitir velocidades de reproducción más rápidas mediante la reproducción reducida, ya que la velocidad de datos es menor porque las tramas Delta no se descodifican.</span><span class="sxs-lookup"><span data-stu-id="a4de7-121">Often the pipeline can support faster playback rates using thinned playback, because the data rate is lower because delta frames are not decoded.</span></span>

<span data-ttu-id="a4de7-122">El ligero no cambia las marcas de tiempo ni las duraciones de los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="a4de7-122">Thinning does not change the time stamps or durations on the samples.</span></span> <span data-ttu-id="a4de7-123">Por ejemplo, si la tasa nominal de la secuencia de vídeo es de 25 fotogramas por segundo, la duración de cada fotograma se mantiene marcada como 40 milisegundos, incluso si el origen de medios está quitando todos los fotogramas Delta.</span><span class="sxs-lookup"><span data-stu-id="a4de7-123">For example, if the nominal rate of the video stream is 25 frames per second, the duration of each frame is still marked as 40 milliseconds, even if the media source is dropping all of the delta frames.</span></span> <span data-ttu-id="a4de7-124">Esto significa que habrá un intervalo de tiempo entre el final de un fotograma y el inicio de la siguiente.</span><span class="sxs-lookup"><span data-stu-id="a4de7-124">That means there will be a time gap between the end of one frame and the start of the next.</span></span>

## <a name="scrubbing"></a><span data-ttu-id="a4de7-125">Scrubbing</span><span class="sxs-lookup"><span data-stu-id="a4de7-125">Scrubbing</span></span>

<span data-ttu-id="a4de7-126">La *limpieza* es el proceso de búsqueda instantánea de puntos específicos en el flujo interactuando con una barra de desplazamiento, una escala de tiempo u otra representación visual del tiempo.</span><span class="sxs-lookup"><span data-stu-id="a4de7-126">*Scrubbing* is the process of instantaneously seeking to specific points in the stream by interacting with a scrollbar, timeline, or other visual representation of time.</span></span> <span data-ttu-id="a4de7-127">El término proviene de la era de los reproductores de cintas carretes cuando se produce un carrete hacia atrás y hacia delante para buscar una sección, como la limpieza del cabezal de reproducción con la cinta.</span><span class="sxs-lookup"><span data-stu-id="a4de7-127">The term comes from the era of reel-to-reel tape players when rocking a reel back and forth to locate a section was like scrubbing the playback head with the tape.</span></span>

<span data-ttu-id="a4de7-128">La limpieza se implementa en Media Foundation estableciendo la velocidad de reproducción en cero.</span><span class="sxs-lookup"><span data-stu-id="a4de7-128">Scrubbing is implemented in Media Foundation by setting the playback rate to zero.</span></span> <span data-ttu-id="a4de7-129">Para obtener más información, vea [Cómo realizar la limpieza](how-to-perform-scrubbing.md).</span><span class="sxs-lookup"><span data-stu-id="a4de7-129">For more information, see [How to Perform Scrubbing](how-to-perform-scrubbing.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4de7-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4de7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4de7-131">Control de tasa</span><span class="sxs-lookup"><span data-stu-id="a4de7-131">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="a4de7-132">Búsqueda, avance rápido y reproducción inversa</span><span class="sxs-lookup"><span data-stu-id="a4de7-132">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[<span data-ttu-id="a4de7-133">Interfaces de servicio</span><span class="sxs-lookup"><span data-stu-id="a4de7-133">Service Interfaces</span></span>](service-interfaces.md)
</dt> </dl>

 

 



