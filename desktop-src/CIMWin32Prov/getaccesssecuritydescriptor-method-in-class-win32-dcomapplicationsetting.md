---
description: Obtiene el descriptor de seguridad que controla quién puede acceder a una aplicación DCOM.
ms.assetid: 5ddd563b-f731-47ac-8a13-20940adfa86d
ms.tgt_platform: multiple
title: Método GetAccessSecurityDescriptor de la Win32_DCOMApplicationSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 326b68eebfdf5ffe785d0d94849c46d03fd3e40e3713e8ab0469d663d26b55da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077635"
---
# <a name="getaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Método GetAccessSecurityDescriptor de la clase \_ DCOMApplicationSetting de Win32

El **método WMI GetAccessSecurityDescriptor** obtiene el descriptor de seguridad que controla quién puede acceder a una aplicación DCOM. El descriptor de seguridad es una instancia de la [**clase \_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) La cuenta que ejecuta el script o la aplicación que llama a este método debe tener los privilegios **SeSecurityPrivilege** y **SeRestorePrivilege.** Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetAccessSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descriptor* \[ out\]
</dt> <dd>

Descriptor de seguridad que se establece para la aplicación DCOM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error. Para obtener más información, vea [Códigos de retorno de WMI](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Success**
</dt> <dd>

0

Completado correctamente.

</dd> <dt>

**2**
</dt> <dd>

El usuario no tiene acceso a la información solicitada

</dd> <dt>

**8**
</dt> <dd>

Error desconocido

</dd> <dt>

**9**
</dt> <dd>

El usuario no tiene los privilegios adecuados para ejecutar el método

</dd> <dt>

**21**
</dt> <dd>

Un parámetro especificado en la llamada al método no es válido

</dd> <dt>

**Otros**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentarios

La [**instancia de \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos SECURITY DESCRIPTOR [**\_ \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) y una lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL). Para obtener más información, [vea Access Control enumeración](/windows/desktop/SecAuthZ/access-control-lists).

Si **se concede o se habilita SeSecurityPrivilege** al obtener un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto. Para obtener más información, vea [**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [Ejecución de operaciones con privilegios.](/windows/desktop/WmiSdk/executing-privileged-operations)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)
</dt> <dt>

[**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

