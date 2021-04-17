---
title: Funciones de edición enriquecidas
description: Funciones de edición enriquecidas
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99f776b9a08095fa66645713e107a3d66920e80f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105653206"
---
# <a name="rich-edit-functions"></a>Funciones de edición enriquecidas

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br/></td>
<td>La función <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> es una función de devolución de llamada definida por la aplicación que se usa con el mensaje de <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br/></td>
<td>La función <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> es una función de devolución de llamada definida por la aplicación que se usa con los mensajes <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> y <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> . Se utiliza para transferir un flujo de datos dentro o fuera de un control Rich Edit. El tipo <strong>EDITSTREAMCALLBACK</strong> define un puntero a esta función de devolución de llamada. <em>EditStreamCallback</em> es un marcador de posición para el nombre de la función definida por la aplicación. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br/></td>
<td>La función <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> es una función de devolución de llamada definida por la aplicación que se usa con el mensaje de <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> . Determina el índice de caracteres de la separación de palabras o la clase de caracteres y las marcas de separación de palabras de los caracteres del texto especificado. El tipo <strong>EDITWORDBREAKPROCEX</strong> define un puntero a esta función de devolución de llamada. <em>EditWordBreakProcEx</em> es un marcador de posición para el nombre de la función definida por la aplicación. <br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a><br/></td>
<td>Recupera el carácter alfanumérico matemático de formato de transformación Unicode (UTF)-32 que corresponde al carácter de plano básico multilingüe (BMP) y al estilo matemático especificados. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a><br/></td>
<td>Recupera el estilo matemático y el código de carácter de plano básico multilingüe (BMP) vertical que corresponde al byte final especificado de un par suplente matemático.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a><br/></td>
<td>La función <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> es una función de devolución de llamada definida por la aplicación que se usa con el mensaje de <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> . Determina cómo se realiza la división en guiones en un control Rich Edit de Microsoft.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br/></td>
<td>Convierte los objetos matemáticos e inline integrados en el intervalo especificado en un formato lineal.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br/></td>
<td>Convierte las matemáticas de formato lineal de un intervalo en un formulario integrado, o modifica el formulario integrado actual. <br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br/></td>
<td>Convierte los caracteres matemáticos en el intervalo especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br/></td>
<td>Registra dos nombres de clase, REListBox20W y RECombobox20W, que se pueden usar para crear ventanas de cuadro de lista o de cuadro combinado de edición enriquecida. <br/>
<blockquote>
[!Note]<br />
Diseñado para uso interno; no se recomienda para su uso en aplicaciones de. Es posible que esta función no se admita en versiones futuras.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

