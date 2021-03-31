---
title: Trabajar con receptores de escritor
description: Trabajar con receptores de escritor
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- Advanced Systems Format (ASF), receptores de escritor
- ASF (formato de sistemas avanzados), receptores de escritor
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, receptores de escritor
- receptores de escritor, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788667"
---
# <a name="working-with-writer-sinks"></a><span data-ttu-id="3821b-109">Trabajar con receptores de escritor</span><span class="sxs-lookup"><span data-stu-id="3821b-109">Working with Writer Sinks</span></span>

<span data-ttu-id="3821b-110">El objeto de escritor del SDK de Windows Media Format procesa los datos de los medios de entrada en un flujo de bits.</span><span class="sxs-lookup"><span data-stu-id="3821b-110">The writer object of the Windows Media Format SDK processes input media data into a bit stream.</span></span> <span data-ttu-id="3821b-111">Sin embargo, el objeto de escritor no entrega el flujo de bits a su destino final (ya sea a un archivo o a una ubicación de red).</span><span class="sxs-lookup"><span data-stu-id="3821b-111">However, the writer object does not deliver the bit stream to its final destination (either to a file or a network location).</span></span> <span data-ttu-id="3821b-112">Para escribir el contenido ASF en un formato utilizable, debe utilizar receptores de escritor.</span><span class="sxs-lookup"><span data-stu-id="3821b-112">To write the ASF content to a usable format, you must use writer sinks.</span></span>

<span data-ttu-id="3821b-113">El objeto de escritor admite tres tipos de receptores: receptores de archivos, receptores de red y receptores de envío.</span><span class="sxs-lookup"><span data-stu-id="3821b-113">The writer object supports three types of sinks: file sinks, network sinks, and push sinks.</span></span> <span data-ttu-id="3821b-114">Un receptor de archivos escribe el contenido ASF en un archivo ASF en disco.</span><span class="sxs-lookup"><span data-stu-id="3821b-114">A file sink writes ASF content to an ASF file on disk.</span></span> <span data-ttu-id="3821b-115">Un receptor de red difunde el contenido ASF de una dirección de red.</span><span class="sxs-lookup"><span data-stu-id="3821b-115">A network sink broadcasts ASF content from a network address.</span></span> <span data-ttu-id="3821b-116">Un receptor de inserciones envía datos a un servidor que ejecuta Windows Media Services para que el servidor pueda hacer que el contenido esté disponible para el público previsto.</span><span class="sxs-lookup"><span data-stu-id="3821b-116">A push sink delivers data to a server running Windows Media Services so that the server can make the content available to its intended audience.</span></span> <span data-ttu-id="3821b-117">También puede crear sus propios receptores para proporcionar datos ASF de la forma que necesite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3821b-117">You can also create your own sinks to deliver ASF data in whatever way is required by your application.</span></span> <span data-ttu-id="3821b-118">Para obtener información acerca de los receptores de red y los receptores de envío, consulte [envío de datos ASF a través de una red](sending-asf-data-over-a-network.md).</span><span class="sxs-lookup"><span data-stu-id="3821b-118">For information about network sinks and push sinks, see [Sending ASF Data Over a Network](sending-asf-data-over-a-network.md).</span></span> <span data-ttu-id="3821b-119">En el resto de esta sección se describen los receptores de escritor.</span><span class="sxs-lookup"><span data-stu-id="3821b-119">The remainder of this section discusses writer sinks.</span></span>

<span data-ttu-id="3821b-120">Puede configurar uno o varios receptores para cada instancia del escritor que use.</span><span class="sxs-lookup"><span data-stu-id="3821b-120">You can configure one or more sinks for each instance of the writer you use.</span></span> <span data-ttu-id="3821b-121">Cada receptor solo controla un destino.</span><span class="sxs-lookup"><span data-stu-id="3821b-121">Each sink handles only a single destination.</span></span> <span data-ttu-id="3821b-122">Por ejemplo, si desea escribir tres archivos a la vez, debe crear y configurar un receptor de archivos independiente para cada uno.</span><span class="sxs-lookup"><span data-stu-id="3821b-122">For example, if you want to write three files at once, you must create and configure a separate file sink for each.</span></span>

<span data-ttu-id="3821b-123">En las secciones siguientes se describe el uso de receptores de escritor.</span><span class="sxs-lookup"><span data-stu-id="3821b-123">The following sections describe the use of writer sinks.</span></span>



| <span data-ttu-id="3821b-124">Sección</span><span class="sxs-lookup"><span data-stu-id="3821b-124">Section</span></span>                                                                      | <span data-ttu-id="3821b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="3821b-125">Description</span></span>                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="3821b-126">Agregar receptores al escritor</span><span class="sxs-lookup"><span data-stu-id="3821b-126">Adding Sinks to the Writer</span></span>](adding-sinks-to-the-writer.md)                 | <span data-ttu-id="3821b-127">Describe cómo agregar receptores al escritor.</span><span class="sxs-lookup"><span data-stu-id="3821b-127">Describes how to add sinks to the writer.</span></span>                                        |
| [<span data-ttu-id="3821b-128">Enumerar receptores</span><span class="sxs-lookup"><span data-stu-id="3821b-128">Enumerating Sinks</span></span>](enumerating-sinks.md)                                   | <span data-ttu-id="3821b-129">Describe cómo enumerar los receptores que se han agregado al escritor.</span><span class="sxs-lookup"><span data-stu-id="3821b-129">Describes how to enumerate the sinks that have been added to the writer.</span></span>         |
| [<span data-ttu-id="3821b-130">Obtener mensajes de error de un receptor</span><span class="sxs-lookup"><span data-stu-id="3821b-130">Getting Error Messages from a Sink</span></span>](getting-error-messages-from-a-sink.md) | <span data-ttu-id="3821b-131">Describe cómo configurar receptores para proporcionar mensajes de estado a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3821b-131">Describes how to configure sinks to deliver status messages to your application.</span></span> |
| [<span data-ttu-id="3821b-132">Uso de receptores de archivos</span><span class="sxs-lookup"><span data-stu-id="3821b-132">Using File Sinks</span></span>](using-file-sinks.md)                                     | <span data-ttu-id="3821b-133">Describe cómo usar un receptor de archivos de escritor para crear un archivo ASF en disco.</span><span class="sxs-lookup"><span data-stu-id="3821b-133">Describes how to use a writer file sink to create an ASF file on disk.</span></span>           |
| [<span data-ttu-id="3821b-134">Usar receptores personalizados</span><span class="sxs-lookup"><span data-stu-id="3821b-134">Using Custom Sinks</span></span>](using-custom-sinks.md)                                 | <span data-ttu-id="3821b-135">Describe cómo crear y usar sus propios receptores personalizados para proporcionar datos ASF.</span><span class="sxs-lookup"><span data-stu-id="3821b-135">Describes how to create and use your own custom sinks to deliver ASF data.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="3821b-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3821b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3821b-137">**Interfaz IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="3821b-137">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="3821b-138">**Interfaz IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="3821b-138">**IWMWriterSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[<span data-ttu-id="3821b-139">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="3821b-139">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




