---
title: Errores comunes (AD DS)
description: La tabla siguiente contiene una lista de errores comunes que pueden producirse en función del ámbito del grupo que se anida.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- ANUNCIOS de errores comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "104487251"
---
# <a name="common-errors-ad-ds"></a>Errores comunes (AD DS)

La tabla siguiente contiene una lista de errores comunes que pueden producirse en función del ámbito del grupo que se anida.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>HRESULT</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x8007001F</td>
<td>Error general. Este error se produce si intenta:
<ul>
<li>Agregue un grupo local de dominio a un grupo global o universal o a un grupo local de dominio de otro dominio. Los grupos locales de dominio solo se pueden agregar como miembros a otros grupos locales de dominio del mismo dominio.</li>
<li>Agregue un grupo universal a un grupo global. Los grupos universales se pueden agregar a grupos locales de dominio y universales, pero no a grupos globales.</li>
</ul></td>
</tr>
<tr class="even">
<td>0x8007202F</td>
<td><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>. Este error se produce si intenta agregar un grupo de seguridad a otro grupo en un dominio que se ejecuta en modo mixto. Los grupos de seguridad no se pueden anidar en modo mixto; los grupos de seguridad solo se pueden anidar en modo nativo.</td>
</tr>
</tbody>
</table>



 

 

 




