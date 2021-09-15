---
description: 'Más información sobre: Campos Server2003Grbits'
title: Campos Server2003Grbits (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ed7a99118674d955fc6a882ac08407e45837af77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360104"
---
# <a name="server2003grbits-fields"></a>Campos Server2003Grbits

Incluir miembros protegidos  
Incluir miembros heredados  

El [tipo Server2003Grbits](./server2003grbits-class.md) expone los miembros siguientes.

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
<td>Esta opción solicita que la tabla temporal solo se cree si el administrador de tablas temporales puede usar la implementación optimizada para los resultados intermedios de la consulta. Si alguna característica de la tabla temporal impediría el uso de esta optimización, se producirá un error en la operación JET_errCannotMaterializeForwardOnlySort. Un efecto secundario de esta opción es permitir que la tabla temporal contenga registros con claves de índice duplicadas. Consulte <a href="hh558517(v=exchg.10).md">Único</a> para obtener más información.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo público" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Todas las transacciones confirmadas previamente por cualquier sesión que aún no se hayan vaciado en el archivo de registro de transacciones se vaciarán inmediatamente. Esta API esperará hasta que se hayan vaciado las transacciones antes de volver al autor de la llamada. Esta opción se puede usar incluso si la sesión no está actualmente en una transacción. Esta opción no se puede usar en combinación con ninguna otra opción.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Server2003Grbits (clase)](./server2003grbits-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
