---
description: Ejemplo de filtro de metrónomo
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Ejemplo de filtro de metrónomo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686344"
---
# <a name="metronome-filter-sample"></a><span data-ttu-id="3d4e7-103">Ejemplo de filtro de metrónomo</span><span class="sxs-lookup"><span data-stu-id="3d4e7-103">Metronome Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="3d4e7-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d4e7-104">Description</span></span>

<span data-ttu-id="3d4e7-105">Este filtro de ejemplo muestra cómo implementar un reloj de referencia.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-105">This sample filter shows how to implement a reference clock.</span></span> <span data-ttu-id="3d4e7-106">El filtro usa la entrada de micrófono predeterminada para escuchar picos de audio (como clics, clapss de mano o tos), que usa para determinar la velocidad de reloj.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-106">The filter uses your default microphone input to listen for audio spikes (such as clicks, hand claps, or coughs), which it uses to determine a clock rate.</span></span>

## <a name="usage"></a><span data-ttu-id="3d4e7-107">Uso</span><span class="sxs-lookup"><span data-stu-id="3d4e7-107">Usage</span></span>

<span data-ttu-id="3d4e7-108">Compile el proyecto de ejemplo y copie el archivo DLL de filtro (Metronom.ax) en el directorio del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-108">Build the sample project and copy the filter DLL (Metronom.ax) to your Windows system directory.</span></span> <span data-ttu-id="3d4e7-109">Ejecute el archivo metrónomo. reg para registrar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-109">Run the Metronom.reg file to register the DLL.</span></span>

<span data-ttu-id="3d4e7-110">Para usar el filtro:</span><span class="sxs-lookup"><span data-stu-id="3d4e7-110">To use the filter:</span></span>

1.  <span data-ttu-id="3d4e7-111">Cree un gráfico de filtro en GraphEdit que representa una secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-111">Build a filter graph in GraphEdit that renders a video stream.</span></span>
2.  <span data-ttu-id="3d4e7-112">Elimine las secuencias de audio representadas.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-112">Delete any rendered audio streams.</span></span>
3.  <span data-ttu-id="3d4e7-113">Agregue el filtro metrónomo al gráfico.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-113">Add the Metronome filter to the graph.</span></span> <span data-ttu-id="3d4e7-114">Aparece en la categoría filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-114">It appears in the DirectShow Filters category.</span></span>
4.  <span data-ttu-id="3d4e7-115">Ejecute el gráfico.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-115">Run the graph.</span></span> <span data-ttu-id="3d4e7-116">El vídeo empezará a reproducirse a velocidad normal.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-116">The video will begin playing at normal speed.</span></span>
5.  <span data-ttu-id="3d4e7-117">Clap sus manos o use un metrónomo para establecer una nueva velocidad.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-117">Clap your hands or use a metronome to set a new speed.</span></span>

## <a name="programming-notes"></a><span data-ttu-id="3d4e7-118">Notas de programación</span><span class="sxs-lookup"><span data-stu-id="3d4e7-118">Programming Notes</span></span>

<span data-ttu-id="3d4e7-119">Este filtro solo funciona para vídeo.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-119">This filter works only for video.</span></span> <span data-ttu-id="3d4e7-120">El representador de audio no es capaz de sincronizar con diferentes velocidades de reloj.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-120">The audio renderer is not capable of synchronizing to radically different clock rates.</span></span>

<span data-ttu-id="3d4e7-121">Si Clap 92 veces por minuto (una vez cada ~ 652 MS), el vídeo se reproducirá a la tarifa normal.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-121">If you clap 92 times per minute (once every ~652 ms), the video will play at the normal rate.</span></span> <span data-ttu-id="3d4e7-122">Puede cambiar este valor predeterminado cambiando el valor de la constante `BPM` en metrónomo. cpp.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-122">You can change this default by changing the value of the constant `BPM` in Metronom.cpp.</span></span>

<span data-ttu-id="3d4e7-123">Si detiene aplausos durante un período de tiempo y, a continuación, vuelve a iniciar aplausos, debe comenzar de nuevo con la misma velocidad o el filtro lo omitirá.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-123">If you stop clapping for a period of time and then start clapping again, you must start again at approximately the same speed, or the filter will ignore it.</span></span> <span data-ttu-id="3d4e7-124">Además, la velocidad de reproducción de vídeo está limitada por la velocidad de la CPU.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-124">Also, the video playback rate is limited by the CPU speed.</span></span> <span data-ttu-id="3d4e7-125">Si supera el límite durante un período de tiempo, el filtro dejará de responder a los cambios de velocidad.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-125">If you exceed the limit for any length of time, the filter will stop responding to rate changes.</span></span> <span data-ttu-id="3d4e7-126">Si esto ocurre, detenga el gráfico y reinícielo.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-126">If this happens, stop the graph and restart.</span></span>

<span data-ttu-id="3d4e7-127">Si implementa su propio reloj, las reglas más importantes son que los relojes de referencia no deben ir hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-127">If you implement your own clock, the most important rules is that reference clocks must not go backward.</span></span> <span data-ttu-id="3d4e7-128">Es decir, nunca deben notificar un valor de tiempo menor que el valor de hora anterior.</span><span class="sxs-lookup"><span data-stu-id="3d4e7-128">That is, they must never report a time value less than the previous time value.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="3d4e7-129">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="3d4e7-129">Downloading the Sample</span></span>

<span data-ttu-id="3d4e7-130">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3d4e7-130">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="3d4e7-131">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ \] raíz del SDK* \\ \\ \\ filtros DirectShow de multimedia \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="3d4e7-131">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Metronome.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d4e7-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d4e7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d4e7-133">**Clase CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="3d4e7-133">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="3d4e7-134">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="3d4e7-134">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



