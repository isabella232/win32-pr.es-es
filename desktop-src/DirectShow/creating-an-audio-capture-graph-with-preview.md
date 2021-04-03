---
description: Creación de un gráfico de captura de audio con vista previa
ms.assetid: 73c0b799-060b-4b20-b072-6a0c5c30de20
title: Creación de un gráfico de captura de audio con vista previa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2962dc0ffa08e19618d81a03515e970dcb439913
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103998028"
---
# <a name="creating-an-audio-capture-graph-with-preview"></a><span data-ttu-id="95178-103">Creación de un gráfico de captura de audio con vista previa</span><span class="sxs-lookup"><span data-stu-id="95178-103">Creating an Audio Capture Graph with Preview</span></span>

<span data-ttu-id="95178-104">El gráfico de filtros descrito en [creación de un gráfico de captura de audio](creating-an-audio-capture-graph.md) realiza la captura solo, sin vista previa.</span><span class="sxs-lookup"><span data-stu-id="95178-104">The filter graph described in [Creating an Audio Capture Graph](creating-an-audio-capture-graph.md) performs capture only, with no preview.</span></span> <span data-ttu-id="95178-105">Para obtener una vista previa y capturar al mismo tiempo, el gráfico de filtros debe utilizar el [filtro tee de anclaje infinito](infinite-pin-tee-filter.md).</span><span class="sxs-lookup"><span data-stu-id="95178-105">To preview and capture at the same time, the filter graph needs to use the [Infinite Pin Tee Filter](infinite-pin-tee-filter.md).</span></span> <span data-ttu-id="95178-106">Este filtro tiene un PIN de entrada y crea tantos clavijas de salida como sea necesario.</span><span class="sxs-lookup"><span data-stu-id="95178-106">This filter has one input pin and creates as many output pins as needed.</span></span> <span data-ttu-id="95178-107">(Se inicia con un PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="95178-107">(It starts with one output pin.</span></span> <span data-ttu-id="95178-108">Cada vez que se conecta un PIN de salida, se crea otro.) El filtro tee de anclaje infinito ofrece cada ejemplo que recibe, sin cambios, a través de todos los pin de salida.</span><span class="sxs-lookup"><span data-stu-id="95178-108">Each time you connect an output pin, it creates another one.) The Infinite Pin Tee filter delivers every sample that it receives, unchanged, through all of its output pins.</span></span>

<span data-ttu-id="95178-109">Conecte el filtro de captura de audio a la patilla infinita tee y conecte el PIN infinito a tee y al filtro de [representador de DirectSound](directsound-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="95178-109">Connect the Audio Capture Filter to the Infinite Pin Tee, and connect the Infinite Pin Tee to the multiplexer and the [DirectSound Renderer Filter](directsound-renderer-filter.md).</span></span> <span data-ttu-id="95178-110">Conecte el multiplexor al escritor de archivos, como antes.</span><span class="sxs-lookup"><span data-stu-id="95178-110">Connect the multiplexer to the file writer, as before.</span></span> <span data-ttu-id="95178-111">En el diagrama siguiente se muestra el gráfico de filtros resultante para un archivo AVI.</span><span class="sxs-lookup"><span data-stu-id="95178-111">The following diagram illustrates the resulting filter graph for an AVI file.</span></span>

![gráfico de captura de audio con vista previa](images/audio-capture-graph.png)

<span data-ttu-id="95178-113">Dado que el representador de DirectSound es el representador de audio predeterminado, simplemente se puede llamar al método [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) en el PIN de salida de tee del PIN infinito.</span><span class="sxs-lookup"><span data-stu-id="95178-113">Because the DirectSound Renderer is the default audio renderer, you can simply call the [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) method on the Infinite Pin Tee's output pin.</span></span> <span data-ttu-id="95178-114">Filter Graph Manager usa [Intelligent Connect](intelligent-connect.md) para crear el representador, agregarlo al gráfico de filtro y conectar los pin.</span><span class="sxs-lookup"><span data-stu-id="95178-114">The Filter Graph Manager uses [Intelligent Connect](intelligent-connect.md) to create the renderer, add it to the filter graph, and connect the pins.</span></span>

> [!Note]  
> <span data-ttu-id="95178-115">Si captura audio desde un micrófono y obtiene una vista previa de un altavoz en el mismo equipo, puede crear comentarios de audio.</span><span class="sxs-lookup"><span data-stu-id="95178-115">If you capture audio from a microphone and preview it from a speaker on the same computer, you might create audio feedback.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="95178-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95178-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95178-117">Captura de audio</span><span class="sxs-lookup"><span data-stu-id="95178-117">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 



