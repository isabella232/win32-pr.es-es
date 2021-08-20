---
description: Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones. Estas funciones de API planas se encapsulan mediante la clase AdjustableArrowCap de C++.
ms.assetid: 809d8b1e-ccdd-4156-b650-1bb7443a59fa
title: Funciones AdjustableArrowCap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52487252c5b684cc762248b35c0fe5f45e8e3759993ba3b99ab01343b84c412d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977835"
---
# <a name="adjustablearrowcap-functions"></a>Funciones AdjustableArrowCap

Windows GDI+ expone una API plana que consta de aproximadamente 600 funciones, que se implementan en Gdiplus.dll y se declaran en Gdiplusflat.h. Las funciones del GDI+ API plana se encapsulan mediante una colección de aproximadamente 40 clases de C++. Se recomienda no llamar directamente a las funciones de la API plana. Siempre que realice llamadas a GDI+, debe hacerlo llamando a los métodos y funciones proporcionados por los contenedores de C++. Los Servicios de soporte técnico del producto de Microsoft no proporcionarán compatibilidad con el código que llama directamente a la API plana. Para obtener más información sobre el uso de estos métodos de contenedor, [consulte GDI+ Flat API](-gdiplus-flatapi-flat.md).

La clase [**AdjustableArrowCap**](/windows/desktop/api/gdipluslinecaps/nl-gdipluslinecaps-adjustablearrowcap) de C++ encapsula las siguientes funciones de API planas.

## <a name="adjustablearrowcap-functions-and-corresponding-wrapper-methods"></a>Funciones AdjustableArrowCap y métodos contenedor correspondientes



| Función plana                                                                                                          | Método de contenedor                                                                                                                | Descripción                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GpStatus WINGDIPAPI GdipCreateAdjustableArrowCap(alto REAL, ancho REAL, bool isFilled, extremo GpAdjustableArrowCap) \* \* | [**AdjustableArrowCap::AdjustableArrowCap**](/windows/win32/api/gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-adjustablearrowcap(inreal_inreal_inbool)) | Crea un extremo de línea de flecha ajustable con el alto y el ancho especificados. El extremo de la línea de flecha se puede rellenar o no rellenar. El valor predeterminado del conjunto intermedio es cero.                                                                              |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapHeight(GpAdjustableArrowCap \* cap, REAL height)                           | [**AdjustableArrowCap::SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight)                                  | El [**método AdjustableArrowCap::SetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setheight) establece el alto del extremo de flecha. Esta es la distancia desde la base de la flecha hasta su vértice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapHeight(GpAdjustableArrowCap \* cap, ALTURA \* REAL)                         | [**AdjustableArrowCap::GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight)                                         | El [**método AdjustableArrowCap::GetHeight**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getheight) obtiene el alto del extremo de flecha. El alto es la distancia desde la base de la flecha hasta su vértice.                                  |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapWidth(GpAdjustableArrowCap \* cap, ancho REAL)                             | [**AdjustableArrowCap::SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth)                                     | El [**método AdjustableArrowCap::SetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setwidth) establece el ancho del extremo de flecha. El ancho es la distancia entre los puntos de conexión de la base de la flecha.                          |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapWidth(GpAdjustableArrowCap \* cap, ancho \* REAL)                           | [**AdjustableArrowCap::GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth)                                           | El [**método AdjustableArrowCap::GetWidth**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getwidth) obtiene el ancho del extremo de flecha. El ancho es la distancia entre los puntos de conexión de la base de la flecha.                                |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapMiddleInset(GpAdjustableArrowCap \* cap, REAL middleInset)                 | [**AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset)                   | El [**método AdjustableArrowCap::SetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setmiddleinset) establece el número de unidades que el punto medio de la base desplaza hacia el vértice.                                 |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapMiddleInset(GpAdjustableArrowCap \* cap, REAL \* middleInset)<br/>    | [**AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset)                               | El [**método AdjustableArrowCap::GetMiddleInset**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-getmiddleinset) obtiene el valor del conjunto. El conjunto intermedio es el número de unidades que el punto medio de la base se desplaza hacia el vértice. |
| GpStatus WINGDIPAPI GdipSetAdjustableArrowCapFillState(GpAdjustableArrowCap \* cap, BOOL fillState)<br/>          | [**AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate)                          | El [**método AdjustableArrowCap::SetFillState**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-setfillstate) establece el estado de relleno del extremo de flecha. Si no se rellena el extremo de la flecha, solo se dibuja el contorno.                         |
| GpStatus WINGDIPAPI GdipGetAdjustableArrowCapFillState(GpAdjustableArrowCap \* cap, BOOL \* fillState)<br/>        | [**AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled)                                           | El [**método AdjustableArrowCap::IsFilled**](/windows/desktop/api/Gdipluslinecaps/nf-gdipluslinecaps-adjustablearrowcap-isfilled) determina si se rellena el extremo de la flecha.                                                                                               |



 

 

