---
description: Compatibilidad con ASF en Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Compatibilidad con ASF en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707549"
---
# <a name="asf-support-in-media-foundation"></a><span data-ttu-id="eb2f8-103">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb2f8-103">ASF Support in Media Foundation</span></span>

<span data-ttu-id="eb2f8-104">Media Foundation admite archivos multimedia en el formato de sistemas avanzados (ASF):</span><span class="sxs-lookup"><span data-stu-id="eb2f8-104">Media Foundation supports media files in the Advanced Systems Format (ASF):</span></span>

-   <span data-ttu-id="eb2f8-105">Windows Media Video (archivos WMV)</span><span class="sxs-lookup"><span data-stu-id="eb2f8-105">Windows Media Video (WMV files)</span></span>
-   <span data-ttu-id="eb2f8-106">Windows Media Audio (archivos WMA)</span><span class="sxs-lookup"><span data-stu-id="eb2f8-106">Windows Media Audio (WMA files)</span></span>

<span data-ttu-id="eb2f8-107">Media Foundation proporciona varios objetos para leer y escribir archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-107">Media Foundation provides several objects for reading and writing ASF files.</span></span> <span data-ttu-id="eb2f8-108">Estos objetos se proporcionan en dos capas arquitectónicas diferentes.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-108">These objects are provided in two different architectural layers.</span></span>

<span data-ttu-id="eb2f8-109">En primer lugar, la capa de *canalización* contiene objetos que funcionan dentro de la [canalización Media Foundation](media-foundation-pipeline.md) y que se ajustan a las API definidas por la canalización.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-109">First, the *pipeline* layer contains objects that work inside the [Media Foundation pipeline](media-foundation-pipeline.md) and conform to the APIs defined by the pipeline.</span></span> <span data-ttu-id="eb2f8-110">La capa de canalización ASF contiene:</span><span class="sxs-lookup"><span data-stu-id="eb2f8-110">The ASF pipeline layer contains:</span></span>

-   <span data-ttu-id="eb2f8-111">[Origen de medios ASF](asf-media-source.md): analiza los archivos ASF y entrega los paquetes de datos de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-111">[ASF Media Source](asf-media-source.md): Parses ASF files and delivers the audio/video data packets.</span></span>
-   <span data-ttu-id="eb2f8-112">[Códecs de Windows Media](windows-media-codecs.md): descodificar o codificar secuencias de audio o vídeo de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-112">[Windows Media Codecs](windows-media-codecs.md): Decode or encode Windows Media audio or video streams.</span></span>
-   <span data-ttu-id="eb2f8-113">[Receptor de medios ASF](asf-media-sinks.md): recibe paquetes de datos y escribe un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-113">[ASF Media Sink](asf-media-sinks.md): Receives data packets and writes an ASF file.</span></span>

<span data-ttu-id="eb2f8-114">En segundo lugar, la capa de contenedor de WM proporciona un control de bajo nivel sobre el análisis y la escritura de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-114">Second, the WM Container layer provides low-level control over parsing and writing an ASF file.</span></span> <span data-ttu-id="eb2f8-115">La capa de canalización usa WMContainer internamente.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-115">The pipeline layer uses WMContainer internally.</span></span> <span data-ttu-id="eb2f8-116">Las aplicaciones también pueden usar WMContainer para el análisis y la escritura de ASF de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-116">Applications can also use WMContainer for low-level ASF parsing and writing.</span></span>

![diagrama que muestra los elementos de la capa de canalización y el contenedor de WM](images/asf-components.png)

## <a name="in-this-section"></a><span data-ttu-id="eb2f8-118">En esta sección</span><span class="sxs-lookup"><span data-stu-id="eb2f8-118">In this section</span></span>



| <span data-ttu-id="eb2f8-119">Tema</span><span class="sxs-lookup"><span data-stu-id="eb2f8-119">Topic</span></span>                                                                         | <span data-ttu-id="eb2f8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb2f8-120">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb2f8-121">Estructura de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="eb2f8-121">ASF File Structure</span></span>](asf-file-structure.md)<br/>                       | <span data-ttu-id="eb2f8-122">Información general de la estructura de archivos ASF y los objetos proporcionados por Media Foundation para trabajar con archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-122">Overview of the ASF file structure and the objects provided by Media Foundation to work with ASF files.</span></span><br/> |
| [<span data-ttu-id="eb2f8-123">Componentes ASF de capa de canalización</span><span class="sxs-lookup"><span data-stu-id="eb2f8-123">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)<br/> | <span data-ttu-id="eb2f8-124">Describe cómo analizar y crear archivos ASF con la capa de canalización.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-124">Describes how to parse and author ASF files using the pipeline layer.</span></span><br/>                                   |
| [<span data-ttu-id="eb2f8-125">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="eb2f8-125">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)<br/>       | <span data-ttu-id="eb2f8-126">Describe cómo analizar y crear archivos ASF con el nivel WMContainer.</span><span class="sxs-lookup"><span data-stu-id="eb2f8-126">Describes how to parse and author ASF files using the WMContainer layer.</span></span><br/>                                |



 

<span data-ttu-id="eb2f8-127">Para obtener información detallada acerca de la estructura de un archivo ASF, consulte la especificación ASF, que se puede descargar desde este [sitio web de Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="eb2f8-127">For detailed information about the structure of an ASF file, see the ASF specification, which can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb2f8-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb2f8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb2f8-129">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eb2f8-129">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




