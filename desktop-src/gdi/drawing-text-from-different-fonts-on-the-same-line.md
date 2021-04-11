---
description: Los distintos estilos de tipo dentro de una familia de fuentes pueden tener distintos anchos.
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: Dibujar texto de fuentes diferentes en la misma línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eae2a7a332bd929b9a965462ce802734679f9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276011"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>Dibujar texto de fuentes diferentes en la misma línea

Los distintos estilos de tipo dentro de una familia de fuentes pueden tener distintos anchos. Por ejemplo, los estilos de negrita y cursiva de una familia siempre son más amplios que el estilo romano para un tamaño de punto especificado. Cuando se muestran o se imprimen varios estilos de tipo en una sola línea, se debe realizar un seguimiento del ancho de la línea para evitar que se muestren o se impriman entre sí los caracteres.

Puede usar dos funciones para recuperar el ancho (o la extensión) del texto de la fuente actual. La función [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) calcula el ancho y el alto de una cadena de caracteres. Si la cadena contiene uno o más caracteres de tabulación, el ancho de la cadena se basa en una matriz especificada de posiciones de tabulación. La función [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) calcula el ancho y el alto de una línea de texto.

Cuando es necesario, el sistema sintetiza una fuente cambiando los mapas de bits de los caracteres. Para sintetizar un carácter en una fuente en negrita, el sistema dibuja el carácter dos veces: en el punto inicial y de nuevo un píxel a la derecha del punto inicial. Para sintetizar un carácter en una fuente en cursiva, el sistema dibuja dos filas de píxeles en la parte inferior de la celda de carácter, desplaza el punto inicial un píxel hacia la derecha, dibuja las dos filas siguientes y continúa hasta que se dibuja el carácter. Al desplazarse por los píxeles, cada carácter aparece distorsionado a la derecha. La cantidad de recorte es una función del alto del carácter.

Una manera de escribir una línea de texto que contiene varias fuentes es usar la función [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) después de cada llamada a [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) y agregar la longitud a una posición actual. En el ejemplo siguiente se escribe la línea "This is a Sample String". usar caracteres en negrita para "Esto es un", cambia a caracteres en cursiva por "sample" y, a continuación, vuelve a caracteres en negrita para "String". Después de imprimir todas las cadenas, restaura los caracteres predeterminados del sistema.


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



En este ejemplo, la función [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) inicializa los miembros de una estructura de [tamaño](/previous-versions//dd145106(v=vs.85)) con la longitud y el alto de la cadena especificada. La función [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) recupera el voladizo de la fuente actual. Dado que el voladizo es cero si la fuente es una fuente TrueType, el valor sobresaliente no cambia la posición de la cadena. En el caso de las fuentes de trama, es importante usar el valor sobresaliente.

El voladizo se resta de la cadena en negrita una vez, para colocar los caracteres posteriores más cerca del final de la cadena si la fuente es una fuente de trama. Dado que el voladizo afecta al principio y al final de la cadena en cursiva en una fuente de trama, los glifos se inician a la derecha de la ubicación especificada y finalizan a la izquierda del extremo de la última celda de carácter. (La función [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) recupera la extensión de las celdas de caracteres, no la extensión de los glifos). Para tener en cuenta el voladizo en la cadena en cursiva de trama, el ejemplo resta el voladizo antes de colocar la cadena y la resta de nuevo antes de colocar los caracteres posteriores.

La función [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) agrega espacio adicional a los caracteres de salto en una línea de texto. Puede usar la función [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) para determinar la extensión de una cadena y, a continuación, restar esa extensión de la cantidad total de espacio que debe ocupar la línea y utilizar la función [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) para distribuir el espacio adicional entre los caracteres de salto de la cadena. La función [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) agrega espacio adicional a cada celda de carácter de la fuente seleccionada, incluido el carácter de salto. (Puede utilizar la función [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) para determinar la cantidad actual de espacio adicional que se agrega a las celdas de caracteres; el valor predeterminado es cero).

Puede colocar caracteres con mayor precisión mediante la función [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) o [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) para recuperar el ancho de caracteres individuales de una fuente. La función [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) es más precisa que la función [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , pero solo se puede usar con fuentes TrueType.

El espaciado ABC también permite que una aplicación realice una alineación de texto muy precisa. Por ejemplo, cuando la aplicación alinea a la derecha una fuente de líneas romanos sin usar el espaciado ABC, el ancho de avance se calcula como el ancho de caracteres. Esto significa que el espacio en blanco a la derecha del glifo en el mapa de bits está alineado, no el propio glifo. Mediante el uso de anchos ABC, las aplicaciones tienen más flexibilidad en la selección de ubicación y eliminación de espacios en blanco al alinear texto, porque tienen información que les permite controlar con precisión el espaciado entre caracteres.

 

 
