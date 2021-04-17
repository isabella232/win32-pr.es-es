---
title: Guía de programación del SDK de Windows Media Format
description: Guía de programación del SDK de Windows Media Format
ms.assetid: 9b382c88-e4a9-4aed-a250-250fabface44
keywords:
- SDK de Windows Media Format, guía de programación
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), guía de programación
- ASF (formato de sistemas avanzados), guía de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4ea4f6819a31693d7c9d149717324ef6dcc65a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705105"
---
# <a name="windows-media-format-sdk-programming-guide"></a><span data-ttu-id="2af22-107">Guía de programación del SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="2af22-107">Windows Media Format SDK Programming Guide</span></span>

<span data-ttu-id="2af22-108">La guía de programación está pensada para ayudarle a aprender a usar el kit de desarrollo de software (SDK) de Microsoft Windows Media Format para crear aplicaciones que funcionen con archivos con el formato de sistemas avanzados (ASF).</span><span class="sxs-lookup"><span data-stu-id="2af22-108">The Programming Guide is intended to help you learn how to use the Microsoft Windows Media Format Software Development Kit (SDK) to build applications that work with files using the Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="2af22-109">Puede usar el SDK de Windows Media Format para crear aplicaciones que escriban secuencias multimedia digitales y lean secuencias de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2af22-109">You can use the Windows Media Format SDK to create applications that write digital media streams to and read streams from ASF files.</span></span> <span data-ttu-id="2af22-110">Este SDK también admite la edición de metadatos en archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2af22-110">This SDK also supports the editing of metadata in ASF files.</span></span> <span data-ttu-id="2af22-111">Además, este SDK se puede usar para leer y manipular metadatos en archivos MP3.</span><span class="sxs-lookup"><span data-stu-id="2af22-111">In addition, this SDK can be used to read and manipulate metadata in MP3 files.</span></span>

<span data-ttu-id="2af22-112">En las secciones siguientes se explica con detalle los pasos necesarios para escribir, leer y editar archivos ASF mediante este SDK.</span><span class="sxs-lookup"><span data-stu-id="2af22-112">The following sections explain in detail the steps required to write, read, and edit ASF files by using this SDK.</span></span>



| <span data-ttu-id="2af22-113">Sección</span><span class="sxs-lookup"><span data-stu-id="2af22-113">Section</span></span>                                                                            | <span data-ttu-id="2af22-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2af22-114">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2af22-115">Introducción</span><span class="sxs-lookup"><span data-stu-id="2af22-115">Getting Started</span></span>](getting-started.md)                                             | <span data-ttu-id="2af22-116">Proporciona información general sobre cómo preparar el uso de este SDK.</span><span class="sxs-lookup"><span data-stu-id="2af22-116">Provides general information about getting ready to use this SDK.</span></span>                                                 |
| [<span data-ttu-id="2af22-117">Usar los métodos de devolución de llamada</span><span class="sxs-lookup"><span data-stu-id="2af22-117">Using the Callback Methods</span></span>](using-the-callback-methods.md)                       | <span data-ttu-id="2af22-118">Describe los métodos de devolución de llamada utilizados en muchas tareas diferentes.</span><span class="sxs-lookup"><span data-stu-id="2af22-118">Describes the callback methods used in many different tasks.</span></span>                                                      |
| [<span data-ttu-id="2af22-119">Trabajar con perfiles</span><span class="sxs-lookup"><span data-stu-id="2af22-119">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="2af22-120">Describe cómo utilizar, editar y crear perfiles.</span><span class="sxs-lookup"><span data-stu-id="2af22-120">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="2af22-121">Escribir archivos ASF</span><span class="sxs-lookup"><span data-stu-id="2af22-121">Writing ASF Files</span></span>](writing-asf-files.md)                                         | <span data-ttu-id="2af22-122">Describe cómo usar el objeto de escritor para crear archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2af22-122">Describes how to use the writer object to create ASF files.</span></span>                                                       |
| [<span data-ttu-id="2af22-123">Leer archivos ASF</span><span class="sxs-lookup"><span data-stu-id="2af22-123">Reading ASF Files</span></span>](reading-asf-files.md)                                         | <span data-ttu-id="2af22-124">Describe cómo recibir contenido de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2af22-124">Describes how to receive content from ASF files.</span></span>                                                                  |
| [<span data-ttu-id="2af22-125">Trabajar con metadatos</span><span class="sxs-lookup"><span data-stu-id="2af22-125">Working with Metadata</span></span>](working-with-metadata.md)                                 | <span data-ttu-id="2af22-126">Describe cómo administrar el contenido de la sección de encabezado de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="2af22-126">Describes how to manage the contents of the header section of an ASF file.</span></span>                                        |
| [<span data-ttu-id="2af22-127">Trabajar con índices</span><span class="sxs-lookup"><span data-stu-id="2af22-127">Working with Indexes</span></span>](working-with-indexes.md)                                   | <span data-ttu-id="2af22-128">Describe cómo trabajar con índices.</span><span class="sxs-lookup"><span data-stu-id="2af22-128">Describes how to work with indexes.</span></span>                                                                               |
| [<span data-ttu-id="2af22-129">Trabajar con perfiles</span><span class="sxs-lookup"><span data-stu-id="2af22-129">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="2af22-130">Describe cómo utilizar, editar y crear perfiles.</span><span class="sxs-lookup"><span data-stu-id="2af22-130">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="2af22-131">Usar comandos de script</span><span class="sxs-lookup"><span data-stu-id="2af22-131">Using Script Commands</span></span>](using-script-commands.md)                                 | <span data-ttu-id="2af22-132">Describe cómo usar comandos de script en los archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2af22-132">Describes how to use script commands in your ASF files.</span></span>                                                           |
| [<span data-ttu-id="2af22-133">Copiar datos de un archivo a otro</span><span class="sxs-lookup"><span data-stu-id="2af22-133">Copying Data from One File to Another</span></span>](copying-data-from-one-file-to-another.md) | <span data-ttu-id="2af22-134">Describe cómo copiar datos de un archivo ASF a otro, sin descodificar y codificar.</span><span class="sxs-lookup"><span data-stu-id="2af22-134">Describes how to copy data from one ASF file to another, with without decoding and encoding.</span></span>                      |
| [<span data-ttu-id="2af22-135">Habilitar la compatibilidad con DRM</span><span class="sxs-lookup"><span data-stu-id="2af22-135">Enabling DRM Support</span></span>](enabling-drm-support.md)                                   | <span data-ttu-id="2af22-136">Describe cómo habilitar la compatibilidad para la reproducción de archivos ASF protegidos con DRM.</span><span class="sxs-lookup"><span data-stu-id="2af22-136">Describes how to enable support for playback of DRM-protected ASF files.</span></span>                                          |
| [<span data-ttu-id="2af22-137">Implementación de la funcionalidad de red</span><span class="sxs-lookup"><span data-stu-id="2af22-137">Implementing Network Functionality</span></span>](implementing-network-functionality.md)       | <span data-ttu-id="2af22-138">Describe el uso de este SDK para realizar las operaciones de red que son esenciales para los medios de streaming correctos.</span><span class="sxs-lookup"><span data-stu-id="2af22-138">Describes the use of this SDK to perform the network operations that are essential to successful streaming media.</span></span> |
| [<span data-ttu-id="2af22-139">Temas avanzados</span><span class="sxs-lookup"><span data-stu-id="2af22-139">Advanced Topics</span></span>](advanced-topics.md)                                             | <span data-ttu-id="2af22-140">Describe cómo usar algunas de las características avanzadas de este SDK en sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2af22-140">Describes how to use some of the advanced features of this SDK in your applications.</span></span>                              |
| [<span data-ttu-id="2af22-141">DirectShow y Windows Media</span><span class="sxs-lookup"><span data-stu-id="2af22-141">DirectShow and Windows Media</span></span>](directshow-and-windows-media.md)                   | <span data-ttu-id="2af22-142">Describe cómo puede usar Microsoft DirectShow para crear y leer archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="2af22-142">Describes how you can use Microsoft DirectShow to create and read ASF files.</span></span>                                      |
| [<span data-ttu-id="2af22-143">Consideraciones del proyecto</span><span class="sxs-lookup"><span data-stu-id="2af22-143">Project Considerations</span></span>](project-considerations.md)                               | <span data-ttu-id="2af22-144">Proporciona detalles sobre cómo finalizar y distribuir las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="2af22-144">Provides details about finishing and distributing your applications.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="2af22-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2af22-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2af22-146">**Acerca del SDK de Windows Media Format**</span><span class="sxs-lookup"><span data-stu-id="2af22-146">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="2af22-147">**SDK de Windows Media Format 11**</span><span class="sxs-lookup"><span data-stu-id="2af22-147">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




