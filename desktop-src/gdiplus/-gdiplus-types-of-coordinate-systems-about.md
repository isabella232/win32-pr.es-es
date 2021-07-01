---
description: 'Windows GDI+ usa tres espacios de coordenadas: mundo, página y dispositivo.'
ms.assetid: eb20f5e9-25f5-4f27-8ea5-83f6819425ed
title: Tipos de sistemas de coordenadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e259f43d4fc0d6a74021f3a6125f85652f51ac95
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120630"
---
# <a name="types-of-coordinate-systems"></a>Tipos de sistemas de coordenadas

Windows GDI+ usa tres espacios de coordenadas: mundo, página y dispositivo. Al realizar la llamada , los puntos que se pasan al método `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` [**Graphics::D rawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inconstpoint__inconstpoint_)) (0, 0) y (160, 80) están en el espacio de coordenadas mundial. Antes de que GDI+ pueda dibujar la línea en la pantalla, las coordenadas pasan a través de una secuencia de transformaciones. Una transformación convierte las coordenadas globales en coordenadas de página y otra transformación convierte las coordenadas de página en coordenadas de dispositivo.

Imagine que quiere trabajar con un sistema de coordenadas que tenga su origen en el cuerpo del área cliente en lugar de en la esquina superior izquierda. Por ejemplo, si quiere que el origen sea 100 píxeles desde el borde izquierdo del área cliente y 50 píxeles desde la parte superior del área cliente. En la ilustración siguiente se muestra este tipo de sistema de coordenadas.

![captura de pantalla de una ventana que contiene ejes de coordenadas etiquetados](images/aboutgdip05-art01.png)

Al realizar la llamada `myGraphics.DrawLine(&myPen, 0, 0, 160, 80)` a , obtiene la línea que se muestra en la ilustración siguiente.

![captura de pantalla de la ventana anterior, pero con una línea azul que se extiende diagonalmente desde el origen](images/aboutgdip05-art02.png)

Las coordenadas de los puntos de conexión de la línea en los tres espacios de coordenadas son las siguientes:



| Space       |  Coordenadas del punto de conexión                       |
|--------|-------------------------|
| World  | (0, 0) a (160, 80)     |
| Página   | (100, 50) a (260, 130) |
| Dispositivo | (100, 50) a (260, 130) |



 

Tenga en cuenta que el espacio de coordenadas de página tiene su origen en la esquina superior izquierda del área cliente; este siempre será el caso. Tenga en cuenta también que, dado que la unidad de medida es el píxel, las coordenadas del dispositivo son las mismas que las coordenadas de página. Si establece la unidad de medida en algo distinto de píxeles (por ejemplo, pulgadas), las coordenadas del dispositivo serán diferentes de las coordenadas de página.

La transformación que asigna coordenadas globales a coordenadas de página se denomina *transformación* del mundo y se mantiene mediante un [**objeto Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) En el ejemplo anterior, la transformación del mundo es una traducción de 100 unidades en la dirección x y 50 unidades en la dirección y. En el ejemplo siguiente se establece la transformación del mundo de un **objeto Graphics** y, a continuación, se usa ese objeto **Graphics** para dibujar la línea mostrada en la ilustración anterior.


```
myGraphics.TranslateTransform(100.0f, 50.0f);

myGraphics.DrawLine(&myPen, 0, 0, 160, 80);
```



La transformación que asigna coordenadas de página a coordenadas de dispositivo se denomina transformación *de página*. La [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona cuatro métodos para manipular e inspeccionar la transformación de página: [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit), [**Graphics::GetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpageunit), [**Graphics::SetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpagescale)y [**Graphics::GetPageScale**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getpagescale). La **clase Graphics** también proporciona dos métodos, [**Graphics::GetDpiX**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpix) y [**Graphics::GetDpiY,**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-getdpiy)para examinar los puntos horizontales y verticales por pulgada del dispositivo de pantalla.

Puede usar el método [**Graphics::SetPageUnit**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setpageunit) de la [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para especificar una unidad de medida. En el ejemplo siguiente se dibuja una línea de (0, 0) a (2, 1) donde el punto (2, 1) está 2 pulgadas a la derecha y 1 pulgada hacia abajo desde el punto (0, 0).


```
myGraphics.SetPageUnit(UnitInch);

myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



> [!Note]
> Si no especifica un ancho de lápiz al construir el lápiz, en el ejemplo anterior se dibujará una línea de una pulgada de ancho. Puede especificar el ancho del lápiz en el segundo argumento para el constructor [**Pen:**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen)
> <br/><br/>
> `Pen myPen(Color(255, 0, 0, 0), 1/myGraphics.GetDpiX())`.

 

Si suponemos que el dispositivo de pantalla tiene 96 puntos por pulgada en la dirección horizontal y 96 puntos por pulgada en la dirección vertical, los puntos de conexión de la línea del ejemplo anterior tienen las coordenadas siguientes en los tres espacios de coordenadas:



| Space       | Coordenadas del punto de conexión                    |
|--------|---------------------|
| World  | (0, 0) a (2, 1)    |
| Página   | (0, 0) a (2, 1)    |
| Dispositivo | (0, 0, a (192, 96) |



 

Puede combinar el mundo y las transformaciones de página para lograr diversos efectos. Por ejemplo, supongamos que quiere usar pulgadas como unidad de medida y desea que el origen del sistema de coordenadas esté a 2 pulgadas del borde izquierdo del área cliente y 1/2 pulgada desde la parte superior del área cliente. En el ejemplo siguiente se establecen las transformaciones de página y mundo de un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y, a continuación, se dibuja una línea de (0, 0) a (2, 1).


```
myGraphics.TranslateTransform(2.0f, 0.5f);
myGraphics.SetPageUnit(UnitInch);
myGraphics.DrawLine(&myPen, 0, 0, 2, 1);
```



En la ilustración siguiente se muestra el sistema de líneas y coordenadas.

![captura de pantalla de la ventana anterior, pero más ancha, con los ejes situados a la izquierda y etiquetados de forma diferente](images/aboutgdip05-art03.png)

Si suponemos que el dispositivo de pantalla tiene 96 puntos por pulgada en la dirección horizontal y 96 puntos por pulgada en la dirección vertical, los puntos de conexión de la línea del ejemplo anterior tienen las coordenadas siguientes en los tres espacios de coordenadas:



| Space       | Coordenadas del punto de conexión                        |
|--------|-------------------------|
| World  | (0, 0) a (2, 1)        |
| Página   | (2, 0,5) a (4, 1,5)    |
| Dispositivo | (192, 48) a (384, 144) |



 

 

 
