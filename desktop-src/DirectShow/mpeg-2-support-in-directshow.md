---
description: Compatibilidad con MPEG-2 en DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Compatibilidad con MPEG-2 en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537798"
---
# <a name="mpeg-2-support-in-directshow"></a><span data-ttu-id="ef732-103">Compatibilidad con MPEG-2 en DirectShow</span><span class="sxs-lookup"><span data-stu-id="ef732-103">MPEG-2 Support in DirectShow</span></span>

<span data-ttu-id="ef732-104">En esta sección se describen los componentes que puede usar para reproducir contenido MPEG-2 en DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ef732-104">This section describes the components that you can use to play MPEG-2 content in DirectShow.</span></span>

> [!Note]  
> <span data-ttu-id="ef732-105">Aunque DVD video se basa en MPEG-2, esta sección no describe la reproducción ni la navegación por DVD.</span><span class="sxs-lookup"><span data-stu-id="ef732-105">Although DVD video is based on MPEG-2, this section does not describe DVD playback or navigation.</span></span> <span data-ttu-id="ef732-106">Para obtener información acerca del DVD en DirectShow, consulte [aplicaciones de DVD](dvd-applications.md).</span><span class="sxs-lookup"><span data-stu-id="ef732-106">For information about DVD in DirectShow, see [DVD Applications](dvd-applications.md).</span></span>

 

<span data-ttu-id="ef732-107">Los datos MPEG-2 pueden provienen de un archivo local o de un origen en directo, como una difusión de red o un dispositivo D-VHS.</span><span class="sxs-lookup"><span data-stu-id="ef732-107">MPEG-2 data can come from a local file, or from a live source, such as a network broadcast or D-VHS device.</span></span> <span data-ttu-id="ef732-108">La reproducción de archivos se denomina *modo de extracción* porque el filtro del analizador extrae los datos del archivo en el gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="ef732-108">File playback is called *pull mode* because the parser filter pulls data from the file into the filter graph.</span></span> <span data-ttu-id="ef732-109">Los orígenes en directo se denominan el *modo de extracción* porque el filtro de origen envía datos al gráfico.</span><span class="sxs-lookup"><span data-stu-id="ef732-109">Live sources are called *push mode* because the source filter pushes data into the graph.</span></span>

<span data-ttu-id="ef732-110">DirectShow proporciona dos filtros que pueden analizar secuencias del sistema MPEG-2:</span><span class="sxs-lookup"><span data-stu-id="ef732-110">DirectShow provides two filters that can parse MPEG-2 system streams:</span></span>

-   <span data-ttu-id="ef732-111">[Demultiplexador MPEG-2](mpeg-2-demultiplexer.md) ("Demux"): este filtro admite el modo de extracción para flujos de programa y secuencias de transporte.</span><span class="sxs-lookup"><span data-stu-id="ef732-111">[MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux"): This filter supports push mode for program streams and transport streams.</span></span> <span data-ttu-id="ef732-112">En Windows XP y versiones posteriores, también admite el modo de extracción para las secuencias de programa.</span><span class="sxs-lookup"><span data-stu-id="ef732-112">In Windows XP and later, it also supports pull mode for program streams.</span></span>
-   <span data-ttu-id="ef732-113">[Separador MPEG-2](mpeg-2-splitter.md): este filtro admite el modo de extracción para las secuencias de programa en plataformas de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="ef732-113">[MPEG-2 Splitter](mpeg-2-splitter.md): This filter supports pull mode for program streams on downlevel platforms.</span></span> <span data-ttu-id="ef732-114">Este filtro está en desuso en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ef732-114">This filter is deprecated in Windows XP and later.</span></span>

<span data-ttu-id="ef732-115">Para usar el separador MPEG-2 Demux o MPEG-2, debe tener descodificadores de audio y vídeo de MPEG-2 compatibles con DirectShow que acepten secuencias elementales (PES).</span><span class="sxs-lookup"><span data-stu-id="ef732-115">To use the MPEG-2 demux or MPEG-2 splitter, you must have DirectShow-compatible MPEG-2 audio and video decoders that accept packetized elementary streams (PES).</span></span>

<span data-ttu-id="ef732-116">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="ef732-116">This section contains the following topics:</span></span>

-   [<span data-ttu-id="ef732-117">Información general de los sistemas MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ef732-117">Overview of MPEG-2 Systems</span></span>](overview-of-mpeg-2-systems.md)
-   [<span data-ttu-id="ef732-118">Usar el demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ef732-118">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
-   [<span data-ttu-id="ef732-119">Usar el divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="ef732-119">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
-   [<span data-ttu-id="ef732-120">Propiedades de ejemplo MPEG</span><span class="sxs-lookup"><span data-stu-id="ef732-120">MPEG Sample Properties</span></span>](mpeg-sample-properties.md)

## <a name="related-topics"></a><span data-ttu-id="ef732-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef732-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef732-122">Ejemplo de filtro de analizador de PSI</span><span class="sxs-lookup"><span data-stu-id="ef732-122">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 



