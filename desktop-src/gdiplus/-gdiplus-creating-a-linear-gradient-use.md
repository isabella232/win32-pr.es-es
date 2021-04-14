---
description: GDI+ proporciona degradados lineales horizontales, verticales y diagonales. De forma predeterminada, el color de un degradado lineal cambia de forma uniforme. Sin embargo, puede personalizar un degradado lineal para que el color cambie de manera no uniforme.
ms.assetid: 9b0236b2-be6b-4918-a106-5b0e6c3dd5ff
title: Crear un degradado lineal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d66b9f5a3a07061e8b3d19140c25a9f3a33052a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104565171"
---
# <a name="creating-a-linear-gradient"></a>Crear un degradado lineal

GDI+ proporciona degradados lineales horizontales, verticales y diagonales. De forma predeterminada, el color de un degradado lineal cambia de forma uniforme. Sin embargo, puede personalizar un degradado lineal para que el color cambie de manera no uniforme.

-   [Degradados lineales horizontales](#horizontal-linear-gradients)
-   [Personalizar degradados lineales](#customizing-linear-gradients)
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



El constructor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) recibe cuatro argumentos: dos puntos y dos colores. El primer punto (0,0) está asociado al primer color (rojo) y el segundo (200, 10) se asocia al segundo color (azul). Como cabría esperar, la línea dibujada de (0,0) a (200, 10) cambia gradualmente de rojo a azul.

La decenas en los puntos (50, 10) y (200, 10) no es importante. Lo importante es que los dos puntos tienen la misma segunda coordenada; la línea que los conecta es horizontal. La elipse y el rectángulo también cambian gradualmente de rojo a azul, ya que la coordenada horizontal va de 0 a 200.

En la ilustración siguiente se muestra la línea, la elipse y el rectángulo. Tenga en cuenta que el degradado de color se repite a medida que la coordenada horizontal aumenta más allá de 200.

![Ilustración que muestra un degradado horizontal que rellena una línea y una elipse, y un rectángulo que es más largo que la elipse](images/lineargradient1.png)

## <a name="customizing-linear-gradients"></a>Personalizar degradados lineales

En el ejemplo anterior, los componentes de color cambian linealmente a medida que se desplaza de una coordenada horizontal de 0 a una coordenada horizontal de 200. Por ejemplo, un punto cuya primera coordenada sea la mitad entre 0 y 200 tendrá un componente azul que se encuentra a la mitad de la distancia entre 0 y 255.

GDI+ permite ajustar el modo en que un color varía de un borde de un degradado al otro. Supongamos que desea crear un pincel de degradado que cambie de negro a rojo según la tabla siguiente.



| Coordenada horizontal | Componentes RGB |
|-----------------------|----------------|
| 0                     | (0, 0, 0)      |
| 40                    | (128, 0, 0)    |
| 200                   | (255, 0, 0)    |



 

Tenga en cuenta que el componente rojo está a mitad de intensidad cuando la coordenada horizontal es solo el 20 por ciento del camino de 0 a 200.

En el ejemplo siguiente se llama al método [**LinearGradientBrush:: SetBlend**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-lineargradientbrush-setblend) de un objeto [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) para asociar tres intensidades relativas con tres posiciones relativas. Como en la tabla anterior, una intensidad relativa de 0,5 está asociada a una posición relativa de 0,2. El código rellena una elipse y un rectángulo con el pincel de degradado.


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



En la ilustración siguiente se muestra la elipse y el rectángulo resultantes.

![Ilustración que muestra un degradado horizontal que rellena una elipse y un rectángulo que es más largo que la elipse](images/lineargradient2.png)

## <a name="diagonal-linear-gradients"></a>Degradados lineales diagonales

Los degradados de los ejemplos anteriores han sido horizontales; es decir, el color cambia gradualmente a medida que se mueve a lo largo de cualquier línea horizontal. También puede definir degradados verticales y degradados diagonales. En el código siguiente se pasan los puntos (0,0) y (200, 100) a un constructor [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) . El color azul está asociado a (0,0) y el color verde está asociado a (200, 100). Una línea (con el ancho de lápiz 10) y una elipse se rellenan con el pincel de degradado lineal.


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



En la ilustración siguiente se muestra la línea y la elipse. Tenga en cuenta que el color de la elipse cambia gradualmente a medida que se mueve a lo largo de cualquier línea que sea paralela a la línea que se pasa a través de (0,0) y (200, 100).

![Ilustración que muestra un degradado diagonal que rellena una elipse y una línea diagonal](images/lineargradient3.png)

 

 



