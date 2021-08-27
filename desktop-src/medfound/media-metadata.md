---
description: Metadatos multimedia
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Metadatos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef9f8a852bbce2dfb8d38a5883acc219cde8019
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477091"
---
# <a name="media-metadata"></a>Metadatos multimedia

Los archivos multimedia contienen propiedades que describen el contenido del archivo. En Microsoft Media Foundation, estas propiedades se pueden clasificar de la siguiente manera:

-   **Los atributos de tipo multimedia** especifican los parámetros de codificación, como el algoritmo de codificación (subtipo multimedia), el tamaño del fotograma de vídeo, la velocidad de fotogramas de vídeo, la velocidad de bits de audio y la frecuencia de muestreo de audio. Para obtener más información sobre los atributos de tipo de medio, vea [Tipos de medios](media-types.md).
-   **Los** metadatos contienen información descriptiva para el contenido multimedia, como título, intérprete, compositor y género. Los metadatos también pueden describir los parámetros de codificación. Puede ser más rápido acceder a esta información a través de metadatos que a través de atributos de tipo multimedia.
-   **Las propiedades de DRM** contienen información sobre las restricciones de uso. Actualmente Media Foundation no admite propiedades DRM a través de metadatos, a excepción de la propiedad **\_ \_ IsProtected de DRM de PKEY.**

Hay dos maneras de leer metadatos en Media Foundation:

-   La [**interfaz IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (Media Foundation metadatos de la versión 1).
-   Interfaz Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) (metadatos de Shell).

Los metadatos del shell pertenecen no solo a los archivos multimedia, sino también a una gama mucho más amplia de archivos en el sistema.

En la tabla siguiente se comparan las características y limitaciones de cada API de metadatos.




| Media Foundation metadatos v1 | Metadatos del shell | 
|------------------------------|----------------|
| Requiere Windows Vista o posterior. | Requiere Windows 7.<blockquote>[!Note]<br />Los metadatos del shell en general no requieren Windows 7, pero Media Foundation los metadatos de Shell antes de Windows 7.</blockquote><br /> | 
| Las propiedades no son compatibles con el sistema de propiedades de Shell. | Las propiedades son compatibles con el sistema de propiedades de Shell. | 
| Las propiedades se pueden aplicar a todo el archivo o en el nivel de secuencia. | Solo se admiten las propiedades de nivel de archivo. No se admiten propiedades de nivel de flujo. | 
| Las propiedades pueden tener valores en varios idiomas. | No se admiten valores en varios idiomas. | 
| Las claves de propiedad son cadenas de caracteres anchos. | Las claves de propiedad <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>son valores PROPERTYKEY.</strong></a> | 
| Los valores de propiedad <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>son valores PROPVARIANT.</strong></a> | Los valores de propiedad <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>son valores PROPVARIANT.</strong></a> | 




 

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Proveedores de metadatos de Shell](shell-metadata-providers.md)<br/>                       | A partir Windows 7, Media Foundation los metadatos a través de la [**interfaz IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)<br/> |
| [Propiedades de metadatos para archivos multimedia](metadata-properties-for-media-files.md)<br/> | En este tema se enumeran las propiedades de metadatos más comunes para los archivos multimedia.<br/>                                                           |
| [Proveedores de metadatos en Windows Vista](metadata-providers-in-windows-vista.md)<br/> | En Windows Vista, Media Foundation los metadatos a través de la [**interfaz IMFMetadata.**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata)<br/>                   |



 

Si va a implementar un origen multimedia personalizado y desea exponer los metadatos del shell, vea Proveedores de metadatos [personalizados para archivos multimedia.](custom-metadata-providers-for-media-files.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation de programación](media-foundation-programming-guide.md)
</dt> </dl>

 

 
