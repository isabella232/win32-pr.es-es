---
description: El escritor de receptor es un componente para la codificación de archivos de audio o de vídeo.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Escritor de receptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360476"
---
# <a name="sink-writer"></a><span data-ttu-id="b84bb-103">Escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="b84bb-103">Sink Writer</span></span>

<span data-ttu-id="b84bb-104">El escritor de receptor es un componente para la codificación de archivos de audio o de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b84bb-104">The sink writer is a component for encoding audio or video files.</span></span>

<span data-ttu-id="b84bb-105">En el diagrama siguiente se muestra, en un nivel alto, cómo una aplicación utiliza el escritor de receptor para codificar y el archivo de audio o vídeo.</span><span class="sxs-lookup"><span data-stu-id="b84bb-105">The following diagram shows, at a high level, how an application uses the sink writer to encode and audio/video file.</span></span>

![diagrama que muestra el escritor del receptor.](images/encoding09.png)

<span data-ttu-id="b84bb-107">El escritor de receptor hospeda un receptor de medios y, opcionalmente, uno o más codificadores.</span><span class="sxs-lookup"><span data-stu-id="b84bb-107">The sink writer hosts a media sink and optionally one or more encoders.</span></span> <span data-ttu-id="b84bb-108">Los codificadores convierten datos de audio o vídeo sin comprimir en bitstreams codificados.</span><span class="sxs-lookup"><span data-stu-id="b84bb-108">The encoders convert uncompressed audio or video data to encoded bitstreams.</span></span> <span data-ttu-id="b84bb-109">El receptor de medios envía el bitstreams a un archivo.</span><span class="sxs-lookup"><span data-stu-id="b84bb-109">The media sink outputs the bitstreams to a file.</span></span> <span data-ttu-id="b84bb-110">El escritor del receptor realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="b84bb-110">The sink writer performs the following tasks:</span></span>

-   <span data-ttu-id="b84bb-111">Carga el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="b84bb-111">Loads the media sink.</span></span>
-   <span data-ttu-id="b84bb-112">Busca y carga los codificadores.</span><span class="sxs-lookup"><span data-stu-id="b84bb-112">Finds and loads the encoders.</span></span>
-   <span data-ttu-id="b84bb-113">Administra el flujo de datos a los codificadores y al receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="b84bb-113">Manages the data flow to the encoders and the media sink.</span></span>

<span data-ttu-id="b84bb-114">La aplicación pasa datos de audio o vídeo al escritor de receptor como entrada.</span><span class="sxs-lookup"><span data-stu-id="b84bb-114">The application passes audio/video data to the sink writer as input.</span></span> <span data-ttu-id="b84bb-115">No importa el modo en que la aplicación obtiene o genera los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="b84bb-115">It does not matter how the application obtains or generates the input data.</span></span> <span data-ttu-id="b84bb-116">Una opción es usar el [lector de origen](source-reader.md), tal y como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="b84bb-116">One option is to use the [Source Reader](source-reader.md), as shown in the following diagram.</span></span> <span data-ttu-id="b84bb-117">Sin embargo, el escritor del receptor no requiere el uso del lector de origen.</span><span class="sxs-lookup"><span data-stu-id="b84bb-117">However, the sink writer does not require the use of the source reader.</span></span> <span data-ttu-id="b84bb-118">Estos dos componentes son independientes.</span><span class="sxs-lookup"><span data-stu-id="b84bb-118">These two components are independent.</span></span>

![diagrama que muestra el lector de origen y el escritor del receptor.](images/encoding02.png)

## <a name="in-this-section"></a><span data-ttu-id="b84bb-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b84bb-120">In this section</span></span>

-   [<span data-ttu-id="b84bb-121">Uso del escritor de receptor</span><span class="sxs-lookup"><span data-stu-id="b84bb-121">Using the Sink Writer</span></span>](using-the-sink-writer.md)
-   [<span data-ttu-id="b84bb-122">Tutorial: uso del escritor de receptores para codificar vídeo</span><span class="sxs-lookup"><span data-stu-id="b84bb-122">Tutorial: Using the Sink Writer to Encode Video</span></span>](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a><span data-ttu-id="b84bb-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b84bb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b84bb-124">Codificación y creación de archivos</span><span class="sxs-lookup"><span data-stu-id="b84bb-124">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="b84bb-125">Información general de la codificación en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b84bb-125">Overview of Encoding in Media Foundation</span></span>](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



