---
description: En algunos casos, una aplicación debe ser capaz de enumerar las fuentes disponibles y seleccionar la más adecuada para una operación determinada.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Enumerar las fuentes instaladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276009"
---
# <a name="enumerating-the-installed-fonts"></a><span data-ttu-id="1b27a-103">Enumerar las fuentes instaladas</span><span class="sxs-lookup"><span data-stu-id="1b27a-103">Enumerating the Installed Fonts</span></span>

<span data-ttu-id="1b27a-104">En algunos casos, una aplicación debe ser capaz de enumerar las fuentes disponibles y seleccionar la más adecuada para una operación determinada.</span><span class="sxs-lookup"><span data-stu-id="1b27a-104">In some instances, an application must be able to enumerate the available fonts and select the one most appropriate for a particular operation.</span></span> <span data-ttu-id="1b27a-105">Una aplicación puede enumerar las fuentes disponibles mediante una llamada a la función [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) o [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) .</span><span class="sxs-lookup"><span data-stu-id="1b27a-105">An application can enumerate the available fonts by calling the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) or [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function.</span></span> <span data-ttu-id="1b27a-106">Estas funciones envían información acerca de las fuentes disponibles a una función de devolución de llamada que la aplicación proporciona.</span><span class="sxs-lookup"><span data-stu-id="1b27a-106">These functions send information about the available fonts to a callback function that the application supplies.</span></span> <span data-ttu-id="1b27a-107">La función de devolución de llamada recibe información en las estructuras [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) y [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="1b27a-107">The callback function receives information in [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) and [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structures.</span></span> <span data-ttu-id="1b27a-108">(La estructura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) contiene información sobre una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="1b27a-108">(The [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure contains information about a TrueType font.</span></span> <span data-ttu-id="1b27a-109">Cuando la función de devolución de llamada recibe información sobre una fuente que no es TrueType, la información se encuentra en una estructura [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) .) Con esta información, una aplicación puede limitar las opciones del usuario a las fuentes que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="1b27a-109">When the callback function receives information about a non-TrueType font, the information is contained in a [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.) By using this information, an application can limit the user's choices to only those fonts that are available.</span></span>

<span data-ttu-id="1b27a-110">La función [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) es similar a la función [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) , pero incluye alguna funcionalidad adicional.</span><span class="sxs-lookup"><span data-stu-id="1b27a-110">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function is similar to the [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) function but includes some extra functionality.</span></span> <span data-ttu-id="1b27a-111">**EnumFontFamilies** permite a una aplicación aprovechar los estilos disponibles con las fuentes TrueType.</span><span class="sxs-lookup"><span data-stu-id="1b27a-111">**EnumFontFamilies** allows an application to take advantage of styles available with TrueType fonts.</span></span> <span data-ttu-id="1b27a-112">Las aplicaciones nuevas y actualizadas deben usar **EnumFontFamilies** en lugar de **EnumFonts**.</span><span class="sxs-lookup"><span data-stu-id="1b27a-112">New and upgraded applications should use **EnumFontFamilies** instead of **EnumFonts**.</span></span>

<span data-ttu-id="1b27a-113">Las fuentes TrueType se organizan en torno a un nombre de tipo de letra (por ejemplo, Courier New) y nombres de estilo (por ejemplo, cursiva, negrita y extra-negrita).</span><span class="sxs-lookup"><span data-stu-id="1b27a-113">TrueType fonts are organized around a typeface name (for example, Courier New) and style names (for example, italic, bold, and extra-bold).</span></span> <span data-ttu-id="1b27a-114">La función [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) enumera todos los estilos asociados a un nombre de familia especificado, no solo los atributos Bold y Italic.</span><span class="sxs-lookup"><span data-stu-id="1b27a-114">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function enumerates all the styles associated with a specified family name, not simply the bold and italic attributes.</span></span> <span data-ttu-id="1b27a-115">Por ejemplo, cuando el sistema incluye una fuente TrueType denominada Courier New Extra-Bold, **EnumFontFamilies** la enumera con las otras fuentes Courier New.</span><span class="sxs-lookup"><span data-stu-id="1b27a-115">For example, when the system includes a TrueType font called Courier New Extra-Bold, **EnumFontFamilies** lists it with the other Courier New fonts.</span></span> <span data-ttu-id="1b27a-116">Las capacidades de **EnumFontFamilies** son útiles para las fuentes con estilos muchos o inusuales y para las fuentes que cruzan los bordes internacionales.</span><span class="sxs-lookup"><span data-stu-id="1b27a-116">The capabilities of **EnumFontFamilies** are helpful for fonts with many or unusual styles and for fonts that cross international borders.</span></span>

<span data-ttu-id="1b27a-117">Si una aplicación no proporciona un nombre de tipo de letra, las funciones [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) y [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) proporcionan información acerca de una fuente en cada familia disponible.</span><span class="sxs-lookup"><span data-stu-id="1b27a-117">If an application does not supply a typeface name, the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions supply information about one font in each available family.</span></span> <span data-ttu-id="1b27a-118">Para enumerar todas las fuentes en un contexto de dispositivo, la aplicación puede especificar **null** para el nombre del tipo de letra, compilar una lista de los tipos de letra disponibles y, a continuación, enumerar cada fuente de cada tipo de letra.</span><span class="sxs-lookup"><span data-stu-id="1b27a-118">To enumerate all the fonts in a device context, the application can specify **NULL** for the typeface name, compile a list of the available typefaces, and then enumerate each font in each typeface.</span></span>

<span data-ttu-id="1b27a-119">En el ejemplo siguiente se usa la función [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) para recuperar el número de familias de fuentes raster, Vector y TrueType disponibles.</span><span class="sxs-lookup"><span data-stu-id="1b27a-119">The following example uses the [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function to retrieve the number of available raster, vector, and TrueType font families.</span></span>


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



<span data-ttu-id="1b27a-120">En este ejemplo se usan dos máscaras, RASTER \_ FONTTYPE y TrueType \_ FONTTYPE, para determinar el tipo de fuente que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="1b27a-120">This example uses two masks, RASTER\_FONTTYPE and TRUETYPE\_FONTTYPE, to determine the type of font being enumerated.</span></span> <span data-ttu-id="1b27a-121">Si \_ se establece el bit FONTTYPE de trama, la fuente es una fuente de trama.</span><span class="sxs-lookup"><span data-stu-id="1b27a-121">If the RASTER\_FONTTYPE bit is set, the font is a raster font.</span></span> <span data-ttu-id="1b27a-122">Si \_ se establece el bit FONTTYPE de TrueType, la fuente es una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="1b27a-122">If the TRUETYPE\_FONTTYPE bit is set, the font is a TrueType font.</span></span> <span data-ttu-id="1b27a-123">Si no se establece ningún bit, la fuente es una fuente de vector.</span><span class="sxs-lookup"><span data-stu-id="1b27a-123">If neither bit is set, the font is a vector font.</span></span> <span data-ttu-id="1b27a-124">Una tercera máscara, dispositivo \_ FONTTYPE, se establece cuando un dispositivo (por ejemplo, una impresora láser) admite la descarga de fuentes TrueType; es cero si el dispositivo es un adaptador de pantalla, una impresora de matriz de puntos u otro dispositivo de trama.</span><span class="sxs-lookup"><span data-stu-id="1b27a-124">A third mask, DEVICE\_FONTTYPE, is set when a device (for example, a laser printer) supports downloading TrueType fonts; it is zero if the device is a display adapter, dot-matrix printer, or other raster device.</span></span> <span data-ttu-id="1b27a-125">Una aplicación también puede usar la máscara del dispositivo \_ FONTTYPE para distinguir las fuentes de trama proporcionadas por GDI de las fuentes proporcionadas por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b27a-125">An application can also use the DEVICE\_FONTTYPE mask to distinguish GDI-supplied raster fonts from device-supplied fonts.</span></span> <span data-ttu-id="1b27a-126">El sistema puede simular atributos de negrita, cursiva, subrayado y tachado para fuentes de tramas proporcionadas por GDI, pero no para fuentes proporcionadas por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b27a-126">The system can simulate bold, italic, underline, and strikeout attributes for GDI-supplied raster fonts, but not for device-supplied fonts.</span></span>

<span data-ttu-id="1b27a-127">Una aplicación también puede comprobar los bits 1 y 2 en el miembro **tmPitchAndFamily** de la estructura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) para identificar una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="1b27a-127">An application can also check bits 1 and 2 in the **tmPitchAndFamily** member of the [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure to identify a TrueType font.</span></span> <span data-ttu-id="1b27a-128">Si el bit 1 es 0 y el bit 2 es 1, la fuente es una fuente TrueType.</span><span class="sxs-lookup"><span data-stu-id="1b27a-128">If bit 1 is 0 and bit 2 is 1, the font is a TrueType font.</span></span>

<span data-ttu-id="1b27a-129">Las fuentes vectoriales se clasifican como el \_ juego de caracteres OEM en lugar del \_ juego de caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="1b27a-129">Vector fonts are categorized as OEM\_CHARSET instead of ANSI\_CHARSET.</span></span> <span data-ttu-id="1b27a-130">Algunas aplicaciones identifican las fuentes vectoriales mediante esta información, comprobando el miembro **tmCharSet** de la estructura [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) .</span><span class="sxs-lookup"><span data-stu-id="1b27a-130">Some applications identify vector fonts by using this information, checking the **tmCharSet** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span> <span data-ttu-id="1b27a-131">Normalmente, esta categorización impide que el asignador de fuentes elija las fuentes vectoriales, a menos que se soliciten específicamente.</span><span class="sxs-lookup"><span data-stu-id="1b27a-131">This categorization usually prevents the font mapper from choosing vector fonts unless they are specifically requested.</span></span> <span data-ttu-id="1b27a-132">(La mayoría de las aplicaciones ya no usan fuentes vectoriales porque sus trazos son líneas únicas y tardan más tiempo en dibujarse que las fuentes TrueType, que ofrecen muchas de las mismas características de escala y giro que requieren las fuentes vectoriales).</span><span class="sxs-lookup"><span data-stu-id="1b27a-132">(Most applications no longer use vector fonts because their strokes are single lines and they take longer to draw than TrueType fonts, which offer many of the same scaling and rotation features that required vector fonts.)</span></span>

 

 
