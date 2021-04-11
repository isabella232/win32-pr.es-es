---
description: Windows GDI+ proporciona la clase Image y la clase Bitmap para almacenar imágenes en memoria y manipular imágenes en memoria.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Usar codificadores y descodificadores de imágenes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154213"
---
# <a name="using-image-encoders-and-decoders"></a>Usar codificadores y descodificadores de imágenes

Windows GDI+ proporciona la clase [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) y la clase [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para almacenar imágenes en memoria y manipular imágenes en memoria. GDI+ escribe imágenes en archivos de disco con la ayuda de codificadores de imágenes y carga imágenes de archivos de disco con la ayuda de los descodificadores de imágenes. Un codificador traduce los datos de una **imagen** o un objeto de **mapa de bits** a un formato de archivo de disco designado. Un descodificador traduce los datos de un archivo de disco al formato requerido por los objetos de **imagen** y de **mapa de bits** . GDI+ tiene codificadores y descodificadores integrados que admiten los siguientes tipos de archivo:

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

GDI+ también tiene descodificadores integrados que admiten los siguientes tipos de archivo:

-   WMF
-   EMF
-   ICON

En los temas siguientes se describen con más detalle los codificadores y descodificadores:

-   [Enumerar los codificadores instalados](-gdiplus-listing-installed-encoders-use.md)
-   [Enumerar descodificadores instalados](-gdiplus-listing-installed-decoders-use.md)
-   [Recuperar el identificador de clase para un codificador](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [Determinar los parámetros admitidos por un codificador](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [Convertir una imagen BMP en una imagen PNG](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [Establecer el nivel de compresión JPEG](-gdiplus-setting-jpeg-compression-level-use.md)
-   [Transformar una imagen JPEG sin pérdida de información](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [Creación y almacenamiento de una imagen de trama múltiple](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [Copiar fotogramas individuales de una imagen de Multiple-Frame](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



