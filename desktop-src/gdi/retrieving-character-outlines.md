---
description: Puede usar la función GetGlyphOutline para recuperar el contorno de un glifo de una fuente TrueType.
ms.assetid: 9b255dfa-3c1d-4707-927d-a2d5f4117f6a
title: Recuperar contornos de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638193632d4992dfb53f29a3dfe66a858b3e1fb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072464"
---
# <a name="retrieving-character-outlines"></a>Recuperar contornos de caracteres

Puede usar la [función GetGlyphOutline](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea) para recuperar el contorno de un glifo de una fuente TrueType. El contorno del glifo devuelto por [**la función GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) es para un glifo ajustado en cuadrícula. (Se ha modificado un glifo ajustado en cuadrícula para que su imagen de mapa de bits se ajuste lo más posible al diseño original del glifo). Si la aplicación requiere un contorno de glifo sin modificar, solicite el contorno del glifo para un carácter de una fuente cuyo tamaño es igual a las unidades em de la fuente. (Para crear una fuente con este tamaño, establezca el miembro **lfHeight** de la estructura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) en el valor negativo del valor del miembro **ntmSizeEM** de la [estructura NEWTEXTMETRIC).](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)

[**GetGlyphOutline**](/windows/win32/api/wingdi/nf-wingdi-getglyphoutlinea) devuelve el contorno como mapa de bits o como una serie de polilíneas y splines. Cuando una aplicación recupera un contorno de glifo como una serie de polilíneas y splines, la información se devuelve en una estructura [TTPOLYGONHEADER](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) seguida de tantas estructuras [TTPOLYCURVE](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) como sea necesario para describir el glifo. Todos los puntos se devuelven como [estructuras POINTFX](/windows/win32/api/wingdi/ns-wingdi-pointfx) y representan posiciones absolutas, no movimientos relativos. El punto inicial especificado por el **miembro pfxStart** de la [**estructura TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) es el punto donde comienza el contorno de un contorno. Las [**estructuras TTPOLYCURVE**](/windows/win32/api/wingdi/ns-wingdi-ttpolycurve) siguientes pueden ser registros de polilínea o registros spline.

Para representar un contorno de caracteres TrueType, debe usar los registros de polilínea y spline. El sistema puede representar fácilmente polilíneas y splines. Cada registro de polilínea y spline contiene tantos puntos secuenciales como sea posible, para minimizar el número de registros devueltos.

El punto inicial especificado en la [**estructura TTPOLYGONHEADER**](/windows/win32/api/wingdi/ns-wingdi-ttpolygonheader) siempre está en el contorno del glifo. El punto especificado actúa como punto inicial y final para el contorno.

En esta sección se proporciona información sobre los temas siguientes.

-   [Registros de polilínea](polyline-records.md)
-   [Registros spline](spline-records.md)

 

 
