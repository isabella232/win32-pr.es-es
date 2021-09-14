---
description: Actualiza el descriptor de seguridad de inicio de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de una clase \_ SecurityDescriptor de Win32.
ms.assetid: 72245d22-1a0a-4069-b5d6-9d59e4de4aab
ms.tgt_platform: multiple
title: Método SetLaunchSecurityDescriptor de la Win32_DCOMApplicationSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetLaunchSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a99919246d7b36aa265d36ae0f75e8347ea6a25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174066"
---
# <a name="setlaunchsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a>Método SetLaunchSecurityDescriptor de la clase \_ DCOMApplicationSetting de Win32

El **método SetLaunchSecurityDescriptor** actualiza el descriptor de seguridad de inicio de la aplicación DCOM con un nuevo descriptor de seguridad definido por una instancia de una clase [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Este descriptor de seguridad controla quién puede iniciar la aplicación. La cuenta que ejecuta el script o la aplicación que llama a este método debe tener los privilegios **SeSecurityPrivilege** y **SeRestorePrivilege.** Para obtener más información, vea [Cambiar la seguridad de acceso en objetos protegibles.](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetLaunchSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descriptor* \[ En\]
</dt> <dd>

Descriptor de seguridad para establecer que controla quién puede iniciar la aplicación DCOM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error. Para obtener más información, vea [Códigos de retorno wmi](/windows/desktop/WmiSdk/wmi-return-codes) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Success**
</dt> <dd>

0

Finalización correcta.

</dd> <dt>

**2**
</dt> <dd>

El usuario no tiene acceso a la información solicitada.

</dd> <dt>

**8**
</dt> <dd>

Error desconocido.

</dd> <dt>

**9**
</dt> <dd>

El usuario no tiene los privilegios adecuados para ejecutar el método .

</dd> <dt>

**21**
</dt> <dd>

Un parámetro especificado en la llamada al método no es válido.

</dd> <dt>

**Otros**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Observaciones

La [**instancia \_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos [**SECURITY DESCRIPTOR \_ \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL) y una lista de [*control*](/windows/desktop/SecGloss/s-gly) de acceso del sistema (SACL). Para obtener más información, [vea Access Control enumeraciones](/windows/desktop/SecAuthZ/access-control-lists).

Si no se concede o se habilita **SeSecurityPrivilege** al obtener un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto. Para obtener más información, vea [**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [Ejecución de operaciones con privilegios.](/windows/desktop/WmiSdk/executing-privileged-operations)

Puede actualizar la DACL y la SACL en la instancia [**\_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) al llamar a este método, pero también puede actualizar solo la DACL o solo la SACL.

Los valores siguientes de [**SECURITY \_ DESCRIPTOR \_ CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determinan si se actualizan dacl, sacl o ambos.

-   **\_SE DACL \_ PRESENT**

    Indica que se debe actualizar la DACL. Si no se establece, WMI conserva el valor original de la DACL.

-   **\_SE SACL \_ PRESENT**

    Indica que se debe actualizar la SACL. Si no se establece, WMI conserva el valor original de sacl. Para actualizar la SACL, la cuenta debe tener habilitado el privilegio **SeSecurityPrivilege.** Para el scripting, el nombre de privilegio **es SeSecurityPrivilege.** Para obtener más información, vea [**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants).

Si las propiedades de administrador de grupo y administrador de propietarios no son **NULL,** se actualizan. De lo contrario, WMI conserva los valores originales. Para obtener más información, vea [Objetos de descriptor de seguridad WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).

Cuando una sacl nueva es **NULL en** una llamada a este método, el descriptor de seguridad SACL del objeto protegible de destino se deja sin modificar.

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

 

