---
description: 'Más información sobre: Método Api.RetrieveColumn'
title: Método Api.RetrieveColumn
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 392fb670cbe9f64025cd2270c52dc7bc317507821d25b3cf842d323db6ddccc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840425"
---
# <a name="apiretrievecolumn-method"></a>Método Api.RetrieveColumn

Incluir miembros protegidos  
Incluir miembros heredados  

## <a name="overload-list"></a>Lista de sobrecarga

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valor de columna única del registro actual. El registro es ese registro asociado a la entrada de índice en la posición actual del cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera un valor de columna única del registro actual. El registro es ese registro asociado a la entrada de índice en la posición actual del cursor. Como alternativa, esta función puede recuperar una columna de un registro que se crea en el búfer de copia de cursor. Esta función también puede recuperar datos de columna de una entrada de índice que hace referencia al registro actual. Además de recuperar el valor de columna real, JetRetrieveColumn también se puede usar para recuperar el tamaño de una columna, antes de recuperar los propios datos de columna para que los búferes de la aplicación se puedan dimensionar correctamente.</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[Api (clase)](./api-class.md)

[Miembros de api](./api-members.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
