---
title: Método StartService de la clase Win32_Service (Servicios de Escritorio remoto)
description: 'Método StartService de la clase Win32_Service (Servicios de Escritorio remoto): intenta colocar el servicio al que se hace referencia en su estado de inicio.'
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- Método StartService Servicios de Escritorio remoto
- Método StartService Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto método , StartService
topic_type:
- apiref
api_name:
- Win32_Service.StartService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1a921f863ea2e06b7c84cf5ed66424d37f70be34f71c7c5975c95ff3d4308e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119514365"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a>Método StartService de la clase Win32_Service (Servicios de Escritorio remoto)

El **método StartService** intenta colocar el servicio al que se hace referencia en su estado de inicio.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) es igual a 0, 1 o 2.

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

**21**
</dt> <dd>

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

</dd> </dl>

## <a name="remarks"></a>Comentarios

Aunque puede parecer que no hay ninguna diferencia práctica entre un servicio que se detiene y un servicio que está en pausa, los dos estados aparecen de forma diferente al SCM. Un servicio detenido es un servicio que no se está ejecutando y debe pasar por todo el procedimiento de inicio del servicio. Sin embargo, un servicio en pausa todavía se está ejecutando, pero se ha suspendido su funcionamiento. Por este problema, un servicio en pausa no necesita pasar por todo el procedimiento de inicio del servicio, sino que necesita un procedimiento diferente para reanudar el funcionamiento.

Debe usar el método adecuado para iniciar un servicio que se ha detenido o para reanudar un servicio que se ha pausado. Los [**métodos \_ del servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** y [**ResumeService**](win32-terminalservice-resumeservice.md) deben usarse en las situaciones siguientes:

-   Si un servicio está detenido actualmente, debe usar el **método StartService** para reiniciarlo. [**ResumeService**](win32-terminalservice-resumeservice.md) no puede iniciar un servicio que está detenido actualmente.
-   Si un servicio está en pausa, debe usar [**ResumeService**](win32-terminalservice-resumeservice.md). Si usa el **método StartService** en un servicio en pausa, recibirá el mensaje "El servicio ya se está ejecutando". Sin embargo, el servicio permanece en pausa hasta que se le envía el código de control de servicio de reanudación.

Si inicia un servicio detenido que depende de otro servicio, se inician ambos servicios. Cuando se inicia un servicio con este método, los servicios dependientes no se inician automáticamente. Debe usar la clase de asociación [**Win32 \_ DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) y la consulta [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) para buscar los dependientes e iniciarlos por separado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Servicio \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Clases de sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**TerminalService de Win32 \_**](win32-terminalservice.md)
</dt> <dt>

[Tareas wmi: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

