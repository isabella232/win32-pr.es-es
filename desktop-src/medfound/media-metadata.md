---
description: Metadatos de medios
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Metadatos de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717376"
---
# <a name="media-metadata"></a><span data-ttu-id="ceb12-103">Metadatos de medios</span><span class="sxs-lookup"><span data-stu-id="ceb12-103">Media Metadata</span></span>

<span data-ttu-id="ceb12-104">Los archivos multimedia contienen propiedades que describen el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="ceb12-104">Media files contain properties that describe the contents of the file.</span></span> <span data-ttu-id="ceb12-105">En Microsoft Media Foundation, estas propiedades se pueden categorizar de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="ceb12-105">In Microsoft Media Foundation, these properties can be categorized as follows:</span></span>

-   <span data-ttu-id="ceb12-106">Los **atributos de tipo de medio** especifican los parámetros de codificación, como el algoritmo de codificación (subtipo de medio), el tamaño del fotograma de vídeo, la velocidad de fotogramas de vídeo, la velocidad de bits de audio y la velocidad de muestra de audio.</span><span class="sxs-lookup"><span data-stu-id="ceb12-106">**Media-type attributes** specify the encoding parameters, such as the encoding algorithm (media subtype), video frame size, video frame rate, audio bit rate, and audio sample rate.</span></span> <span data-ttu-id="ceb12-107">Para obtener más información sobre los atributos de tipo de medio, consulte [tipos de medios](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="ceb12-107">For more information about media-type attributes, see [Media Types](media-types.md).</span></span>
-   <span data-ttu-id="ceb12-108">Los **metadatos** contienen información descriptiva para el contenido multimedia, como el título, el intérprete, el compositor y el género.</span><span class="sxs-lookup"><span data-stu-id="ceb12-108">**Metadata** contains descriptive information for the media content, such as title, artist, composer, and genre.</span></span> <span data-ttu-id="ceb12-109">Los metadatos también pueden describir los parámetros de codificación.</span><span class="sxs-lookup"><span data-stu-id="ceb12-109">Metadata can also describe encoding parameters.</span></span> <span data-ttu-id="ceb12-110">Puede ser más rápido acceder a esta información a través de metadatos que a través de atributos de tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="ceb12-110">It can be faster to access this information through metadata than through media-type attributes.</span></span>
-   <span data-ttu-id="ceb12-111">**Las propiedades DRM** contienen información sobre las restricciones de uso.</span><span class="sxs-lookup"><span data-stu-id="ceb12-111">**DRM properties** contain information on usage restrictions.</span></span> <span data-ttu-id="ceb12-112">Actualmente Media Foundation no admite las propiedades DRM a través de metadatos, con la excepción de la propiedad **\_ \_ IsProtected de DRM de PKEY** .</span><span class="sxs-lookup"><span data-stu-id="ceb12-112">Currently Media Foundation does not support DRM properties through metadata, with the exception of the **PKEY\_DRM\_IsProtected** property.</span></span>

<span data-ttu-id="ceb12-113">Hay dos maneras de leer los metadatos en Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="ceb12-113">There are two ways to read metadata in Media Foundation:</span></span>

-   <span data-ttu-id="ceb12-114">La interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (metadatos de la versión 1 de Media Foundation).</span><span class="sxs-lookup"><span data-stu-id="ceb12-114">The [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface (Media Foundation version 1 metadata).</span></span>
-   <span data-ttu-id="ceb12-115">La interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de Shell de Windows (metadatos de Shell).</span><span class="sxs-lookup"><span data-stu-id="ceb12-115">The Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface (Shell metadata).</span></span>

<span data-ttu-id="ceb12-116">Los metadatos de Shell no solo pertenecen a los archivos multimedia sino a una gama mucho más amplia de archivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="ceb12-116">Shell metadata pertains not only to media files but to a much wider range of files on the system.</span></span>

<span data-ttu-id="ceb12-117">En la tabla siguiente se comparan las características y las limitaciones de cada API de metadatos.</span><span class="sxs-lookup"><span data-stu-id="ceb12-117">The following table compares the features and limitations of each metadata API.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ceb12-118">Metadatos de Media Foundation v1</span><span class="sxs-lookup"><span data-stu-id="ceb12-118">Media Foundation v1 Metadata</span></span></th>
<th><span data-ttu-id="ceb12-119">Metadatos de Shell</span><span class="sxs-lookup"><span data-stu-id="ceb12-119">Shell Metadata</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ceb12-120">Requiere Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="ceb12-120">Requires Windows Vista or later.</span></span></td>
<td><span data-ttu-id="ceb12-121">Requiere Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ceb12-121">Requires Windows 7.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ceb12-122">Los metadatos de Shell en general no requieren Windows 7, pero Media Foundation no admiten metadatos de Shell antes de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ceb12-122">Shell metadata in general does not require Windows 7, but Media Foundation did not support Shell metadata prior to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ceb12-123">Las propiedades no son compatibles con el sistema de propiedades de Shell.</span><span class="sxs-lookup"><span data-stu-id="ceb12-123">Properties are not compatible with Shell property system.</span></span></td>
<td><span data-ttu-id="ceb12-124">Las propiedades son compatibles con el sistema de propiedades de Shell.</span><span class="sxs-lookup"><span data-stu-id="ceb12-124">Properties are compatible with the Shell property system.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ceb12-125">Las propiedades se pueden aplicar a todo el archivo o en el nivel de flujo.</span><span class="sxs-lookup"><span data-stu-id="ceb12-125">Properties can apply to the entire file, or at the stream level.</span></span></td>
<td><span data-ttu-id="ceb12-126">Solo se admiten las propiedades de nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="ceb12-126">Only file-level properties are supported.</span></span> <span data-ttu-id="ceb12-127">No se admiten las propiedades de nivel de secuencia.</span><span class="sxs-lookup"><span data-stu-id="ceb12-127">Stream-level properties are not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ceb12-128">Las propiedades pueden tener valores en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="ceb12-128">Properties can have values in multiple languages.</span></span></td>
<td><span data-ttu-id="ceb12-129">No se admiten valores en varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="ceb12-129">Values in multiple languages are not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ceb12-130">Las claves de propiedad son cadenas de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="ceb12-130">Property keys are wide-character strings.</span></span></td>
<td><span data-ttu-id="ceb12-131">Las claves de propiedad son valores <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ceb12-131">Property keys are <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ceb12-132">Los valores de propiedad son valores de <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ceb12-132">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
<td><span data-ttu-id="ceb12-133">Los valores de propiedad son valores de <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ceb12-133">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a><span data-ttu-id="ceb12-134">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ceb12-134">In this section</span></span>



| <span data-ttu-id="ceb12-135">Tema</span><span class="sxs-lookup"><span data-stu-id="ceb12-135">Topic</span></span>                                                                                     | <span data-ttu-id="ceb12-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceb12-136">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ceb12-137">Proveedores de metadatos de Shell</span><span class="sxs-lookup"><span data-stu-id="ceb12-137">Shell Metadata Providers</span></span>](shell-metadata-providers.md)<br/>                       | <span data-ttu-id="ceb12-138">A partir de Windows 7, Media Foundation expone metadatos a través de la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="ceb12-138">Starting in Windows 7, Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span><br/> |
| [<span data-ttu-id="ceb12-139">Propiedades de metadatos para archivos multimedia</span><span class="sxs-lookup"><span data-stu-id="ceb12-139">Metadata Properties for Media Files</span></span>](metadata-properties-for-media-files.md)<br/> | <span data-ttu-id="ceb12-140">En este tema se enumeran las propiedades de metadatos más comunes para los archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="ceb12-140">This topic lists the most common metadata properties for media files.</span></span><br/>                                                           |
| [<span data-ttu-id="ceb12-141">Proveedores de metadatos en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ceb12-141">Metadata Providers in Windows Vista</span></span>](metadata-providers-in-windows-vista.md)<br/> | <span data-ttu-id="ceb12-142">En Windows Vista, Media Foundation expone metadatos a través de la interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="ceb12-142">In Windows Vista, Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span><br/>                   |



 

<span data-ttu-id="ceb12-143">Si va a implementar un origen multimedia personalizado y desea exponer metadatos de Shell, consulte [proveedores de metadatos personalizados para archivos multimedia](custom-metadata-providers-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="ceb12-143">If you are implementing a custom media source and want to expose Shell metadata, see [Custom Metadata Providers for Media Files](custom-metadata-providers-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ceb12-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ceb12-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ceb12-145">Guía de programación de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ceb12-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 
