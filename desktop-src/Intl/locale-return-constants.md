---
description: '\_Constantes devueltas por la configuración regional \*'
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Constantes de LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d3e5017a6463457b7bc36358e9956365430c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278610"
---
# <a name="locale_return-constants"></a>\_Constantes devueltas por la configuración regional \*

En este tema se definen las \_ constantes de retorno de la configuración regional \* utilizadas por NLS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LOCALE_RETURN_GENITIVE_NAMES</td>
<td><strong>Windows 7 y versiones posteriores:</strong> Recupere los nombres de genitivo de los meses, que son los nombres que se usan cuando los nombres de los meses se combinan con otros elementos. Por ejemplo, en ucraniano, el equivalente de enero se escribe &quot; Січень &quot; cuando el mes se denomina por sí solo. Sin embargo, cuando el nombre del mes se usa en combinación, por ejemplo, en una fecha como el 5 de enero de 2003, se usa la forma genitivo del nombre. En el ejemplo ucraniano, el nombre del mes en genitivo se muestra como &quot; 5 січня 2003 &quot; . La lista de nombres de meses de genitivo comienza con enero y está delimitada por signos de punto y coma. Si no hay 13 meses, use un punto y coma en su lugar al final de la lista.
<blockquote>
[!Note]<br />
Los nombres de mes de genitivo no existen en todos los idiomas.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>LOCALE_RETURN_NUMBER</td>
<td><strong>Windows Me/98, Windows NT 4,0 y versiones posteriores:</strong> Recupere un número. Esta constante provoca que <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> o <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> recuperen un valor como un número en lugar de como una cadena. El búfer que recibe el valor debe ser al menos la longitud de un valor DWORD. Esta constante se puede combinar con cualquier otra constante que tenga un nombre que comience por &quot; LOCALE_I &quot; .</td>
</tr>
</tbody>
</table>



 

 

 




