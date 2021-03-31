---
title: Determinar las clases asociadas a una instancia de objeto
description: Cada objeto de Active Directory Domain Services tiene dos atributos cuyos valores identifican la jerarquía de clases de objeto de las que el objeto es una instancia.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486627"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Determinar las clases asociadas a una instancia de objeto

Cada objeto de Active Directory Domain Services tiene dos atributos cuyos valores identifican la jerarquía de clases de objeto de las que el objeto es una instancia.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>structuralObjectClass</strong></td>
<td>Identifica las clases estructurales y abstractas de las que el objeto es una instancia de. Por ejemplo, los valores de un objeto de usuario pueden ser:
<ul>
<li><strong>top</strong></li>
<li><strong>person</strong></li>
<li><strong>organizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifica las clases incluidas en <strong>structuralObjectClass</strong>, además de las clases auxiliares que se adjuntan dinámicamente. Por ejemplo, si una &quot; &quot; clase auxiliar de vehículo se adjunta a un objeto de usuario, los valores pueden ser:
<ul>
<li><strong>top</strong></li>
<li><strong>automóvil</strong></li>
<li><strong>person</strong></li>
<li><strong>organizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

Tenga en cuenta que ninguno de estos atributos incluye clases auxiliares que se vinculan estáticamente con las clases de objeto de las que el objeto es una instancia. Por ejemplo, la clase auxiliar **securityPrincipal** se vincula estáticamente a la clase **User** porque se incluye en los valores **systemAuxiliaryClass** del objeto **ClassSchema** del usuario; no se incluye en los atributos **objectClass** o **structuralObjectClass** de las instancias de la clase User.

 

 




