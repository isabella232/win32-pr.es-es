---
description: El cierre&\# 8194; El método de clase WMI descarga programas y dll hasta que es seguro apagar el equipo.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Método Shutdown de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496727"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Método Shutdown de la \_ clase Win32 OperatingSystem

El método **Shutdown** de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) descarga programas y dll hasta que es seguro apagar el equipo.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Shutdown();
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

En ocasiones, los equipos deben quitarse de la red, quizás para realizar tareas de mantenimiento programado, ya que el equipo no funciona correctamente o para completar un proceso de configuración. Por ejemplo, si un servidor DHCP está entregando direcciones IP erróneas, es posible que desee apagar el equipo hasta que se pueda enviar un técnico de servicio para solucionar el problema. Si sospecha que se ha producido una infracción de seguridad, es posible que tenga que apagar determinados servidores para asegurarse de que no se pueda tener acceso a ellos hasta que se resuelva el problema de seguridad. Algunas operaciones de configuración (como cambiar el nombre de un equipo) requieren que se reinicie el equipo para que el cambio surta efecto.

Este método apaga inmediatamente el equipo, si es posible. El sistema detiene todos los procesos en ejecución, vacía todos los búferes de archivo en el disco y, a continuación, apaga el sistema. El proceso de llamada debe tener el privilegio de **\_ \_ nombre de cierre se** , tal y como se describe en el ejemplo siguiente.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Para obtener más información sobre cómo establecer un privilegio, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations) y [ejecutar operaciones con privilegios mediante VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript). Para más opciones de apagado, como un cierre de sesión o un cierre forzado, consulte el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .

## <a name="examples"></a>Ejemplos

El siguiente código VBScript cierra el equipo local.

> [!Note]  
> Debe tener el privilegio SHUTDOWN para invocar correctamente el método shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



El siguiente código Perl cierra el equipo local.

> [!Note]  
> Debe tener el privilegio SHUTDOWN para invocar correctamente el método shutdown.

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



El siguiente código VBScript cierra el equipo remoto especificado. Rellene *\_ \_ nombre del sistema remoto* con el nombre del sistema remoto que se va a cerrar.

> [!Note]  
> Debe tener el privilegio RemoteShutdown para invocar correctamente el método **Shutdown** .

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
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

[Tareas WMI: administración de escritorio](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Ejecutar operaciones con privilegios mediante VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

