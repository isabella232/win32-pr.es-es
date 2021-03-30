---
title: Tipos de medios
description: Tipos de medios
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, tipos de medios
- Advanced Systems Format (ASF), tipos de medios
- ASF (formato de sistemas avanzados), tipos de medios
- tipos de medios, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35005498e8b0625f404e9a54a51cddc65fbfd7bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148853"
---
# <a name="media-types"></a><span data-ttu-id="58f0c-107">Tipos de medios</span><span class="sxs-lookup"><span data-stu-id="58f0c-107">Media Types</span></span>

<span data-ttu-id="58f0c-108">Los tipos de medios identifican los distintos tipos de medios que puede usar el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="58f0c-108">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="58f0c-109">Todos los tipos de medios son valores GUID que se han asignado a constantes en el SDK.</span><span class="sxs-lookup"><span data-stu-id="58f0c-109">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="58f0c-110">Los valores de GUID representados por las constantes que se enumeran en esta sección se enumeran en la sección [identificadores de tipo de medio](media-type-identifiers.md) de esta referencia.</span><span class="sxs-lookup"><span data-stu-id="58f0c-110">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="58f0c-111">En la tabla siguiente se enumeran los tipos de medios principales.</span><span class="sxs-lookup"><span data-stu-id="58f0c-111">The following table lists major media types.</span></span> <span data-ttu-id="58f0c-112">Estas constantes definen la clasificación de alto nivel de los medios digitales compatibles con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="58f0c-112">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="58f0c-113">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="58f0c-113">Major type</span></span>                | <span data-ttu-id="58f0c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="58f0c-114">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58f0c-115">Vídeo de WMMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="58f0c-115">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="58f0c-116">Un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="58f0c-116">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="58f0c-117">\_Audio WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="58f0c-117">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="58f0c-118">Secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="58f0c-118">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="58f0c-119">\_Script WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="58f0c-119">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="58f0c-120">Secuencia de script.</span><span class="sxs-lookup"><span data-stu-id="58f0c-120">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="58f0c-121">WMMEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="58f0c-121">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="58f0c-122">Flujo que contiene archivos de datos.</span><span class="sxs-lookup"><span data-stu-id="58f0c-122">A stream that contains data files.</span></span> <span data-ttu-id="58f0c-123">Las secuencias Web, que constan de archivos HTML, también tienen este tipo principal.</span><span class="sxs-lookup"><span data-stu-id="58f0c-123">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="58f0c-124">Imagen de WMMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="58f0c-124">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="58f0c-125">Secuencia de imágenes JPEG para un archivo de audio ilustrado (como en una presentación).</span><span class="sxs-lookup"><span data-stu-id="58f0c-125">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="58f0c-126">\_Texto WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="58f0c-126">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="58f0c-127">Secuencia de texto.</span><span class="sxs-lookup"><span data-stu-id="58f0c-127">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="58f0c-128">Además de los tipos de medios principales admitidos explícitamente, puede crear sus propios tipos de datos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="58f0c-128">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="58f0c-129">En el caso de los tipos de datos arbitrarios personalizados, debe asegurarse de que el GUID que usa no coincide con un tipo principal existente.</span><span class="sxs-lookup"><span data-stu-id="58f0c-129">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="58f0c-130">A menudo, un flujo multimedia tendrá un subtipo además de su tipo principal.</span><span class="sxs-lookup"><span data-stu-id="58f0c-130">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="58f0c-131">En las secciones siguientes se enumeran los subtipos admitidos.</span><span class="sxs-lookup"><span data-stu-id="58f0c-131">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="58f0c-132">Sección</span><span class="sxs-lookup"><span data-stu-id="58f0c-132">Section</span></span>                                                        | <span data-ttu-id="58f0c-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="58f0c-133">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58f0c-134">Subtipos de medios sin comprimir</span><span class="sxs-lookup"><span data-stu-id="58f0c-134">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="58f0c-135">Describe los subtipos disponibles para los medios sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="58f0c-135">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="58f0c-136">Estos son los tipos que normalmente se asocian a los medios de entrada o salida.</span><span class="sxs-lookup"><span data-stu-id="58f0c-136">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="58f0c-137">Subtipos de medios comprimidos</span><span class="sxs-lookup"><span data-stu-id="58f0c-137">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="58f0c-138">Describe los subtipos disponibles para los medios comprimidos.</span><span class="sxs-lookup"><span data-stu-id="58f0c-138">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="58f0c-139">Estos son los tipos asociados normalmente a los elementos multimedia en una secuencia dentro de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="58f0c-139">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="58f0c-140">Formatos de entrada de vídeo</span><span class="sxs-lookup"><span data-stu-id="58f0c-140">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="58f0c-141">Enumera los formatos de vídeo que se aceptan como entradas para el códec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="58f0c-141">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="58f0c-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58f0c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58f0c-143">**Identificadores de tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="58f0c-143">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="58f0c-144">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="58f0c-144">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




