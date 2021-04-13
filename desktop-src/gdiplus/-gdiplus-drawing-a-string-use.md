---
description: En el tema dibujar una línea se muestra cómo escribir una aplicación de Windows que usa Windows GDI+ para dibujar una línea.
ms.assetid: fcf45b19-456c-4551-8901-d587a73a5638
title: Dibujo de una cadena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a88e76fd38dd640a402edf202dc6cdbd3008a76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276395"
---
# <a name="drawing-a-string"></a>Dibujo de una cadena

En el tema [dibujar una línea](-gdiplus-drawing-a-line-use.md) se muestra cómo escribir una aplicación de Windows que usa Windows GDI+ para dibujar una línea. Para dibujar una cadena, reemplace la función **OnPaint** que se muestra en ese tema por la siguiente función **OnPaint** :


```
VOID OnPaint(HDC hdc)
{
   Graphics    graphics(hdc);
   SolidBrush  brush(Color(255, 0, 0, 255));
   FontFamily  fontFamily(L"Times New Roman");
   Font        font(&fontFamily, 24, FontStyleRegular, UnitPixel);
   PointF      pointF(10.0f, 20.0f);
   
   graphics.DrawString(L"Hello World!", -1, &font, pointF, &brush);
}
```



El código anterior crea varios objetos GDI+. El objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona el método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) , que realiza el dibujo real. El objeto [**SolidBrush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) especifica el color de la cadena.

El constructor [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) recibe un único argumento de cadena que identifica la familia de fuentes. La dirección del objeto **FontFamily** es el primer argumento que se pasa al constructor [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . El segundo argumento pasado al constructor [Font](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(constfont_)) especifica el tamaño de fuente y el tercer argumento especifica el estilo. El valor **FontStyleRegular** es un miembro de la enumeración [**fontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , que se declara en Gdiplusenums. h. El último argumento del constructor de **fuente** indica que el tamaño de la fuente (en este caso, 24 en este caso) se mide en píxeles. El valor **UnitPixel** es un miembro de la enumeración [**Unit**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-unit) .

El primer argumento que se pasa al método [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) es la dirección de una cadena de caracteres anchos. El segundo argumento,-1, especifica que la cadena está terminada en NULL. (Si la cadena no termina en null, el segundo argumento debe especificar el número de caracteres anchos de la cadena). El tercer argumento es la dirección del objeto de [**fuente**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . El cuarto argumento es una referencia a un objeto de [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf) que especifica la ubicación donde se dibujará la cadena. El último argumento es la dirección del objeto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) , que especifica el color de la cadena.

 

 
