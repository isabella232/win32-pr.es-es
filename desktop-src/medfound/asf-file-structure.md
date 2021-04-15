---
description: En este tema se describe la estructura de un archivo de formato de sistema avanzado (ASF).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Estructura de archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539657"
---
# <a name="asf-file-structure"></a><span data-ttu-id="163a4-103">Estructura de archivos ASF</span><span class="sxs-lookup"><span data-stu-id="163a4-103">ASF File Structure</span></span>

<span data-ttu-id="163a4-104">En este tema se describe la estructura de un archivo de formato de sistema avanzado (ASF).</span><span class="sxs-lookup"><span data-stu-id="163a4-104">This topic describes the structure of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="163a4-105">Para obtener información detallada acerca de los archivos ASF, descargue la [especificación ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="163a4-105">For detailed information about ASF files, download the [ASF Specification](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span> <span data-ttu-id="163a4-106">También puede usar la herramienta [Windows Media ASF Viewer 9 series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) para ver la estructura de un archivo ASF existente.</span><span class="sxs-lookup"><span data-stu-id="163a4-106">You can also use the [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) tool to see the structure of an existing ASF file.</span></span>

<span data-ttu-id="163a4-107">La unidad base de la organización para los archivos ASF se denomina *objeto*.</span><span class="sxs-lookup"><span data-stu-id="163a4-107">The base unit of organization for ASF files is called an *object*.</span></span> <span data-ttu-id="163a4-108">Un objeto de archivo ASF contiene los datos siguientes.</span><span class="sxs-lookup"><span data-stu-id="163a4-108">An ASF file object contains the following data.</span></span>



| <span data-ttu-id="163a4-109">Datos</span><span class="sxs-lookup"><span data-stu-id="163a4-109">Data</span></span>                                                        | <span data-ttu-id="163a4-110">Tamaño</span><span class="sxs-lookup"><span data-stu-id="163a4-110">Size</span></span>     |
|-------------------------------------------------------------|----------|
| <span data-ttu-id="163a4-111">GUID que identifica el objeto.</span><span class="sxs-lookup"><span data-stu-id="163a4-111">A GUID that identifies the object.</span></span>                          | <span data-ttu-id="163a4-112">128 bits</span><span class="sxs-lookup"><span data-stu-id="163a4-112">128 bits</span></span> |
| <span data-ttu-id="163a4-113">El tamaño del objeto.</span><span class="sxs-lookup"><span data-stu-id="163a4-113">The size of the object.</span></span>                                     | <span data-ttu-id="163a4-114">64 bits.</span><span class="sxs-lookup"><span data-stu-id="163a4-114">64-bits.</span></span> |
| <span data-ttu-id="163a4-115">Datos de objeto.</span><span class="sxs-lookup"><span data-stu-id="163a4-115">Object data.</span></span> <span data-ttu-id="163a4-116">Los datos del objeto pueden contener otros objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-116">The object data can contain other ASF objects.</span></span> | <span data-ttu-id="163a4-117">Varía.</span><span class="sxs-lookup"><span data-stu-id="163a4-117">Varies.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="163a4-118">Un objeto de archivo ASF es simplemente un fragmento de datos.</span><span class="sxs-lookup"><span data-stu-id="163a4-118">An ASF file object is simply a chunk of data.</span></span> <span data-ttu-id="163a4-119">No es un objeto en el sentido de la programación del equipo.</span><span class="sxs-lookup"><span data-stu-id="163a4-119">It is not an object in the computer programming sense.</span></span>

 

<span data-ttu-id="163a4-120">Un archivo ASF contiene tres tipos de objetos de archivo de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="163a4-120">An ASF file contains three types of top-level file objects.</span></span>



| <span data-ttu-id="163a4-121">ASF (objeto de archivo)</span><span class="sxs-lookup"><span data-stu-id="163a4-121">ASF File Object</span></span>                                                                                                                      | <span data-ttu-id="163a4-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="163a4-122">Description</span></span>                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="163a4-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Objeto de encabezado</span><span class="sxs-lookup"><span data-stu-id="163a4-123"><span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Header Object</span></span><br/>         | <span data-ttu-id="163a4-124">Contiene información acerca del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-124">Contains information about the ASF file.</span></span><br/>  |
| <span data-ttu-id="163a4-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Objeto de datos</span><span class="sxs-lookup"><span data-stu-id="163a4-125"><span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Data Object</span></span><br/>                     | <span data-ttu-id="163a4-126">Contiene paquetes de datos multimedia.</span><span class="sxs-lookup"><span data-stu-id="163a4-126">Contains packets of media data.</span></span><br/>           |
| <span data-ttu-id="163a4-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Objeto (s) de índice</span><span class="sxs-lookup"><span data-stu-id="163a4-127"><span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Index Object(s)</span></span><br/> | <span data-ttu-id="163a4-128">Contiene uno o más índices.</span><span class="sxs-lookup"><span data-stu-id="163a4-128">Contains one or more indexes.</span></span> <span data-ttu-id="163a4-129">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="163a4-129">(Optional.)</span></span><br/> |



 

<span data-ttu-id="163a4-130">En el diagrama siguiente se muestra la estructura de archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-130">The following diagram shows the ASF file structure.</span></span>

![diagrama que muestra la estructura de archivos ASF, incluidos los elementos del encabezado, los datos y el índice](images/asf-components04.png)

<span data-ttu-id="163a4-132">Este diagrama no se dibuja en la escala; Normalmente, el objeto de datos consta de la mayor parte del archivo.</span><span class="sxs-lookup"><span data-stu-id="163a4-132">This diagram is not drawn to scale; typically the Data Object comprises most of the file.</span></span>

### <a name="header-object"></a><span data-ttu-id="163a4-133">Objeto de encabezado</span><span class="sxs-lookup"><span data-stu-id="163a4-133">Header Object</span></span>

<span data-ttu-id="163a4-134">El objeto de encabezado es obligatorio y aparece al principio de cada archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-134">The Header Object is mandatory and appears at the beginning of every ASF file.</span></span> <span data-ttu-id="163a4-135">Contiene atributos de archivo globales e información acerca de las secuencias del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-135">It contains global file attributes and information about the streams in the ASF file.</span></span> <span data-ttu-id="163a4-136">Esta información se usa para interpretar y reproducir los datos en el archivo.</span><span class="sxs-lookup"><span data-stu-id="163a4-136">This information is used to interpret and play the data in the file.</span></span>

<span data-ttu-id="163a4-137">El objeto de encabezado contiene varios subobjetos maalmacén:</span><span class="sxs-lookup"><span data-stu-id="163a4-137">The Header Object contains several madatory sub-objects:</span></span>

-   <span data-ttu-id="163a4-138">El objeto de propiedades de archivo describe los atributos globales del archivo, como el tamaño del archivo, la duración de la reproducción, el número de paquetes de datos, el tamaño de paquete mínimo y máximo y la velocidad de bits máxima.</span><span class="sxs-lookup"><span data-stu-id="163a4-138">The File Properties Object describes global attributes of the file, such as the file size, play duration, number of data packets, minimum and maximum packet size, and maximum bit rate.</span></span>
-   <span data-ttu-id="163a4-139">El objeto de extensión de encabezado permite agregar funcionalidad adicional a un archivo ASF manteniendo la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="163a4-139">The Header Extension Object enables additional functionality to be added to an ASF file while maintaining backward compatibility.</span></span>
-   <span data-ttu-id="163a4-140">El objeto Stream Properties describe un flujo en el archivo.</span><span class="sxs-lookup"><span data-stu-id="163a4-140">The Stream Properties Object describes one stream in the file.</span></span> <span data-ttu-id="163a4-141">Un archivo ASF debe contener al menos un flujo y, por consiguiente, al menos un objeto de propiedades de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="163a4-141">An ASF file must contain at least one stream, and therefore at least one Stream Properties Object.</span></span>

<span data-ttu-id="163a4-142">El objeto de encabezado puede contener información adicional opcional, incluidos los metadatos sobre el archivo (como el título y el autor), una lista de los códecs que se usan para codificar el archivo y la información de protección del contenido.</span><span class="sxs-lookup"><span data-stu-id="163a4-142">The Header Object can contain additional optional information, including metadata about the file (such as title and author), a list of the codecs used to encode the file, and content protection information.</span></span>

### <a name="data-object"></a><span data-ttu-id="163a4-143">Objetos de datos</span><span class="sxs-lookup"><span data-stu-id="163a4-143">Data Object</span></span>

<span data-ttu-id="163a4-144">El objeto de datos ASF contiene todos los datos multimedia del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-144">The ASF Data Object contains all of the media data for the ASF file.</span></span> <span data-ttu-id="163a4-145">Este objeto es obligatorio y debe seguir el objeto de encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-145">This object is mandatory and must follow the ASF Header Object.</span></span>

<span data-ttu-id="163a4-146">El objeto de datos se divide en *paquetes* de datos.</span><span class="sxs-lookup"><span data-stu-id="163a4-146">The Data Object is divided into data *packets*.</span></span> <span data-ttu-id="163a4-147">Cada paquete contiene datos de una o varias secuencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="163a4-147">Each packet contains data for one or several streams in the file.</span></span> <span data-ttu-id="163a4-148">Un paquete de datos contiene un encabezado de paquete de datos que proporciona información de análisis de paquetes, seguida de los datos de carga de los datos multimedia digitales reales.</span><span class="sxs-lookup"><span data-stu-id="163a4-148">A data packet contains a data packet header that provides packet parsing information, followed by the payload data the actual digital media data.</span></span> <span data-ttu-id="163a4-149">Todos los paquetes de datos tienen un tiempo de presentación asociado a él y se organizan en el orden recibido.</span><span class="sxs-lookup"><span data-stu-id="163a4-149">All of the data packets have a presentation time associated with it and are arranged in the order received.</span></span>

<span data-ttu-id="163a4-150">La información sobre el contenido del objeto de datos, como el tamaño de paquete y el número de paquetes, se almacena en el objeto de encabezado.</span><span class="sxs-lookup"><span data-stu-id="163a4-150">Information about the contents of the Data Object, such as the packet size and packet count, is stored in the Header Object.</span></span>

### <a name="index-object"></a><span data-ttu-id="163a4-151">Index (objeto)</span><span class="sxs-lookup"><span data-stu-id="163a4-151">Index Object</span></span>

<span data-ttu-id="163a4-152">El objeto index es opcional y es el último objeto del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-152">The Index Object is optional and is the last object in the ASF file.</span></span> <span data-ttu-id="163a4-153">Un archivo ASF puede contener más de un objeto de índice.</span><span class="sxs-lookup"><span data-stu-id="163a4-153">An ASF file can contain more than one Index Object.</span></span> <span data-ttu-id="163a4-154">El objeto index proporciona acceso aleatorio basado en el tiempo en el objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="163a4-154">The Index Object provides time-based random access into the ASF Data Object.</span></span>

<span data-ttu-id="163a4-155">Un objeto de índice simple es otro tipo de índice.</span><span class="sxs-lookup"><span data-stu-id="163a4-155">A Simple Index Object is another type of index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="163a4-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="163a4-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="163a4-157">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="163a4-157">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




