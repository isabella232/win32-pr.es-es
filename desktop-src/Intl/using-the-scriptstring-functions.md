---
description: Para una aplicación que trabaja con texto sin formato, Uniscribe proporciona las funciones \* ScriptString.
ms.assetid: bfbba5df-ce06-4012-a7b1-55d8ea580942
title: Uso de las funciones ScriptString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6685af7dad2c9e1b8d0cf460d526155f967a9105e1b107047afb99c18a5124f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389411"
---
# <a name="using-the-scriptstring-functions"></a>Uso de las funciones ScriptString

Para una aplicación que trabaja con texto sin formato, Uniscribe proporciona las funciones **ScriptString \** _. Estas funciones son similares a [_ *ExtTextOut* *](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)y [**GetTextExtent,**](/cpp/mfc/reference/cdc-class#gettextextent)pero proporcionan compatibilidad completa con scripts complejos, incluida la colocación del elemento de inserción. Estas funciones son similares a las otras funciones de Uniscribe, pero se adaptan a los requisitos más sencillos del procesamiento de texto sin formato.

En la tabla siguiente se **detallan las funciones ScriptString \*** y cualquier homólogo de las otras funciones de Uniscribe.



<table>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse"><strong>ScriptStringAnalyse</strong></a></td>
<td>Analiza texto sin formato. Esta función corresponde a las funciones siguientes:<br/> <dl><a href="/windows/desktop/api/Usp10/nf-usp10-scriptitemize"><strong>ScriptItemize</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptshape"><strong>ScriptShape</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptplace"><strong>ScriptPlace</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptbreak"><strong>ScriptBreak</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptjustify"><strong>ScriptJustify</strong></a><br />
<a href="/windows/desktop/api/Usp10/nf-usp10-scriptlayout"><strong>ScriptLayout</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox"><strong>ScriptStringCPtoX</strong></a></td>
<td>Recupera la coordenada x de una posición de carácter. Esta función corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptcptox"><strong>ScriptCPtoX.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringfree"><strong>ScriptStringFree</strong></a></td>
<td>Libera una <a href="script-string-analysis.md"><strong>SCRIPT_STRING_ANALYSIS</strong></a> estructura.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths"><strong>ScriptStringGetLogicalWidths</strong></a></td>
<td>Convierte los anchos visuales en anchos lógicos. Esta función corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths"><strong>ScriptGetLogicalWidths.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder"><strong>ScriptStringGetOrder</strong></a></td>
<td>Mapas posiciones de glifo de caracteres de forma similar a <a href="/windows/desktop/api/wingdi/nf-wingdi-getcharacterplacementa">GetCharacterPlacement</a>, solo para uso heredado. Esta función no funciona bien con scripts que generan más de un glifo por punto de código.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringout"><strong>ScriptStringOut</strong></a></td>
<td>Muestra texto sin formato. Esta función corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scripttextout"><strong>ScriptTextOut.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars"><strong>ScriptString_pcOutChars</strong></a></td>
<td>Devuelve un puntero a la longitud de una cadena de texto sin formato recortada.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr"><strong>ScriptString_pLogAttr</strong></a></td>
<td>Devuelve un puntero al búfer de atributos lógicos para una cadena de texto sin formato analizada.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize"><strong>ScriptString_pSize</strong></a></td>
<td>Devuelve un puntero al tamaño (ancho y alto) de una cadena de texto sin formato analizada.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate"><strong>ScriptStringValidate</strong></a></td>
<td>Identifica secuencias de punto de código no válidas en el script dado. Esta función es diferente de <a href="/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap"><strong>ScriptGetCMap,</strong></a>que identifica los puntos de código que no están presentes en una fuente.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp"><strong>ScriptStringXtoCP</strong></a></td>
<td>Convierte una coordenada x en una posición de carácter. Esta función corresponde a <a href="/windows/desktop/api/Usp10/nf-usp10-scriptxtocp"><strong>ScriptXtoCP.</strong></a></td>
</tr>
</tbody>
</table>

Para mostrar solo texto sin formato sin modificaciones, una aplicación debe llamar a [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse), [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)y, a continuación, [**a ScriptStringFree.**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) Las demás funciones se usan para modificar el texto sin formato antes de mostrarse.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
