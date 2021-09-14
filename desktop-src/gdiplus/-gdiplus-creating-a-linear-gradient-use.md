---
description: GDI+ proporciona degradados lineales horizontales, verticales y diagonales. De forma predeterminada, el color de un degradado lineal cambia uniformemente. Sin embargo, puede personalizar un degradado lineal para que el color cambie de forma no uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Crear un degradado lineal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258063"
---
# <a name="creating-a-linear-gradient"></a>Crear un degradado lineal

GDI+ proporciona degradados lineales horizontales, verticales y diagonales. De forma predeterminada, el color de un degradado lineal cambia uniformemente. Sin embargo, puede personalizar un degradado lineal para que el color cambie de forma no uniforme.

-   [Degradados lineales horizontales](#horizontal-linear-gradients)
-   [Personalización de degradados lineales](#customizing-linear-gradients)
-   [Degradados lineales diagonales](#diagonal-linear-gradients)

## <a name="horizontal-linear-gradients"></a>Degradados lineales horizontales

En el ejemplo siguiente se usa un pincel de degradado lineal horizontal para rellenar una línea, una elipse y un rectángulo:


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 255, 0, 0),   // opaque red
   Color(255, 0, 0, 255));  // opaque blue

Pen pen(&linGrBrush);

graphics.DrawLine(&pen, 0, 10, 200, 10);
graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



El constructor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) recibe cuatro argumentos: dos puntos y dos colores. El primer punto (0, 10) está asociado al primer color (rojo) y el segundo punto (200, 10) está asociado al segundo color (azul). Como se esperaría, la línea dibujada de (0, 10) a (200, 10) cambia gradualmente de rojo a azul.

Los 10 puntos (50, 10) y (200, 10) no son importantes. Lo importante es que los dos puntos tienen la misma segunda coordenada: la línea que los conecta es horizontal. Los puntos suspensivos y el rectángulo también cambian gradualmente de rojo a azul, ya que la coordenada horizontal va de 0 a 200.

En la ilustración siguiente se muestra la línea, la elipse y el rectángulo. Tenga en cuenta que el degradado de color se repite a medida que la coordenada horizontal aumenta más allá de 200.

![ilustración que muestra un degradado horizontal que rellena una línea y una elipse, y un rectángulo que es más largo que la elipse.](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a>Personalización de degradados lineales

En el ejemplo anterior, los componentes de color cambian linealmente a medida que se mueve de una coordenada horizontal de 0 a una coordenada horizontal de 200. Por ejemplo, un punto cuya primera coordenada está a medio camino entre 0 y 200 tendrá un componente azul que está a medio camino entre 0 y 255.

GDI+ permite ajustar la forma en que un color varía de un borde de un degradado al otro. Supongamos que desea crear un pincel de degradado que cambie de negro a rojo según la tabla siguiente.



| Coordenada horizontal | Componentes RGB |
|-----------------------|----------------|
| 0                     | (0, 0, 0)      |
| 40                    | (128, 0, 0)    |
| 200                   | (255, 0, 0)    |



 

Tenga en cuenta que el componente rojo tiene una intensidad media cuando la coordenada horizontal es solo el 20 por ciento del camino de 0 a 200.

En el ejemplo siguiente se llama al método [**LinearGradientBrush::SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) de un objeto [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) para asociar tres intensidades relativas a tres posiciones relativas. Como en la tabla anterior, una intensidad relativa de 0,5 está asociada a una posición relativa de 0,2. El código rellena una elipse y un rectángulo con el pincel de degradado.


```
LinearGradientBrush linGrBrush(
   Point(0, 10),
   Point(200, 10),
   Color(255, 0, 0, 0),     // opaque black 
   Color(255, 255, 0, 0));  // opaque red

REAL relativeIntensities[] = {0.0f, 0.5f, 1.0f};
REAL relativePositions[]   = {0.0f, 0.2f, 1.0f};

linGrBrush.SetBlend(relativeIntensities, relativePositions, 3);

graphics.FillEllipse(&linGrBrush, 0, 30, 200, 100);
graphics.FillRectangle(&linGrBrush, 0, 155, 500, 30);
```



En la ilustración siguiente se muestran los puntos suspensivos y el rectángulo resultantes.

![ilustración que muestra un degradado horizontal que rellena una elipse y un rectángulo que es más largo que el de la elipse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a>Degradados lineales diagonales

Los degradados de los ejemplos anteriores han sido horizontales; es decir, el color cambia gradualmente a medida que se mueve por cualquier línea horizontal. También puede definir degradados verticales y degradados diagonales. El código siguiente pasa los puntos (0, 0) y (200, 100) a un constructor [**LinearGradientBrush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) El color azul está asociado a (0, 0) y el color verde está asociado a (200, 100). Una línea (con ancho de lápiz 10) y una elipse se rellenan con el pincel de degradado lineal.


```
LinearGradientBrush linGrBrush(
   Point(0, 0),
   Point(200, 100),
   Color(255, 0, 0, 255),   // opaque blue
   Color(255, 0, 255, 0));  // opaque green

Pen pen(&linGrBrush, 10);

graphics.DrawLine(&pen, 0, 0, 600, 300);
graphics.FillEllipse(&linGrBrush, 10, 100, 200, 100);
```



En la ilustración siguiente se muestra la línea y la elipse. Tenga en cuenta que el color de los puntos suspensivos cambia gradualmente a medida que avanza por cualquier línea paralela a la línea que pasa a través de (0, 0) y (200, 100).

![ilustración que muestra un degradado diagonal que rellena una elipse y una línea diagonal](images/lineargradient3.png)

 

 



