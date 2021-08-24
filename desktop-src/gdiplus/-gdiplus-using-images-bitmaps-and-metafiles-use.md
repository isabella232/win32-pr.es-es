---
description: Obtenga información sobre el uso de imágenes, mapas de bits y metarchivos. Windows GDI+ proporciona la clase Image para trabajar con imágenes de trama (mapas de bits) e imágenes vectoriales (metarchivos).
ms.assetid: 57e3bf33-5490-4f4a-addf-356ef8f1aeed
title: Uso de imágenes, mapas de bits y metarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcb0a4d4bad09a931e62da8fe33e27638fede528ad8b29ec3b49417c7bd6e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466415"
---
# <a name="using-images-bitmaps-and-metafiles"></a>Uso de imágenes, mapas de bits y metarchivos

Windows GDI+ proporciona la [**clase Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) para trabajar con imágenes de trama (mapas de bits) e imágenes vectoriales (metarchivos). Tanto [**la clase Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) como la clase [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) heredan de la clase **Image.** La **clase Bitmap** amplía las funciones de la clase **Image** proporcionando métodos adicionales para cargar, guardar y manipular imágenes de trama. La **clase Metafile** amplía las funciones de la **clase Image** proporcionando métodos adicionales para grabar y examinar imágenes vectoriales.

En los temas siguientes se tratan [**las clases Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image), [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)y [**Metafile**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile) con más detalle:

-   [Cargar y mostrar mapas de bits](-gdiplus-loading-and-displaying-bitmaps-use.md)
-   [Carga y visualización de metarchivos](-gdiplus-loading-and-displaying-metafiles-use.md)
-   [Grabación de metarchivos](-gdiplus-recording-metafiles-use.md)
-   [Recorte y escalado de imágenes](-gdiplus-cropping-and-scaling-images-use.md)
-   [Rotación, reflexión y sesgo de imágenes](-gdiplus-rotating-reflecting-and-skewing-images-use.md)
-   [Uso del modo de interpolación para controlar la calidad de la imagen durante el escalado](-gdiplus-using-interpolation-mode-to-control-image-quality-during-scaling-use.md)
-   [Creación de imágenes en miniatura](-gdiplus-creating-thumbnail-images-use.md)
-   [Usar un mapa de bits almacenado en caché para mejorar el rendimiento](-gdiplus-using-a-cached-bitmap-to-improve-performance-use.md)
-   [Mejorar el rendimiento evitando el escalado automático](-gdiplus-improving-performance-by-avoiding-automatic-scaling-use.md)
-   [Leer y escribir metadatos](-gdiplus-reading-and-writing-metadata-use.md)

 

 



