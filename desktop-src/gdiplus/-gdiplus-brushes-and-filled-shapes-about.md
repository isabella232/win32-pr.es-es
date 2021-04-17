---
description: Una figura cerrada, como un rectángulo o una elipse, consta de un contorno y un interior.
ms.assetid: 889558d5-9181-43ff-b862-e92966324208
title: Pinceles y formas rellenas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb772be88ce26325337fd9c88fc0319631895e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559918"
---
# <a name="brushes-and-filled-shapes"></a>Pinceles y formas rellenas

Una figura cerrada, como un rectángulo o una elipse, consta de un contorno y un interior. El contorno se dibuja con un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y el interior se rellena con un objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . Windows GDI+ proporciona varias clases de pincel para rellenar los interiores de las figuras cerradas: [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), [**HatchBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush), [**TextureBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-texturebrush), [**LinearGradientBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush)y [**PathGradientBrush**](/windows/win32/api/gdipluspath/nl-gdipluspath-pathgradientbrush). Todas estas clases heredan de la clase **Brush** . En la ilustración siguiente se muestra un rectángulo relleno con un pincel sólido y una elipse rellena con un pincel de trama.

![Ilustración que muestra un rectángulo azul y una elipse magenta rellena con un patrón de trama azul](images/aboutgdip02-art17.png)

 

-   [Pinceles sólidos](#solid-brushes)
-   [Pinceles de trama](#hatch-brushes)
-   [Pinceles de textura](#texture-brushes)
-   [Pinceles de degradado](#gradient-brushes)

## <a name="solid-brushes"></a>Pinceles sólidos

Para rellenar una forma cerrada, necesita un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) . El objeto **Graphics** proporciona métodos, como [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inconstrectf_)) y [FillEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inconstrectf_)), y el objeto **Brush** almacena atributos del relleno, como el color y el patrón. La dirección del objeto **Brush** se pasa como uno de los argumentos al método Fill. En el ejemplo siguiente se rellena una elipse con un color rojo sólido.


```
SolidBrush mySolidBrush(Color(255, 255, 0, 0));
myGraphics.FillEllipse(&mySolidBrush, 0, 0, 60, 40);
```



Tenga en cuenta que en el ejemplo anterior, el pincel es de tipo [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush), que hereda de [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush).

## <a name="hatch-brushes"></a>Pinceles de trama

Al rellenar una forma con un pincel de trama, se especifica un color de primer plano, un color de fondo y un estilo de trama. El color de primer plano es el color del sombreado.


```
HatchBrush myHatchBrush(
   HatchStyleVertical, 
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0));
```



GDI+ proporciona más de 50 estilos de trama, que se especifican en [**HatchStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-hatchstyle). Los tres estilos que se muestran en la siguiente ilustración son horizontal, ForwardDiagonal y Cross.

![Ilustración que muestra tres elipses de color verde azulado, cada una con un estilo de trama diferente](images/aboutgdip02-art18.png)

 

## <a name="texture-brushes"></a>Pinceles de textura

Con un pincel de textura, puede rellenar una forma con un patrón almacenado en un mapa de bits. Por ejemplo, supongamos que la siguiente imagen se almacena en un archivo de disco denominado MyTexture.bmp.

![captura de pantalla de un cuadrado pequeño relleno con varios colores](images/aboutgdip02-art19.png)

En el ejemplo siguiente se rellena una elipse repitiendo la imagen almacenada en MyTexture.bmp.


```
Image myImage(L"MyTexture.bmp");
TextureBrush myTextureBrush(&myImage);
myGraphics.FillEllipse(&myTextureBrush, 0, 0, 100, 50);
```



En la ilustración siguiente se muestra la elipse rellenada.

![Ilustración en la que se muestra una elipse rellena con el patrón definido previamente](images/aboutgdip02-art20.png)

 

## <a name="gradient-brushes"></a>Pinceles de degradado

Puede usar un pincel de degradado para rellenar una forma con un color que cambie gradualmente de una parte de la forma a otra. Por ejemplo, un pincel de degradado horizontal cambiará el color a medida que se desplaza desde el lado izquierdo de una figura a la derecha. En el ejemplo siguiente se rellena una elipse con un pincel de degradado horizontal que cambia de azul a verde a medida que se desplaza desde el lado izquierdo de la elipse hasta el lado derecho.


```
LinearGradientBrush myLinearGradientBrush(
   myRect,
   Color(255, 0, 0, 255),
   Color(255, 0, 255, 0),
   LinearGradientModeHorizontal);
myGraphics.FillEllipse(&myLinearGradientBrush, myRect); 
```



En la ilustración siguiente se muestra la elipse rellenada.

![Ilustración que muestra una elipse con un relleno de degradado: Blue de la derecha a la izquierda](images/aboutgdip02-art21.png)

Un pincel de degradado de trazado puede configurarse para cambiar el color a medida que se desplaza desde el centro de una figura hacia el límite.

![Ilustration de una elipse azul oscuro en el centro, sombreando el azul claro en el borde](images/aboutgdip02-art22.png)

Los pinceles de degradado de trazado son bastante flexibles. El pincel de degradado que se usa para rellenar el triángulo de la siguiente ilustración cambia gradualmente de rojo en el centro a cada uno de tres colores diferentes en los vértices.

![Ilustración de un triángulo que está en rojo en el centro y sombreado a un color diferente en cada vértice](images/aboutgdip02-art23.png)

 

 



