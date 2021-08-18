---
description: Una curva spline cardinal es una curva que pasa sin problemas a través de un conjunto determinado de puntos.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Dibujo de splines cardinales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9124e27254fc77135d265d9bab98d2332c02d345e60add1fcd96fc68c814df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036823"
---
# <a name="drawing-cardinal-splines"></a>Dibujo de splines cardinales

Una curva spline cardinal es una curva que pasa sin problemas a través de un conjunto determinado de puntos. Para dibujar una spline cardinal, cree un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y pase la dirección de una matriz de puntos al método [**Graphics::D rawCurve.**](/previous-versions//ms536070(v=vs.85)) En el ejemplo siguiente se dibuja una curva spline cardinal en forma de campana que pasa a través de cinco puntos designados:


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



En la ilustración siguiente se muestra la curva y cinco puntos.

![ilustración de una spline cardinal que pasa a través de un conjunto de cinco puntos](images/cardinalspline1.png)

Puede usar el [**método Graphics::D rawClosedCurve**](/previous-versions//ms536143(v=vs.85)) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar una curva spline cardinal cerrada. En una curva spline cardinal cerrada, la curva continúa hasta el último punto de la matriz y se conecta con el primer punto de la matriz.

En el ejemplo siguiente se dibuja una curva spline cardinal cerrada que pasa a través de seis puntos designados.


```
Point points[] = {Point(60, 60),
   Point(150, 80),
   Point(200, 40),
   Point(180, 120),
   Point(120, 100),
   Point(80, 160)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawClosedCurve(&pen, points, 6);
```



En la ilustración siguiente se muestra la spline cerrada junto con los seis puntos:

![ilustración de una spline cardinal cerrada que pasa a través de un conjunto de seis puntos](images/cardinalspline1a.png)

Puede cambiar la forma en que una curva spline cardinal se inclina pasando un argumento de tensión al método [**Graphics::D rawCurve.**](/previous-versions//ms536070(v=vs.85)) En el ejemplo siguiente se dibujan tres splines cardinales que pasan por el mismo conjunto de puntos:


```
Point points[] = {Point(20, 50),
                  Point(100, 10),
                  Point(200, 100),
                  Point(300, 50),
                  Point(400, 80)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5, 0.0f);  // tension 0.0
graphics.DrawCurve(&pen, points, 5, 0.6f);  // tension 0.6
graphics.DrawCurve(&pen, points, 5, 1.0f);  // tension 1.0
```



En la ilustración siguiente se muestran las tres curvas spline junto con sus valores de tensión. Tenga en cuenta que cuando la tensión es 0, los puntos se conectan mediante líneas rectas.

![ilustración de tres curvas spline cardinales que pasan por el mismo conjunto de puntos, pero en diferentes momentos](images/cardinalspline2.png)

 

 
