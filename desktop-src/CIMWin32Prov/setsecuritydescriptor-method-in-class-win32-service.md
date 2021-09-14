---
description: 'Método SetSecurityDescriptor de la clase Win32_Service (proveedores WMI CIMWin32): escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.'
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20619a459171841d0a3bd5b7acabe984dc835dac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072335"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método SetSecurityDescriptor de la clase Win32_Service (proveedores WMI CIMWin32)

El **método SetSecurityDescriptor** escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descriptor* \[ En\]
</dt> <dd>

Descriptor de seguridad asociado al servicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error. Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Se aceptó la solicitud.

</dd> <dt>

**1**
</dt> <dd>

No se admite la solicitud.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tenía el acceso necesario.

</dd> <dt>

**3**
</dt> <dd>

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>

**4**
</dt> <dd>

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>

**5**
</dt> <dd>

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** property) es igual a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

El servicio no se ha iniciado.

</dd> <dt>

**7**
</dt> <dd>

El servicio no respondió a tiempo a la solicitud de inicio.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Error desconocido al iniciar el servicio.

</dd> <dt>

**Falta el privilegio**
</dt> <dd>

9

No se encontró la ruta de acceso del directorio al archivo ejecutable del servicio.

</dd> <dt>

**10**
</dt> <dd>

El servicio ya se está ejecutando.

</dd> <dt>

**11**
</dt> <dd>

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>

**12**
</dt> <dd>

Se ha quitado del sistema una dependencia en la que se basa este servicio.

</dd> <dt>

**13**
</dt> <dd>

El servicio no pudo encontrar el servicio necesario de un servicio dependiente.

</dd> <dt>

**14**
</dt> <dd>

El servicio se ha deshabilitado del sistema.

</dd> <dt>

**15**
</dt> <dd>

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>

**16**
</dt> <dd>

Este servicio se está quitando del sistema.

</dd> <dt>

**17**
</dt> <dd>

El servicio no tiene ningún subproceso de ejecución.

</dd> <dt>

**18**
</dt> <dd>

El servicio tiene dependencias circulares cuando se inicia.

</dd> <dt>

**19**
</dt> <dd>

Un servicio se ejecuta con el mismo nombre.

</dd> <dt>

**20**
</dt> <dd>

El nombre del servicio tiene caracteres no válidos.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**22**
</dt> <dd>

La cuenta con la que se ejecuta este servicio no es válida o carece de los permisos para ejecutar el servicio.

</dd> <dt>

**23**
</dt> <dd>

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**24**
</dt> <dd>

El servicio se encuentra en pausa actualmente en el sistema.

</dd> <dt>

**Otros**
</dt> <dd>

22 4294967295

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Servicio \_ Win32**](win32-service.md)
</dt> <dt>

[**Constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

