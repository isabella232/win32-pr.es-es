---
description: 'Más información sobre: constantes de control de errores'
title: Constantes de control de errores
TOCTitle: Error Handling Constants
ms:assetid: 5a1f9438-2d36-483e-9820-d0de30ee5e01
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269258(v=EXCHG.10)
ms:contentKeyID: 32765560
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
ms.openlocfilehash: 1ab59a8e0c721558e5c056d25798c5d1273bd86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707333"
---
# <a name="error-handling-constants"></a>Constantes de control de errores


_**Se aplica a:** Windows | Windows Server_

## <a name="error-handling-constants"></a>Constantes de control de errores

Las constantes siguientes se utilizan para establecer el intervalo para los parámetros del sistema [JET_paramExceptionAction](./error-handling-parameters.md) .

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
<td><p>JET_ExceptionMsgBox<br />
0x0001</p></td>
<td><p>Muestra un cuadro de mensaje cuando se produce una excepción.</p></td>
</tr>
<tr class="even">
<td><p>JET_ExceptionNone<br />
0x0002</p></td>
<td><p>No hace nada cuando se produce una excepción.</p></td>
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

[Parámetros de control de errores](./error-handling-parameters.md)
