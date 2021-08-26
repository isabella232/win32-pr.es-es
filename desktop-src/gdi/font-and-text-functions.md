---
description: Las siguientes funciones se usan con fuentes y texto.
ms.assetid: 69c04ed7-52da-4cb6-9fd2-f2a8c044df8b
title: Funciones de fuente y texto (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e243ea92cf8fdcecc159495102caa70f6a9a55128acf6df9c6d83e1c2b84737a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015355"
---
# <a name="font-and-text-functions-windows-gdi"></a>Funciones de fuente y texto (Windows GDI)

Las siguientes funciones se usan con fuentes y texto.



| Función                                                   | Descripción                                                                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AddFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontmemresourceex)       | Agrega una fuente incrustada a la tabla de fuentes del sistema.                                                                      |
| [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)                 | Agrega un recurso de fuente a la tabla de fuentes del sistema.                                                                       |
| [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)             | Agrega una fuente privada o no enumerable a la tabla de fuentes del sistema.                                                      |
| [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)                           | Crea una fuente lógica.                                                                                              |
| [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)           | Crea una fuente lógica a partir de una estructura .                                                                             |
| [**CreateFontIndirectEx**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirectexa)       | Crea una fuente lógica a partir de una estructura .                                                                             |
| [**Drawtext**](/windows/desktop/api/Winuser/nf-winuser-drawtext)                               | Dibuja texto con formato en un rectángulo.                                                                                 |
| [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)                           | Dibuja texto con formato en rectángulo.                                                                                   |
| [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85))             | Función de devolución de llamada definida por la aplicación que se usa [**con EnumFontFamiliesEx para**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa) procesar fuentes. |
| [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa)           | Enumera todas las fuentes del sistema con determinadas características.                                                     |
| [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)                           | Dibuja una cadena de caracteres.                                                                                            |
| [**GetAspectRatioFilterEx**](/windows/desktop/api/Wingdi/nf-wingdi-getaspectratiofilterex)   | Obtiene la configuración del filtro de relación de aspecto.                                                                        |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)               | Obtiene los anchos de caracteres consecutivos de la fuente TrueType.                                                    |
| [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata)     | Obtiene los anchos de caracteres consecutivos de la fuente actual.                                                     |
| [**GetCharABCWidthsI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsi)             | Obtiene los anchos de los índices de glifo consecutivos o de una matriz de índices de glifo de la fuente TrueType.               |
| [**GetCharacterPlacement**](/windows/desktop/api/Wingdi/nf-wingdi-getcharacterplacementa)     | Obtiene información sobre una cadena de caracteres.                                                                           |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)                   | Obtiene los anchos de caracteres consecutivos de la fuente actual.                                                     |
| [**GetCharWidthFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata)             | Obtiene los anchos fraccionales de caracteres consecutivos de la fuente actual.                                          |
| [**GetCharWidthI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthi)                     | Obtiene los anchos de índices de glifo consecutivos o una matriz de índices de glifo de la fuente actual.                     |
| [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata)                         | Obtiene los datos de métricas de una fuente TrueType.                                                                                |
| [**GetFontLanguageInfo**](/windows/desktop/api/Wingdi/nf-wingdi-getfontlanguageinfo)         | Devuelve información sobre la fuente seleccionada para un contexto de presentación.                                                   |
| [**GetFontUnicodeRanges**](/windows/desktop/api/Wingdi/nf-wingdi-getfontunicoderanges)       | Indica qué caracteres Unicode son compatibles con una fuente.                                                              |
| [**GetGlyphIndices**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphindicesa)                 | Convierte una cadena en una matriz de índices de glifo.                                                                  |
| [**GetGlyphOutline**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea)                 | Obtiene el contorno o mapa de bits de un carácter de la fuente TrueType.                                                     |
| [**GetKerningPairs**](/windows/desktop/api/WinGdi/nf-wingdi-getkerningpairsa)                 | Obtiene los pares de kerning de caracteres para una fuente.                                                                         |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)     | Obtiene las métricas de texto para las fuentes TrueType.                                                                                |
| [**GetRasterizerCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getrasterizercaps)             | Indica si las fuentes TrueType están instaladas.                                                                          |
| [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)         | Calcula el ancho y alto de una cadena de caracteres, incluidas las pestañas.                                                 |
| [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)                       | Obtiene la configuración de alineación de texto para un contexto de dispositivo.                                                                |
| [**GetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)     | Obtiene el espaciado entre caracteres actual para un contexto de dispositivo.                                                        |
| [**GetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)                       | Obtiene el color de texto de un contexto de dispositivo.                                                                            |
| [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa)       | Obtiene el número de caracteres de una cadena que cabe dentro de un espacio.                                              |
| [**GetTextExtentExPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointi)     | Obtiene el número de índices de glifo que caben dentro de un espacio.                                                       |
| [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)       | Calcula el ancho y alto de una cadena de texto.                                                                   |
| [**GetTextExtentPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpointi)         | Calcula el ancho y alto de una matriz de índices de glifo.                                                          |
| [**GetTextFace**](/windows/desktop/api/Wingdi/nf-wingdi-gettextfacea)                         | Obtiene el nombre de la fuente seleccionada en un contexto de dispositivo.                                                    |
| [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)                   | Rellena un búfer con las métricas de una fuente.                                                                          |
| [**PolyTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)                         | Dibuja varias cadenas con los colores de fuente y texto en un contexto de dispositivo.                                            |
| [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex) | Quita una fuente cuyo origen se insertó en un documento de la tabla de fuentes del sistema.                                   |
| [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)           | Quita las fuentes de un archivo de la tabla de fuentes del sistema.                                                              |
| [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)       | Quita una fuente privada o no enumerable de la tabla de fuentes del sistema.                                                 |
| [**SetMapperFlags**](/windows/desktop/api/Wingdi/nf-wingdi-setmapperflags)                   | Modifica el algoritmo utilizado para asignar fuentes lógicas a fuentes físicas.                                                    |
| [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign)                       | Establece las marcas de alineación de texto para un contexto de dispositivo.                                                                  |
| [**SetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)     | Establece el espaciado entre caracteres.                                                                                     |
| [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)                       | Establece el color del texto para un contexto de dispositivo.                                                                            |
| [**SetTextJustification**](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)       | Especifica la cantidad de espacio que el sistema debe agregar a los caracteres de interrupción de una cadena.                             |
| [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)                     | Escribe una cadena de caracteres en una ubicación, expandiendo las pestañas a los valores especificados.                                         |
| [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)                                 | Escribe una cadena de caracteres en una ubicación.                                                                             |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Estas funciones solo se proporcionan por compatibilidad con versiones de 16 bits de Windows.

-   [**CreateScalableFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-createscalablefontresourcea)
-   [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)
-   [**EnumFontFamProc**](/previous-versions//dd162621(v=vs.85))
-   [**EnumFonts**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa)
-   [**EnumFontsProc**](/previous-versions//dd162623(v=vs.85))
-   [**GetCharWidth**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidtha)
-   [**GetTextExtentPoint**](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa)

 

 
