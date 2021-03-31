---
title: Objeto de Writer
description: Objeto de Writer
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- SDK de Windows Media Format, objetos de escritor
- Advanced Systems Format (ASF), objetos Writer
- ASF (formato de sistemas avanzados), objetos de escritor
- objetos, objetos de escritura
- objetos de escritura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789238"
---
# <a name="writer-object"></a><span data-ttu-id="19023-108">Objeto de Writer</span><span class="sxs-lookup"><span data-stu-id="19023-108">Writer Object</span></span>

<span data-ttu-id="19023-109">El objeto de escritor se utiliza para escribir archivos multimedia digitales mediante la estructura de archivos de Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="19023-109">The writer object is used to write digital media files using the advanced systems format (ASF) file structure.</span></span> <span data-ttu-id="19023-110">El proceso de escritura de un archivo multimedia digital implica muchos pasos internos del escritor, que coordina la compresión, la packetización y la multiplexación.</span><span class="sxs-lookup"><span data-stu-id="19023-110">The process of writing a digital media file involves many steps internal to the writer, which coordinates compression, packetization, and multiplexing.</span></span>

<span data-ttu-id="19023-111">El objeto escritor incluye interfaces para la salida a archivos o una red, admite una interfaz de devolución de llamada y puede crear uno o más objetos de propiedades de medios de entrada.</span><span class="sxs-lookup"><span data-stu-id="19023-111">The writer object includes interfaces for output to files or a network, supports one callback interface, and can create one or more input media properties objects.</span></span>

<span data-ttu-id="19023-112">La función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)crea el objeto de escritor, que establece un puntero a una interfaz **IWMWriter** .</span><span class="sxs-lookup"><span data-stu-id="19023-112">The writer object is created by the function [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), which sets a pointer to an **IWMWriter** interface.</span></span> <span data-ttu-id="19023-113">Las demás interfaces del objeto de escritor se pueden obtener llamando al método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="19023-113">The other interfaces of the writer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="19023-114">El objeto de escritor admite las siguientes interfaces.</span><span class="sxs-lookup"><span data-stu-id="19023-114">The following interfaces are supported by the writer object.</span></span>



| <span data-ttu-id="19023-115">Interfaz</span><span class="sxs-lookup"><span data-stu-id="19023-115">Interface</span></span>                                          | <span data-ttu-id="19023-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="19023-116">Description</span></span>                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19023-117">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="19023-117">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | <span data-ttu-id="19023-118">Proporciona métodos para generar claves [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="19023-118">Provides methods to generate [*DRM*](wmformat-glossary.md) keys.</span></span>                                                                                                |
| [<span data-ttu-id="19023-119">**IWMDRMWriter2**</span><span class="sxs-lookup"><span data-stu-id="19023-119">**IWMDRMWriter2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | <span data-ttu-id="19023-120">Configura el objeto de escritor para escribir un archivo que contiene una secuencia precifrada que se ajusta al protocolo Windows Media DRM 10 para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="19023-120">Configures the writer object to write a file containing a pre-encrypted stream that conforms to the Windows Media DRM 10 for Network Devices protocol.</span></span>                                                    |
| [<span data-ttu-id="19023-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="19023-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | <span data-ttu-id="19023-122">Administra la especificación y recuperación de la información de encabezado, como metadatos, [*marcadores*](wmformat-glossary.md), etc.</span><span class="sxs-lookup"><span data-stu-id="19023-122">Manages the specification and retrieval of header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                                           |
| [<span data-ttu-id="19023-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="19023-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | <span data-ttu-id="19023-124">Administra la enumeración a través de la información de códec disponible.</span><span class="sxs-lookup"><span data-stu-id="19023-124">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="19023-125">Hereda todos los métodos de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="19023-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                            |
| [<span data-ttu-id="19023-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="19023-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | <span data-ttu-id="19023-127">Administra la enumeración a través de la información de códec disponible.</span><span class="sxs-lookup"><span data-stu-id="19023-127">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="19023-128">Hereda todos los métodos de **IWMHeaderInfo** y **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="19023-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>                                                                     |
| [<span data-ttu-id="19023-129">**IWMWatermarkInfo**</span><span class="sxs-lookup"><span data-stu-id="19023-129">**IWMWatermarkInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | <span data-ttu-id="19023-130">Proporciona acceso a información sobre los sistemas de marcas de agua presentes en el sistema.</span><span class="sxs-lookup"><span data-stu-id="19023-130">Provides access to information about watermarking systems present on the system.</span></span>                                                                                                                          |
| [<span data-ttu-id="19023-131">**IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="19023-131">**IWMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | <span data-ttu-id="19023-132">Inicia y detiene la escritura de archivos ASF; incluye métodos para asignar búferes, establecer y recuperar propiedades de entrada, establecer perfiles y nombres de archivos de salida y desbloquear el escritor.</span><span class="sxs-lookup"><span data-stu-id="19023-132">Starts and stops the writing of ASF files; it includes methods for allocating buffers, setting and retrieving input properties, setting profiles and output file names, and unlocking the writer.</span></span>         |
| [<span data-ttu-id="19023-133">**IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="19023-133">**IWMWriterAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | <span data-ttu-id="19023-134">Agrega, obtiene y quita objetos de receptor especificados; Recupera estadísticas, el número de receptores y el tiempo de reloj en el que está trabajando el escritor; y realiza otras funciones avanzadas.</span><span class="sxs-lookup"><span data-stu-id="19023-134">Adds, gets, and removes specified sink objects; retrieves statistics, number of sinks, and the clock time the writer is working to; and performs other advanced functions.</span></span>                                |
| [<span data-ttu-id="19023-135">**IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="19023-135">**IWMWriterAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | <span data-ttu-id="19023-136">Proporciona cierta funcionalidad avanzada, especialmente para controlar el vídeo desentrelazado.</span><span class="sxs-lookup"><span data-stu-id="19023-136">Provides some advanced functionality, particularly for handling deinterlaced video.</span></span> <span data-ttu-id="19023-137">Hereda todos los métodos de **IWMWriterAdvanced**.</span><span class="sxs-lookup"><span data-stu-id="19023-137">Inherits all of the methods of **IWMWriterAdvanced**.</span></span>                                                                 |
| [<span data-ttu-id="19023-138">**IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="19023-138">**IWMWriterAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | <span data-ttu-id="19023-139">Proporciona funcionalidad adicional de escritura, incluida la capacidad de obtener estadísticas detalladas del escritor.</span><span class="sxs-lookup"><span data-stu-id="19023-139">Provides additional writer functionality, including the ability to get detailed writer statistics.</span></span> <span data-ttu-id="19023-140">Hereda todos los métodos de **IWMWriterAdvanced** y **IWMWriterAdvanced2**.</span><span class="sxs-lookup"><span data-stu-id="19023-140">Inherits all of the methods of **IWMWriterAdvanced** and **IWMWriterAdvanced2**.</span></span>                       |
| [<span data-ttu-id="19023-141">**IWMWriterPostView**</span><span class="sxs-lookup"><span data-stu-id="19023-141">**IWMWriterPostView**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | <span data-ttu-id="19023-142">Administra cierta funcionalidad de escritura avanzada relacionada con los ejemplos de postview.</span><span class="sxs-lookup"><span data-stu-id="19023-142">Manages some advanced writing functionality related to postviewing samples.</span></span> <span data-ttu-id="19023-143">La vista previa está viendo la salida, normalmente desde un codificador, para comprobar que el proceso de codificación y descodificación funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="19023-143">Postviewing is viewing the output, usually from an encoder, to check that the encoding/decoding process is working correctly.</span></span> |
| [<span data-ttu-id="19023-144">**IWMWriterPreprocess**</span><span class="sxs-lookup"><span data-stu-id="19023-144">**IWMWriterPreprocess**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | <span data-ttu-id="19023-145">Administra las fases de preprocesamiento realizadas por el escritor.</span><span class="sxs-lookup"><span data-stu-id="19023-145">Manages preprocessing passes made by the writer.</span></span> <span data-ttu-id="19023-146">Los pasos de preprocesamiento se usan para mejorar la calidad de la salida codificada.</span><span class="sxs-lookup"><span data-stu-id="19023-146">Preprocessing passes are used to improve the quality of encoded output.</span></span>                                                                                  |



 

<span data-ttu-id="19023-147">La aplicación debe implementar la siguiente interfaz de devolución de llamada para realizar el seguimiento del progreso de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="19023-147">The following callback interface must be implemented by the application to track the progress of postviewing.</span></span>



| <span data-ttu-id="19023-148">Interfaz</span><span class="sxs-lookup"><span data-stu-id="19023-148">Interface</span></span>                                                      | <span data-ttu-id="19023-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="19023-149">Description</span></span>                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="19023-150">**IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="19023-150">**IWMWriterPostViewCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | <span data-ttu-id="19023-151">Administra el modo en que se reciben los ejemplos sin comprimir del objeto escritor para obtener una vista previa de lo que está haciendo el códec.</span><span class="sxs-lookup"><span data-stu-id="19023-151">Manages how uncompressed samples are received from the writer object to preview what the codec is doing.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="19023-152">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="19023-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19023-153">**de la empresa**</span><span class="sxs-lookup"><span data-stu-id="19023-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="19023-154">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="19023-154">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




