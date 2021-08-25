---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. Estas funciones de API planas se encapsulan mediante la clase C++ CachedBitmap.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: Funciones CachedBitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1835cd668df90a7703a4aebdd60d37d877fe571f376d440080f5668ec3926a26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888335"
---
# <a name="cachedbitmap-functions"></a>Funciones CachedBitmap

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h. Las funciones del GDI+ API plana se encapsulan mediante una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++. Los Servicios de soporte técnico de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos contenedor, [consulte GDI+ Flat API](-gdiplus-flatapi-flat.md).

Las siguientes funciones de API planas se encapsulan mediante [**la clase C++ CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>Funciones CachedBitmap y métodos contenedor correspondientes



| Función plana                                                                                                             | Método contenedor                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap( GpBitmap \* bitmap, GpGraphics \* graphics, GpCachedBitmap \* \* cachedBitmap )   | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Crea un [**objeto CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) basado en un objeto [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y un [**objeto Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) El mapa de bits almacenado en caché toma los datos de píxeles del objeto **Bitmap** y los almacena en un formato optimizado para el dispositivo de visualización asociado al **objeto Graphics.** |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap(GpCachedBitmap \* cachedBitmap)<br/>                                      | ~CachedBitmap()                                                                                 | Limpia los recursos utilizados por un [**objeto CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap( GpGraphics \* graphics, GpCachedBitmap \* cachedBitmap, INT x, INT y )            | [**Graphics::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | El [**método Graphics::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) dibuja la imagen almacenada en un [**objeto CachedBitmap.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap)                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits( HEMFMETAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapMode, INT eFlags )<br/> | [**Metarchivo::EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Convierte un metarchivo de formato mejorado en un metarchivo Windows metarchivo (WMF) y almacena los registros convertidos en un búfer especificado.                                                                                                                                                                                                                                                                                       |



 

 

