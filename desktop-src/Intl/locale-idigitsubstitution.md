---
description: LOCALE \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6288da45212d55bdc5ad505e432cfb848ad9bdf6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631913"
---
# <a name="locale_idigitsubstitution"></a>LOCALE \_ IDIGITSUBSTITUTION

**Windows 2000:** Forma de dígitos. Por ejemplo, los dígitos árabe, tailandés e indic tienen formas clásicas diferentes de los dígitos europeos. Para las configuraciones regionales con [LOCALE \_ SNATIVEDIGITS](locale-snative-constants.md) especificados como valores distintos de ASCII 0-9, este valor especifica si se debe dar preferencia a esos otros dígitos con fines de presentación. Por ejemplo, si se elige un valor de 2, siempre se usan los dígitos especificados por LOCALE \_ SNATIVEDIGITS. Si se elige un 1, siempre se usan los dígitos ASCII 0-9. Si se elige un 0, ascii se usa en algunas circunstancias y los dígitos especificados por LOCALE SNATIVEDIGITS se usan en otras, dependiendo \_ del contexto.



<table>
<colgroup>
<col  />
<col  />
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
<td>Sustitución basada en contexto. Los dígitos se muestran en función del texto anterior en la misma salida. Los dígitos europeos siguen los scripts latinos, Arabic-Indic los dígitos siguen el texto árabe y otros dígitos nacionales siguen el texto escrito en otros scripts. Cuando no hay texto anterior, la configuración regional y el orden de lectura mostrados determinan la sustitución de dígitos, como se muestra en la tabla siguiente.
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
<td>No se usa ninguna sustitución</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>1</td>
<td>No se usa ninguna sustitución. Compatibilidad completa con Unicode.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Sustitución de dígitos nativos. Las formas nacionales se muestran según LOCALE_SNATIVEDIGITS.</td>
</tr>
</tbody>
</table>



 

 

 



