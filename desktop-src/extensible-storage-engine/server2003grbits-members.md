---
description: 'Más información acerca de: miembros de Server2003Grbits'
title: Miembros de Server2003Grbits (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910230"
---
# <a name="server2003grbits-members"></a>Miembros de Server2003Grbits

Incluir miembros protegidos  
Incluir miembros heredados  

Grbits que se han agregado a la versión 2003 de Windows Server de ESENT.

El tipo [Server2003Grbits](./server2003grbits-class.md) expone los siguientes miembros.

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
<td><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></td>
<td>Si una columna determinada no está presente en el registro y tiene un valor predeterminado definido por el usuario, no se devolverá ningún valor de columna. Esta opción impedirá que se llame a la devolución de llamada que calcula el valor predeterminado definido por el usuario para la columna al enumerar los valores de esa columna.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">ForwardOnly</a></td>
<td>Esta opción solicita que la tabla temporal se cree solo si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta. Si alguna característica de la tabla temporal impidiera el uso de esta optimización, la operación producirá un error con JET_errCannotMaterializeForwardOnlySort. Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas. Consulte <a href="hh558517(v=exchg.10).md">Unique</a> para obtener más información.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Todas las transacciones confirmadas previamente por cualquier sesión que todavía no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada. Esta opción puede usarse incluso si la sesión no está actualmente en una transacción. Esta opción no se puede usar en combinación con ninguna otra opción.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Clase Server2003Grbits](./server2003grbits-class.md)

[Espacio de nombres Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
