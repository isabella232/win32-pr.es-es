---
description: Modelo conceptual
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Modelo conceptual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a653d3658e0785fcc729be335fc4d648ea9bc91af676678aece0c43ce046f419
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806565"
---
# <a name="the-conceptual-model"></a>Modelo conceptual

En esta sección se describen los objetos, las propiedades y los recursos que constituyen el modelo conceptual de WPD.

### <a name="objects"></a>Objetos

En WPD, las entidades lógicas de los dispositivos se conocen como objetos . Normalmente, pero no siempre, representan datos en el dispositivo. Los objetos tienen propiedades y los identificadores de objeto hacen referencia a ellos. Entre los ejemplos de objetos se incluyen imágenes y carpetas en una cámara, canciones y listas de reproducción en un reproductor multimedia, contactos en un teléfono móvil, entre otros.

Los objetos también pueden representar partes funcionales o informativos del dispositivo. Algunos ejemplos de estos son los controles de reproductor (reproducir, grabar y pausar), la configuración de la cámara, las funcionalidades de SMS de un teléfono móvil, entre otros.

En los dos temas siguientes se proporcionan ejemplos e ilustraciones de dos tipos de objetos: el objeto Image y el objeto Mediacast.

### <a name="image-object"></a>Objeto Image

Un objeto de imagen representa una imagen fija. En el diagrama siguiente se muestran las relaciones entre un objeto Image, sus propiedades y sus recursos.

![diagrama que muestra un objeto wpd y su relación con sus propiedades y recursos](images/wpd-overview-figure2.gif)

Para obtener más información sobre el objeto Image y sus propiedades, vea el tema [**\_ WPD CONTENT \_ TYPE \_ IMAGE.**](wpd-content-type-image.md)

### <a name="mediacast-object"></a>Objeto Mediacast

Un objeto Mediacast se puede pensar en como un objeto contenedor que agrupa contenido relacionado, igual que una lista de reproducción que agrupa música. A menudo, un objeto Mediacast se usa para agrupar el contenido multimedia que se publicó en línea. Por ejemplo, un canal RSS se puede representar como un objeto Mediacast cuyas referencias de objeto apuntan a objetos de contenido que representan cada elemento del canal. En el diagrama siguiente se muestra la relación entre un objeto Mediacast y los tres objetos de audio que contiene.

![diagrama que muestra la estructura jerárquica de un objeto medicast y tres objetos que contiene](images/mediacast1.gif)

Las referencias al objeto de audio se especifican en la [propiedad WPD \_ OBJECT \_ REFERENCES](object-properties.md) para el objeto Mediacast. Para obtener más información sobre las propiedades admitidas por un objeto Mediacast, vea el tema [**WPD \_ CONTENT TYPE \_ MEDIA \_ \_ CAST.**](wpd-content-type-media-cast.md)

### <a name="properties"></a>Propiedades

Las propiedades de objeto proporcionan un mecanismo para intercambiar metadatos que describen objetos. Por ejemplo, un objeto de imagen puede incluir propiedades que describen su nombre de archivo, tamaño, formato, ancho en píxeles, y así sucesivamente.

Las propiedades tienen un valor actual, así como atributos. WPD define un conjunto de propiedades estándar que integran las definiciones de API y DDI. Los proveedores no se limitan a las propiedades de WPD predefinidas y pueden agregar sus propias propiedades.

### <a name="property-attributes"></a>Atributos de propiedad

Los atributos de propiedad describen los derechos de acceso, los valores válidos y otra información relacionada con una propiedad. Por ejemplo, la propiedad que representa la velocidad de bits podría oscilar entre 8 kilobits por segundo (Kbps) y 20 Kbps con un valor de paso de 1 Kbps.

Los derechos de acceso indican si los autores de la llamada pueden leer, escribir o eliminar la propiedad. Los valores válidos indican restricciones para los valores de propiedad. Se dice que los valores válidos son de un formato específico. Los formularios de valor válidos incluyen Range (es decir, property puede tomar un valor de Min a Max con el paso especificado), Enumeration (es decir, property value es uno de los de la lista especificada) y None (es decir, no hay valores válidos específicos).

### <a name="resources"></a>Recursos

Los recursos son marcadores de posición para los datos binarios. Un objeto puede tener más de un recurso. Por ejemplo, si el objeto representó un archivo de imagen con una anotación de audio, los recursos de este objeto podrían ser los siguientes:

-   Un recurso predeterminado. Este recurso representa todo el archivo de imagen. (Esto incluye todos los datos incrustados, como anotaciones de audio, miniaturas, y así sucesivamente)
-   Un recurso en miniatura. Este recurso representa los datos en miniatura de la imagen.
-   Un recurso de anotación de audio. Este recurso representa los datos de audio asociados a la imagen.

### <a name="resource-attributes"></a>Atributos de recursos

De forma similar a los atributos de propiedad, los atributos de recursos describen los derechos de acceso, el tamaño, el formato y otra información relacionada con un recurso. Por ejemplo, los atributos de un recurso de anotación de audio en un objeto de imagen pueden especificar la velocidad de bits, el número de canales y el formato de datos del audio.

### <a name="rendering-profiles-and-resource-attributes"></a>Perfiles de representación y atributos de recursos

El perfil de representación es un método que las aplicaciones usan para detectar los atributos válidos para un recurso determinado. Por ejemplo, un teléfono móvil puede admitir mapas de bits con restricciones específicas en los valores de ancho y alto mínimo y máximo. Al consultar los perfiles de representación para el objeto de mapa de bits, una aplicación puede recuperar esos valores exactos.

La siguiente salida de ejemplo identifica la información del perfil de representación que el dispositivo devolvería si se admiten mapas de bits con un alto mínimo de 10 píxeles, un ancho mínimo de 20 píxeles, una altura máxima de 1000 píxeles y un ancho máximo de 2000 píxeles.


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



Consulte el [tema Recuperación](retrieving-the-rendering-capabilities-supported-by-a-device.md) de las funcionalidades de representación compatibles con un dispositivo en la guía de programación para obtener una descripción de cómo la aplicación puede recuperar un perfil de representación (y los atributos de recursos asociados).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción a la aplicación**](application-overview.md)
</dt> </dl>

 

 



