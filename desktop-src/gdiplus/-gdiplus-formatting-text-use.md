---
description: Para aplicar formato especial al texto, inicialice un objeto StringFormat y pase la dirección de ese objeto al método DrawString de la clase Graphics.
ms.assetid: 4014a602-88f6-4fac-b4b2-3dafdcff8f33
title: Formato de texto (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6b2cc6109e7b946e9b4e98645c9445b8268bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552217"
---
# <a name="formatting-text-gdi"></a>Formato de texto (GDI+)

Para aplicar formato especial al texto, inicialice un objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) y pase la dirección de ese objeto al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

Para dibujar texto con formato en un rectángulo, se necesitan los objetos [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font), [**RectF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rectf), [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)y [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) .

-   [Alinear texto](#aligning-text)
-   [Configuración de tabulaciones](#setting-tab-stops)
-   [Dibujo de texto vertical](#drawing-vertical-text)

## <a name="aligning-text"></a>Alinear texto

En el ejemplo siguiente se dibuja texto en un rectángulo. Cada línea de texto está centrada (de lado a lado) y todo el bloque de texto está centrado (de arriba abajo) en el rectángulo.


```
WCHAR string[] = 
   L"Use StringFormat and RectF objects to center text in a rectangle.";
                       
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 120.0f, 140.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

// Center-justify each line of text.
stringFormat.SetAlignment(StringAlignmentCenter);

// Center the block of text (top to bottom) in the rectangle.
stringFormat.SetLineAlignment(StringAlignmentCenter);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



En la ilustración siguiente se muestra el rectángulo y el texto centrado.

![captura de pantalla de una ventana que contiene un rectángulo que contiene seis líneas de texto, centrado horizontalmente](images/fontstext3.png)

El código anterior llama a dos métodos del objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) : [**StringFormat:: SetAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setalignment) y [**StringFormat:: SetLineAlignment**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setlinealignment). La llamada a **StringFormat:: SetAlignment** especifica que cada línea de texto está centrada en el rectángulo proporcionado por el tercer argumento pasado al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) . La llamada a **StringFormat:: SetLineAlignment** especifica que el bloque de texto está centrado (de arriba abajo) en el rectángulo.

El valor [* * * * StringAlignmentCenter * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringalignment) * * es un elemento de la enumeración **StringAlignment** , que se declara en Gdiplusenums. h.

## <a name="setting-tab-stops"></a>Configuración de tabulaciones

Puede establecer las tabulaciones para el texto llamando al método [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) de un objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) y, a continuación, pasando la dirección de ese objeto **StringFormat** al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .

En el ejemplo siguiente se establecen tabulaciones en 150, 250 y 350. Después, el código muestra una lista con pestañas de nombres y puntuaciones de pruebas.


```
WCHAR string[150] = 
   L"Name\tTest 1\tTest 2\tTest 3\n";

StringCchCatW(string, 150, L"Joe\t95\t88\t91\n");
StringCchCatW(string, 150, L"Mary\t98\t84\t90\n");
StringCchCatW(string, 150, L"Sam\t42\t76\t98\n");
StringCchCatW(string, 150, L"Jane\t65\t73\t92\n");
                       
FontFamily   fontFamily(L"Courier New");
Font         font(&fontFamily, 12, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 450.0f, 100.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));
REAL         tabs[] = {150.0f, 100.0f, 100.0f};

stringFormat.SetTabStops(0.0f, 3, tabs);

graphics.DrawString(string, -1, &font, rectF, &stringFormat, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
            
```



En la ilustración siguiente se muestra el texto con pestañas.

![Ilustración de un rectángulo que contiene cuatro columnas de texto; cada columna se alinea a la izquierda](images/fontstext4.png)

En el código anterior se pasan tres argumentos al método [**StringFormat:: SetTabStops**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-settabstops) . El tercer argumento es la dirección de una matriz que contiene los desplazamientos de tabulación. El segundo argumento indica que hay tres desplazamientos en esa matriz. El primer argumento pasado a **StringFormat:: SetTabStops** es 0, que indica que el primer desplazamiento de la matriz se mide desde la posición 0, el borde izquierdo del rectángulo delimitador.

## <a name="drawing-vertical-text"></a>Dibujo de texto vertical

Puede usar un objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) para especificar que el texto se dibuje verticalmente en lugar de horizontalmente.

En el ejemplo siguiente se pasa el valor [* * * * StringFormatFlagsDirectionVertical * * * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) al método [**StringFormat:: SetFormatFlags**](/windows/win32/api/Gdiplusstringformat/nf-gdiplusstringformat-stringformat-setformatflags) de un objeto [**StringFormat**](/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat) . La dirección de ese objeto **StringFormat** se pasa al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . El valor [* * * * StringFormatFlagsDirectionVertical * *](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-stringformatflags) * * es un elemento de la enumeración **StringFormatFlags** , que se declara en Gdiplusenums. h.


```
WCHAR string[] = L"Vertical text";
                     
FontFamily   fontFamily(L"Lucida Console");
Font         font(&fontFamily, 14, FontStyleRegular, UnitPoint);
PointF       pointF(40.0f, 10.0f);
StringFormat stringFormat;
SolidBrush   solidBrush(Color(255, 0, 0, 255));

stringFormat.SetFormatFlags(StringFormatFlagsDirectionVertical);

graphics.DrawString(string, -1, &font, pointF, &stringFormat, &solidBrush);
            
```



En la ilustración siguiente se muestra el texto vertical.

![Ilustración que muestra una ventana que contiene el texto girado 90 grados en el sentido de las agujas del reloj](images/fontstext5.png)

 

 



