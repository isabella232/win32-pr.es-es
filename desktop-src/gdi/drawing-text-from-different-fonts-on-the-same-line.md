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
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a><span data-ttu-id="2f450-103">Dibujar texto de fuentes diferentes en la misma línea</span><span class="sxs-lookup"><span data-stu-id="2f450-103">Drawing Text from Different Fonts on the Same Line</span></span>

<span data-ttu-id="2f450-104">Los distintos estilos de tipo dentro de una familia de fuentes pueden tener distintos anchos.</span><span class="sxs-lookup"><span data-stu-id="2f450-104">Different type styles within a font family can have different widths.</span></span> <span data-ttu-id="2f450-105">Por ejemplo, los estilos de negrita y cursiva de una familia siempre son más amplios que el estilo romano para un tamaño de punto especificado.</span><span class="sxs-lookup"><span data-stu-id="2f450-105">For example, bold and italic styles of a family are always wider than the roman style for a specified point size.</span></span> <span data-ttu-id="2f450-106">Cuando se muestran o se imprimen varios estilos de tipo en una sola línea, se debe realizar un seguimiento del ancho de la línea para evitar que se muestren o se impriman entre sí los caracteres.</span><span class="sxs-lookup"><span data-stu-id="2f450-106">When you display or print several type styles on a single line, you must keep track of the width of the line to avoid having characters displayed or printed on top of one another.</span></span>

<span data-ttu-id="2f450-107">Puede usar dos funciones para recuperar el ancho (o la extensión) del texto de la fuente actual.</span><span class="sxs-lookup"><span data-stu-id="2f450-107">You can use two functions to retrieve the width (or extent) of text in the current font.</span></span> <span data-ttu-id="2f450-108">La función [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) calcula el ancho y el alto de una cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2f450-108">The [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta) function computes the width and height of a character string.</span></span> <span data-ttu-id="2f450-109">Si la cadena contiene uno o más caracteres de tabulación, el ancho de la cadena se basa en una matriz especificada de posiciones de tabulación.</span><span class="sxs-lookup"><span data-stu-id="2f450-109">If the string contains one or more tab characters, the width of the string is based upon a specified array of tab-stop positions.</span></span> <span data-ttu-id="2f450-110">La función [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) calcula el ancho y el alto de una línea de texto.</span><span class="sxs-lookup"><span data-stu-id="2f450-110">The [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function computes the width and height of a line of text.</span></span>

<span data-ttu-id="2f450-111">Cuando es necesario, el sistema sintetiza una fuente cambiando los mapas de bits de los caracteres.</span><span class="sxs-lookup"><span data-stu-id="2f450-111">When necessary, the system synthesizes a font by changing the character bitmaps.</span></span> <span data-ttu-id="2f450-112">Para sintetizar un carácter en una fuente en negrita, el sistema dibuja el carácter dos veces: en el punto inicial y de nuevo un píxel a la derecha del punto inicial.</span><span class="sxs-lookup"><span data-stu-id="2f450-112">To synthesize a character in a bold font, the system draws the character twice: at the starting point, and again one pixel to the right of the starting point.</span></span> <span data-ttu-id="2f450-113">Para sintetizar un carácter en una fuente en cursiva, el sistema dibuja dos filas de píxeles en la parte inferior de la celda de carácter, desplaza el punto inicial un píxel hacia la derecha, dibuja las dos filas siguientes y continúa hasta que se dibuja el carácter.</span><span class="sxs-lookup"><span data-stu-id="2f450-113">To synthesize a character in an italic font, the system draws two rows of pixels at the bottom of the character cell, moves the starting point one pixel to the right, draws the next two rows, and continues until the character has been drawn.</span></span> <span data-ttu-id="2f450-114">Al desplazarse por los píxeles, cada carácter aparece distorsionado a la derecha.</span><span class="sxs-lookup"><span data-stu-id="2f450-114">By shifting pixels, each character appears to be sheared to the right.</span></span> <span data-ttu-id="2f450-115">La cantidad de recorte es una función del alto del carácter.</span><span class="sxs-lookup"><span data-stu-id="2f450-115">The amount of shear is a function of the height of the character.</span></span>

<span data-ttu-id="2f450-116">Una manera de escribir una línea de texto que contiene varias fuentes es usar la función [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) después de cada llamada a [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) y agregar la longitud a una posición actual.</span><span class="sxs-lookup"><span data-stu-id="2f450-116">One way to write a line of text that contains multiple fonts is to use the [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function after each call to [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) and add the length to a current position.</span></span> <span data-ttu-id="2f450-117">En el ejemplo siguiente se escribe la línea "This is a Sample String".</span><span class="sxs-lookup"><span data-stu-id="2f450-117">The following example writes the line "This is a sample string."</span></span> <span data-ttu-id="2f450-118">usar caracteres en negrita para "Esto es un", cambia a caracteres en cursiva por "sample" y, a continuación, vuelve a caracteres en negrita para "String".</span><span class="sxs-lookup"><span data-stu-id="2f450-118">using bold characters for "This is a", switches to italic characters for "sample", then returns to bold characters for "string."</span></span> <span data-ttu-id="2f450-119">Después de imprimir todas las cadenas, restaura los caracteres predeterminados del sistema.</span><span class="sxs-lookup"><span data-stu-id="2f450-119">After printing all the strings, it restores the system default characters.</span></span>


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



<span data-ttu-id="2f450-120">En este ejemplo, la función [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) inicializa los miembros de una estructura de [tamaño](/previous-versions//dd145106(v=vs.85)) con la longitud y el alto de la cadena especificada.</span><span class="sxs-lookup"><span data-stu-id="2f450-120">In this example, the [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) function initializes the members of a [SIZE](/previous-versions//dd145106(v=vs.85)) structure with the length and height of the specified string.</span></span> <span data-ttu-id="2f450-121">La función [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) recupera el voladizo de la fuente actual.</span><span class="sxs-lookup"><span data-stu-id="2f450-121">The [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) function retrieves the overhang for the current font.</span></span> <span data-ttu-id="2f450-122">Dado que el voladizo es cero si la fuente es una fuente TrueType, el valor sobresaliente no cambia la posición de la cadena.</span><span class="sxs-lookup"><span data-stu-id="2f450-122">Because the overhang is zero if the font is a TrueType font, the overhang value does not change the string placement.</span></span> <span data-ttu-id="2f450-123">En el caso de las fuentes de trama, es importante usar el valor sobresaliente.</span><span class="sxs-lookup"><span data-stu-id="2f450-123">For raster fonts, however, it is important to use the overhang value.</span></span>

<span data-ttu-id="2f450-124">El voladizo se resta de la cadena en negrita una vez, para colocar los caracteres posteriores más cerca del final de la cadena si la fuente es una fuente de trama.</span><span class="sxs-lookup"><span data-stu-id="2f450-124">The overhang is subtracted from the bold string once, to bring subsequent characters closer to the end of the string if the font is a raster font.</span></span> <span data-ttu-id="2f450-125">Dado que el voladizo afecta al principio y al final de la cadena en cursiva en una fuente de trama, los glifos se inician a la derecha de la ubicación especificada y finalizan a la izquierda del extremo de la última celda de carácter.</span><span class="sxs-lookup"><span data-stu-id="2f450-125">Because overhang affects both the beginning and end of the italic string in a raster font, the glyphs start at the right of the specified location and end at the left of the endpoint of the last character cell.</span></span> <span data-ttu-id="2f450-126">(La función [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) recupera la extensión de las celdas de caracteres, no la extensión de los glifos). Para tener en cuenta el voladizo en la cadena en cursiva de trama, el ejemplo resta el voladizo antes de colocar la cadena y la resta de nuevo antes de colocar los caracteres posteriores.</span><span class="sxs-lookup"><span data-stu-id="2f450-126">(The [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) function retrieves the extent of the character cells, not the extent of the glyphs.) To account for the overhang in the raster italic string, the example subtracts the overhang before placing the string and subtracts it again before placing subsequent characters.</span></span>

<span data-ttu-id="2f450-127">La función [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) agrega espacio adicional a los caracteres de salto en una línea de texto.</span><span class="sxs-lookup"><span data-stu-id="2f450-127">The [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) function adds extra space to the break characters in a line of text.</span></span> <span data-ttu-id="2f450-128">Puede usar la función [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) para determinar la extensión de una cadena y, a continuación, restar esa extensión de la cantidad total de espacio que debe ocupar la línea y utilizar la función [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) para distribuir el espacio adicional entre los caracteres de salto de la cadena.</span><span class="sxs-lookup"><span data-stu-id="2f450-128">You can use the [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) function to determine the extent of a string, then subtract that extent from the total amount of space the line should occupy, and use the [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) function to distribute the extra space among the break characters in the string.</span></span> <span data-ttu-id="2f450-129">La función [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) agrega espacio adicional a cada celda de carácter de la fuente seleccionada, incluido el carácter de salto.</span><span class="sxs-lookup"><span data-stu-id="2f450-129">The [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) function adds extra space to every character cell in the selected font, including the break character.</span></span> <span data-ttu-id="2f450-130">(Puede utilizar la función [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) para determinar la cantidad actual de espacio adicional que se agrega a las celdas de caracteres; el valor predeterminado es cero).</span><span class="sxs-lookup"><span data-stu-id="2f450-130">(You can use the [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) function to determine the current amount of extra space being added to the character cells; the default setting is zero.)</span></span>

<span data-ttu-id="2f450-131">Puede colocar caracteres con mayor precisión mediante la función [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) o [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) para recuperar el ancho de caracteres individuales de una fuente.</span><span class="sxs-lookup"><span data-stu-id="2f450-131">You can place characters with greater precision by using the [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) or [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) function to retrieve the widths of individual characters in a font.</span></span> <span data-ttu-id="2f450-132">La función [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) es más precisa que la función [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) , pero solo se puede usar con fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="2f450-132">The [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa) function is more accurate than the [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a) function, but it can only be used with TrueType fonts.</span></span>

<span data-ttu-id="2f450-133">El espaciado ABC también permite que una aplicación realice una alineación de texto muy precisa.</span><span class="sxs-lookup"><span data-stu-id="2f450-133">ABC spacing also allows an application to perform very accurate text alignment.</span></span> <span data-ttu-id="2f450-134">Por ejemplo, cuando la aplicación alinea a la derecha una fuente de líneas romanos sin usar el espaciado ABC, el ancho de avance se calcula como el ancho de caracteres.</span><span class="sxs-lookup"><span data-stu-id="2f450-134">For example, when the application right aligns a raster roman font without using ABC spacing, the advance width is calculated as the character width.</span></span> <span data-ttu-id="2f450-135">Esto significa que el espacio en blanco a la derecha del glifo en el mapa de bits está alineado, no el propio glifo.</span><span class="sxs-lookup"><span data-stu-id="2f450-135">This means the white space to the right of the glyph in the bitmap is aligned, not the glyph itself.</span></span> <span data-ttu-id="2f450-136">Mediante el uso de anchos ABC, las aplicaciones tienen más flexibilidad en la selección de ubicación y eliminación de espacios en blanco al alinear texto, porque tienen información que les permite controlar con precisión el espaciado entre caracteres.</span><span class="sxs-lookup"><span data-stu-id="2f450-136">By using ABC widths, applications have more flexibility in the placement and removal of white space when aligning text, because they have information that allows them to finely control intercharacter spacing.</span></span>

 

 
