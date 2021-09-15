---
description: En algunos casos, una aplicación debe ser capaz de enumerar las fuentes disponibles y seleccionar la más adecuada para una operación determinada.
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: Enumerar las fuentes instaladas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580497"
---
# <a name="enumerating-the-installed-fonts"></a>Enumerar las fuentes instaladas

En algunos casos, una aplicación debe ser capaz de enumerar las fuentes disponibles y seleccionar la más adecuada para una operación determinada. Una aplicación puede enumerar las fuentes disponibles llamando a la función [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) [o EnumFontFamilies.](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) Estas funciones envían información sobre las fuentes disponibles a una función de devolución de llamada que proporciona la aplicación. La función de devolución de llamada recibe información en [las estructuras LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) [y NEWTEXTMETRIC.](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) (La [**estructura NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) contiene información sobre una fuente TrueType. Cuando la función de devolución de llamada recibe información sobre una fuente que no es TrueType, la información se incluye en una [estructura TEXTMETRIC).](/windows/win32/api/wingdi/ns-wingdi-textmetrica) Con esta información, una aplicación puede limitar las opciones del usuario a solo las fuentes que están disponibles.

La [**función EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) es similar a la función [**EnumFonts,**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) pero incluye alguna funcionalidad adicional. **EnumFontFamilies permite** que una aplicación aproveche los estilos disponibles con las fuentes TrueType. Las aplicaciones nuevas y actualizadas deben **usar EnumFontFamilies en** lugar **de EnumFonts**.

Las fuentes TrueType se organizan en torno a un nombre de tipo de letra (por ejemplo, Courier New) y nombres de estilo (por ejemplo, cursiva, negrita y negrita adicional). La [**función EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) enumera todos los estilos asociados a un nombre de familia especificado, no solo los atributos en negrita y cursiva. Por ejemplo, cuando el sistema incluye una fuente TrueType denominada Courier New Extra-Bold, **EnumFontFamilies** la muestra con las otras fuentes de Courier New. Las funcionalidades **de EnumFontFamilies** son útiles para las fuentes con muchos estilos o inusuales y para las fuentes que cruzan las fronteras internacionales.

Si una aplicación no proporciona un nombre de tipo de letra, las funciones [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) y [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) suministran información sobre una fuente en cada familia disponible. Para enumerar todas las fuentes de un contexto de dispositivo, la aplicación puede especificar **NULL** para el nombre del tipo de letra, compilar una lista de los tipos de letra disponibles y, a continuación, enumerar cada fuente de cada tipo de letra.

En el ejemplo siguiente se usa la función [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) para recuperar el número de familias de fuentes raster, vector y TrueType disponibles.


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



En este ejemplo se usan dos máscaras, RASTER \_ FONTTYPE y TRUETYPE FONTTYPE, para determinar el tipo de \_ fuente que se enumera. Si se establece \_ el bit FONTTYPE de RASTER, la fuente es una fuente de trama. Si se establece el \_ bit TRUETYPE FONTTYPE, la fuente es una fuente TrueType. Si no se establece ningún bit, la fuente es una fuente vectorial. Una tercera máscara, DEVICE FONTTYPE, se establece cuando un dispositivo (por ejemplo, una impresora de rayos) admite la descarga de fuentes TrueType; es cero si el dispositivo es un adaptador de pantalla, una impresora de matriz de puntos u otro dispositivo de \_ trama. Una aplicación también puede usar la máscara DEVICE FONTTYPE para distinguir las fuentes de trama proporcionadas por GDI de las fuentes \_ proporcionadas por el dispositivo. El sistema puede simular atributos de negrita, cursiva, subrayado y tachado para las fuentes de trama proporcionadas por GDI, pero no para las fuentes proporcionadas por el dispositivo.

Una aplicación también puede comprobar los bits 1 y 2 en el **miembro tmPopenAndFamily** de la estructura [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) para identificar una fuente TrueType. Si el bit 1 es 0 y el bit 2 es 1, la fuente es una fuente TrueType.

Las fuentes vectoriales se clasifican como CHARSET de OEM \_ en lugar de ANSI \_ CHARSET. Algunas aplicaciones identifican fuentes vectoriales mediante esta información, comprobando el **miembro tmCharSet** de la [**estructura NEWTEXTMETRIC.**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) Esta categorización normalmente impide que el asignador de fuentes elija fuentes vectoriales a menos que se soliciten específicamente. (La mayoría de las aplicaciones ya no usan fuentes vectoriales porque sus trazos son líneas únicas y tardan más tiempo en dibujarse que las fuentes TrueType, que ofrecen muchas de las mismas características de escalado y rotación que requerían fuentes vectoriales).

 

 
