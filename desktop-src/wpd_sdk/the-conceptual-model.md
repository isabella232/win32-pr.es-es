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
# <a name="the-conceptual-model"></a>Modelo conceptual

En esta sección se describen los objetos, las propiedades y los recursos que constituyen el modelo conceptual de WPD.

### <a name="objects"></a>de la empresa

En WPD, las entidades lógicas en los dispositivos se conocen como objetos. Normalmente, pero no siempre, representan los datos del dispositivo. Los objetos tienen propiedades y los identificadores de objeto hacen referencia a ellos. Entre los ejemplos de objetos se incluyen imágenes y carpetas en una cámara, canciones y listas de reproducción en un reproductor de media, contactos en un teléfono móvil, etc.

Los objetos también pueden representar partes funcionales o informativas del dispositivo. Algunos ejemplos son los controles del reproductor (reproducir/grabar/pausar), la configuración de la cámara, las capacidades de SMS de un teléfono móvil, etc.

En los dos temas siguientes se proporcionan ejemplos e ilustraciones de dos tipos de objetos: el objeto Image y el objeto Mediacast.

### <a name="image-object"></a>Objeto Image

Un objeto Image representa una imagen fija. En el diagrama siguiente se muestran las relaciones entre un objeto de imagen, sus propiedades y sus recursos.

![diagrama que muestra un objeto WPD y su relación con sus propiedades y recursos](images/wpd-overview-figure2.gif)

Para obtener más información sobre el objeto de imagen y sus propiedades, vea el tema sobre el [**\_ tipo de contenido de \_ \_ WPD**](wpd-content-type-image.md) .

### <a name="mediacast-object"></a>Objeto Mediacast

Un objeto Mediacast puede considerarse como un objeto contenedor que agrupa el contenido relacionado, al igual que una lista de reproducción agrupa música. A menudo, se usa un objeto Mediacast para agrupar el contenido multimedia que se publicó en línea. Por ejemplo, un canal RSS se puede representar como un objeto Mediacast cuyas referencias de objeto apuntan a objetos de contenido que representan cada elemento del canal. En el diagrama siguiente se muestra la relación entre un objeto Mediacast y los tres objetos de audio que contiene.

![diagrama que muestra la estructura jerárquica de un objeto medicast y tres objetos que contiene](images/mediacast1.gif)

Las referencias al objeto de audio se especifican en la propiedad [ \_ \_ referencias de objeto WPD](object-properties.md) para el objeto Mediacast. Para obtener más información sobre las propiedades admitidas por un objeto Mediacast, consulte el tema sobre la [**\_ conversión de contenido \_ \_ multimedia \_ del tipo de contenido de WPD**](wpd-content-type-media-cast.md) .

### <a name="properties"></a>Propiedades

Las propiedades de objeto proporcionan un mecanismo para intercambiar metadatos que describen objetos. Por ejemplo, un objeto Image puede incluir propiedades que describen su nombre de archivo, tamaño, formato, ancho en píxeles, etc.

Las propiedades tienen un valor actual, así como los atributos. WPD define un conjunto de propiedades estándar que componen las definiciones de API y DDI. Los proveedores no se limitan a las propiedades de WPD predefinidas y pueden agregar los suyos propios.

### <a name="property-attributes"></a>Atributos de propiedad

Los atributos de propiedad describen los derechos de acceso, los valores válidos y otra información relacionada con una propiedad. Por ejemplo, la propiedad que representa la velocidad de bits puede ser un intervalo de 8 kilobits por segundo (kbps) a 20 Kbps con un valor de paso de 1 kbps.

Los derechos de acceso indican si los llamadores pueden leer, escribir o eliminar la propiedad. Los valores válidos indican las restricciones de los valores de propiedad. Se dice que los valores válidos son de un formato específico. Los formatos de valor válidos incluyen el intervalo (es decir, la propiedad puede tomar un valor entre min y Max con el paso especificado), la enumeración (es decir, el valor de propiedad es uno de los de la lista especificada) y None (es decir, no hay valores válidos específicos).

### <a name="resources"></a>Recursos

Los recursos son marcadores de posición para datos binarios. Un objeto puede tener más de un recurso. Por ejemplo, si el objeto representa un archivo de imagen con una anotación de audio, los recursos de este objeto podrían ser los siguientes:

-   Un recurso predeterminado. Este recurso representa el archivo de imagen completo. (Esto incluye los datos incrustados, como anotaciones de audio, miniaturas, etc.)
-   Un recurso de miniatura. Este recurso representa los datos en miniatura de la imagen.
-   Un recurso de anotación de audio. Este recurso representa los datos de audio asociados a la imagen.

### <a name="resource-attributes"></a>Atributos de recursos

De forma similar a los atributos de propiedad, los atributos de recursos describen los derechos de acceso, el tamaño, el formato y otra información relacionada con un recurso. Por ejemplo, los atributos de un recurso de anotación de audio en un objeto de imagen pueden especificar la velocidad de bits, el número de canales y el formato de datos del audio.

### <a name="rendering-profiles-and-resource-attributes"></a>Perfiles de representación y atributos de recursos

El perfil de representación es un método que las aplicaciones usan para detectar los atributos válidos para un recurso determinado. Por ejemplo, un teléfono móvil puede admitir mapas de bits con restricciones específicas en los valores de ancho y alto mínimo y máximo. Al consultar los perfiles de representación del objeto de mapa de bits, una aplicación puede recuperar esos valores exactos.

La salida de ejemplo siguiente identifica la información de Perfil de representación que el dispositivo devolverá si admite mapas de bits con una altura mínima de 10 píxeles, una anchura mínima de 20 píxeles, una altura máxima de 1000 píxeles y un ancho máximo de 2000 píxeles.


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



Consulte el tema [recuperación de las capacidades de representación compatibles con un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md) en la guía de programación para obtener una descripción de cómo la aplicación puede recuperar un perfil de representación (y los atributos de recurso asociados).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general de la aplicación**](application-overview.md)
</dt> </dl>

 

 



