---
title: Método PauseService de la clase Win32_Service (Servicios de Escritorio remoto)
description: Intenta poner el servicio en estado de pausa.
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- Método PauseService Servicios de Escritorio remoto
- Método PauseService Servicios de Escritorio remoto, clase Win32_Service
- Win32_Service de clase Servicios de Escritorio remoto, método PauseService
topic_type:
- apiref
api_name:
- Win32_Service.PauseService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69951a77530b3aff89148b08e19f3a7c4da8f5b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676661"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a>Método PauseService de la clase Win32_Service (Servicios de Escritorio remoto)

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** intenta poner el servicio en estado de pausa.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 PauseService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Se aceptó la solicitud.

</dd> <dt>

**1**
</dt> <dd>

No se admite la solicitud.

</dd> <dt>

**2**
</dt> <dd>

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

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** Property) es igual a 0, 1 o 2.

</dd> <dt>

**6**
</dt> <dd>

El servicio no se ha iniciado.

</dd> <dt>

**7**
</dt> <dd>

El servicio no respondió a tiempo a la solicitud de inicio.

</dd> <dt>

**8**
</dt> <dd>

Error desconocido al iniciar el servicio.

</dd> <dt>

**9**
</dt> <dd>

No se encontró la ruta de acceso al directorio del archivo ejecutable del servicio.

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

Una dependencia de la que depende este servicio se ha quitado del sistema.

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

El servicio tiene dependencias circulares al iniciarse.

</dd> <dt>

**19**
</dt> <dd>

Se está ejecutando un servicio con el mismo nombre.

</dd> <dt>

**20**
</dt> <dd>

El nombre del servicio tiene caracteres no válidos.

</dd> <dt>

**21**
</dt> <dd>

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**22**
</dt> <dd>

La cuenta con la que se ejecuta este servicio no es válida o carece de permisos para ejecutar el servicio.

</dd> <dt>

**23**
</dt> <dd>

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**24**
</dt> <dd>

El servicio se encuentra en pausa actualmente en el sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Después de determinar qué servicios se pueden detener o pausar, puede utilizar los métodos [**StopService**](win32-terminalservice-stopservice.md) y **PauseService** para detener y pausar los servicios. La decisión de detener un servicio en lugar de pausarlo, o viceversa, depende de varios factores, entre los que se incluyen los siguientes:

-   ¿Se puede pausar el servicio? Si no es así, la única opción es detener el servicio.
-   ¿Necesita seguir controlando las solicitudes de cliente para los usuarios que ya están conectados al servicio? Si es así, al pausar un servicio normalmente se le permite administrar los clientes existentes a la vez que deniega el acceso a los clientes nuevos. Por el contrario, cuando se detiene un servicio, todos los clientes se desconectan inmediatamente.
-   ¿Necesita volver a configurar un servicio y hacer que los cambios surtan efecto inmediatamente? Aunque se pueden cambiar las propiedades del servicio mientras se pausa un servicio, la mayoría de ellos no surtirán efecto hasta que el servicio se detenga y se reinicie realmente.

El código de scripting necesario para detener un servicio es casi idéntico al código necesario para pausar el servicio.

## <a name="examples"></a>Ejemplos

En el ejemplo de [aplicación pausar los servicios que se ejecutan con una cuenta específica](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) de VBScript se detienen todos los servicios que se ejecutan en la misma cuenta de servicio

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Clases de sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**Win32 \_ TerminalService**](win32-terminalservice.md)
</dt> <dt>

[Tareas WMI: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

