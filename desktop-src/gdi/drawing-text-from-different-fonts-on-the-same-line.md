---
description: Los distintos estilos de tipo dentro de una familia de fuentes pueden tener anchos diferentes.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Dibujar texto de distintas fuentes en la misma línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad28f13c94e568073504f07e8722e5d688cb12aa1b376b0f52fad752574e6f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038053"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Dibujar texto de distintas fuentes en la misma línea

Los distintos estilos de tipo dentro de una familia de fuentes pueden tener anchos diferentes. Por ejemplo, los estilos en negrita y cursiva de una familia siempre son más anchos que el estilo román para un tamaño de punto especificado. Al mostrar o imprimir varios estilos de tipo en una sola línea, debe realizar un seguimiento del ancho de la línea para evitar que se muestren o impriman caracteres entre sí.

Puede usar dos funciones para recuperar el ancho (o la extensión) del texto en la fuente actual. La [función GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) calcula el ancho y alto de una cadena de caracteres. Si la cadena contiene uno o varios caracteres de tabulación, el ancho de la cadena se basa en una matriz especificada de posiciones de tabulación. La [función GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) calcula el ancho y alto de una línea de texto.

Cuando sea necesario, el sistema sintetiza una fuente cambiando los mapas de bits de caracteres. Para sintetizar un carácter en una fuente en negrita, el sistema dibuja el carácter dos veces: en el punto inicial y de nuevo un píxel a la derecha del punto inicial. Para sintetizar un carácter en una fuente cursiva, el sistema dibuja dos filas de píxeles en la parte inferior de la celda de caracteres, mueve el punto inicial un píxel a la derecha, dibuja las dos filas siguientes y continúa hasta que se ha dibujado el carácter. Al desplazar píxeles, parece que cada carácter se corta a la derecha. La cantidad de cizalla es una función del alto del carácter.

Una manera de escribir una línea de texto que contenga varias fuentes es usar la función [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) después de cada llamada a [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) y agregar la longitud a una posición actual. En el ejemplo siguiente se escribe la línea "Esta es una cadena de ejemplo". con caracteres en negrita para "This is a", cambia a caracteres en cursiva para "sample" y, a continuación, vuelve a los caracteres en negrita para "string". Después de imprimir todas las cadenas, restaura los caracteres predeterminados del sistema.


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



En este ejemplo, la función [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) inicializa los miembros de una estructura [SIZE](/previous-versions//dd145106(v=vs.85)) con la longitud y el alto de la cadena especificada. La [función GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) recupera el sobresalto de la fuente actual. Dado que el sobresalto es cero si la fuente es una fuente TrueType, el valor de sobresalto no cambia la ubicación de la cadena. Sin embargo, para las fuentes de trama, es importante usar el valor de sobresalga.

El sobresalto se resta de la cadena en negrita una vez para acercar los caracteres posteriores al final de la cadena si la fuente es una fuente de trama. Dado que el sobresalto afecta tanto al principio como al final de la cadena cursiva en una fuente de trama, los glifos comienzan a la derecha de la ubicación especificada y terminan a la izquierda del punto de conexión de la última celda de caracteres. (La [**función GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) recupera la extensión de las celdas de caracteres, no la extensión de los glifos). Para tener en cuenta el sobresalto en la cadena de cursiva de trama, en el ejemplo se resta el sobresalto antes de colocar la cadena y se resta de nuevo antes de colocar los caracteres posteriores.

La [función SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) agrega espacio adicional a los caracteres de interrupción en una línea de texto. Puede usar la función [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) para determinar la extensión de una cadena, restar esa extensión de la cantidad total de espacio que debe ocupar la línea y usar la función [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) para distribuir el espacio adicional entre los caracteres de interrupción de la cadena. La [función SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) agrega espacio adicional a cada celda de caracteres de la fuente seleccionada, incluido el carácter de interrupción. (Puede usar la función [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) para determinar la cantidad actual de espacio adicional que se agrega a las celdas de caracteres; el valor predeterminado es cero).

Puede colocar caracteres con mayor precisión mediante la función [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) o [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) para recuperar los anchos de los caracteres individuales de una fuente. La [**función GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) es más precisa que la función [**GetCharWidth32,**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) pero solo se puede usar con fuentes TrueType.

El espaciado ABC también permite que una aplicación realice una alineación de texto muy precisa. Por ejemplo, cuando la aplicación alinea a la derecha una fuente de trama román sin usar el espaciado ABC, el ancho de avance se calcula como el ancho del carácter. Esto significa que el espacio en blanco a la derecha del glifo del mapa de bits está alineado, no el propio glifo. Mediante el uso de anchos ABC, las aplicaciones tienen más flexibilidad en la colocación y eliminación de espacios en blanco al alinear texto, ya que tienen información que les permite controlar correctamente el espaciado entre caracteres.

 

 
