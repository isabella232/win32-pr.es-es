---
description: Ejemplo de filtro de ámbito
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Ejemplo de filtro de ámbito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494891"
---
# <a name="scope-filter-sample"></a><span data-ttu-id="34cbf-103">Ejemplo de filtro de ámbito</span><span class="sxs-lookup"><span data-stu-id="34cbf-103">Scope Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="34cbf-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="34cbf-104">Description</span></span>

<span data-ttu-id="34cbf-105">El filtro de ámbito es un filtro de representador que muestra los datos de sonido como formas de onda.</span><span class="sxs-lookup"><span data-stu-id="34cbf-105">The Scope filter is a renderer filter that displays sound data as wave forms.</span></span>

## <a name="usage"></a><span data-ttu-id="34cbf-106">Uso</span><span class="sxs-lookup"><span data-stu-id="34cbf-106">Usage</span></span>

<span data-ttu-id="34cbf-107">Para usar este filtro, abra GraphEdit y represente un archivo de audio (o un archivo de vídeo con una secuencia de audio).</span><span class="sxs-lookup"><span data-stu-id="34cbf-107">To use this filter, open GraphEdit and render an audio file (or a video file with an audio stream).</span></span> <span data-ttu-id="34cbf-108">Desconecte el representador de audio temporalmente e inserte el filtro de ejemplo Infinite-Pin Tee ([ejemplo de filtro InfTee](inftee-filter-sample.md)).</span><span class="sxs-lookup"><span data-stu-id="34cbf-108">Disconnect the audio renderer temporarily and insert the Infinite-Pin Tee ([InfTee Filter Sample](inftee-filter-sample.md)) sample filter.</span></span> <span data-ttu-id="34cbf-109">Vuelva a conectar el representador de audio.</span><span class="sxs-lookup"><span data-stu-id="34cbf-109">Reconnect the audio renderer.</span></span> <span data-ttu-id="34cbf-110">A continuación, conecte el segundo PIN de salida del filtro Infinite-Pin Tee al filtro de ámbito.</span><span class="sxs-lookup"><span data-stu-id="34cbf-110">Then connect the Infinite-Pin Tee filter's second output pin to the Scope filter.</span></span> <span data-ttu-id="34cbf-111">Ahora ejecute el gráfico.</span><span class="sxs-lookup"><span data-stu-id="34cbf-111">Now run the graph.</span></span>

<span data-ttu-id="34cbf-112">La ventana ámbito se implementa como un cuadro de diálogo, no como una ventana real.</span><span class="sxs-lookup"><span data-stu-id="34cbf-112">The Scope window is implemented as a dialog box, not as an actual window.</span></span> <span data-ttu-id="34cbf-113">Los desarrolladores que crean paneles de control para modificar los parámetros de filtro en tiempo real pueden querer usar una técnica como esta en lugar de las páginas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="34cbf-113">Developers creating control panels to alter filter parameters in real time might want to use a technique like this rather than property pages.</span></span>

<span data-ttu-id="34cbf-114">El filtro de ámbito muestra la configuración de un subproceso independiente para procesar los datos.</span><span class="sxs-lookup"><span data-stu-id="34cbf-114">The Scope filter demonstrates setting up a separate thread to process data.</span></span> <span data-ttu-id="34cbf-115">En este caso, los datos se copian en un búfer independiente en el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) y, a continuación, se dibujan en la ventana de ámbito en el subproceso independiente.</span><span class="sxs-lookup"><span data-stu-id="34cbf-115">In this case, the data is just copied to a separate buffer on the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, and is then drawn on the Scope window on the separate thread.</span></span>

<span data-ttu-id="34cbf-116">El filtro de ámbito también le permite supervisar la salida de audio para determinar si está recortando, de modo que pueda ajustar la ganancia.</span><span class="sxs-lookup"><span data-stu-id="34cbf-116">The Scope filter also enables you to monitor audio output to determine if you are clipping, so you can adjust the gain.</span></span>

<span data-ttu-id="34cbf-117">Este filtro aparece en GraphEdit como "Oscilloscope".</span><span class="sxs-lookup"><span data-stu-id="34cbf-117">This filter appears in GraphEdit as "Oscilloscope."</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="34cbf-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="34cbf-118">Downloading the Sample</span></span>

<span data-ttu-id="34cbf-119">Para descargar los ejemplos del SDK de DirectShow, instale la versión más reciente de la [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="34cbf-119">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="34cbf-120">Este ejemplo se instala en la siguiente ruta de acceso: ejemplos *\[ raíz \] del SDK* ámbito de filtros de DirectShow de \\ \\ multimedia \\ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="34cbf-120">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\Scope.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34cbf-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="34cbf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34cbf-122">Ejemplos de DirectShow</span><span class="sxs-lookup"><span data-stu-id="34cbf-122">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



