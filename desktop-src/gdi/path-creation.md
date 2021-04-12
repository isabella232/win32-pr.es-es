---
description: Para crear una ruta de acceso y seleccionarla en un controlador de dominio, primero es necesario definir los puntos que lo describen.
ms.assetid: 3691c3ab-f634-476d-a56b-1c187cb12120
title: Creación de la ruta de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caec86d5d7ca5548d021e3c959eac93633f8880c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275990"
---
# <a name="path-creation"></a>Creación de la ruta de acceso

Para crear una ruta de acceso y seleccionarla en un controlador de dominio, primero es necesario definir los puntos que lo describen. Para ello, se llama a la función [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) , se especifican las funciones de dibujo apropiadas y, a continuación, se llama a la función [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) . Esta combinación de funciones (**BeginPath**, Drawing functions y **EndPath**) constituye un *corchete de trazado*. A continuación se muestra la lista de funciones de dibujo que se pueden usar.

-   [**AngleArc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc)
-   [**Arc**](/windows/desktop/api/Wingdi/nf-wingdi-arc)
-   [**ArcTo**](/windows/desktop/api/Wingdi/nf-wingdi-arcto)
-   [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord)
-   [**CloseFigure**](/windows/desktop/api/Wingdi/nf-wingdi-closefigure)
-   [**Elipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)
-   [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto)
-   [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex)
-   [**Gráfico circular**](/windows/desktop/api/Wingdi/nf-wingdi-pie)
-   [**Polibézier**](/windows/desktop/api/Wingdi/nf-wingdi-polybezier)
-   [**Polibézierto**](/windows/desktop/api/Wingdi/nf-wingdi-polybezierto)
-   [**Polidraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw)
-   [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)
-   [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline)
-   [**Polilineto**](/windows/desktop/api/Wingdi/nf-wingdi-polylineto)
-   [**Polipolígono**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon)
-   [**Polipolyline**](/windows/desktop/api/Wingdi/nf-wingdi-polypolyline)
-   [**Rectángulo**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle)
-   [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect)
-   [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Cuando una aplicación llama a [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath), el sistema selecciona la ruta de acceso asociada al controlador de dominio especificado. (Si anteriormente se había seleccionado otra ruta de acceso en el controlador de dominio, el sistema la elimina sin guardarla). Una vez que el sistema selecciona la ruta de acceso en el controlador de dominio, una aplicación puede operar en la ruta de uno de los siguientes modos:

-   Dibuja el contorno del trazado (usando el lápiz actual).
-   Pinte el interior del trazado (usando el pincel actual).
-   Dibuje el contorno y rellene el interior del trazado.
-   Modifique la ruta de acceso (convirtiendo las curvas en segmentos de línea).
-   Convierta la ruta de acceso en una ruta de acceso de clip.
-   Convierta la ruta de acceso en una región.
-   Acople la ruta de acceso convirtiendo cada curva del trazado en una serie de segmentos de línea.
-   Recupera las coordenadas de las líneas y curvas que componen una ruta de acceso.

 

 



