---
title: Características de archivos ASF
description: Características de archivos ASF
ms.assetid: 6e180f27-69ef-4fe0-b06c-b2ead7be8a05
keywords:
- SDK de Windows Media Format, características de archivo ASF
- Windows Media Format SDK, características
- Advanced Systems Format (ASF), características de archivo
- ASF (formato de sistemas avanzados), características de archivo
- Advanced Systems Format (ASF), características
- ASF (formato de sistemas avanzados), características
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871d2986ad85716fe198b9a16e1a3772d1cca5f8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "105705065"
---
# <a name="asf-file-features"></a><span data-ttu-id="333eb-109">Características de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="333eb-109">ASF File Features</span></span>

<span data-ttu-id="333eb-110">El propósito principal del SDK de Windows Media Format es proporcionar compatibilidad para encapsular datos multimedia digitales en archivos de formato de sistema avanzado (ASF) y entregar los medios a una aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="333eb-110">The primary purpose of the Windows Media Format SDK is to provide support for encapsulating digital media data in Advanced Systems Format (ASF) files and delivering the media to a client application.</span></span> <span data-ttu-id="333eb-111">Los escenarios de entrega pueden variar ampliamente de una aplicación a otra, pero todos usan la estructura de archivos ASF entre la creación y la entrega.</span><span class="sxs-lookup"><span data-stu-id="333eb-111">Delivery scenarios can vary widely from application to application, but all use the ASF file structure between authoring and delivery.</span></span> <span data-ttu-id="333eb-112">Los archivos ASF se ajustan a una estructura bien definida pero muy flexible.</span><span class="sxs-lookup"><span data-stu-id="333eb-112">ASF files conform to a well defined but very flexible structure.</span></span> <span data-ttu-id="333eb-113">Para obtener más información acerca de la estructura de archivos ASF, consulte [información general del formato ASF](overview-of-the-asf-format.md).</span><span class="sxs-lookup"><span data-stu-id="333eb-113">For more information about the ASF file structure, see [Overview of the ASF Format](overview-of-the-asf-format.md).</span></span>

<span data-ttu-id="333eb-114">En la especificación ASF se proporciona información detallada acerca de los datos de un archivo ASF, que puede descargar desde el [sitio web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span><span class="sxs-lookup"><span data-stu-id="333eb-114">Detailed information about the data in an ASF file is provided in the ASF specification, which you can download from the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

<span data-ttu-id="333eb-115">El SDK de Windows Media Format proporciona compatibilidad para las características de la especificación ASF principalmente a través del perfil que se usa para crear un archivo.</span><span class="sxs-lookup"><span data-stu-id="333eb-115">The Windows Media Format SDK provides support for the features of the ASF specification mostly through the profile that is used to create a file.</span></span> <span data-ttu-id="333eb-116">Para obtener más información sobre los perfiles, vea [perfiles](profiles.md).</span><span class="sxs-lookup"><span data-stu-id="333eb-116">For more information about profiles, see [Profiles](profiles.md).</span></span>

<span data-ttu-id="333eb-117">En esta sección se describen las características siguientes.</span><span class="sxs-lookup"><span data-stu-id="333eb-117">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="333eb-118">Secuencias de audio y vídeo</span><span class="sxs-lookup"><span data-stu-id="333eb-118">Audio and Video Streams</span></span>](audio-and-video-streams.md)
-   [<span data-ttu-id="333eb-119">Flujos de imagen</span><span class="sxs-lookup"><span data-stu-id="333eb-119">Image Streams</span></span>](image-streams.md)
-   [<span data-ttu-id="333eb-120">Flujos arbitrarios</span><span class="sxs-lookup"><span data-stu-id="333eb-120">Arbitrary Streams</span></span>](arbitrary-streams.md)
-   [<span data-ttu-id="333eb-121">Comandos de script</span><span class="sxs-lookup"><span data-stu-id="333eb-121">Script Commands</span></span>](script-commands.md)
-   [<span data-ttu-id="333eb-122">Extensiones de unidad de datos</span><span class="sxs-lookup"><span data-stu-id="333eb-122">Data Unit Extensions</span></span>](data-unit-extensions.md)
-   [<span data-ttu-id="333eb-123">Compatibilidad con código de tiempo SMPTE</span><span class="sxs-lookup"><span data-stu-id="333eb-123">SMPTE Time Code Support</span></span>](smpte-time-code-support.md)
-   [<span data-ttu-id="333eb-124">Exclusión mutua</span><span class="sxs-lookup"><span data-stu-id="333eb-124">Mutual Exclusion</span></span>](mutual-exclusion.md)
-   [<span data-ttu-id="333eb-125">Priorización de flujos</span><span class="sxs-lookup"><span data-stu-id="333eb-125">Stream Prioritization</span></span>](stream-prioritization.md)
-   [<span data-ttu-id="333eb-126">Uso compartido de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="333eb-126">Bandwidth Sharing</span></span>](bandwidth-sharing.md)
-   [<span data-ttu-id="333eb-127">Índices</span><span class="sxs-lookup"><span data-stu-id="333eb-127">Indexes</span></span>](indexes.md)
-   [<span data-ttu-id="333eb-128">Marcadores</span><span class="sxs-lookup"><span data-stu-id="333eb-128">Markers</span></span>](markers.md)
-   [<span data-ttu-id="333eb-129">Respuesta del lector a las características de ASF</span><span class="sxs-lookup"><span data-stu-id="333eb-129">Reader Response to ASF Features</span></span>](reader-response-to-asf-features.md)

## <a name="related-topics"></a><span data-ttu-id="333eb-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="333eb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="333eb-131">**Características**</span><span class="sxs-lookup"><span data-stu-id="333eb-131">**Features**</span></span>](features.md)
</dt> </dl>

 

 




