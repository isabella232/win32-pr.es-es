---
description: El Windows Imaging Component (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imagen.
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Windows Información general sobre componentes de creación de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73eeb50935144e0781cc6282e8af48c932d5f787
ms.sourcegitcommit: e3dd89486530e3657279bee8d66d923b613703e4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2021
ms.locfileid: "129146732"
---
# <a name="windows-imaging-component-overview"></a>Windows Información general sobre componentes de creación de imágenes

El Windows Imaging Component (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imagen. WIC permite que los proveedores de software independientes (ISV) y los proveedores de hardware independientes (IHV) desarrollen sus propios códecs de imagen y obtengan la misma compatibilidad con la plataforma que los formatos de imagen estándar (por ejemplo, TIFF, JPEG, PNG, GIF, BMP y HDPhoto). Se usa un único conjunto coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de imagen, por lo que cualquier aplicación que use WIC obtiene compatibilidad automática con nuevos formatos de imagen en cuanto se instala el códec. El marco de metadatos extensible permite que las aplicaciones lean y escriban sus propios metadatos propietarios directamente en los archivos de imagen, por lo que los metadatos nunca se pierden ni se separan de la imagen.

En este tema se incluyen las secciones siguientes.

-   [Windows Características de componentes de creación de imágenes](#windows-imaging-component-features)
-   [Códecs nativos](#native-codecs)
-   [Temas relacionados](#related-topics)

## <a name="windows-imaging-component-features"></a>Windows Características de componentes de creación de imágenes

Las características principales de WIC son:

-   Permite a los desarrolladores de aplicaciones realizar operaciones de procesamiento de imágenes en cualquier formato de imagen a través de un único conjunto coherente de interfaces comunes, sin necesidad de conocimientos previos de formatos de imagen específicos.
-   Proporciona una arquitectura extensible "plug and play" para códecs de imagen, formatos de píxeles y metadatos, con detección automática en tiempo de ejecución de nuevos formatos.
-   Admite la lectura y escritura de metadatos arbitrarios en archivos de imagen, con la capacidad de conservar metadatos no reconocidos durante la edición.
-   Conserva los datos de imagen de profundidad de bits alta, hasta 32 bits por canal, en toda la canalización de procesamiento de imágenes.
-   Proporciona compatibilidad integrada con los formatos de imagen, los formatos de píxel y los esquemas de metadatos más populares.

## <a name="native-codecs"></a>Códecs nativos

WIC incluye varios códecs integrados. Los siguientes códecs estándar se proporcionan con la plataforma. 

| Códec                                                                                             | Tipos Mime                       | Decodificadores | Codificadores |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| BMP (formato Windows mapa de bits), especificación BMP v5.                                                | image/bmp                        | Sí      | Sí      |
| GIF (Formato de intercambio de gráficos 89a), especificación GIF 89a/89 m                                  | image/gif                        | Sí      | Sí      |
| ICO (formato de icono)                                                                                 | image/ico                        | Sí      | No       |
| JPEG (Grupo conjunto de expertos en fotografía), JFIF Specification 1.02                                  | image/jpeg, image/jpe, image/jpg | Sí      | Sí      |
| PNG (gráficos de red portátiles), especificación PNG 1.2                                            | image/png                        | Sí      | Sí      |
| TIFF (Tagged Image File Format), especificación TIFF 6.0                                           | image/tiff, image/tif            | Sí      | Sí      |
| Windows Media Photo, [HD Photo Specification 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | image/vnd.ms-photo               | Sí      | Sí      |
| DDS (DirectDraw Surface)                                                                          | image/vnd.ms-dds                 | Sí      | Sí      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[CÓDEC de ejemplo de AITCodec](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 
