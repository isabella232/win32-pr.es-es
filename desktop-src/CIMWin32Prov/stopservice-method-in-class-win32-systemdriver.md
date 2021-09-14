---
description: Coloca el servicio representado por el objeto SystemDriver de Win32 \_ en estado detenido.
ms.assetid: 0fa8ef44-39eb-448e-8d33-38a5af9a0c13
ms.tgt_platform: multiple
title: Método StopService de la Win32_SystemDriver (Sdoias.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb45a414ea9cc7198487dbb61d122722816f4728
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062570"
---
# <a name="stopservice-method-of-the-win32_systemdriver-class"></a>Método StopService de la clase \_ SystemDriver de Win32

El método de clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** coloca el servicio representado por el objeto [**\_ SystemDriver de Win32**](win32-systemdriver.md) en estado detenido.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si el servicio se detuvo correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

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

**8**
</dt> <dd>

Se produjo un error desconocido al iniciar el servicio.

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

La cuenta en la que se va a ejecutar este servicio no es válida o carece de los permisos para ejecutar el servicio.

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

El siguiente código de PowerShell detiene el servicio "Clase de impresora USB de Microsoft".


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StopService()
"Stop Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

