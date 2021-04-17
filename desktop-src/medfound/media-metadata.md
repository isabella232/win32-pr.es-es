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
# <a name="media-metadata"></a>Metadatos de medios

Los archivos multimedia contienen propiedades que describen el contenido del archivo. En Microsoft Media Foundation, estas propiedades se pueden categorizar de la manera siguiente:

-   Los **atributos de tipo de medio** especifican los parámetros de codificación, como el algoritmo de codificación (subtipo de medio), el tamaño del fotograma de vídeo, la velocidad de fotogramas de vídeo, la velocidad de bits de audio y la velocidad de muestra de audio. Para obtener más información sobre los atributos de tipo de medio, consulte [tipos de medios](media-types.md).
-   Los **metadatos** contienen información descriptiva para el contenido multimedia, como el título, el intérprete, el compositor y el género. Los metadatos también pueden describir los parámetros de codificación. Puede ser más rápido acceder a esta información a través de metadatos que a través de atributos de tipo de medio.
-   **Las propiedades DRM** contienen información sobre las restricciones de uso. Actualmente Media Foundation no admite las propiedades DRM a través de metadatos, con la excepción de la propiedad **\_ \_ IsProtected de DRM de PKEY** .

Hay dos maneras de leer los metadatos en Media Foundation:

-   La interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (metadatos de la versión 1 de Media Foundation).
-   La interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) de Shell de Windows (metadatos de Shell).

Los metadatos de Shell no solo pertenecen a los archivos multimedia sino a una gama mucho más amplia de archivos del sistema.

En la tabla siguiente se comparan las características y las limitaciones de cada API de metadatos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Metadatos de Media Foundation v1</th>
<th>Metadatos de Shell</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Requiere Windows Vista o posterior.</td>
<td>Requiere Windows 7.
<blockquote>
[!Note]<br />
Los metadatos de Shell en general no requieren Windows 7, pero Media Foundation no admiten metadatos de Shell antes de Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Las propiedades no son compatibles con el sistema de propiedades de Shell.</td>
<td>Las propiedades son compatibles con el sistema de propiedades de Shell.</td>
</tr>
<tr class="odd">
<td>Las propiedades se pueden aplicar a todo el archivo o en el nivel de flujo.</td>
<td>Solo se admiten las propiedades de nivel de archivo. No se admiten las propiedades de nivel de secuencia.</td>
</tr>
<tr class="even">
<td>Las propiedades pueden tener valores en varios idiomas.</td>
<td>No se admiten valores en varios idiomas.</td>
</tr>
<tr class="odd">
<td>Las claves de propiedad son cadenas de caracteres anchos.</td>
<td>Las claves de propiedad son valores <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> .</td>
</tr>
<tr class="even">
<td>Los valores de propiedad son valores de <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</td>
<td>Los valores de propiedad son valores de <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                     | Descripción                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Proveedores de metadatos de Shell](shell-metadata-providers.md)<br/>                       | A partir de Windows 7, Media Foundation expone metadatos a través de la interfaz [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .<br/> |
| [Propiedades de metadatos para archivos multimedia](metadata-properties-for-media-files.md)<br/> | En este tema se enumeran las propiedades de metadatos más comunes para los archivos multimedia.<br/>                                                           |
| [Proveedores de metadatos en Windows Vista](metadata-providers-in-windows-vista.md)<br/> | En Windows Vista, Media Foundation expone metadatos a través de la interfaz [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .<br/>                   |



 

Si va a implementar un origen multimedia personalizado y desea exponer metadatos de Shell, consulte [proveedores de metadatos personalizados para archivos multimedia](custom-metadata-providers-for-media-files.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
