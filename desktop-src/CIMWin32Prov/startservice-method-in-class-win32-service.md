---
description: 'Método StartService de la clase Win32_Service (proveedores WMI CIMWin32): intenta colocar el servicio al que se hace referencia en su estado de inicio.'
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Método StartService de la clase Win32_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a630b9d926ff5377312f1c67630a20816ab38b6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974169"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Método StartService de la clase Win32_Service (proveedores WMI CIMWin32)

El **método StartService** intenta colocar el servicio al que se hace referencia en su estado de inicio.

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
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

Aunque puede parecer que no hay ninguna diferencia práctica entre un servicio que se detiene y un servicio que está en pausa, los dos estados aparecen de forma diferente al SCM. Un servicio detenido es un servicio que no se está ejecutando y debe pasar por todo el procedimiento de inicio del servicio. Sin embargo, un servicio en pausa todavía se está ejecutando, pero se ha suspendido su funcionamiento. Por este problema, un servicio en pausa no necesita pasar por todo el procedimiento de inicio del servicio, sino que necesita un procedimiento diferente para reanudar el funcionamiento.

Debe usar el método adecuado para iniciar un servicio que se ha detenido o para reanudar un servicio que se ha pausado. Los [**métodos \_ del servicio Win32**](win32-service.md) **StartService** y [**ResumeService**](resumeservice-method-in-class-win32-service.md) deben usarse en las situaciones siguientes:

-   Si un servicio está detenido actualmente, debe usar el **método StartService** para reiniciarlo. [**ResumeService**](resumeservice-method-in-class-win32-service.md) no puede iniciar un servicio que está detenido actualmente.
-   Si un servicio está en pausa, debe usar [**ResumeService**](resumeservice-method-in-class-win32-service.md). Si usa el **método StartService** en un servicio en pausa, recibirá el mensaje "El servicio ya se está ejecutando". Sin embargo, el servicio permanece en pausa hasta que se le envía el código de control de servicio de reanudación.

Si inicia un servicio detenido que depende de otro servicio, se inician ambos servicios. Cuando se inicia un servicio con este método, los servicios dependientes no se inician automáticamente. Debe usar la clase de asociación [**Win32 \_ DependentService**](win32-dependentservice.md) y la consulta [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) para buscar los dependientes e iniciarlos por separado.

## <a name="examples"></a>Ejemplos

El [ejemplo de PowerShell Habilitar RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) de forma remota habilita el Escritorio remoto remoto.

El ejemplo de PowerShell [Detener, Iniciar, Habilitar](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) o Deshabilitar servicio inicia, detiene, habilita o deshabilita un servicio.

En el siguiente ejemplo de código de VBSScript se muestra cómo iniciar un servicio específico desde instancias del [**servicio Win32 \_**](win32-service.md).


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



En el ejemplo de código perl siguiente se muestra cómo iniciar un servicio específico desde instancias del [**servicio Win32 \_**](win32-service.md).


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



El siguiente ejemplo de código VBScript, NetDDE, depende del servicio NetDDEDSDM. El script busca la clase de la que depende NetDDE y la inicia, lo que no inicia automáticamente NetDDE.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
```



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

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Servicio \_ Win32**](win32-service.md)
</dt> <dt>

[Tareas wmi: servicios](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

