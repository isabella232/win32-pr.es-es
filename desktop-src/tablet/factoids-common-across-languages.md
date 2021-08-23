---
description: Una serie de factoids describen la entrada que es común a todos los reconocedores de idioma y no necesitan tener formatos diferentes para distintos idiomas. En la tabla siguiente se enumeran los factoids que son comunes en todos los lenguajes.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids Common Across Languages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3424396f5c102fb7db911e8fc8a45c45a3bd26f040d53c2a955b74a16f818c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597385"
---
# <a name="factoids-common-across-languages"></a>Factoids Common Across Languages

Una serie de factoids describen la entrada que es común a todos los reconocedores de idioma y no necesitan tener formatos diferentes para distintos idiomas. En la tabla siguiente se enumeran los factoids que son comunes en todos los lenguajes.



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
<td><strong>Dígitos</strong></td>
<td>Establece el sesgo de un solo dígito. El reconocedor está sesgado hacia la devolución de solo dígitos cuando se establece este factoid.<br/></td>
<td>0-9<br/></td>
</tr>
<tr class="even">
<td><strong>Correo electrónico</strong></td>
<td>Establece el sesgo de una dirección de correo electrónico.<br/></td>
<td>someone@example.com<br/></td>
</tr>
<tr class="odd">
<td><strong>Web</strong></td>
<td>Establece el sesgo para varios formatos de dirección URL.<br/>
<blockquote>
[!Note]<br />
La configuración predeterminada para el reconocedor incluye el <strong>elemento factoid</strong> web. Por este problema, es posible que no observe una gran diferencia entre el elemento <strong>factoid web</strong> y la configuración predeterminada. Sin embargo, el <strong>elemento factoid</strong> web ayuda a eliminar los espacios entre las palabras de una dirección URL.
</blockquote>
<br/></td>
<td>http: \\ microsoft.net<br/> https://microsoft.us/<br/> https: \\ www.microsoft.au\<br/> https://microsoft.com<br/> www.microsoft_world.com<br/> www.microsoft.us\<br/> http: \\www.microsoft.com\myfile.htm<br/> http: \\www.microsoft.com\myfile.html<br/> http: \\ www.microsoft.com\myfile.asp<br/> http: \\ www.microsoft.uk<br/> http: \\ www.microsoft.info<br/> www.microsoft.biz<br/></td>
</tr>
<tr class="even">
<td><strong>Predeterminado</strong></td>
<td>Devuelve el reconocedor a su configuración predeterminada.<br/></td>
<td>La configuración predeterminada de factoids para idiomas del oeste incluye el diccionario del sistema, el diccionario de usuarios, varios signos de puntuación y los factoids <strong>Web</strong> y <strong>Number.</strong><br/> La configuración predeterminada de factoids para idiomas de Asia Oriental incluye todos los caracteres admitidos por el reconocedor.<br/></td>
</tr>
<tr class="odd">
<td><strong>None</strong></td>
<td>Deshabilita todos los factoids, diccionarios y el modelo de lenguaje.<br/></td>
<td>Este factoid solo debe usarse cuando no quiera que el reconocedor use reglas de gramática o diccionarios, incluido el diccionario del sistema. Este factoid es útil para la entrada de cadenas aleatorias, como códigos de producto. No use la marca Coerce con este factoid.<br/></td>
</tr>
</tbody>
</table>



 

 

 




