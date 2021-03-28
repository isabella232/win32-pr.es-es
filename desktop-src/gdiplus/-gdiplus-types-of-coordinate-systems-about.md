---
description: 'Windows GDI+ usa tres espacios de coordenadas: World, Page y Device.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Tipos de sistemas de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05908196662918eb93f4fa6e2b356a6989ed5a58
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104557329"
---
# <a name="types-of-coordinate-systems"></a>Tipos de sistemas de coordenadas

Windows GDI+ usa tres espacios de coordenadas: World, Page y Device. Cuando se realiza la llamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , los puntos que se pasan al método [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) (0,0) y (160, 80) se encuentran en el espacio de coordenadas del mundo. Antes de que GDI+ pueda dibujar la línea en la pantalla, las coordenadas pasan a través de una secuencia de transformaciones. Una transformación convierte coordenadas universales en coordenadas de página y otra transformación convierte las coordenadas de página en coordenadas de dispositivo.

Supongamos que desea trabajar con un sistema de coordenadas que tiene su origen en el cuerpo del área cliente en lugar de en la esquina superior izquierda. Por ejemplo, Imagine que desea que el origen sea 100 píxeles desde el borde izquierdo del área cliente y 50 píxeles desde la parte superior del área cliente. En la ilustración siguiente se muestra este tipo de sistema de coordenadas.

![captura de pantalla de una ventana que contiene ejes de coordenadas con etiqueta](images/aboutgdip05-art01.png)

Al realizar la llamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` , se obtiene la línea que se muestra en la siguiente ilustración.

![captura de pantalla de la ventana anterior, pero con una línea azul que se extiende diagonalmente desde el origen](images/aboutgdip05-art02.png)

Las coordenadas de los extremos de la línea en los tres espacios de coordenadas son las siguientes:



|        |                         |
|--------|-------------------------|
| World  | (0,0) a (160, 80)     |
| Página   | (100, 50) a (260, 130) |
| Dispositivo | (100, 50) a (260, 130) |



 

Tenga en cuenta que el espacio de coordenadas de la página tiene su origen en la esquina superior izquierda del área cliente; siempre será el caso. Tenga en cuenta también que, dado que la unidad de medida es el píxel, las coordenadas del dispositivo son las mismas que las coordenadas de la página. Si establece la unidad de medida en un valor distinto de píxeles (por ejemplo, pulgadas), las coordenadas del dispositivo serán diferentes de las coordenadas de la página.

La transformación que asigna coordenadas universales a coordenadas de página se denomina *transformación universal* y se mantiene mediante un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . En el ejemplo anterior, la transformación universal es una traducción de 100 unidades en la dirección x y 50 unidades en la dirección y. En el ejemplo siguiente se establece la transformación universal de un objeto **Graphics** y, a continuación, se usa ese objeto **Graphics** para dibujar la línea mostrada en la ilustración anterior.


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



La transformación que asigna coordenadas de página a coordenadas del dispositivo se denomina *transformación de página*. La [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona cuatro métodos para manipular e inspeccionar la transformación de página: [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics:: GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics:: SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)y [**Graphics:: GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale). La clase **Graphics** también proporciona dos métodos, [**Graphics:: GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) y [**Graphics:: GetDpiY**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy), para examinar los puntos verticales y horizontales por pulgada del dispositivo de pantalla.

Puede usar el método [**Graphics:: SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para especificar una unidad de medida. En el ejemplo siguiente se dibuja una línea de (0,0) a (2, 1) donde el punto (2, 1) tiene 2 pulgadas a la derecha y una pulgada hacia abajo desde el punto (0,0).


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> Si no especifica un ancho de lápiz al crear el lápiz, el ejemplo anterior dibujará una línea de ancho de una pulgada. Puede especificar el ancho del lápiz en el segundo argumento del constructor [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) :
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

Si damos por hecho que el dispositivo de pantalla tiene 96 puntos por pulgada en la dirección horizontal y 96 puntos por pulgada en la dirección vertical, los extremos de la línea del ejemplo anterior tienen las coordenadas siguientes en los tres espacios de coordenadas:



|        |                     |
|--------|---------------------|
| World  | (0,0) a (2, 1)    |
| Página   | (0,0) a (2, 1)    |
| Dispositivo | (0, 0, a (192, 96) |



 

Puede combinar las transformaciones de página y el mundo para lograr una gran variedad de efectos. Por ejemplo, supongamos que desea usar pulgadas como unidad de medida y desea que el origen del sistema de coordenadas sea 2 pulgadas desde el borde izquierdo del área de cliente y 1/2 de la pulgada desde la parte superior del área cliente. En el ejemplo siguiente se establecen las transformaciones mundo y página de un objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y, a continuación, se dibuja una línea de (0,0) a (2, 1).


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



En la ilustración siguiente se muestra la línea y el sistema de coordenadas.

![captura de pantalla de la ventana anterior, pero más ancha, con los ejes situados a la izquierda y etiquetados de manera diferente](images/aboutgdip05-art03.png)

Si damos por hecho que el dispositivo de pantalla tiene 96 puntos por pulgada en la dirección horizontal y 96 puntos por pulgada en la dirección vertical, los extremos de la línea del ejemplo anterior tienen las coordenadas siguientes en los tres espacios de coordenadas:



|        |                         |
|--------|-------------------------|
| World  | (0,0) a (2, 1)        |
| Página   | (2, 0,5) a (4, 1,5)    |
| Dispositivo | (192, 48) a (384, 144) |



 

 

 
