---
description: Enumera los tipos ace definidos actualmente.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa93490c4cf74ac33e3b15eeb888f011f81aa2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073734"
---
# <a name="ace"></a>AS

Una **ACE es** una entrada de control de [*acceso*](/windows/desktop/SecGloss/a-gly) en una lista de control [*de acceso*](/windows/desktop/SecGloss/a-gly) (ACL).

En la tabla siguiente se enumeran los tipos **ace** definidos actualmente.




| Tipo ace | Estructura | Tipo de ACL | 
|----------|-----------|----------|
| <ul><li>Acceso permitido</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a> | Discrecional | 
| <ul><li>Acceso permitido</li><li>Permite la devolución de llamada durante la comprobación de acceso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a> | Discrecional | 
| <ul><li>Acceso permitido</li><li>Específico del objeto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a> | Discrecional | 
| <ul><li>Acceso permitido</li><li>Específico del objeto</li><li>Permite la devolución de llamada durante la comprobación de acceso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a> | Discrecional | 
| <ul><li>Acceso denegado</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a> | Discrecional | 
| <ul><li>Acceso denegado</li><li>Permite la devolución de llamada durante la comprobación de acceso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a> | Discrecional | 
| <ul><li>Acceso denegado</li><li>Específico del objeto</li><li>Permite la devolución de llamada durante la comprobación de acceso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a> | Discrecional | 
| <ul><li>Acceso denegado</li><li>Específico del objeto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a> | Discrecional | 
| <ul><li>Alarma del sistema</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a> | Sistema | 
| <ul><li>Alarma del sistema</li><li>Permite la devolución de llamada durante la comprobación de acceso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a> | Sistema | 
| <ul><li>Alarma del sistema</li><li>Específico del objeto</li><li>Permite la devolución de llamada durante la comprobación de acceso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Alarma del sistema</li><li>Específico del objeto</li></ul> | <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Auditoría del sistema</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a> | Sistema | 
| <ul><li>Auditoría del sistema</li><li>Permite la devolución de llamada durante la comprobación de acceso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a> | Sistema | 
| <ul><li>Auditoría del sistema</li><li>Específico del objeto</li><li>Permite la devolución de llamada durante la comprobación de acceso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Auditoría del sistema</li><li>Específico del objeto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a> | Sistema | 




 

Actualmente no se admiten las ACE de alarma del sistema y de alarma del sistema específicas del objeto.

> [!Note]  
> Cada ACE comienza con una [**estructura \_ ACE HEADER.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) El formato de los datos que sigue al encabezado varía según el tipo ace especificado en el encabezado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Winnt.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**ACE \_ DE \_ ACCESO PERMITIDO**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ACE \_ DE ACCESO \_ DENEGADO**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**ACE \_ DE ALARMA DEL \_ SISTEMA**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**ACE \_ DE AUDITORÍA DEL \_ SISTEMA**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

