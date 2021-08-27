---
description: 'Más información sobre: Miembros de VistaGrbits'
title: Miembros vistaGrbits (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: be9908627d4351ec710fa6b1791d24779ab501b8e61bb342d96a3a0ec4afa87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978165"
---
# <a name="vistagrbits-members"></a>Miembros de VistaGrbits

Incluir miembros protegidos  
Incluir miembros heredados  

Grbits que se han agregado a la versión vista de ESENT.

El [tipo VistaGrbits](./vistagrbits-class.md) expone los miembros siguientes.

## <a name="fields"></a>Campos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></td>
<td>La sesión de instantáneas continúa después de JetOSSnapshotThaw y requerirá una llamada a la función JetOSSnapshotEnd.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></td>
<td>Si se especifica esta marca para un índice que tiene más de una columna de clave que es una columna con varios valores, se creará una entrada de índice para cada resultado de un producto cruzado de todos los valores de esas columnas de clave. De lo contrario, el índice solo tendría una entrada para cada valor múltiple en la columna de clave más significativa que es una columna con varios valores y cada una de esas entradas de índice usaría el primer valor múltiple de cualquier otra columna de clave que sea de varias columnas con varios valores. Por ejemplo, si especificó esta marca para un índice sobre la columna A que tiene los valores rojo y azul y sobre la columna B que tiene los valores 1 y 2, se crearían las siguientes entradas de &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; índice: &quot; red , &quot; &quot; 1 &quot; ; &quot; rojo, &quot; &quot; 2 &quot; ; &quot; blue &quot; , &quot; 1 &quot; ; &quot; azul, &quot; &quot; 2 &quot; . De lo contrario, se crearían las siguientes entradas de índice: &quot; &quot; rojo, &quot; 1 &quot; ; &quot; azul, &quot; &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></td>
<td>Si se especifica esta marca, se producirá un error en cualquier actualización del índice que provocaría un error en una clave truncada con <a href="hh564840(v=exchg.10).md">KeyTruncated</a>. De lo contrario, las claves se truncarán en modo silencioso.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></td>
<td>Indexe sobre varias columnas con varios valores, pero solo con valores de la misma itagSequence.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></td>
<td>Los registros de transacciones deben existir en el directorio del archivo de registro (es decir, no se puede iniciar automáticamente una nueva secuencia).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></td>
<td>Realice la recuperación, pero detenga en la fase de deshacer. Permite reproducir todos los registros presentes y, a continuación, se pueden copiar y reproducir registros adicionales.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></td>
<td>Falta la entrada del mapa de base de datos de forma predeterminada en la misma ubicación.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">TruncateDone</a></td>
<td>El motor puede marcar los encabezados de base de datos según corresponda (por ejemplo, una copia de seguridad completa completada), aunque no se haya completado la llamada para truncar.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></td>
<td>Si la recuperación automática se realiza correctamente, trunca los archivos de registro.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[VistaGrbits (clase)](./vistagrbits-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
