---
description: 'Más información acerca de: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666257"
---
# <a name="jet_snp"></a>JET_SNP


_**Se aplica a:** Windows | Windows Server_

## <a name="jet_snp"></a>JET_SNP

El **JET_SNP** grupo de constantes describe el tipo de la operación para la que se va a obtener información de progreso. Estas constantes se utilizan como el parámetro *SNP* de la función de devolución de llamada [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante o valor</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_snpRepair<br />
2</p></td>
<td><p>La devolución de llamada es para una operación de reparación.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpCompact<br />
4</p></td>
<td><p>La devolución de llamada es para desfragmentación de la base de datos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpRestore<br />
8</p></td>
<td><p>La devolución de llamada es para una operación de restauración.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpBackup<br />
9</p></td>
<td><p>La devolución de llamada es para una operación de copia de seguridad.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgrade<br />
10</p></td>
<td><p>No se admite.</p>
<p><strong>Windows 2000:</strong>  La devolución de llamada es para la operación de actualización del formato de la base de datos.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpScrub<br />
11</p></td>
<td><p>La devolución de llamada es para una operación de ceros de base de datos (es decir, limpieza).</p>
<p><strong>Windows server 2003 y windows 2000 Server:</strong>  No compatible.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgradeRecordFormat<br />
12</p></td>
<td><p>La devolución de llamada es para el proceso de actualización del formato de registro de todas las páginas de base de datos.</p>
<p><strong>Windows server 2003 y windows 2000 Server:</strong>  No compatible.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requiere Windows Vista, Windows XP o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Declarado en esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte también

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
