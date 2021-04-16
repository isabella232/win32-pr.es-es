---
description: El receptor de medios ASF es el último componente de la canalización de codificación que permite que una aplicación escriba un archivo ASF.
ms.assetid: 65bb8822-5eb0-46a3-ab9e-c55ae466e982
title: Receptores de medios ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6bcd3e6b91403185342607e8c4374eb32069c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678645"
---
# <a name="asf-media-sinks"></a><span data-ttu-id="c6ff4-103">Receptores de medios ASF</span><span class="sxs-lookup"><span data-stu-id="c6ff4-103">ASF Media Sinks</span></span>

<span data-ttu-id="c6ff4-104">El receptor de medios ASF es el último componente de la canalización de codificación que permite que una aplicación escriba un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-104">The ASF media sink is the final component in the encoding pipeline that enables an application to write an ASF file.</span></span>

<span data-ttu-id="c6ff4-105">Media Foundation proporciona dos tipos de receptores de medios ASF:</span><span class="sxs-lookup"><span data-stu-id="c6ff4-105">Media Foundation provides two types of ASF media sinks:</span></span>

-   <span data-ttu-id="c6ff4-106">El *receptor de archivos ASF* se usa para archivar los datos multimedia ASF en un archivo.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-106">*ASF file sink* is used to archive ASF media data to a file.</span></span>
-   <span data-ttu-id="c6ff4-107">El *receptor de streaming ASF* se utiliza para escribir contenido ASF en una secuencia de bytes que se puede transmitir por secuencias a través de la red.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-107">*ASF streaming sink* is used to write ASF content in a byte stream that can be streamed across the network.</span></span>

<span data-ttu-id="c6ff4-108">Los receptores de medios ASF contienen uno o varios receptores de secuencias, que representan los datos que se van a escribir para cada flujo en el archivo ASF de salida.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-108">ASF media sinks contain one or more stream sinks, which represents the data to write for each stream in the output ASF file.</span></span> <span data-ttu-id="c6ff4-109">En el caso de las aplicaciones de codificación que se ejecutan en Windows Vista, debe configurar manualmente la topología de codificación creando y configurando el receptor de medios ASF y agregándolo a la topología.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-109">For encoding applications that run on Windows Vista, you must manually configure the encoding topology by creating and configuring the ASF media sink and then adding it to the topology.</span></span> <span data-ttu-id="c6ff4-110">En Windows 7, si usa los objetos de transcodificación rápida para crear la topología, no tiene que crear el receptor de medios directamente y la aplicación no llama a ningún método en el receptor de medios ni en ninguno de los receptores de flujo.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-110">In Windows 7, if you are using the fast transcode objects to create the topology, you do not have create the media sink directly and the application does not call any methods on the media sink or any of the stream sinks.</span></span> <span data-ttu-id="c6ff4-111">Los objetos de transcodificación rápida crean instancias de los receptores de medios necesarios y lo agregan a la topología antes de devolver una referencia a la aplicación del llamador.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-111">The fast transcode objects instantiate the required media sinks and add it to the topology before returning a reference to the caller application.</span></span> <span data-ttu-id="c6ff4-112">Sin embargo, en el caso de los objetos de transcodificación rápida, existen algunas restricciones que se aplican en función del tipo de codificación.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-112">However for fast transcode objects, there are some restrictions that apply depending on the type of encoding.</span></span>

-   [<span data-ttu-id="c6ff4-113">Modelo de objetos de receptor multimedia ASF</span><span class="sxs-lookup"><span data-stu-id="c6ff4-113">ASF Media Sink Object Model</span></span>](#asf-media-sink-object-model)
-   [<span data-ttu-id="c6ff4-114">Receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="c6ff4-114">ASF File Sink</span></span>](#asf-file-sink)
-   [<span data-ttu-id="c6ff4-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6ff4-115">Related topics</span></span>](#related-topics)

## <a name="asf-media-sink-object-model"></a><span data-ttu-id="c6ff4-116">Modelo de objetos de receptor multimedia ASF</span><span class="sxs-lookup"><span data-stu-id="c6ff4-116">ASF Media Sink Object Model</span></span>

<span data-ttu-id="c6ff4-117">Los receptores de medios ASF implementan la interfaz [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) y exponen las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-117">ASF media sinks implement the [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface and exposes the following interfaces.</span></span> <span data-ttu-id="c6ff4-118">Una aplicación puede obtener una referencia a estas interfaces llamando a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el receptor de medios de ASF que se usa para generar ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-118">An application can get a reference to these interfaces by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the ASF media sink it is using for generating output samples.</span></span>



| <span data-ttu-id="c6ff4-119">Interfaz</span><span class="sxs-lookup"><span data-stu-id="c6ff4-119">Interface</span></span>                                                  | <span data-ttu-id="c6ff4-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6ff4-120">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6ff4-121">**IMFMediaSink**</span><span class="sxs-lookup"><span data-stu-id="c6ff4-121">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                       | <span data-ttu-id="c6ff4-122">Se requiere para todos los receptores de medios.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-122">Required for all media sinks.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="c6ff4-123">**IMFFinalizableMediaSink**</span><span class="sxs-lookup"><span data-stu-id="c6ff4-123">**IMFFinalizableMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) | <span data-ttu-id="c6ff4-124">Implementado por el receptor de archivos ASF que escribe el contenido multimedia generado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-124">Implemented by the ASF file sink that writes the generated media content to a file.</span></span> <span data-ttu-id="c6ff4-125">Puede usar los métodos de esta interfaz para vaciar los datos y actualizar el objeto de encabezado ASF del archivo de salida final.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-125">You can use the methods on this interface to flush data and update the ASF Header Object of the final output file.</span></span> |
| [<span data-ttu-id="c6ff4-126">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="c6ff4-126">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)             | <span data-ttu-id="c6ff4-127">Recibe notificaciones de cambio de estado del reloj de presentación.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-127">Receives state-change notifications from the presentation clock.</span></span>                                                                                                                                       |
| [<span data-ttu-id="c6ff4-128">**IMFASFContentInfo**</span><span class="sxs-lookup"><span data-stu-id="c6ff4-128">**IMFASFContentInfo**</span></span>](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)             | <span data-ttu-id="c6ff4-129">El objeto ASF ContentInfo es un objeto de nivel WMContainer que almacena principalmente información del objeto de encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-129">The ASF ContentInfo object is a WMContainer level object that mainly stores ASF Header Object information.</span></span> <span data-ttu-id="c6ff4-130">Se utiliza para crear receptores de medios ASF.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-130">This is used to create ASF media sinks.</span></span>                                                     |
| [<span data-ttu-id="c6ff4-131">**IMFMetadata**</span><span class="sxs-lookup"><span data-stu-id="c6ff4-131">**IMFMetadata**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)                         | <span data-ttu-id="c6ff4-132">Se utiliza para describir los metadatos del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-132">Used to describe the metadata for the ASF file.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="c6ff4-133">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="c6ff4-133">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider)         | <span data-ttu-id="c6ff4-134">Recupera una colección de metadatos, ya sea para una presentación completa o para un flujo en la presentación.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-134">Retrieves a collection of metadata, either for an entire presentation, or for one stream in the presentation.</span></span>                                                                                          |



 

## <a name="asf-file-sink"></a><span data-ttu-id="c6ff4-135">Receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="c6ff4-135">ASF File Sink</span></span>

<span data-ttu-id="c6ff4-136">El receptor de archivos ASF es una implementación de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) proporcionada por Media Foundation que una aplicación puede usar para archivar datos multimedia ASF en un archivo.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-136">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span>

<span data-ttu-id="c6ff4-137">Debe crear, configurar y llamar a métodos en el receptor de archivos o cualquiera de sus receptores de flujo Si usa los objetos de capa de canalización para escribir un nuevo archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-137">You need to create, configure, and call methods on the file sink or any of its stream sinks if you are using the pipeline layer objects to write a new ASF file.</span></span> <span data-ttu-id="c6ff4-138">Después de configurar el receptor de archivos, puede agregarlo a la canalización de codificación.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-138">After configuring the file sink you can then add it to the encoding pipeline.</span></span>

<span data-ttu-id="c6ff4-139">Estos son los pasos generales para usar el receptor de archivos ASF:</span><span class="sxs-lookup"><span data-stu-id="c6ff4-139">Here are the general steps for using the ASF file sink:</span></span>

1.  <span data-ttu-id="c6ff4-140">Cree el receptor de archivos en proceso o fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-140">Create the file sink in-process or out-of-process.</span></span>
2.  <span data-ttu-id="c6ff4-141">Configure el receptor de archivos con todos los flujos, propiedades de codificación e información de metadatos.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-141">Configure the file sink with all the streams, encoding properties, and metadata information.</span></span>
3.  <span data-ttu-id="c6ff4-142">Asocie el receptor de archivos al nodo de la topología de salida; para ello, enumere los receptores de flujo o realice un seguimiento de los números de flujo con en el receptor.</span><span class="sxs-lookup"><span data-stu-id="c6ff4-142">Associate the file sink with the output topology node either by enumerating the stream sinks or by keeping track of the stream numbers with in the sink.</span></span>

<span data-ttu-id="c6ff4-143">Los temas siguientes contienen información detallada sobre cómo trabajar con el receptor de archivos ASF:</span><span class="sxs-lookup"><span data-stu-id="c6ff4-143">The following topics contain detailed information about working with the ASF file sink:</span></span>

-   [<span data-ttu-id="c6ff4-144">Crear el receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="c6ff4-144">Creating the ASF File Sink</span></span>](creating-the-asf-file-sink.md)
-   [<span data-ttu-id="c6ff4-145">Agregar información de secuencias al receptor de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="c6ff4-145">Adding Stream Information to the ASF File Sink</span></span>](adding-stream-information-to-the-asf-file-sink.md)
-   [<span data-ttu-id="c6ff4-146">Establecer propiedades en el receptor de archivos</span><span class="sxs-lookup"><span data-stu-id="c6ff4-146">Setting Properties in the File Sink</span></span>](setting-properties-in-the-file-sink.md)
-   [<span data-ttu-id="c6ff4-147">Agregar metadatos al receptor de archivos</span><span class="sxs-lookup"><span data-stu-id="c6ff4-147">Adding Metadata to the File Sink</span></span>](adding-metadata-to-the-file-sink.md)
-   [<span data-ttu-id="c6ff4-148">El modelo de búfer de depósito con fugas</span><span class="sxs-lookup"><span data-stu-id="c6ff4-148">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)

## <a name="related-topics"></a><span data-ttu-id="c6ff4-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6ff4-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6ff4-150">Componentes ASF de capa de canalización</span><span class="sxs-lookup"><span data-stu-id="c6ff4-150">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="c6ff4-151">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6ff4-151">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
