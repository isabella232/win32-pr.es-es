---
description: Acerca de la API de Transcode
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Acerca de la API de Transcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569156"
---
# <a name="about-the-transcode-api"></a><span data-ttu-id="a9063-103">Acerca de la API de Transcode</span><span class="sxs-lookup"><span data-stu-id="a9063-103">About the Transcode API</span></span>

<span data-ttu-id="a9063-104">En el diagrama siguiente se muestra cómo se relaciona la API de Transcode con el resto de la canalización de codificación de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a9063-104">The following diagram shows how the transcode API relates to the rest of the Media Foundation encoding pipeline.</span></span>

![un diagrama que muestra la API de transcodificación.](images/encoding08.png)

<span data-ttu-id="a9063-106">La canalización de codificación contiene los siguientes objetos de procesamiento de datos:</span><span class="sxs-lookup"><span data-stu-id="a9063-106">The encoding pipeline contains the following data-processing objects:</span></span>

-   <span data-ttu-id="a9063-107">Origen de medios</span><span class="sxs-lookup"><span data-stu-id="a9063-107">Media source</span></span>
-   <span data-ttu-id="a9063-108">Descodificador</span><span class="sxs-lookup"><span data-stu-id="a9063-108">Decoder</span></span>
-   <span data-ttu-id="a9063-109">Remuestreador de audio y ajuste de vídeo</span><span class="sxs-lookup"><span data-stu-id="a9063-109">Video resizer or audio resampler</span></span>
-   <span data-ttu-id="a9063-110">Codificador</span><span class="sxs-lookup"><span data-stu-id="a9063-110">Encoder</span></span>
-   <span data-ttu-id="a9063-111">Receptor de medios</span><span class="sxs-lookup"><span data-stu-id="a9063-111">Media sink</span></span>

<span data-ttu-id="a9063-112">El ajuste de tamaño de vídeo solo es necesario si el tamaño del vídeo de salida difiere del origen.</span><span class="sxs-lookup"><span data-stu-id="a9063-112">The video resizer is needed only if the size of the output video differs from the source.</span></span> <span data-ttu-id="a9063-113">El remuestreador de audio solo es necesario si es necesario volver a muestrear el audio antes de la codificación.</span><span class="sxs-lookup"><span data-stu-id="a9063-113">The audio resampler is needed only if the audio needs to be resampled before encoding.</span></span> <span data-ttu-id="a9063-114">El par descodificador/codificador es necesario para la transcodificación, pero no para remuxing.</span><span class="sxs-lookup"><span data-stu-id="a9063-114">The decoder/encoder pair is required for transcoding, but not for remuxing.</span></span>

<span data-ttu-id="a9063-115">La *topología* de codificación es el conjunto de objetos de canalización (origen, descodificador, tamaño, remuestreador, codificador y receptor de medios), además de los puntos de conexión entre ellos.</span><span class="sxs-lookup"><span data-stu-id="a9063-115">The encoding *topology* is the set of pipeline objects (source, decoder, resizer, resampler, encoder, and media sink), plus the connection points between them.</span></span> <span data-ttu-id="a9063-116">Para obtener más información sobre las topologías, vea [topologías](topologies.md).</span><span class="sxs-lookup"><span data-stu-id="a9063-116">For more information about topologies, see [Topologies](topologies.md).</span></span>

<span data-ttu-id="a9063-117">Los distintos componentes son responsables de crear los distintos objetos de canalización:</span><span class="sxs-lookup"><span data-stu-id="a9063-117">Different components are responsible for creating the various pipeline objects:</span></span>

-   <span data-ttu-id="a9063-118">Normalmente, la aplicación usa la [resolución de origen](source-resolver.md) para crear el origen de medios.</span><span class="sxs-lookup"><span data-stu-id="a9063-118">The application typically uses the [Source Resolver](source-resolver.md) to create the media source.</span></span>
-   <span data-ttu-id="a9063-119">La [sesión multimedia](media-session.md) carga y configura el descodificador, el tamaño de vídeo y el remuestreador de audio.</span><span class="sxs-lookup"><span data-stu-id="a9063-119">The [Media Session](media-session.md) loads and configures the decoder, video resizer, and audio resampler.</span></span> <span data-ttu-id="a9063-120">Internamente, usa el cargador de topología para hacerlo (consulte [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span><span class="sxs-lookup"><span data-stu-id="a9063-120">Internally, it uses the topology loader to do this (see [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).</span></span>
-   <span data-ttu-id="a9063-121">La API de Transcode carga y configura el codificador y el receptor de medios.</span><span class="sxs-lookup"><span data-stu-id="a9063-121">The transcode API loads and configures the encoder and the media sink.</span></span>

<span data-ttu-id="a9063-122">Las aplicaciones avanzadas pueden configurar el codificador y el receptor multimedia directamente, en lugar de usar la API de Transcode.</span><span class="sxs-lookup"><span data-stu-id="a9063-122">Advanced applications can configure the encoder and the media sink directly, rather than using the transcode API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9063-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a9063-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9063-124">API de transcodificación</span><span class="sxs-lookup"><span data-stu-id="a9063-124">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="a9063-125">Uso de la API de Transcode</span><span class="sxs-lookup"><span data-stu-id="a9063-125">Using the Transcode API</span></span>](fast-transcode-objects.md)
</dt> </dl>

 

 



