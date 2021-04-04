---
title: Receptores
description: Receptores
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- SDK de Windows Media Format, receptores
- SDK de Windows Media Format, receptores de archivo
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- Formato de sistemas avanzados (ASF), receptores de archivo
- ASF (formato de sistemas avanzados), receptores de archivo
- SDK de Windows Media Format, receptores de red
- SDK de Windows Media Format, receptores de envío
- Advanced Systems Format (ASF), receptores de red
- ASF (formato de sistemas avanzados), receptores de red
- Advanced Systems Format (ASF), receptores de envío
- ASF (formato de sistemas avanzados), receptores de inserciones
- receptores, acerca de
- receptores de archivos, acerca de
- receptores de red
- receptores de extracción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077340"
---
# <a name="sinks"></a><span data-ttu-id="1cba7-119">Receptores</span><span class="sxs-lookup"><span data-stu-id="1cba7-119">Sinks</span></span>

<span data-ttu-id="1cba7-120">El objeto escritor del SDK de Windows Media Format entrega el contenido procesado a los receptores.</span><span class="sxs-lookup"><span data-stu-id="1cba7-120">The writer object of the Windows Media Format SDK delivers processed content to sinks.</span></span> <span data-ttu-id="1cba7-121">Cada receptor es un objeto que proporciona datos.</span><span class="sxs-lookup"><span data-stu-id="1cba7-121">Each sink is an object that delivers data.</span></span> <span data-ttu-id="1cba7-122">El punto de entrega depende del tipo de receptor.</span><span class="sxs-lookup"><span data-stu-id="1cba7-122">The point of delivery depends upon the type of sink.</span></span> <span data-ttu-id="1cba7-123">Hay tres tipos de receptores: receptores de archivos, receptores de red y receptores de envío.</span><span class="sxs-lookup"><span data-stu-id="1cba7-123">There are three types of sinks: file sinks, network sinks, and push sinks.</span></span>

## <a name="file-sinks"></a><span data-ttu-id="1cba7-124">Receptores de archivo</span><span class="sxs-lookup"><span data-stu-id="1cba7-124">File Sinks</span></span>

<span data-ttu-id="1cba7-125">Los receptores de archivos escriben contenido ASF en un archivo de una unidad local o de red.</span><span class="sxs-lookup"><span data-stu-id="1cba7-125">File sinks write ASF content to a file on a local or network drive.</span></span> <span data-ttu-id="1cba7-126">Cuando se usa el objeto de escritor para escribir un archivo sin agregar explícitamente un receptor de archivos, el escritor creará uno para el usuario con el nombre que se pasa a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span><span class="sxs-lookup"><span data-stu-id="1cba7-126">When you use the writer object to write a file without explicitly adding a file sink, the writer will create one for you using the name you pass to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span></span> <span data-ttu-id="1cba7-127">Puede asignar varios receptores de archivo a un objeto de escritura para escribir el contenido en varios archivos a la vez.</span><span class="sxs-lookup"><span data-stu-id="1cba7-127">You can assign multiple file sinks to a writer object to write the content in several files at once.</span></span>

<span data-ttu-id="1cba7-128">Mediante el uso de un receptor de archivos, puede controlar muchos aspectos del archivo.</span><span class="sxs-lookup"><span data-stu-id="1cba7-128">By using a file sink, you can control many aspects of the file.</span></span> <span data-ttu-id="1cba7-129">Las siguientes características están disponibles a través de un receptor de archivos.</span><span class="sxs-lookup"><span data-stu-id="1cba7-129">The following features are available through a file sink.</span></span>

-   <span data-ttu-id="1cba7-130">Supervisión de estadísticas de archivo.</span><span class="sxs-lookup"><span data-stu-id="1cba7-130">File statistics monitoring.</span></span> <span data-ttu-id="1cba7-131">Puede supervisar el tamaño y la duración del archivo a medida que se crea.</span><span class="sxs-lookup"><span data-stu-id="1cba7-131">You can monitor the file size and duration as it is being created.</span></span>
-   <span data-ttu-id="1cba7-132">Creación parcial de archivos de contenido.</span><span class="sxs-lookup"><span data-stu-id="1cba7-132">Partial content file creation.</span></span> <span data-ttu-id="1cba7-133">Los receptores de archivos pueden configurarse para comenzar a escribir contenido en un momento específico y finalizar la escritura en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="1cba7-133">File sinks can be configured to begin writing content at a specific time and to end writing at a specific time.</span></span> <span data-ttu-id="1cba7-134">Esto le permite crear varios archivos que contienen diferentes secciones del mismo contenido en el mismo paso de escritura.</span><span class="sxs-lookup"><span data-stu-id="1cba7-134">This enables you to create multiple files containing different sections of the same content in the same writing pass.</span></span>

## <a name="network-sinks"></a><span data-ttu-id="1cba7-135">Receptores de red</span><span class="sxs-lookup"><span data-stu-id="1cba7-135">Network Sinks</span></span>

<span data-ttu-id="1cba7-136">Los receptores de red retransmiten contenido a una dirección de red.</span><span class="sxs-lookup"><span data-stu-id="1cba7-136">Network sinks broadcast content to a network address.</span></span> <span data-ttu-id="1cba7-137">La lectura de clientes puede conectarse a la dirección para recibir la difusión.</span><span class="sxs-lookup"><span data-stu-id="1cba7-137">Reading clients can connect to the address to receive the broadcast.</span></span>

## <a name="push-sinks"></a><span data-ttu-id="1cba7-138">Receptores de extracción</span><span class="sxs-lookup"><span data-stu-id="1cba7-138">Push Sinks</span></span>

<span data-ttu-id="1cba7-139">Los receptores de extracción entregan contenido del escritor a un servidor que ejecuta Windows Media Services.</span><span class="sxs-lookup"><span data-stu-id="1cba7-139">Push sinks deliver content from the writer to a server running Windows Media Services.</span></span> <span data-ttu-id="1cba7-140">Los receptores de envío se usan normalmente en escenarios en los que un equipo codifica el contenido en directo y lo entrega a uno o varios servidores para una distribución amplia.</span><span class="sxs-lookup"><span data-stu-id="1cba7-140">Push sinks are typically used in scenarios where one computer encodes live content and delivers it to one or more servers for wide distribution.</span></span> <span data-ttu-id="1cba7-141">El uso de un receptor de inserciones le permite dedicar equipos a tareas específicas, lo que ahorra ancho de banda y capacidad de procesamiento en cada servidor.</span><span class="sxs-lookup"><span data-stu-id="1cba7-141">Using a push sink enables you to dedicate computers to specific tasks, saving bandwidth and processing power on each server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1cba7-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1cba7-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1cba7-143">**Características de escritura de archivos**</span><span class="sxs-lookup"><span data-stu-id="1cba7-143">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="1cba7-144">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="1cba7-144">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




