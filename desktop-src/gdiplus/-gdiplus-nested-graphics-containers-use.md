---
description: Windows GDI+ proporciona contenedores que puede usar para reemplazar o aumentar temporalmente parte del estado en un objeto gráfico.
ms.assetid: f3fce8ef-903a-4b9d-b76c-562739d02eb3
title: Contenedores de gráficos anidados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f9d9feac3494b423d844cb1e3da359af33eaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001664"
---
# <a name="nested-graphics-containers"></a>Contenedores de gráficos anidados

Windows GDI+ proporciona contenedores que puede usar para reemplazar o aumentar temporalmente parte del estado en un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Puede crear un contenedor llamando al método [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) de un objeto **Graphics** . Puede llamar a **Graphics:: BeginContainer** repetidamente para formar contenedores anidados.

## <a name="transformations-in-nested-containers"></a>Transformaciones en contenedores anidados

En el ejemplo siguiente se crea un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un contenedor dentro de ese objeto **Graphics** . La transformación universal del objeto **Graphics** es una traducción de 100 unidades en la dirección x y 80 unidades en la dirección y. La transformación universal del contenedor es una rotación de 30 grados. El código realiza la llamada


```
DrawRectangle(&pen, -60, -30, 120, 60)
```



ocasiones. La primera llamada a [**Graphics::D rawrectangle**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) está *dentro del contenedor*; es decir, la llamada se encuentra entre las llamadas a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)) y [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer). La segunda llamada a **Graphics::D rawrectangle** es después de la llamada a **Graphics:: EndContainer**.


```
Graphics           graphics(hdc);
Pen                pen(Color(255, 255, 0, 0));
GraphicsContainer  graphicsContainer;

graphics.TranslateTransform(100.0f, 80.0f);

graphicsContainer = graphics.BeginContainer();
   graphics.RotateTransform(30.0f);
   graphics.DrawRectangle(&pen, -60, -30, 120, 60);
graphics.EndContainer(graphicsContainer);

graphics.DrawRectangle(&pen, -60, -30, 120, 60);
```



En el código anterior, el rectángulo dibujado desde dentro del contenedor se transforma primero por la transformación universal del contenedor (rotación) y, a continuación, por la transformación universal del objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) (traslación). El rectángulo dibujado desde fuera del contenedor solo se transforma por la transformación universal del objeto **Graphics** (traslación). En la ilustración siguiente se muestran los dos rectángulos.

![captura de pantalla de una ventana con dos rectángulos rojos centrados en el mismo punto, pero con diferentes giros](images/nestedcontainers1.png)

 

## <a name="clipping-in-nested-containers"></a>Recorte en contenedores anidados

En el ejemplo siguiente se muestra cómo los contenedores anidados controlan las regiones de recorte. El código crea un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y un contenedor dentro de ese objeto **Graphics** . La región de recorte del objeto **Graphics** es un rectángulo y la región de recorte del contenedor es una elipse. El código realiza dos llamadas al método [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) . La primera llamada a **Graphics::D rawline** está dentro del contenedor y la segunda llamada a **graphics::D rawline** está fuera del contenedor (después de la llamada a [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer)). La primera línea se recorta por la intersección de las dos regiones de recorte. La segunda línea solo se recorta en la región de recorte rectangular del objeto **Graphics** .


```
Graphics           graphics(hdc);
GraphicsContainer  graphicsContainer;
Pen                redPen(Color(255, 255, 0, 0), 2);
Pen                bluePen(Color(255, 0, 0, 255), 2);
SolidBrush         aquaBrush(Color(255, 180, 255, 255));
SolidBrush         greenBrush(Color(255, 150, 250, 130));

graphics.SetClip(Rect(50, 65, 150, 120));
graphics.FillRectangle(&aquaBrush, 50, 65, 150, 120);

graphicsContainer = graphics.BeginContainer();
   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(75, 50, 100, 150);

  // Construct a region based on the path.
   Region region(&path);
   graphics.FillRegion(&greenBrush, &region);

   graphics.SetClip(&region);
   graphics.DrawLine(&redPen, 50, 0, 350, 300);
graphics.EndContainer(graphicsContainer);

graphics.DrawLine(&bluePen, 70, 0, 370, 300);
```



En la ilustración siguiente se muestran las dos líneas recortadas.

![Ilustración de una elipse dentro de un rectángulo, con una línea recortada por la elipse y la otra por el rectángulo](images/nestedcontainers2.png)

Como muestran los dos ejemplos anteriores, las transformaciones y las regiones de recorte son acumulativas en contenedores anidados. Si establece las transformaciones mundiales del contenedor y del objeto de [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , ambas transformaciones se aplicarán a los elementos que se dibujen desde dentro del contenedor. En primer lugar, se aplicará la transformación del contenedor y la transformación del objeto de **gráficos** se aplicará en segundo lugar. Si establece las regiones de recorte del contenedor y el objeto de **gráficos** , los elementos dibujados desde dentro del contenedor se recortarán por la intersección de las dos regiones de recorte.

## <a name="quality-settings-in-nested-containers"></a>Configuración de calidad en contenedores anidados

Los valores de calidad ( [**SmoothingMode**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode), [**TextRenderingHint**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)y similares) en los contenedores anidados no son acumulativos. en su lugar, los valores de calidad del contenedor reemplazan temporalmente la configuración de calidad de un objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Al crear un nuevo contenedor, la configuración de calidad de ese contenedor se establece en los valores predeterminados. Por ejemplo, supongamos que tiene un objeto **Graphics** con un modo de suavizado de [* * * * SmoothingModeAntiAlias *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)* * *. Al crear un contenedor, el modo de suavizado dentro del contenedor es el modo de suavizado predeterminado. Puede establecer el modo de suavizado del contenedor y todos los elementos que se dibujen desde dentro del contenedor se dibujarán según el modo que establezca. Los elementos dibujados después de la llamada a [**Graphics:: EndContainer**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-endcontainer) se dibujarán según el modo de suavizado ([* * * * SmoothingModeAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)*) que había antes de la llamada a [**Graphics:: BeginContainer**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-begincontainer(inconstrectf__inconstrectf__inunit)).

## <a name="several-layers-of-nested-containers"></a>Varios niveles de contenedores anidados

No está limitado a un contenedor en un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Puede crear una secuencia de contenedores, cada uno anidado en el anterior, y puede especificar la transformación universal, la región de recorte y la configuración de calidad de cada uno de esos contenedores anidados. Si llama a un método de dibujo desde dentro del contenedor más interno, las transformaciones se aplicarán en orden, comenzando por el contenedor más interno y finalizando con el contenedor más externo. Los elementos dibujados desde dentro del contenedor más interno se recortarán por la intersección de todas las regiones de recorte.

En el ejemplo siguiente se crea un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y se establece su sugerencia de representación de texto en [* * * * TextRenderingHintAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *. El código crea dos contenedores, uno anidado dentro de otro. La sugerencia de representación de texto del contenedor externo está establecida en [* * * * TextRenderingHintSingleBitPerPixel * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* * y la sugerencia de representación de texto del contenedor interno está establecida en [* * * * TextRenderingHintAntiAlias * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-textrenderinghint)* *. El código dibuja tres cadenas: una del contenedor interno, una del contenedor externo y otra del propio objeto **gráfico** .


```
Graphics graphics(hdc);
GraphicsContainer innerContainer;
GraphicsContainer outerContainer;
SolidBrush brush(Color(255, 0, 0, 255));
FontFamily fontFamily(L"Times New Roman");
Font font(&fontFamily, 36, FontStyleRegular, UnitPixel);

graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);

outerContainer = graphics.BeginContainer();

   graphics.SetTextRenderingHint(TextRenderingHintSingleBitPerPixel);

   innerContainer = graphics.BeginContainer();
      graphics.SetTextRenderingHint(TextRenderingHintAntiAlias);
      graphics.DrawString(L"Inner Container", 15, &font,
         PointF(20, 10), &brush);
   graphics.EndContainer(innerContainer);

   graphics.DrawString(L"Outer Container", 15, &font, PointF(20, 50), &brush);

graphics.EndContainer(outerContainer);

graphics.DrawString(L"Graphics Object", 15, &font, PointF(20, 90), &brush);
```



En la ilustración siguiente se muestran las tres cadenas. Las cadenas dibujadas desde el contenedor interno y el objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) se suavizan mediante el suavizado de contorno. La cadena dibujada desde el contenedor externo no se suaviza mediante el suavizado de contorno debido a la configuración de TextRenderingHintSingleBitPerPixel.

![Ilustración de un rectángulo que contiene la misma cadena allí. solo los caracteres de la primera y la última línea son suaves](images/nestedcontainers3.png)

 

 
