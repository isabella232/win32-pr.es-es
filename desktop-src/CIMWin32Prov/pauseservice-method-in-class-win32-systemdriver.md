---
description: Intenta colocar el servicio administrado por el controlador del sistema lógico en el estado pausado.
ms.assetid: f5e960c1-868b-4b7b-9ea5-0fb8a9cfbafa
ms.tgt_platform: multiple
title: Método PauseService de la clase Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a85c49a8ea81cc9af9a99f238bdafb473ca85050
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000835"
---
# <a name="pauseservice-method-of-the-win32_systemdriver-class"></a>Método PauseService de la \_ clase SystemDriver de Win32

El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** intenta colocar el servicio administrado por el controlador del sistema lógico en el estado pausado.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 PauseService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se aceptó la solicitud **PauseService** , 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

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

El código de control solicitado no se puede enviar al servicio porque el estado del servicio ([**Win32 \_ BaseService**](win32-baseservice.md).**State** Property) es igual a 0, 1 o 2.

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

Se produjo un error desconocido al iniciar el servicio.

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

Una dependencia para la que se basa este servicio se ha quitado del sistema.

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

No hay ningún subproceso de ejecución para el servicio.

</dd> <dt>

**18**
</dt> <dd>

Hay dependencias circulares al iniciarse el servicio.

</dd> <dt>

**19**
</dt> <dd>

Hay un servicio que se ejecuta con el mismo nombre.

</dd> <dt>

**20**
</dt> <dd>

Hay caracteres no válidos en el nombre del servicio.

</dd> <dt>

**21**
</dt> <dd>

Se han pasado parámetros no válidos al servicio.

</dd> <dt>

**22**
</dt> <dd>

La cuenta con la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.

</dd> <dt>

**23**
</dt> <dd>

El servicio existe en la base de datos de servicios disponibles del sistema.

</dd> <dt>

**24**
</dt> <dd>

El servicio se encuentra en pausa actualmente en el sistema.

</dd> </dl>

## <a name="examples"></a>Ejemplos

El siguiente código de PowerShell intenta pausar el servicio "clase de impresora USB de Microsoft".


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.PauseService()
"Pause Service called. The return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
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

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

