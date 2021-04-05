---
description: 'WMI tiene constantes de seguridad usadas para la comprobación de acceso del espacio de nombres de \_ \_ SystemSecurity:: GetCallerAccessRights.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Constantes de derechos de acceso de espacio de nombres (Wbemcli. h)
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
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104081976"
---
# <a name="namespace-access-rights-constants"></a>Constantes de derechos de acceso de espacio de nombres

WMI tiene constantes de seguridad usadas para la comprobación de acceso del espacio de nombres de [**\_ \_ SystemSecurity:: GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md). Para obtener información de seguridad acerca de las listas de control de acceso (ACL, DACL o SACL), consulte [listas de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [**derechos de acceso estándar**](/windows/desktop/SecAuthZ/standard-access-rights). Estas constantes se definen en la enumeración de **\_ \_ marcas de seguridad WBEM** .

<dl> <dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**\_Habilitar WBEM**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Habilita la cuenta y concede al usuario permisos de lectura. Este es un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso habilitar cuenta en la pestaña seguridad del [*control WMI*](gloss-w.md). Para obtener más información, vea [establecer la seguridad del espacio de nombres con el control WMI](setting-namespace-security-with-the-wmi-control.md).


</dt> </dl> </dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**\_ejecución del método WBEM \_**
</dt> <dd> <dl> <dt>

2 (0X2)
</dt> <dt>



Permite la ejecución de métodos. Los proveedores pueden realizar comprobaciones de acceso adicionales. Este es un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso ejecutar métodos en la pestaña seguridad del control WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**\_rellenado completo de WBEM \_ \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Permite que una cuenta de usuario escriba en las clases del repositorio WMI, así como en las instancias. Un usuario no puede escribir en las clases del sistema. Solo los miembros del grupo administradores tienen este permiso. **WBEM \_ El \_ \_ representante de escritura completo** corresponde al permiso de escritura completo en la pestaña seguridad del control WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_representación parcial de la \_ escritura de WBEM \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Permite escribir datos solo en instancias, no en clases. Un usuario no puede escribir clases en el [*repositorio WMI*](gloss-w.md). Solo los miembros del grupo administradores tienen este derecho. **WBEM \_ La \_ \_ representación de escritura parcial** corresponde al permiso de escritura parcial en la pestaña seguridad del control WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_proveedor de escritura WBEM \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Permite escribir clases e instancias en los proveedores. Tenga en cuenta que los proveedores pueden realizar comprobaciones de acceso adicionales al suplantar a un usuario. Este es un derecho de acceso predeterminado para todos los usuarios y corresponde al permiso de escritura de proveedor en la pestaña seguridad del control WMI.


</dt> </dl> </dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_acceso remoto de WBEM \_**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Permite que una cuenta de usuario realice de forma remota las operaciones permitidas por los permisos descritos anteriormente. Solo los miembros del grupo administradores tienen este derecho. **WBEM \_ El \_ acceso remoto** corresponde al permiso Remote enable en la pestaña seguridad del control WMI.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[Proteger los espacios de nombres de WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

