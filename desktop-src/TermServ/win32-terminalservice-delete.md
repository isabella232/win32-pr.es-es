---
title: Método Delete de la clase Win32_Service (Servicios de Escritorio remoto)
description: Delete \ 8194; El método de clase WMI elimina un servicio existente.
ms.assetid: 0F012D6B-BD29-4AC3-AC7E-78EC02C1FF43
ms.tgt_platform: multiple
keywords:
- Eliminar método Servicios de Escritorio remoto
- Método Delete Servicios de Escritorio remoto , Win32_Service clase
- Win32_Service clase Servicios de Escritorio remoto método , Delete
topic_type:
- apiref
api_name:
- Win32_Service.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89e2c30ef39d7b36baf62a486477fcf4a7fa2842
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890769"
---
# <a name="delete-method-of-the-win32_service-class-remote-desktop-services"></a>Método Delete de la clase Win32_Service (Servicios de Escritorio remoto)

El **método de** clase WMI [Delete](/windows/desktop/WmiSdk/retrieving-a-class) elimina un servicio existente.

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores enumerados en la lista siguiente o cualquier otro valor para indicar un error. Para obtener códigos de error adicionales, [**vea Constantes de error WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

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

## <a name="remarks"></a>Observaciones

A medida que cambia la organización, puede decidir quitar determinados servicios de determinados equipos. Los servicios de dentro y de terceros se pueden quitar mediante WMI, mientras que los servicios del sistema operativo se pueden quitar mediante Sysocmgr.exe.

Al preparar la eliminación de servicios, tenga en cuenta la siguiente información:

-   Los servicios deben detenerse antes de quitarlos. Si el servicio se está ejecutando cuando se emite el comando delete, el servicio se marca para su eliminación, pero continúa ejecutándose hasta que se detiene y se cierran todos los identificadores abiertos.

    Si el servicio nunca se detiene, ese servicio nunca se eliminará.

-   La eliminación de un servicio no quita el archivo ejecutable del servicio.

    Al quitar un servicio mediante WMI, se eliminan las entradas del Registro relacionadas en HKEY \_ LOCAL \_ MACHINE SYSTEM \\ \\ CurrentControlSet \\ Services. Como resultado, el servicio ya no está instalado y no está disponible a través del complemento Servicios. Sin embargo, WMI no elimina el archivo ejecutable, lo que significa que podría reinstalar fácilmente el servicio. Para eliminar el archivo ejecutable, debe recuperar el nombre de la ruta de acceso y, a continuación, eliminar el archivo.

-   Al quitar un servicio Windows 2000 base (por ejemplo, DHCP) mediante WMI, se eliminan las entradas del Registro para ese servicio, pero no se quita el acceso directo del menú Herramientas administrativas ni se quita el servicio del Asistente para componentes de Windows. Esto puede confundir a cualquier persona que intente determinar cómo se ha configurado el equipo.

    Por ejemplo, si quita el servicio DHCP mediante un script WMI, el servicio DHCP ya no aparece en el complemento Servicios. Sin embargo, un acceso directo no funcional a la consola DHCP permanece en el menú Herramientas administrativas y, si inicia el Asistente para componentes de Windows, indica que el servicio DHCP está instalado.

    Por este problema, siempre debe usar Sysocmgr.exe para quitar mediante programación Windows 2000 servicios.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se describe cómo eliminar un servicio.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



En el siguiente ejemplo de código Perl se describe cómo eliminar un servicio.


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Servicio \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[Clases de sistema operativo](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[**TerminalService de Win32 \_**](win32-terminalservice.md)
</dt> <dt>

[Tareas wmi: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

