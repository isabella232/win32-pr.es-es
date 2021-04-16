---
description: Enumera los tipos ACE definidos actualmente.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4d06b3457e4df6aea38d3e35acf4f7aaa4e2f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648327"
---
# <a name="ace"></a>PERMISO

Una **ACE** es una [*entrada de control de acceso*](/windows/desktop/SecGloss/a-gly) en una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL).

En la tabla siguiente se enumeran los tipos **ACE** definidos actualmente.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de ACE</th>
<th>Estructura</th>
<th>Tipo de ACL</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Acceso permitido</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a></td>
<td>Discrecional</td>
</tr>
<tr class="even">
<td><ul>
<li>Acceso permitido</li>
<li>Permite la devolución de llamada durante la comprobación de acceso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a></td>
<td>Discrecional</td>
</tr>
<tr class="odd">
<td><ul>
<li>Acceso permitido</li>
<li>Específico del objeto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a></td>
<td>Discrecional</td>
</tr>
<tr class="even">
<td><ul>
<li>Acceso permitido</li>
<li>Específico del objeto</li>
<li>Permite la devolución de llamada durante la comprobación de acceso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Discrecional</td>
</tr>
<tr class="odd">
<td><ul>
<li>Acceso denegado</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a></td>
<td>Discrecional</td>
</tr>
<tr class="even">
<td><ul>
<li>Acceso denegado</li>
<li>Permite la devolución de llamada durante la comprobación de acceso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a></td>
<td>Discrecional</td>
</tr>
<tr class="odd">
<td><ul>
<li>Acceso denegado</li>
<li>Específico del objeto</li>
<li>Permite la devolución de llamada durante la comprobación de acceso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a></td>
<td>Discrecional</td>
</tr>
<tr class="even">
<td><ul>
<li>Acceso denegado</li>
<li>Específico del objeto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a></td>
<td>Discrecional</td>
</tr>
<tr class="odd">
<td><ul>
<li>Alarma del sistema</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>Alarma del sistema</li>
<li>Permite la devolución de llamada durante la comprobación de acceso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>Alarma del sistema</li>
<li>Específico del objeto</li>
<li>Permite la devolución de llamada durante la comprobación de acceso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>Alarma del sistema</li>
<li>Específico del objeto</li>
</ul></td>
<td><a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>Auditoría del sistema</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>Auditoría del sistema</li>
<li>Permite la devolución de llamada durante la comprobación de acceso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="odd">
<td><ul>
<li>Auditoría del sistema</li>
<li>Específico del objeto</li>
<li>Permite la devolución de llamada durante la comprobación de acceso</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
<tr class="even">
<td><ul>
<li>Auditoría del sistema</li>
<li>Específico del objeto</li>
</ul></td>
<td><a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a></td>
<td>System</td>
</tr>
</tbody>
</table>



 

No se admiten actualmente las ACE de alarma y del sistema específico del sistema.

> [!Note]  
> Cada ACE se inicia con una estructura de [**\_ encabezado ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) . El formato de los datos que siguen al encabezado varía según el tipo de ACE especificado en el encabezado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt. h (incluye Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**\_ACE permitido de acceso \_**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ACE de acceso \_ denegado \_**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**\_ACE de alarma del sistema \_**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**\_ACE de auditoría del sistema \_**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

