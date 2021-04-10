---
description: configuración regional \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153746"
---
# <a name="locale_idigitsubstitution"></a>configuración regional \_ IDIGITSUBSTITUTION

**Windows 2000:** Forma de dígitos. Por ejemplo, los dígitos árabe, tailandés y hindú tienen formas clásicas diferentes de los dígitos europeos. En el caso de las configuraciones regionales con la [configuración regional \_ SNATIVEDIGITS](locale-snative-constants.md) especificada como valores distintos del ASCII 0-9, este valor especifica si se debe dar preferencia a esos otros dígitos para la presentación. Por ejemplo, si se elige un valor de 2, siempre se usan los dígitos especificados por SNATIVEDIGITS de configuración regional \_ . Si se elige 1, siempre se usan los dígitos ASCII 0-9. Si se elige 0, se utiliza ASCII en algunas circunstancias y los dígitos especificados por la configuración regional \_ SNATIVEDIGITS se usan en otros, dependiendo del contexto.



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
<td>0</td>
<td>Sustitución basada en contexto. Los dígitos se muestran en función del texto anterior en el mismo resultado. Los dígitos europeos siguen los alfabetos latinos, Arabic-Indic dígitos siguen el texto árabe y otros dígitos nacionales siguen el texto escrito en otros distintos scripts. Cuando no hay texto anterior, la configuración regional y el orden de lectura mostrado determinan la sustitución de dígitos, tal como se muestra en la tabla siguiente.
<table>
<thead>
<tr class="header">
<th>Configuración regional</th>
<th>Orden de lectura</th>
<th>Dígitos usados</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Árabe</td>
<td>De derecha a izquierda</td>
<td>Arabic-Indic</td>
</tr>
<tr class="even">
<td>Tailandés</td>
<td>De izquierda a derecha</td>
<td>Dígitos tailandeses</td>
</tr>
<tr class="odd">
<td>Todos los demás</td>
<td>Any</td>
<td>No se utiliza ninguna sustitución</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>1</td>
<td>No se utiliza ninguna sustitución. Compatibilidad completa con Unicode.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Sustitución de dígitos nativa. Las formas nacionales se muestran según LOCALE_SNATIVEDIGITS.</td>
</tr>
</tbody>
</table>



 

 

 



