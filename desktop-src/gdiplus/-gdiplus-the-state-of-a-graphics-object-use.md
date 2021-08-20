---
description: La clase Graphics está en el centro de Windows GDI+. Para dibujar cualquier cosa, cree un objeto Graphics, establezca sus propiedades y llame a sus métodos (DrawLine, DrawImage, DrawString y similares).
ms.assetid: 7d70f9fe-c0b2-4d65-815d-483d06df96ad
title: Estado de un objeto de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f68a2ba754aadc1f7d2572dcbc2ac40d08d7fe95d382ce60511cd72d441bb80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977335"
---
# <a name="the-state-of-a-graphics-object"></a>Estado de un objeto de gráficos

La [**clase Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) se encuentra en el centro de Windows GDI+. Para dibujar cualquier cosa, cree un objeto **Graphics,** establezca sus propiedades y llame a sus métodos [(DrawLine,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) [DrawImage,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)) [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))y similares).

En el ejemplo siguiente se construye un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un objeto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) y, a continuación, se llama al método [**Graphics::D rawRectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) del **objeto Graphics:**


```
HDC          hdc;
PAINTSTRUCT  ps;

hdc = BeginPaint(hWnd, &ps);
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));  // opaque blue
   graphics.DrawRectangle(&pen, 10, 10, 200, 100);
}
EndPaint(hWnd, &ps);
```



En el código anterior, el [método BeginPaint](/windows/win32/api/winuser/nf-winuser-beginpaint) devuelve un identificador a un contexto de dispositivo y ese identificador se pasa al constructor [**Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Un contexto de dispositivo es una estructura (mantenida por Windows) que contiene información sobre el dispositivo de visualización concreto que se usa.

## <a name="graphics-state"></a>Estado de gráficos

Un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) hace algo más que proporcionar métodos de dibujo, como [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) y [DrawRectangle.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) Un **objeto Graphics** también mantiene el estado de los gráficos, que se puede dividir en las siguientes categorías:

-   Vínculo a un contexto de dispositivo
-   Configuración de calidad
-   Transformaciones
-   Una región de recorte

### <a name="device-context"></a>Contexto del dispositivo

Como programador de aplicaciones, no tiene que pensar en la interacción entre un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y su contexto de dispositivo. Esta interacción se controla mediante GDI+ en segundo plano.

### <a name="quality-settings"></a>Calidad Configuración

Un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tiene varias propiedades que influyen en la calidad de los elementos que se dibujan en la pantalla. Puede ver y manipular estas propiedades llamando a los métodos get y set. Por ejemplo, puede llamar al método [**Graphics::SetTextRenderingHint**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-settextrenderinghint) para especificar el tipo de suavizado de contorno (si hay alguno) aplicado al texto. Otros métodos de conjunto que influyen en la calidad son [**Graphics::SetSmoothingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode), [**Graphics::SetCompositingMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingmode), [**Graphics::SetCompositingQuality**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setcompositingquality)y [**Graphics::SetInterpolationMode**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setinterpolationmode).

En el ejemplo siguiente se dibujan dos puntos suspensivos, uno con el modo de suavizado establecido en [*"SmoothingModeAntiAlias*"](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode) y otro con el modo de suavizado establecido en [*"SmoothingModeHighSpeed*"::](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)


```
Graphics graphics(hdc);
Pen pen(Color(255, 0, 255, 0));  // opaque green

graphics.SetSmoothingMode(SmoothingModeAntiAlias);
graphics.DrawEllipse(&pen, 0, 0, 200, 100);
graphics.SetSmoothingMode(SmoothingModeHighSpeed);
graphics.DrawEllipse(&pen, 0, 150, 200, 100);
```



### <a name="transformations"></a>Transformaciones

Un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantiene dos transformaciones (mundo y página) que se aplican a todos los elementos dibujados por ese objeto **Graphics.** Cualquier transformación afín se puede almacenar en la transformación del mundo. Las transformaciones afín incluyen escalado, rotación, reflexión, sesgo y traducción. La transformación de página se puede usar para escalar y cambiar las unidades (por ejemplo, píxeles a pulgadas). Para obtener más información sobre las transformaciones, vea [Sistemas y transformaciones de coordenadas.](-gdiplus-coordinate-systems-and-transformations-about.md)

En el ejemplo siguiente se establecen las transformaciones de página y mundo de un [**objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) La transformación del mundo se establece en una rotación de 30 grados. La transformación de página se establece para que las coordenadas pasadas al segundo [**Graphics::D rawVelopse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inint_inint_inint_inint)) se traten como milímetros en lugar de píxeles. El código realiza dos llamadas idénticas al **método Graphics::D rawVelopse.** La transformación del mundo se aplica a la primera llamada **a Graphics::D rawVelopse** y ambas transformaciones (mundo y página) se aplican a la segunda llamada **a Graphics::D rawVelopse.**


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0));

graphics.ResetTransform();
graphics.RotateTransform(30.0f);            // World transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
graphics.SetPageUnit(UnitMillimeter);       // Page transformation
graphics.DrawEllipse(&pen, 30, 0, 50, 25);
```



En la ilustración siguiente se muestran los dos puntos suspensivos. Tenga en cuenta que la rotación de 30 grados se centra en el origen del sistema de coordenadas (esquina superior izquierda del área cliente), no en los centros de los puntos suspensivos. Tenga en cuenta también que el ancho del lápiz de 1 significa 1 píxel para la primera elipse y 1 milímetro para la segunda elipse.

![captura de pantalla de una ventana que contiene una elipse pequeña y fina y una elipse grande y más gruesa](images/graphicsascon1.png)

 

### <a name="clipping-region"></a>Región de recorte

Un [**objeto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) mantiene una región de recorte que se aplica a todos los elementos dibujados por ese objeto **Graphics.** Puede establecer la región de recorte llamando al [método SetClip.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode))

En el ejemplo siguiente se crea una región con forma de signo más mediante la formación de la unión de dos rectángulos. Esa región se designa como la región de recorte de un [**objeto Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) A continuación, el código dibuja dos líneas que están restringidas al interior de la región de recorte.


```
Graphics graphics(hdc);
Pen pen(Color(255, 255, 0, 0), 5);  // opaque red, width 5
SolidBrush brush(Color(255, 180, 255, 255));  // opaque aqua

// Create a plus-shaped region by forming the union of two rectangles.
Region region(Rect(50, 0, 50, 150));
region.Union(Rect(0, 50, 150, 50));
graphics.FillRegion(&brush, &region);

// Set the clipping region.
graphics.SetClip(&region);

// Draw two clipped lines.
graphics.DrawLine(&pen, 0, 30, 150, 160);
graphics.DrawLine(&pen, 40, 20, 190, 150);
```



En la ilustración siguiente se muestran las líneas recortadas.

![ilustración en la que se muestra una forma de color cruzada por dos líneas rojas diagonales](images/graphicsascon2.png)

 

 
