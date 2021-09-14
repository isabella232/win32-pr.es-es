---
description: Las siguientes funciones se usan con regiones.
ms.assetid: 3a42fc7a-4c07-4540-99a7-520f99532f33
title: Funciones de región (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0f55549f978dd2868f231b9ff042f6f825459d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072462"
---
# <a name="region-functions-windows-gdi"></a>Funciones de región (Windows GDI)

Las siguientes funciones se usan con regiones.



| Función                                                       | Descripción                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)                               | Combina dos regiones y almacena el resultado en una tercera región.                                |
| [**CreateVelopticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)                 | Crea una región elíptica.                                                                |
| [**CreateVelopticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) | Crea una región elíptica.                                                                |
| [**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)                   | Crea una región poligonal.                                                                  |
| [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)           | Crea una región que consta de una serie de polígonos.                                         |
| [**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)                         | Crea una región rectangular.                                                                |
| [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)         | Crea una región rectangular.                                                                |
| [**CreateRoundRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)               | Crea una región rectangular con esquinas redondeadas.                                           |
| [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn)                                   | Comprueba las dos regiones especificadas para determinar si son idénticas.                    |
| [**ExtCreateRegion**](/windows/desktop/api/Wingdi/nf-wingdi-extcreateregion)                     | Crea una región a partir de la región y los datos de transformación especificados.                          |
| [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn)                                     | Rellena una región mediante el pincel especificado.                                                 |
| [**FrameRgn**](/windows/desktop/api/Wingdi/nf-wingdi-framergn)                                   | Dibuja un borde alrededor de la región especificada mediante el pincel especificado.                     |
| [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)                     | Recupera el modo de relleno de polígono actual.                                                     |
| [**GetRegionData**](/windows/desktop/api/Wingdi/nf-wingdi-getregiondata)                         | Rellena el búfer especificado con datos que describen una región.                                    |
| [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox)                                 | Recupera el rectángulo delimitador de la región especificada.                                    |
| [**InvertRgn**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn)                                 | Invierte los colores de la región especificada.                                                  |
| [**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)                                 | Mueve una región según los desplazamientos especificados.                                                     |
| [**PaintRgn**](/windows/desktop/api/Wingdi/nf-wingdi-paintrgn)                                   | Pinta la región especificada mediante el pincel seleccionado actualmente en el contexto del dispositivo.   |
| [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion)                               | Determina si el punto especificado está dentro de la región especificada.                       |
| [**RectInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-rectinregion)                           | Determina si alguna parte del rectángulo especificado está dentro de los límites de una región. |
| [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)                     | Establece el modo de relleno de polígono para las funciones que rellenan polígonos.                                 |
| [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)                               | Convierte una región en una región rectangular con las coordenadas especificadas.                  |



 

 

 



