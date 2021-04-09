---
description: Devuelve el descriptor de seguridad que controla el acceso al servicio.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor de la clase Win32_Service (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bf8dee49893a5a1d3b628e72b0b0746a6215fb0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080159"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método GetSecurityDescriptor de la clase Win32_Service (proveedores WMI de CIMWin32)

El método **GetSecurityDescriptor** devuelve el descriptor de seguridad que controla el acceso al servicio. El descriptor se devuelve como una instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Descriptor* \[ enuncia\]
</dt> <dd>

Descriptor de seguridad asociado al servicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Se aceptó la solicitud.

</dd> <dt>


</dt> <dd>

1

No se admite la solicitud.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tenía el acceso necesario.

</dd> <dt>


</dt> <dd>

3

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>


</dt> <dd>

4

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>


</dt> <dd>

5

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.

</dd> <dt>


</dt> <dd>

6

El servicio no se ha iniciado.

</dd> <dt>


</dt> <dd>

7

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

No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.

</dd> <dt>


</dt> <dd>

10

El servicio ya se está ejecutando.

</dd> <dt>


</dt> <dd>

11

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>


</dt> <dd>

12

Una dependencia de la que depende este servicio se ha quitado del sistema.

</dd> <dt>


</dt> <dd>

13

El servicio no pudo encontrar el servicio necesario de un servicio dependiente.

</dd> <dt>


</dt> <dd>

14

El servicio se ha deshabilitado del sistema.

</dd> <dt>


</dt> <dd>

15

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>


</dt> <dd>

16

Este servicio se está quitando del sistema.

</dd> <dt>


</dt> <dd>

17

El servicio no tiene ningún subproceso de ejecución.

</dd> <dt>


</dt> <dd>

18

El servicio tiene dependencias circulares al iniciarse.

</dd> <dt>


</dt> <dd>

19

Se está ejecutando un servicio con el mismo nombre.

</dd> <dt>


</dt> <dd>

20

El nombre del servicio tiene caracteres no válidos.

</dd> <dt>

**parámetro no válido**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>


</dt> <dd>

22

La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.

</dd> <dt>


</dt> <dd>

23

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>


</dt> <dd>

24

El servicio se encuentra en pausa actualmente en el sistema.

</dd> <dt>

**Otros**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>Observaciones

La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).

Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto. Para obtener más información, vea [**constantes de privilegios**](/windows/desktop/WmiSdk/privilege-constants) y [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Ejemplos

Al recuperar un descriptor de seguridad en VBScript, asegúrese de "seguridad" y ejecute como administrador, tal como se muestra en el siguiente fragmento de código. De lo contrario, el código puede producir un error de permisos.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



Del mismo modo, en VB.NET, asegúrese de establecer "EnablePrivileges = true" y ejecutar la aplicación como administrador.


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio Win32**](win32-service.md)
</dt> <dt>

[**Constantes de privilegio**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Objetos de descriptor de seguridad WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

