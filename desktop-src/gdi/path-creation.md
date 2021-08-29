---
description: Para crear una ruta de acceso y seleccionarla en un controlador de dominio, primero es necesario definir los puntos que la describen.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Creación de rutas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf2acfeb5c3e31f2f846bff06cf0a0d5b880fc95ed314538036632a83076b8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831555"
---
# <a name="path-creation"></a>Creación de rutas de acceso

Para crear una ruta de acceso y seleccionarla en un controlador de dominio, primero es necesario definir los puntos que la describen. Para ello, se llama a [**la función BeginPath,**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) se especifican las funciones de dibujo adecuadas y, a continuación, se llama a [**la función EndPath.**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) Esta combinación de funciones **(BeginPath,** funciones de dibujo y **EndPath)** constituyen un corchete *de ruta de acceso.* A continuación se muestra la lista de funciones de dibujo que se pueden usar.

-   [**Angle Angle (Ángulo)**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [**Elipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [**Lineto**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [**Gráfico circular**](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [**PolyBezier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [**PolyBezierTo**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [**PolyDraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [**Polígono**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [**Polilínea**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [**PolylineTo**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [**PolyPolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [**Rectángulo**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Cuando una aplicación llama a [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), el sistema selecciona la ruta de acceso asociada al controlador de dominio especificado. (Si otra ruta de acceso se había seleccionado previamente en el controlador de dominio, el sistema elimina esa ruta de acceso sin guardarla). Una vez que el sistema selecciona la ruta de acceso al controlador de dominio, una aplicación puede funcionar en la ruta de acceso de una de las maneras siguientes:

-   Dibuje el contorno de la ruta de acceso (con el lápiz actual).
-   Paint interior de la ruta de acceso (mediante el pincel actual).
-   Dibuje el contorno y rellene el interior de la ruta de acceso.
-   Modifique la ruta de acceso (convertir curvas en segmentos de línea).
-   Convierta la ruta de acceso en una ruta de acceso de recorte.
-   Convierta la ruta de acceso en una región.
-   Aplane la ruta de acceso mediante la conversión de cada curva del trazado en una serie de segmentos de línea.
-   Recupere las coordenadas de las líneas y curvas que componen un trazado.

 

 



