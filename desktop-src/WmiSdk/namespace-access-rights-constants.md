---
description: WMI tiene constantes de seguridad que \_ SystemSecurity::GetCallerAccessRights usa para comprobar el acceso al espacio de \_ nombres.
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Constantes de derechos de acceso de espacio de nombres (Wbemcli.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 6c23bcde9d085a6668fd5c57ee0ff51a7db61784de44d79080e2b2d2d1ee051f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992755"
---
# <a name="namespace-access-rights-constants"></a>Constantes de derechos de acceso de espacio de nombres

WMI tiene constantes de seguridad que [**\_ \_ SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)usa para comprobar el acceso al espacio de nombres. Para obtener información de seguridad sobre las listas de control de acceso (ACL, DACL o SACL), vea Listas de Access Control [(ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [**Derechos de acceso estándar.**](/windows/desktop/SecAuthZ/standard-access-rights) Estas constantes se definen en la **enumeración WBEM \_ SECURITY \_ FLAGS.**

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ENABLE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Habilita la cuenta y concede al usuario permisos de lectura. Se trata de un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso Habilitar cuenta en la ficha Seguridad del [*control WMI*](gloss-w.md). Para obtener más información, vea [Establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ METHOD \_ EXECUTE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Permite la ejecución de métodos. Los proveedores pueden realizar comprobaciones de acceso adicionales. Se trata de un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso Ejecutar métodos en la ficha Seguridad del control WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ FULL \_ WRITE \_ REP**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Permite que una cuenta de usuario escriba en clases del repositorio WMI, así como en instancias de . Un usuario no puede escribir en clases del sistema. Solo los miembros del grupo Administradores tienen este permiso. **WBEM \_ FULL \_ WRITE \_ REP** corresponde al permiso De escritura completa en el ficha Seguridad del control WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ PARTIAL \_ WRITE \_ REP**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Permite escribir datos solo en instancias, no en clases. Un usuario no puede escribir clases en el [*repositorio WMI*](gloss-w.md). Solo los miembros del grupo Administradores tienen este derecho. **WBEM \_ PARTIAL \_ WRITE \_ REP corresponde** al permiso De escritura parcial en la ficha Seguridad del control WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ WRITE \_ PROVIDER**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Permite escribir clases e instancias en proveedores. Tenga en cuenta que los proveedores pueden realizar comprobaciones de acceso adicionales al suplantar a un usuario. Se trata de un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso De escritura del proveedor en ficha Seguridad del control WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ REMOTE \_ ACCESS**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Permite que una cuenta de usuario realice de forma remota las operaciones permitidas por los permisos descritos anteriormente. Solo los miembros del grupo Administradores tienen este derecho. **WBEM \_ REMOTE \_ ACCESS** corresponde al permiso Remote Enable en el ficha Seguridad del control WMI.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wbemcli.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de seguridad WMI](wmi-security-constants.md)
</dt> <dt>

[Protección de espacios de nombres WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

