---
description: Modelo conceptual
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Modelo conceptual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278311"
---
# <a name="the-conceptual-model"></a><span data-ttu-id="20913-103">Modelo conceptual</span><span class="sxs-lookup"><span data-stu-id="20913-103">The Conceptual Model</span></span>

<span data-ttu-id="20913-104">En esta sección se describen los objetos, las propiedades y los recursos que constituyen el modelo conceptual de WPD.</span><span class="sxs-lookup"><span data-stu-id="20913-104">This section describes the objects, properties, and resources that constitute the WPD conceptual model.</span></span>

### <a name="objects"></a><span data-ttu-id="20913-105">de la empresa</span><span class="sxs-lookup"><span data-stu-id="20913-105">Objects</span></span>

<span data-ttu-id="20913-106">En WPD, las entidades lógicas en los dispositivos se conocen como objetos.</span><span class="sxs-lookup"><span data-stu-id="20913-106">In WPD, logical entities on devices are referred to as objects.</span></span> <span data-ttu-id="20913-107">Normalmente, pero no siempre, representan los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20913-107">Typically, but not always, these represent data on the device.</span></span> <span data-ttu-id="20913-108">Los objetos tienen propiedades y los identificadores de objeto hacen referencia a ellos.</span><span class="sxs-lookup"><span data-stu-id="20913-108">Objects have properties, and are referenced by object identifiers.</span></span> <span data-ttu-id="20913-109">Entre los ejemplos de objetos se incluyen imágenes y carpetas en una cámara, canciones y listas de reproducción en un reproductor de media, contactos en un teléfono móvil, etc.</span><span class="sxs-lookup"><span data-stu-id="20913-109">Examples of objects include pictures and folders on a camera, songs and playlists on a media player, contacts on a mobile phone, and so on.</span></span>

<span data-ttu-id="20913-110">Los objetos también pueden representar partes funcionales o informativas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20913-110">Objects can also represent functional or informational parts of the device.</span></span> <span data-ttu-id="20913-111">Algunos ejemplos son los controles del reproductor (reproducir/grabar/pausar), la configuración de la cámara, las capacidades de SMS de un teléfono móvil, etc.</span><span class="sxs-lookup"><span data-stu-id="20913-111">Examples of these include player controls (play/record/pause), camera settings, a mobile phone's SMS capabilities, and so on.</span></span>

<span data-ttu-id="20913-112">En los dos temas siguientes se proporcionan ejemplos e ilustraciones de dos tipos de objetos: el objeto Image y el objeto Mediacast.</span><span class="sxs-lookup"><span data-stu-id="20913-112">The two following topics give examples and illustrations of two types of objects: the Image object and the Mediacast object.</span></span>

### <a name="image-object"></a><span data-ttu-id="20913-113">Objeto Image</span><span class="sxs-lookup"><span data-stu-id="20913-113">Image Object</span></span>

<span data-ttu-id="20913-114">Un objeto Image representa una imagen fija.</span><span class="sxs-lookup"><span data-stu-id="20913-114">An image object represents a still image.</span></span> <span data-ttu-id="20913-115">En el diagrama siguiente se muestran las relaciones entre un objeto de imagen, sus propiedades y sus recursos.</span><span class="sxs-lookup"><span data-stu-id="20913-115">The following diagram shows the relationships between an Image object, its properties, and its resources.</span></span>

![diagrama que muestra un objeto WPD y su relación con sus propiedades y recursos](images/wpd-overview-figure2.gif)

<span data-ttu-id="20913-117">Para obtener más información sobre el objeto de imagen y sus propiedades, vea el tema sobre el [**\_ tipo de contenido de \_ \_ WPD**](wpd-content-type-image.md) .</span><span class="sxs-lookup"><span data-stu-id="20913-117">For more information about the Image object and its properties, see the [**WPD\_CONTENT\_TYPE\_IMAGE**](wpd-content-type-image.md) topic.</span></span>

### <a name="mediacast-object"></a><span data-ttu-id="20913-118">Objeto Mediacast</span><span class="sxs-lookup"><span data-stu-id="20913-118">Mediacast Object</span></span>

<span data-ttu-id="20913-119">Un objeto Mediacast puede considerarse como un objeto contenedor que agrupa el contenido relacionado, al igual que una lista de reproducción agrupa música.</span><span class="sxs-lookup"><span data-stu-id="20913-119">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="20913-120">A menudo, se usa un objeto Mediacast para agrupar el contenido multimedia que se publicó en línea.</span><span class="sxs-lookup"><span data-stu-id="20913-120">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="20913-121">Por ejemplo, un canal RSS se puede representar como un objeto Mediacast cuyas referencias de objeto apuntan a objetos de contenido que representan cada elemento del canal.</span><span class="sxs-lookup"><span data-stu-id="20913-121">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span> <span data-ttu-id="20913-122">En el diagrama siguiente se muestra la relación entre un objeto Mediacast y los tres objetos de audio que contiene.</span><span class="sxs-lookup"><span data-stu-id="20913-122">The following diagram shows the relationship between a Mediacast object and the three audio objects it contains.</span></span>

![diagrama que muestra la estructura jerárquica de un objeto medicast y tres objetos que contiene](images/mediacast1.gif)

<span data-ttu-id="20913-124">Las referencias al objeto de audio se especifican en la propiedad [ \_ \_ referencias de objeto WPD](object-properties.md) para el objeto Mediacast.</span><span class="sxs-lookup"><span data-stu-id="20913-124">The references to the audio object are specified in the [WPD\_OBJECT\_REFERENCES](object-properties.md) property for the Mediacast object.</span></span> <span data-ttu-id="20913-125">Para obtener más información sobre las propiedades admitidas por un objeto Mediacast, consulte el tema sobre la [**\_ conversión de contenido \_ \_ multimedia \_ del tipo de contenido de WPD**](wpd-content-type-media-cast.md) .</span><span class="sxs-lookup"><span data-stu-id="20913-125">For more information about the properties supported by a Mediacast object, see the [**WPD\_CONTENT\_TYPE\_MEDIA\_CAST**](wpd-content-type-media-cast.md) topic.</span></span>

### <a name="properties"></a><span data-ttu-id="20913-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20913-126">Properties</span></span>

<span data-ttu-id="20913-127">Las propiedades de objeto proporcionan un mecanismo para intercambiar metadatos que describen objetos.</span><span class="sxs-lookup"><span data-stu-id="20913-127">Object properties provide a mechanism for exchanging object-describing metadata.</span></span> <span data-ttu-id="20913-128">Por ejemplo, un objeto Image puede incluir propiedades que describen su nombre de archivo, tamaño, formato, ancho en píxeles, etc.</span><span class="sxs-lookup"><span data-stu-id="20913-128">For example, an image object may include properties that describe its filename, size, format, width in pixels, and so on.</span></span>

<span data-ttu-id="20913-129">Las propiedades tienen un valor actual, así como los atributos.</span><span class="sxs-lookup"><span data-stu-id="20913-129">Properties have a current value, as well as attributes.</span></span> <span data-ttu-id="20913-130">WPD define un conjunto de propiedades estándar que componen las definiciones de API y DDI.</span><span class="sxs-lookup"><span data-stu-id="20913-130">WPD defines a set of standard properties that make up the API and DDI definitions.</span></span> <span data-ttu-id="20913-131">Los proveedores no se limitan a las propiedades de WPD predefinidas y pueden agregar los suyos propios.</span><span class="sxs-lookup"><span data-stu-id="20913-131">Vendors are not limited to the predefined WPD properties and are free to add their own.</span></span>

### <a name="property-attributes"></a><span data-ttu-id="20913-132">Atributos de propiedad</span><span class="sxs-lookup"><span data-stu-id="20913-132">Property Attributes</span></span>

<span data-ttu-id="20913-133">Los atributos de propiedad describen los derechos de acceso, los valores válidos y otra información relacionada con una propiedad.</span><span class="sxs-lookup"><span data-stu-id="20913-133">Property attributes describe the access rights, valid values, and other information related to a property.</span></span> <span data-ttu-id="20913-134">Por ejemplo, la propiedad que representa la velocidad de bits puede ser un intervalo de 8 kilobits por segundo (kbps) a 20 Kbps con un valor de paso de 1 kbps.</span><span class="sxs-lookup"><span data-stu-id="20913-134">For example, the property representing bit rate could be a range from 8 kilobits per second (Kbps) to 20 Kbps with a step value of 1 Kbps.</span></span>

<span data-ttu-id="20913-135">Los derechos de acceso indican si los llamadores pueden leer, escribir o eliminar la propiedad.</span><span class="sxs-lookup"><span data-stu-id="20913-135">Access rights indicate whether callers can read, write and/or delete the property.</span></span> <span data-ttu-id="20913-136">Los valores válidos indican las restricciones de los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="20913-136">Valid values indicate restrictions for property values.</span></span> <span data-ttu-id="20913-137">Se dice que los valores válidos son de un formato específico.</span><span class="sxs-lookup"><span data-stu-id="20913-137">Valid values are said to be of a specific form.</span></span> <span data-ttu-id="20913-138">Los formatos de valor válidos incluyen el intervalo (es decir, la propiedad puede tomar un valor entre min y Max con el paso especificado), la enumeración (es decir, el valor de propiedad es uno de los de la lista especificada) y None (es decir, no hay valores válidos específicos).</span><span class="sxs-lookup"><span data-stu-id="20913-138">Valid value forms include Range (that is, property can take a value from Min to Max with specified Step), Enumeration (that is, property value is one of those in the specified List), and None (that is, there are no specific valid values).</span></span>

### <a name="resources"></a><span data-ttu-id="20913-139">Recursos</span><span class="sxs-lookup"><span data-stu-id="20913-139">Resources</span></span>

<span data-ttu-id="20913-140">Los recursos son marcadores de posición para datos binarios.</span><span class="sxs-lookup"><span data-stu-id="20913-140">Resources are placeholders for binary data.</span></span> <span data-ttu-id="20913-141">Un objeto puede tener más de un recurso.</span><span class="sxs-lookup"><span data-stu-id="20913-141">An object can have more than one resource.</span></span> <span data-ttu-id="20913-142">Por ejemplo, si el objeto representa un archivo de imagen con una anotación de audio, los recursos de este objeto podrían ser los siguientes:</span><span class="sxs-lookup"><span data-stu-id="20913-142">For example, if the object represented an image file with an audio annotation, then the resources for this object might be as follows:</span></span>

-   <span data-ttu-id="20913-143">Un recurso predeterminado.</span><span class="sxs-lookup"><span data-stu-id="20913-143">A default resource.</span></span> <span data-ttu-id="20913-144">Este recurso representa el archivo de imagen completo.</span><span class="sxs-lookup"><span data-stu-id="20913-144">This resource represents the entire image file.</span></span> <span data-ttu-id="20913-145">(Esto incluye los datos incrustados, como anotaciones de audio, miniaturas, etc.)</span><span class="sxs-lookup"><span data-stu-id="20913-145">(This includes any embedded data such as audio annotations, thumbnails, and so on)</span></span>
-   <span data-ttu-id="20913-146">Un recurso de miniatura.</span><span class="sxs-lookup"><span data-stu-id="20913-146">A thumbnail resource.</span></span> <span data-ttu-id="20913-147">Este recurso representa los datos en miniatura de la imagen.</span><span class="sxs-lookup"><span data-stu-id="20913-147">This resource represents the thumbnail data for the image.</span></span>
-   <span data-ttu-id="20913-148">Un recurso de anotación de audio.</span><span class="sxs-lookup"><span data-stu-id="20913-148">An audio annotation resource.</span></span> <span data-ttu-id="20913-149">Este recurso representa los datos de audio asociados a la imagen.</span><span class="sxs-lookup"><span data-stu-id="20913-149">This resource represents the audio data associated with the image.</span></span>

### <a name="resource-attributes"></a><span data-ttu-id="20913-150">Atributos de recursos</span><span class="sxs-lookup"><span data-stu-id="20913-150">Resource Attributes</span></span>

<span data-ttu-id="20913-151">De forma similar a los atributos de propiedad, los atributos de recursos describen los derechos de acceso, el tamaño, el formato y otra información relacionada con un recurso.</span><span class="sxs-lookup"><span data-stu-id="20913-151">Similar to property attributes, resource attributes describe the access rights, size, format, and other information related to a resource.</span></span> <span data-ttu-id="20913-152">Por ejemplo, los atributos de un recurso de anotación de audio en un objeto de imagen pueden especificar la velocidad de bits, el número de canales y el formato de datos del audio.</span><span class="sxs-lookup"><span data-stu-id="20913-152">For example, the attributes for an audio annotation resource on an image object may specify the bit rate, channel count, and data format of the audio.</span></span>

### <a name="rendering-profiles-and-resource-attributes"></a><span data-ttu-id="20913-153">Perfiles de representación y atributos de recursos</span><span class="sxs-lookup"><span data-stu-id="20913-153">Rendering Profiles and Resource Attributes</span></span>

<span data-ttu-id="20913-154">El perfil de representación es un método que las aplicaciones usan para detectar los atributos válidos para un recurso determinado.</span><span class="sxs-lookup"><span data-stu-id="20913-154">The rendering profile is one method that applications use to discover the valid attributes for a given resource.</span></span> <span data-ttu-id="20913-155">Por ejemplo, un teléfono móvil puede admitir mapas de bits con restricciones específicas en los valores de ancho y alto mínimo y máximo.</span><span class="sxs-lookup"><span data-stu-id="20913-155">For example, a mobile phone may support bitmaps with specific restrictions on the minimum and maximum width and height values.</span></span> <span data-ttu-id="20913-156">Al consultar los perfiles de representación del objeto de mapa de bits, una aplicación puede recuperar esos valores exactos.</span><span class="sxs-lookup"><span data-stu-id="20913-156">By querying the rendering profiles for the bitmap object, an application can retrieve those exact values.</span></span>

<span data-ttu-id="20913-157">La salida de ejemplo siguiente identifica la información de Perfil de representación que el dispositivo devolverá si admite mapas de bits con una altura mínima de 10 píxeles, una anchura mínima de 20 píxeles, una altura máxima de 1000 píxeles y un ancho máximo de 2000 píxeles.</span><span class="sxs-lookup"><span data-stu-id="20913-157">The following sample output identifies the rendering profile information that the device would return if it supported bitmaps with a minimum height of 10 pixels, a minimum width of 20 pixels, a maximum height of 1000 pixels and a maximum width of 2000 pixels.</span></span>


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



<span data-ttu-id="20913-158">Consulte el tema [recuperación de las capacidades de representación compatibles con un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md) en la guía de programación para obtener una descripción de cómo la aplicación puede recuperar un perfil de representación (y los atributos de recurso asociados).</span><span class="sxs-lookup"><span data-stu-id="20913-158">See the [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md) topic in the programming guide for a description of how your application can retrieve a rendering profile (and the associated resource attributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20913-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20913-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20913-160">**Información general de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="20913-160">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



