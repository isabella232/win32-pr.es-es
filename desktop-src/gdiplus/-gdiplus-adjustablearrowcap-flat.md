---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: Funciones de AdjustableArrowCap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d377b319169a2a10c864db5aec402fe633beb3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997600"
---
# <a name="adjustablearrowcap-functions"></a>Funciones de AdjustableArrowCap

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat. h. Las funciones de la API plana GDI+ se incluyen en una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo mediante una llamada a los métodos y las funciones proporcionados por los contenedores de C++. Los servicios de soporte técnico de Microsoft no proporcionarán soporte técnico para el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, consulte la [API plana de GDI+](-gdiplus-flatapi-flat.md).

Las siguientes funciones de la API plana están incluidas en la clase [**AdjustableArrowCap**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) de C++.

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>Funciones AdjustableArrowCap y métodos contenedores correspondientes



| Función plana                                                                                                          | Wrapper (método)                                                                                                                | Descripción                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap (alto REAL, ancho REAL, BOOL isFilled, \* \* Cap GpAdjustableArrowCap) | [**AdjustableArrowCap::AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Crea un extremo de línea de flecha ajustable con el alto y el ancho especificados. Se puede rellenar o no rellenar el extremo de línea de la flecha. El margen central tiene como valor predeterminado cero.                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight ( \* Cap GpAdjustableArrowCap, height real)                           | [**AdjustableArrowCap:: SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | El método [**AdjustableArrowCap:: SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) establece el alto de la punta de la flecha. Es la distancia desde la base de la flecha hasta su vértice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight ( \* Cap GpAdjustableArrowCap, \* height real)                         | [**AdjustableArrowCap:: GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | El método [**AdjustableArrowCap:: getHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) obtiene el alto de la punta de la flecha. El alto es la distancia desde la base de la flecha hasta su vértice.                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth ( \* Cap GpAdjustableArrowCap, ancho real)                             | [**AdjustableArrowCap:: SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | El método [**AdjustableArrowCap:: SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) establece el ancho de la punta de la flecha. El ancho es la distancia entre los puntos de conexión de la base de la flecha.                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth ( \* Cap GpAdjustableArrowCap, \* ancho real)                           | [**AdjustableArrowCap:: GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | El método [**AdjustableArrowCap:: GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) obtiene el ancho de la punta de la flecha. El ancho es la distancia entre los puntos de conexión de la base de la flecha.                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset ( \* Cap GpAdjustableArrowCap, real middleInset)                 | [**AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | El método [**AdjustableArrowCap:: SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) establece el número de unidades que el punto medio de la base desplaza hacia el vértice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset ( \* Cap GpAdjustableArrowCap, real \* middleInset)<br/>    | [**AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | El método [**AdjustableArrowCap:: GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) obtiene el valor del bajorrelieve. El margen central es el número de unidades que el punto medio de la base desplaza hacia el vértice. |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState ( \* Cap GpAdjustableArrowCap, bool fillState)<br/>          | [**AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | El método [**AdjustableArrowCap:: SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) establece el estado de relleno de la punta de la flecha. Si no se rellena la punta de la flecha, solo se dibuja el contorno.                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState ( \* Cap GpAdjustableArrowCap, bool \* fillState)<br/>        | [**AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | El método [**AdjustableArrowCap:: IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) determina si se rellena la punta de la flecha.                                                                                               |



 

 

