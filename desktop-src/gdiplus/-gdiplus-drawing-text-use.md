---
description: Puede usar el método DrawString de la clase Graphics para dibujar texto en una ubicación especificada o dentro de un rectángulo especificado.
ms.assetid: a873c132-f232-4144-bcc3-ca200055074c
title: Dibujo de texto (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31591d62198bc6ff72cdd7cce0d8ab515dc0e96011457b5bccd601a59ee0293f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115045"
---
# <a name="drawing-text-gdi"></a>Dibujo de texto (GDI+)

Puede usar el método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para dibujar texto en una ubicación especificada o dentro de un rectángulo especificado.

-   [Dibujar texto en una ubicación especificada](#drawing-text-at-a-specified-location)
-   [Dibujar texto en un rectángulo](#drawing-text-in-a-rectangle)

## <a name="drawing-text-at-a-specified-location"></a>Dibujar texto en una ubicación especificada

Para dibujar texto en una ubicación especificada, necesita objetos [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily), [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font), [**PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf)y [**Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

En el ejemplo siguiente se dibuja la cadena "Hello" en la ubicación (30, 10). La familia de fuentes es Times New Roman. La fuente, que es un miembro individual de la familia de fuentes, es Times New Roman, tamaño 24 píxeles, estilo normal. Suponga que **los gráficos** son un objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) existente.

```
FontFamily  fontFamily(L"Times New Roman");
Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
PointF      pointF(30.0f, 10.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(L"Hello", -1, &font, pointF, &solidBrush);

```

En la ilustración siguiente se muestra la salida del código anterior.

![captura de pantalla de una ventana pequeña que contiene el texto "hello"](images/fontstext1.png)

En el ejemplo anterior, el constructor [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) recibe una cadena que identifica la familia de fuentes. La dirección del **objeto FontFamily** se pasa como primer argumento al constructor [**Font.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) El segundo argumento pasado al constructor **Font** especifica el tamaño de la fuente medida en unidades dadas por el cuarto argumento. El tercer argumento especifica el estilo (normal, negrita, cursiva, y así sucesivamente) de la fuente.

El [método DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) recibe cinco argumentos. El primer argumento es la cadena que se va a dibujar y el segundo argumento es la longitud (en caracteres, no en bytes) de esa cadena. Si la cadena termina en null, puede pasar –1 para la longitud. El tercer argumento es la dirección del [**objeto Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) que se construyó anteriormente. El cuarto argumento es un [**objeto PointF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf) que contiene las coordenadas de la esquina superior izquierda de la cadena. El quinto argumento es la dirección de un [**objeto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) que se usará para rellenar los caracteres de la cadena.

## <a name="drawing-text-in-a-rectangle"></a>Dibujar texto en un rectángulo

Uno de los [**métodos DrawString**](https://www.bing.com/search?q=**DrawString**) de la [**clase Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) tiene un *parámetro RectF.* Al llamar a **ese método DrawString,** puede dibujar texto que se ajusta en un rectángulo especificado. Para dibujar texto en un rectángulo, necesita objetos **Graphics**, [**FontFamily,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) [**Font,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) [**RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf)y [**Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)

En el ejemplo siguiente se crea un rectángulo con la esquina superior izquierda (30, 10), el ancho 100 y el alto 122. A continuación, el código dibuja una cadena dentro de ese rectángulo. La cadena está restringida al rectángulo y se ajusta de forma que las palabras individuales no se rompa.

```
WCHAR string[] = 
   L"Draw text in a rectangle by passing a RectF to the DrawString method.";

FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 12, FontStyleBold, UnitPoint);
RectF        rectF(30.0f, 10.0f, 100.0f, 122.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 255));

graphics.DrawString(string, -1, &font, rectF, NULL, &solidBrush);

Pen pen(Color(255, 0, 0, 0));
graphics.DrawRectangle(&pen, rectF);
```

En la ilustración siguiente se muestra el texto dibujado en el rectángulo.

![captura de pantalla de una ventana pequeña que contiene una recangle, dentro de la cual aparece la primera parte de una frase](images/fontstext2.png)

En el ejemplo anterior, el cuarto argumento pasado al método [**DrawString**](https://www.bing.com/search?q=**DrawString**) es un [**objeto RectF**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf) que especifica el rectángulo delimitador para el texto. El quinto parámetro es de tipo [**StringFormat;**](/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat)el argumento **es NULL** porque no se requiere ningún formato de cadena especial.
