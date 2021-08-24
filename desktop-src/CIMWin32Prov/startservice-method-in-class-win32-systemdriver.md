---
description: Intenta colocar el servicio administrado por el controlador del sistema en su estado de inicio.
ms.assetid: 3f9d29aa-b549-4a55-be9c-01fad4932fe6
ms.tgt_platform: multiple
title: Método StartService de la Win32_SystemDriver clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21f6814ef8c96e88b11b6e998da7b3e24334b56782929e37c3d6d97965887af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752275"
---
# <a name="startservice-method-of-the-win32_systemdriver-class"></a>Método StartService de la clase \_ SystemDriver de Win32

El **método StartService** intenta colocar el servicio administrado por el controlador del sistema en su estado de inicio.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.

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

El siguiente código de PowerShell inicia el servicio "Clase de impresora USB de Microsoft".


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StartService()
"Start Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ SystemDriver**](win32-systemdriver.md)
</dt> </dl>

 

