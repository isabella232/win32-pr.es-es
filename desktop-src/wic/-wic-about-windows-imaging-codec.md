---
description: El componente de creación de imágenes de Windows (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imágenes.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Información general sobre componentes de Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277202"
---
# <a name="windows-imaging-component-overview"></a>Información general sobre componentes de Windows Imaging

El componente de creación de imágenes de Windows (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imágenes. WIC permite a los fabricantes de software independientes (ISV) y a los fabricantes de hardware independientes (IHV) desarrollar sus propios códecs de imagen y obtener la misma compatibilidad con la plataforma que los formatos de imagen estándar (por ejemplo, TIFF, JPEG, PNG, GIF, BMP y HDPhoto). Se usa un único conjunto coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de la imagen, por lo que cualquier aplicación que use WIC obtiene la compatibilidad automática con los nuevos formatos de imagen en cuanto se instala el códec. El marco de metadatos extensible permite que las aplicaciones lean y escriban sus propios metadatos de propiedad directamente en archivos de imagen, por lo que los metadatos nunca se pierden ni se separan de la imagen.

En este tema se incluyen las secciones siguientes.

-   [Características de componentes de Windows Imaging](#windows-imaging-component-features)
-   [Códecs nativos](#native-codecs)
-   [Temas relacionados](#related-topics)

## <a name="windows-imaging-component-features"></a>Características de componentes de Windows Imaging

Las características principales de WIC son:

-   Permite a los desarrolladores de aplicaciones realizar operaciones de procesamiento de imágenes en cualquier formato de imagen a través de un único conjunto coherente de interfaces comunes, sin necesidad de tener conocimientos previos de formatos de imagen concretos.
-   Proporciona una arquitectura extensible "plug and Play" para códecs de imagen, formatos de píxeles y metadatos, con detección automática en tiempo de ejecución de nuevos formatos.
-   Admite la lectura y escritura de metadatos arbitrarios en archivos de imagen, con la capacidad de conservar metadatos no reconocidos durante la edición.
-   Conserva los datos de imagen de profundidad de bits alta, hasta 32 bits por canal, a lo largo de la canalización de procesamiento de imágenes.
-   Proporciona compatibilidad integrada para los formatos de imagen más conocidos, formatos de píxel y esquemas de metadatos.

## <a name="native-codecs"></a>Códecs nativos

WIC incluye varios códecs integrados. Los siguientes códecs estándar se proporcionan con la plataforma. 

| Códec                                                                                             | Tipos MIME                       | Descodificadores | Codificadores |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| BMP (formato de mapa de bits de Windows), especificación de BMP V5.                                                | image/bmp                        | Sí      | Sí      |
| GIF (formato de intercambio de gráficos 89A), especificación GIF 89A/89m                                  | image/gif                        | Sí      | Sí      |
| ICO (formato de icono)                                                                                 | imagen/ICO                        | Sí      | No       |
| JPEG (grupo de expertos fotográficos Unidos), especificación JFIF 1,02                                  | image/JPEG, Image/JPE, Image/jpg | Sí      | Sí      |
| PNG (Portable Network Graphics), especificación PNG 1,2                                            | image/png                        | Sí      | Sí      |
| TIFF (Tagged Image File Format), especificación TIFF 6,0                                           | imagen/TIFF, imagen/TIF            | Sí      | Sí      |
| Windows Media Photo, [HD Photo Specification 1,0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | Image/vnd. ms-PHOT                | Sí      | Sí      |
| DDS (superficie de DirectDraw)                                                                          | Image/vnd. ms-DDS                 | Sí      | Sí      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[CÓDEC de ejemplo AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 
