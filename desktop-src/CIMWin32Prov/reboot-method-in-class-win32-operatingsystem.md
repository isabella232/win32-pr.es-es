---
description: El&\# 8194; El método de clase WMI apaga el sistema del equipo y, a continuación, lo reinicia.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Método reboot de la Win32_OperatingSystem clase
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
ms.openlocfilehash: 700d497650e8950c72467bbad8e11cf450b2302f0b68ef762e8a11e3c6aaceee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752735"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Método Reboot de la clase OperatingSystem de Win32 \_

El **método de** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) Reboot apaga el sistema del equipo y, a continuación, lo reinicia.

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Reboot();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener códigos de error, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otros** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

La capacidad de reiniciar un equipo mediante programación permite a los administradores realizar muchas tareas de administración de equipos de forma remota.

Por ejemplo, si crea un script para instalar software o realiza un cambio de configuración que requiere reiniciar un equipo, puede incluir el comando restart en el script y realizar toda la operación de forma remota. El **método Reboot** se puede usar para reiniciar un equipo. Al igual [**que el método Win32Shutdown,**](win32shutdown-method-in-class-win32-operatingsystem.md) el método **Reboot** requiere que el usuario cuyas credenciales de seguridad esté utilizando el script posea el privilegio Shutdown.

## <a name="examples"></a>Ejemplos

El siguiente ejemplo de código de VBScript invoca el método Reboot de la [**clase \_ OperatingSystem de Win32.**](win32-operatingsystem.md)

> [!Note]  
> Debe tener el privilegio Shutdown para invocar correctamente el método Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



El siguiente código Perl invoca el método Reboot de la [**clase \_ OperatingSystem de Win32.**](win32-operatingsystem.md)

> [!Note]  
> Debe tener el privilegio Shutdown para invocar correctamente el método Shutdown.

 


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



El siguiente VBScript invoca el método Reboot de la [**clase \_ OperatingSystem win32**](win32-operatingsystem.md) en un sistema remoto. Rellene REMOTE \_ SYSTEM \_ NAME (NOMBRE DEL SISTEMA REMOTO) con el nombre del sistema remoto que se reiniciará.

> [!Note]  
> Debe tener el privilegio RemoteShutdown para invocar correctamente el método Reboot.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



Después de Perl, invoca el método Reboot de la [**clase \_ OperatingSystem win32**](win32-operatingsystem.md) en un sistema remoto. Rellene REMOTE \_ SYSTEM \_ NAME (NOMBRE DEL SISTEMA REMOTO) con el nombre del sistema remoto que se reiniciará.

> [!Note]  
> Debe tener el privilegio RemoteShutdown para invocar correctamente el método Reboot.

 


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Sistema operativo \_ Win32**](win32-operatingsystem.md)
</dt> <dt>

[**\_Método Cim OperatingSystem.Shutdown**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[Tareas wmi: administración de escritorio](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

