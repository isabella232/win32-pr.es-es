---
description: Un número de Factoids describe la entrada que es común a todos los reconocedores de lenguaje y no necesita tener formatos diferentes para distintos idiomas. En la tabla siguiente se enumeran los Factoids comunes a todos los lenguajes.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids común entre idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1faefbb9991562535f711f867c45bd614c595941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705705"
---
# <a name="factoids-common-across-languages"></a>Factoids común entre idiomas

Un número de Factoids describe la entrada que es común a todos los reconocedores de lenguaje y no necesita tener formatos diferentes para distintos idiomas. En la tabla siguiente se enumeran los Factoids comunes a todos los lenguajes.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Factoid</th>
<th>Definición</th>
<th>Ejemplos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Cifra</strong></td>
<td>Establece la diferencia para un solo dígito. El reconocedor se sesga para devolver solo los dígitos únicos cuando se establece este valor de Factoid.<br/></td>
<td>0-9<br/></td>
</tr>
<tr class="even">
<td><strong>Correo electrónico</strong></td>
<td>Establece la diferencia de una dirección de correo electrónico.<br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><strong>Web</strong></td>
<td>Establece la diferencia para varios formatos de dirección URL.<br/>
<blockquote>
[!Note]<br />
La configuración predeterminada del reconocedor incluye la Factoid <strong>Web</strong> . Por este motivo, es posible que no note una gran diferencia entre el Factoid <strong>Web</strong> y el valor predeterminado. Sin embargo, la Factoid <strong>Web</strong> ayuda a eliminar los espacios entre las palabras de una dirección URL.
</blockquote>
<br/></td>
<td>http: \\ Microsoft.net<br/> https://microsoft.us/<br/> https: \\ www.Microsoft.au \<br/> https://microsoft.com<br/> www.microsoft_world. com<br/> www.microsoft.us \<br/> http: \\www.microsoft.com\myfile.htm<br/> http: \\www.microsoft.com\myfile.html<br/> http: \\ www. Microsoft. com\myfile.asp<br/> http: \\ www.Microsoft.uk<br/> http: \\ www.Microsoft.info<br/> www.microsoft.biz<br/></td>
</tr>
<tr class="even">
<td><strong>Valor predeterminado</strong></td>
<td>Devuelve el reconocedor a su configuración predeterminada.<br/></td>
<td>La configuración predeterminada de Factoids para idiomas occidentales incluye el Diccionario del sistema, el Diccionario del usuario, varios signos de puntuación, y el <strong>Web</strong> y el <strong>número</strong> Factoids.<br/> La configuración predeterminada de Factoids para idiomas de Asia oriental incluye todos los caracteres admitidos por el reconocedor.<br/></td>
</tr>
<tr class="odd">
<td><strong>None</strong></td>
<td>Deshabilita todos los Factoids, diccionarios y el modelo de lenguaje.<br/></td>
<td>Este Factoid solo debe usarse cuando no se desea que el reconocedor use ninguna regla o Diccionario de gramática, incluido el Diccionario del sistema. Este Factoid es útil para la entrada de cadenas aleatorias como códigos de producto. No use la marca coerción con este Factoid.<br/></td>
</tr>
</tbody>
</table>



 

 

 




