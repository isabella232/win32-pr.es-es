---
description: WMI define un conjunto de propiedades del sistema que están asociadas a todas las clases e instancias de clases, además de a las propiedades específicas de la clase.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Propiedades del sistema CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716206"
---
# <a name="cim-system-properties-for-mib-objects"></a>Propiedades del sistema CIM para objetos MIB

WMI define un conjunto de propiedades del sistema que están asociadas a todas las clases e instancias de clases, además de a las propiedades específicas de la clase.

> [!Note]  
> Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

El proveedor SNMP utiliza las siguientes propiedades del sistema CIM al asignar definiciones de objeto MIB a definiciones de clase CIM. Deben existir propiedades obligatorias para que el proveedor SNMP resuelva por completo un objeto de grupo. Si no se define una propiedad obligatoria, se devuelve un error.



<table>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>__CLASS</strong></td>
<td><strong>cadena</strong> Obligación<br/> En el caso de las instancias, la clase a la que pertenece el objeto. En el caso de las clases, es el nombre de clase.<br/></td>
</tr>
<tr class="even">
<td><strong>__DYNASTY</strong></td>
<td><strong>cadena</strong> Opta<br/> Nombre de la clase que es la clase base Ultimate del objeto actual (no su clase primaria inmediata).<br/></td>
</tr>
<tr class="odd">
<td><strong>__GENUS</strong></td>
<td><strong>UInt32</strong> Obligación<br/> Tipo de objeto. Los valores son:<br/> <dl> 1 = clase<br />
2 = instancia<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>__NAMESPACE</strong></td>
<td><strong>cadena</strong> Obligación<br/> Espacio de nombres donde se encuentra el objeto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__PATH</strong></td>
<td><strong>cadena</strong> Obligación<br/> Ruta de acceso absoluta al objeto.<br/></td>
</tr>
<tr class="even">
<td><strong>__PROPERTYCOUNT</strong></td>
<td><strong>UInt32</strong> Obligación<br/> Número de propiedades que no son del sistema definidas para el objeto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__RELPATH</strong></td>
<td><strong>cadena</strong> Obligación<br/> Ruta de acceso relativa al objeto.<br/></td>
</tr>
<tr class="even">
<td><strong>__SERVER</strong></td>
<td><strong>cadena</strong> Obligación<br/> Servidor que proporciona el objeto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__SUPERCLASS</strong></td>
<td><strong>cadena</strong> Opta<br/> Clase primaria inmediata del objeto.<br/></td>
</tr>
</tbody>
</table>



 

 

 




