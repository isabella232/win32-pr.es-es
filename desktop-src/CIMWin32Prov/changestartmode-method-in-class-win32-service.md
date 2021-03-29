---
description: Modifica el modo de inicio de un \_ servicio Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Método ChangeStartMode de la clase Win32_Service (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080181"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método ChangeStartMode de la clase Win32_Service (proveedores WMI de CIMWin32)

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifica el modo de inicio de [**un \_ servicio de Win32**](win32-service.md).

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StartMode* \[ de\]
</dt> <dd>

Modo de inicio del servicio base de Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Inicio de arranque** ("arranque")


</dt> <dd>

Controlador de dispositivo Iniciado por el cargador del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("System")


</dt> <dd>

Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Inicio automático** ("automático")


</dt> <dd>

Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Inicio** de la demanda ("manual")


</dt> <dd>

Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-service.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")


</dt> <dd>

Servicio que ya no se puede iniciar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Se aceptó la solicitud.

</dd> <dt>

**No compatible**
</dt> <dd>

1

No se admite la solicitud.

</dd> <dt>

**Acceso denegado**
</dt> <dd>

2

El usuario no tenía el acceso necesario.

</dd> <dt>

**Servicios dependientes en ejecución**
</dt> <dd>

3

No se puede detener el servicio porque otros servicios que se están ejecutando dependen de él.

</dd> <dt>

**Control de servicio no válido**
</dt> <dd>

4

El código de control solicitado no es válido o no es aceptable para el servicio.

</dd> <dt>

**El servicio no puede aceptar el control**
</dt> <dd>

5

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.

</dd> <dt>

**Servicio no activo**
</dt> <dd>

6

El servicio no se ha iniciado.

</dd> <dt>

**Tiempo de espera de solicitud de servicio**
</dt> <dd>

7

El servicio no respondió a tiempo a la solicitud de inicio.

</dd> <dt>

**Error desconocido**
</dt> <dd>

8

Error desconocido al iniciar el servicio.

</dd> <dt>

**Ruta de acceso no encontrada**
</dt> <dd>

9

No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.

</dd> <dt>

**El servicio ya se está ejecutando**
</dt> <dd>

10

El servicio ya se está ejecutando.

</dd> <dt>

**Base de datos de servicio bloqueada**
</dt> <dd>

11

La base de datos para agregar un nuevo servicio está bloqueada.

</dd> <dt>

**Dependencia de servicio eliminada**
</dt> <dd>

12

Una dependencia de la que depende este servicio se ha quitado del sistema.

</dd> <dt>

**Error de dependencia de servicio**
</dt> <dd>

13

El servicio no pudo encontrar el servicio necesario de un servicio dependiente.

</dd> <dt>

**Servicio deshabilitado**
</dt> <dd>

14

El servicio se ha deshabilitado del sistema.

</dd> <dt>

**Error de inicio de sesión de servicio**
</dt> <dd>

15

El servicio no tiene la autenticación correcta para ejecutarse en el sistema.

</dd> <dt>

**Servicio marcado para eliminación**
</dt> <dd>

16

Este servicio se está quitando del sistema.

</dd> <dt>

**Servicio sin subproceso**
</dt> <dd>

17

El servicio no tiene ningún subproceso de ejecución.

</dd> <dt>

**Estado dependencia circular**
</dt> <dd>

18

El servicio tiene dependencias circulares al iniciarse.

</dd> <dt>

**Estado nombre duplicado**
</dt> <dd>

19

Se está ejecutando un servicio con el mismo nombre.

</dd> <dt>

**Estado nombre no válido**
</dt> <dd>

20

El nombre del servicio tiene caracteres no válidos.

</dd> <dt>

**Estado parámetro no válido**
</dt> <dd>

21

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**Estado cuenta de servicio no válida**
</dt> <dd>

22

La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.

</dd> <dt>

**El servicio de estado existe**
</dt> <dd>

23

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**Servicio ya pausado**
</dt> <dd>

24

El servicio se encuentra en pausa actualmente en el sistema.

</dd> <dt>

**Otros**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="examples"></a>Ejemplos

El siguiente [cambio de StartMode de un](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) ejemplo de PowerShell de servicio, extraído de la galería de TechNet, cambia el modo de inicio de un servicio.


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Servicio Win32**](win32-service.md)
</dt> <dt>

[Tareas WMI: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

