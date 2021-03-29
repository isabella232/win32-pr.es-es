---
description: El reinicio&\# 8194; El método de clase WMI cierra el sistema del equipo y, a continuación, lo reinicia.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Método de reinicio de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000741"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Método de reinicio de la \_ clase Win32 OperatingSystem

El método **reboot** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) apaga el equipo y, a continuación, lo reinicia.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que la operación se ha realizado correctamente. Cualquier otro número indica que hubo un error. Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otro** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

La capacidad de reiniciar un equipo mediante programación permite a los administradores realizar muchas tareas de administración de equipos de forma remota.

Por ejemplo, si crea un script para instalar software o realiza un cambio de configuración que requiera el reinicio de un equipo, puede incluir el comando de reinicio en el script y realizar toda la operación de forma remota. El método de **reinicio** se puede usar para reiniciar un equipo. Al igual que el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , el método de **reinicio** requiere el usuario cuyas credenciales de seguridad usa el script para poseer el privilegio de apagado.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de VBScript se invoca el método de reinicio de la clase [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .

> [!Note]  
> Debe tener el privilegio SHUTDOWN para invocar correctamente el método shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



El siguiente código Perl invoca el método de reinicio de la clase [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .

> [!Note]  
> Debe tener el privilegio SHUTDOWN para invocar correctamente el método shutdown.

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



El siguiente código de VBScript invoca el método de reinicio de la clase [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) en un sistema remoto. Rellene \_ nombre del sistema remoto \_ con el nombre del sistema remoto que se va a reiniciar.

> [!Note]  
> Debe tener el privilegio RemoteShutdown para invocar correctamente el método de reinicio.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



el siguiente Perl invoca el método de reinicio de la clase [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) en un sistema remoto. Rellene \_ nombre del sistema remoto \_ con el nombre del sistema remoto que se va a reiniciar.

> [!Note]  
> Debe tener el privilegio RemoteShutdown para invocar correctamente el método de reinicio.

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
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

[**OperatingSystem de Win32 \_**](win32-operatingsystem.md)
</dt> <dt>

[**CIM \_ OperatingSystem. Shutdown (método)**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[Tareas WMI: administración de escritorio](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

