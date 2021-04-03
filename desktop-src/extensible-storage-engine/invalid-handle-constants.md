---
description: 'Más información sobre: constantes de identificador no válidas'
title: Constantes de identificador no válidas
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083278"
---
# <a name="invalid-handle-constants"></a>Constantes de identificador no válidas


_**Se aplica a:** Windows | Windows Server_

## <a name="invalid-handle-constants"></a>Constantes de identificador no válidas

Las constantes siguientes indican controladores no válidos para distintos aspectos de ESE.

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
<td><p>JET_instanceNil<br />
(~ (JET_INSTANCE) 0)</p></td>
<td><p>Identificador no válido para una instancia de base de datos.<br />
<strong>Windows XP:</strong> Introducido en Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_sesidNil<br />
(~ (JET_SESID) 0)</p></td>
<td><p>Identificador no válido para un identificador de sesión.</p></td>
</tr>
<tr class="odd">
<td><p>JET_tableidNil<br />
(~ (JET_TABLEID) 0)</p></td>
<td><p>Identificador no válido para un ID. de tabla.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNil<br />
((JET_GRBIT) 0)</p></td>
<td><p>Identificador no válido para un grupo de bits.</p></td>
</tr>
<tr class="odd">
<td><p>JET_LSNil<br />
(~ (JET_LS) 0)</p></td>
<td><p>Identificador no válido para el almacenamiento local.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbidNil<br />
((JET_DBID) 0xFFFFFFFF)</p></td>
<td><p>Identificador no válido para el identificador de base de datos.</p></td>
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

