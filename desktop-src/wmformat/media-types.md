---
title: Tipos de medios para el SDK de Windows Media Format
description: Obtenga información acerca de los tipos de medios que puede usar el SDK de Windows Media Format. Los tipos de medios son valores GUID asignados a constantes en el SDK.
ms.assetid: 00dcbb20-09ed-44c5-992c-20f3d17ad47c
keywords:
- Windows Media Format SDK, tipos de medios
- Advanced Systems Format (ASF), tipos de medios
- ASF (formato de sistemas avanzados), tipos de medios
- tipos de medios, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6d15255ab311c67562a6c9dde83650240b0803
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187814"
---
# <a name="media-types-for-windows-media-format-sdk"></a><span data-ttu-id="4ab1e-108">Tipos de medios para el SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="4ab1e-108">Media Types for Windows Media Format SDK</span></span>

<span data-ttu-id="4ab1e-109">Los tipos de medios identifican los distintos tipos de medios que puede usar el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-109">Media types identify the different types of media that can be used by the Windows Media Format SDK.</span></span> <span data-ttu-id="4ab1e-110">Todos los tipos de medios son valores GUID que se han asignado a constantes en el SDK.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-110">All media types are GUID values that have been assigned to constants in the SDK.</span></span> <span data-ttu-id="4ab1e-111">Los valores de GUID representados por las constantes que se enumeran en esta sección se enumeran en la sección [identificadores de tipo de medio](media-type-identifiers.md) de esta referencia.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-111">The GUID values represented by the constants listed in this section are listed in the [Media Type Identifiers](media-type-identifiers.md) section of this reference.</span></span>

<span data-ttu-id="4ab1e-112">En la tabla siguiente se enumeran los tipos de medios principales.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-112">The following table lists major media types.</span></span> <span data-ttu-id="4ab1e-113">Estas constantes definen la clasificación de alto nivel de los medios digitales compatibles con el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-113">These constants define the high level classification of digital media supported by the Windows Media Format SDK.</span></span>



| <span data-ttu-id="4ab1e-114">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="4ab1e-114">Major type</span></span>                | <span data-ttu-id="4ab1e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ab1e-115">Description</span></span>                                                                                             |
|---------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab1e-116">Vídeo de WMMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="4ab1e-116">WMMEDIATYPE\_Video</span></span>        | <span data-ttu-id="4ab1e-117">Un flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-117">A video stream.</span></span>                                                                                         |
| <span data-ttu-id="4ab1e-118">\_Audio WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="4ab1e-118">WMMEDIATYPE\_Audio</span></span>        | <span data-ttu-id="4ab1e-119">Secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-119">An audio stream.</span></span>                                                                                        |
| <span data-ttu-id="4ab1e-120">\_Script WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="4ab1e-120">WMMEDIATYPE\_Script</span></span>       | <span data-ttu-id="4ab1e-121">Secuencia de script.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-121">A script stream.</span></span>                                                                                        |
| <span data-ttu-id="4ab1e-122">WMMEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="4ab1e-122">WMMEDIATYPE\_FileTransfer</span></span> | <span data-ttu-id="4ab1e-123">Flujo que contiene archivos de datos.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-123">A stream that contains data files.</span></span> <span data-ttu-id="4ab1e-124">Las secuencias Web, que constan de archivos HTML, también tienen este tipo principal.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-124">Web streams, which consist of HTML files, also have this major type.</span></span> |
| <span data-ttu-id="4ab1e-125">Imagen de WMMEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="4ab1e-125">WMMEDIATYPE\_Image</span></span>        | <span data-ttu-id="4ab1e-126">Secuencia de imágenes JPEG para un archivo de audio ilustrado (como en una presentación).</span><span class="sxs-lookup"><span data-stu-id="4ab1e-126">A JPEG image stream for an illustrated audio file (as in a slide show).</span></span>                                 |
| <span data-ttu-id="4ab1e-127">\_Texto WMMEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="4ab1e-127">WMMEDIATYPE\_Text</span></span>         | <span data-ttu-id="4ab1e-128">Secuencia de texto.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-128">A text stream.</span></span>                                                                                          |



 

<span data-ttu-id="4ab1e-129">Además de los tipos de medios principales admitidos explícitamente, puede crear sus propios tipos de datos arbitrarios.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-129">In addition to the explicitly supported major media types, you can create your own arbitrary data types.</span></span> <span data-ttu-id="4ab1e-130">En el caso de los tipos de datos arbitrarios personalizados, debe asegurarse de que el GUID que usa no coincide con un tipo principal existente.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-130">For custom arbitrary data types, you must ensure that the GUID you use does not match an existing major type.</span></span>

<span data-ttu-id="4ab1e-131">A menudo, un flujo multimedia tendrá un subtipo además de su tipo principal.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-131">A media stream will often have a subtype in addition to its major type.</span></span> <span data-ttu-id="4ab1e-132">En las secciones siguientes se enumeran los subtipos admitidos.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-132">The following sections list the supported subtypes.</span></span>



| <span data-ttu-id="4ab1e-133">Sección</span><span class="sxs-lookup"><span data-stu-id="4ab1e-133">Section</span></span>                                                        | <span data-ttu-id="4ab1e-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ab1e-134">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ab1e-135">Subtipos de medios sin comprimir</span><span class="sxs-lookup"><span data-stu-id="4ab1e-135">Uncompressed Media Subtypes</span></span>](uncompressed-media-subtypes.md) | <span data-ttu-id="4ab1e-136">Describe los subtipos disponibles para los medios sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-136">Describes the subtypes available for uncompressed media.</span></span> <span data-ttu-id="4ab1e-137">Estos son los tipos que normalmente se asocian a los medios de entrada o salida.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-137">These are the types typically associated with input or output media.</span></span>              |
| [<span data-ttu-id="4ab1e-138">Subtipos de medios comprimidos</span><span class="sxs-lookup"><span data-stu-id="4ab1e-138">Compressed Media Subtypes</span></span>](compressed-media-subtypes.md)     | <span data-ttu-id="4ab1e-139">Describe los subtipos disponibles para los medios comprimidos.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-139">Describes the subtypes available for compressed media.</span></span> <span data-ttu-id="4ab1e-140">Estos son los tipos asociados normalmente a los elementos multimedia en una secuencia dentro de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-140">These are the types typically associated with media in a stream within an ASF file.</span></span> |
| [<span data-ttu-id="4ab1e-141">Formatos de entrada de vídeo</span><span class="sxs-lookup"><span data-stu-id="4ab1e-141">Video Input Formats</span></span>](video-input-formats.md)                 | <span data-ttu-id="4ab1e-142">Enumera los formatos de vídeo que se aceptan como entradas para el códec Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="4ab1e-142">Lists the video formats accepted as inputs for the Windows Media Video 9 codec.</span></span>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="4ab1e-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4ab1e-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ab1e-144">**Identificadores de tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="4ab1e-144">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="4ab1e-145">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="4ab1e-145">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 




