---
description: En este tema se describe cómo trabajar con perfiles ASF en Microsoft Media Foundation.
ms.assetid: 03a0981b-29c3-450d-aa58-bc56a76e6cb6
title: Perfil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616670e7de68fd73c168c474544fc6236f1586e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539646"
---
# <a name="asf-profile"></a><span data-ttu-id="902c3-103">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="902c3-103">ASF Profile</span></span>

<span data-ttu-id="902c3-104">En este tema se describe cómo trabajar con perfiles ASF en Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="902c3-104">This topic describes how to work with ASF profiles in Microsoft Media Foundation.</span></span>

<span data-ttu-id="902c3-105">Un archivo de formato de sistema avanzado (ASF) contiene una o más secuencias.</span><span class="sxs-lookup"><span data-stu-id="902c3-105">An Advanced Systems Format (ASF) file contains one or more streams.</span></span> <span data-ttu-id="902c3-106">Para cada flujo, el encabezado ASF contiene un encabezado de propiedades de secuencia que describe la secuencia.</span><span class="sxs-lookup"><span data-stu-id="902c3-106">For each stream, the ASF header contains a Stream Properties Header that describes the stream.</span></span> <span data-ttu-id="902c3-107">En el nivel [WMContainer](wmcontainer-asf-components.md) , se usan los siguientes objetos para establecer o leer las propiedades de las secuencias ASF:</span><span class="sxs-lookup"><span data-stu-id="902c3-107">At the [WMContainer](wmcontainer-asf-components.md) layer, the following objects are used to set or read the properties of the ASF streams:</span></span>

-   <span data-ttu-id="902c3-108">Objeto de *perfil ASF* : describe las secuencias y sus relaciones entre sí.</span><span class="sxs-lookup"><span data-stu-id="902c3-108">*ASF profile* object: Describes the streams and their relationships with each other.</span></span> <span data-ttu-id="902c3-109">El objeto de perfil ASF expone la interfaz [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="902c3-109">The ASF profile object exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>
-   <span data-ttu-id="902c3-110">Objeto de *configuración de secuencia* : describe una secuencia.</span><span class="sxs-lookup"><span data-stu-id="902c3-110">*Stream configuration* object: Describes one stream.</span></span> <span data-ttu-id="902c3-111">El objeto de configuración de secuencia contiene un tipo de medio que describe el formato de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="902c3-111">The stream configuration object contains a media type that describes the format of the stream.</span></span> <span data-ttu-id="902c3-112">En el caso de las secuencias de audio y vídeo, el tipo de archivo multimedia describe exactamente cómo se configura el flujo y lo usan los códecs que codifican o descodifican la secuencia.</span><span class="sxs-lookup"><span data-stu-id="902c3-112">For audio and video streams, the media type describes exactly how the stream is configured, and is used by codecs that encode or decode the stream.</span></span> <span data-ttu-id="902c3-113">El objeto de configuración de secuencia expone la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="902c3-113">The stream configuration object exposes the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="902c3-114">Un perfil ASF válido contiene al menos un objeto de configuración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="902c3-114">A valid ASF profile contains at least one stream configuration object.</span></span>
-   <span data-ttu-id="902c3-115">Objeto de *exclusión mutua* : describe varias secuencias que no se van a leer simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="902c3-115">*Mutual exclusion* object: Describes multiple streams that are not intended be read concurrently.</span></span> <span data-ttu-id="902c3-116">Un objeto de exclusión mutua expone la interfaz [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) .</span><span class="sxs-lookup"><span data-stu-id="902c3-116">A mutual exclusion object exposes the [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) interface.</span></span> <span data-ttu-id="902c3-117">Un perfil ASF contiene cero o más objetos de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="902c3-117">An ASF profile contains zero or more mutual exclusion objects.</span></span>

<span data-ttu-id="902c3-118">En el diagrama siguiente se muestra la relación entre el perfil ASF y los objetos contenidos en el perfil.</span><span class="sxs-lookup"><span data-stu-id="902c3-118">The following diagram shows the relationship between the ASF profile and the objects that are contained in the profile.</span></span>

![diagrama de árbol de un nodo de perfil ASF con nodos secundarios de configuración de secuencia; los primeros apuntan al tipo de medio, los dos siguientes a la exclusión mutua](images/asf-components02.png)

<span data-ttu-id="902c3-120">Para la reproducción, el perfil ASF se usa para enumerar las secuencias y buscar los formatos de flujo.</span><span class="sxs-lookup"><span data-stu-id="902c3-120">For playback, the ASF profile is used to enumerate the streams and find the stream formats.</span></span> <span data-ttu-id="902c3-121">Para la codificación, el perfil ASF se usa para configurar las secuencias en el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="902c3-121">For encoding, the ASF profile is used to configure the streams in the destination file.</span></span>

<span data-ttu-id="902c3-122">El perfil ASF también se utiliza para configurar el [receptor de medios ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="902c3-122">The ASF profile is also used to configure the [ASF Media Sink](asf-media-sinks.md).</span></span> <span data-ttu-id="902c3-123">Para cada flujo en el perfil ASF, el receptor de medios ASF crea un receptor de flujo correspondiente.</span><span class="sxs-lookup"><span data-stu-id="902c3-123">For each stream in the ASF profile, the ASF media sink creates a corresponding stream sink.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="902c3-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="902c3-124">In this section</span></span>



| <span data-ttu-id="902c3-125">Tema</span><span class="sxs-lookup"><span data-stu-id="902c3-125">Topic</span></span>                                                                                           | <span data-ttu-id="902c3-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="902c3-126">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="902c3-127">Creación de un perfil ASF</span><span class="sxs-lookup"><span data-stu-id="902c3-127">Creating an ASF Profile</span></span>](creating-an-asf-profile.md)<br/>                               | <span data-ttu-id="902c3-128">Describe cómo crear un objeto de perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="902c3-128">Describes how to create an ASF profile object.</span></span><br/>          |
| [<span data-ttu-id="902c3-129">Crear y configurar secuencias ASF</span><span class="sxs-lookup"><span data-stu-id="902c3-129">Creating and Configuring ASF Streams</span></span>](creating-and-configuring-asf-streams.md)<br/>     | <span data-ttu-id="902c3-130">Describe cómo agregar secuencias a un perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="902c3-130">Describes how to add streams to an ASF profile.</span></span><br/>         |
| [<span data-ttu-id="902c3-131">Usar exclusión mutua para secuencias ASF</span><span class="sxs-lookup"><span data-stu-id="902c3-131">Using Mutual Exclusion for ASF Streams</span></span>](using-mutual-exclusion-for-asf-streams.md)<br/> | <span data-ttu-id="902c3-132">Describe cómo agregar exclusiones mutuas a secuencias ASF.</span><span class="sxs-lookup"><span data-stu-id="902c3-132">Describes how to add mutual exclusions to ASF streams.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="902c3-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="902c3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="902c3-134">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="902c3-134">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="902c3-135">Tutorial: 1-pasar la codificación de Windows Media</span><span class="sxs-lookup"><span data-stu-id="902c3-135">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="902c3-136">Tutorial: escribir un archivo WMA con codificación CBR</span><span class="sxs-lookup"><span data-stu-id="902c3-136">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[<span data-ttu-id="902c3-137">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="902c3-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 




