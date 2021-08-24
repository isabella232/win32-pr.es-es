---
description: El&\# 8194; El método de clase WMI descarga programas y archivos DLL hasta que es seguro desactivar el equipo.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Método Shutdown de la Win32_OperatingSystem clase
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
ms.openlocfilehash: 068551ee013634bde9a42584764c36f255bf322bedb97e6ebb3a5075c113e742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800845"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Método Shutdown de la clase OperatingSystem de Win32 \_

El **método de** clase WMI [Shutdown](/windows/desktop/WmiSdk/retrieving-a-class) descarga programas y archivos DLL hasta que es seguro desactivar el equipo.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Shutdown();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener códigos de error, [**vea Constantes de error wmi**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otros** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

En ocasiones, los equipos deben quitarse de la red, quizás para el mantenimiento programado, porque el equipo no funciona correctamente o para completar un proceso de configuración. Por ejemplo, si un servidor DHCP está entregando direcciones IP erróneas, es posible que quiera apagar el equipo hasta que se pueda enviar un técnico de servicio para corregir el problema. Si sospecha que se ha producido una infracción de seguridad, es posible que tenga que apagar determinados servidores para asegurarse de que no se pueda acceder a ellos hasta que se resuelva el problema de seguridad. Algunas operaciones de configuración (como cambiar el nombre de un equipo) requieren que reinicie el equipo antes de que el cambio suba.

Este método apaga inmediatamente el equipo, si es posible. El sistema detiene todos los procesos en ejecución, vacía todos los búferes de archivos en el disco y, a continuación, apaga el sistema. El proceso de llamada debe tener el **SE \_ SHUTDOWN \_ NAME,** como se describe en el ejemplo siguiente.


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



Para obtener más información sobre cómo establecer un privilegio, vea [Ejecutar operaciones](/windows/desktop/WmiSdk/executing-privileged-operations) con privilegios y Ejecutar operaciones [con privilegios mediante VBScript.](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript) Para obtener opciones de apagado adicionales, como un cierre de sesión o un apagado forzado, consulte el [**método Win32Shutdown.**](win32shutdown-method-in-class-win32-operatingsystem.md)

## <a name="examples"></a>Ejemplos

El siguiente código VBScript apaga el equipo local.

> [!Note]  
> Debe tener el privilegio Shutdown para invocar correctamente el método Shutdown.

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



El siguiente código Perl apaga el equipo local.

> [!Note]  
> Debe tener el privilegio Shutdown para invocar correctamente el método Shutdown.

 


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



El siguiente código VBScript apaga el equipo remoto especificado. Rellene *REMOTE \_ SYSTEM NAME \_ con* el nombre del sistema remoto que se debe apagar.

> [!Note]  
> Debe tener el privilegio RemoteShutdown para invocar correctamente el **método Shutdown.**

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[Tareas wmi: administración de escritorio](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[Ejecución de operaciones con privilegios mediante VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

