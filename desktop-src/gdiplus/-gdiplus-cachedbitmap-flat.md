---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: 06718603-e001-49d4-ac5e-decdd98df42b
title: Funciones de CachedBitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ebb19648e38425561d1a1609c5f71368718ffb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812973"
---
# <a name="cachedbitmap-functions"></a>Funciones de CachedBitmap

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h. Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo mediante una llamada a los métodos y las funciones proporcionados por los contenedores de C++. Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).

Las siguientes funciones de la API plana están incluidas en la clase [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) de C++.

## <a name="cachedbitmap-functions-and-corresponding-wrapper-methods"></a>Funciones CachedBitmap y métodos contenedores correspondientes



| Función plana                                                                                                             | Wrapper (método)                                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateCachedBitmap ( \* mapa de bits GpBitmap, GpGraphics \* Graphics, GpCachedBitmap \* \* cachedBitmap)   | [**CachedBitmap::CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) | Crea un objeto [**CachedBitmap:: CachedBitmap**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-cachedbitmap-cachedbitmap(constcachedbitmap_)) basado en un objeto de [**mapa de bits**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) y un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . El mapa de bits almacenado en caché toma los datos de píxeles del objeto de **mapa de bits** y los almacena en un formato optimizado para el dispositivo de pantalla asociado al objeto de **gráficos** . |
| GpStatus WINGDIPAPI GdipDeleteCachedBitmap (GpCachedBitmap \* cachedBitmap)<br/>                                      | ~ CachedBitmap ()                                                                                 | Limpia los recursos usados por un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                                                                                                                |
| GpStatus WINGDIPAPI GdipDrawCachedBitmap (GpGraphics \* Graphics, GpCachedBitmap \* CACHEDBITMAP, int x, int y)            | [**Gráficos::D rawCachedBitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap)          | El método [**Graphics::D rawcachedbitmap**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcachedbitmap) dibuja la imagen almacenada en un objeto [**CachedBitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap) .                                                                                                                                                                                                                                |
| UINT WINGDIPAPI GdipEmfToWmfBits (HENHMETAFILE hemf, UINT cbData16, LPBYTE pData16, INT iMapMode, INT eFlags)<br/> | [**Metarchivo:: EmfToWmfBits**](/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-metafile-emftowmfbits)                         | Convierte un metarchivo de formato mejorado en un metarchivo de formato WMF (WMF) y almacena los registros convertidos en un búfer especificado.                                                                                                                                                                                                                                                                                       |



 

 

