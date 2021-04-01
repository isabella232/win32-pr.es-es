---
description: Win32Shutdown &\# 8194; El método de clase WMI proporciona el conjunto completo de opciones de apagado compatibles con los sistemas operativos Win32. Entre ellas se incluyen cerrar sesión, apagar, reiniciar y forzar el cierre de sesión, el apagado o el reinicio.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Método Win32Shutdown de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907451"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a>Método Win32Shutdown de la \_ clase Win32 OperatingSystem

El método de   [clase WMI](../wmisdk/retrieving-a-class.md) **Win32Shutdown** proporciona el conjunto completo de opciones de apagado compatibles con los sistemas operativos Win32. Entre ellas se incluyen cerrar sesión, apagar, reiniciar y forzar el cierre de sesión, el apagado o el reinicio.

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](../wmisdk/calling-a-method.md).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Conjunto de mapas Dete de marcas para apagar el equipo. Para forzar un comando, agregue la marca Force (4) al valor del comando. Al usar forzar junto con el apagado o el reinicio de un equipo remoto, se cierra inmediatamente todo (incluido WMI, COM, etc.) o se reinicia el equipo remoto. Esto da como resultado un valor devuelto indeterminado.

<dt>

0 (0X0)
</dt> <dd>

**Cerrar sesión** : cierra la sesión del usuario en el equipo. El cierre de sesión detiene todos los procesos asociados con el contexto de seguridad del proceso que llamó a la función Exit, registra el usuario actual en el sistema y muestra el cuadro de diálogo logon.

</dd> <dt>

4 (0x4)
</dt> <dd>

Cierre de **sesión forzado (0 + 4)** : cierra el usuario del equipo inmediatamente y no notifica a las aplicaciones que la sesión de inicio de sesión está finalizando. Esto puede dar lugar a una pérdida de datos.

</dd> <dt>

1 (0x1)
</dt> <dd>

**Apagado** : apaga el equipo hasta un punto en el que es seguro apagar la alimentación. (Todos los búferes de archivos se vacían en el disco y se detienen todos los procesos en ejecución). Los usuarios ven el mensaje `It is now safe to turn off your computer.`

Durante el apagado, el sistema envía un mensaje a cada aplicación en ejecución. Las aplicaciones realizan cualquier limpieza mientras procesan el mensaje y devuelven TRUE para indicar que se pueden terminar.

</dd> <dt>

5 (0X5)
</dt> <dd>

**Cierre forzado (1 + 4)** : apaga el equipo hasta un punto en el que es seguro apagar la alimentación. (Todos los búferes de archivos se vacían en el disco y se detienen todos los procesos en ejecución). Los usuarios ven el mensaje` It is now safe to turn off your computer.`

Cuando se usa el enfoque de cierre forzado, todos los servicios, incluido WMI, se apagan inmediatamente. Por este motivo, no podrá recibir un valor devuelto si está ejecutando el script en un equipo remoto.

</dd> <dt>

2 (0X2)
</dt> <dd>

**Reiniciar** : cierra y reinicia el equipo.

</dd> <dt>

6 (0x6)
</dt> <dd>

**Reinicio forzado (2 + 4)** : cierra y reinicia el equipo.

Cuando se utiliza el enfoque de reinicio forzado, todos los servicios, incluido WMI, se apagan inmediatamente. Por este motivo, no podrá recibir un valor devuelto si está ejecutando el script en un equipo remoto.

</dd> <dt>

8 (0x8)
</dt> <dd>

**Apaga el** equipo y apaga la alimentación (si es compatible con el equipo en cuestión).

</dd> <dt>

12 (0xC)
</dt> <dd>

**Apagado forzado (8 + 4)** : apaga el equipo y apaga la alimentación (si es compatible con el equipo en cuestión).

Cuando se usa el enfoque de apagado forzado, todos los servicios, incluido WMI, se apagan inmediatamente. Por este motivo, no podrá recibir un valor devuelto si está ejecutando el script en un equipo remoto.

</dd> </dl> </dd> <dt>

*Reservado* \[ de\]
</dt> <dd>

Un medio para extender **Win32Shutdown**. Actualmente, se omite el parámetro *Reserved* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que la operación se ha realizado correctamente. Cualquier otro número indica que hubo un error. Para ver los códigos de error, consulte [**constantes error de WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](../debug/system-error-codes.md).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otro** (1 – 4294967295)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Para una administración más eficaz de los equipos de una organización, los administradores necesitan la capacidad de apagar o reiniciar un equipo de forma remota o de cerrar la sesión de un usuario de forma remota. La capacidad de llevar a cabo estas tareas permite a los administradores instalar software, volver a configurar el equipo, quitar equipos de la red y realizar otras tareas sin tener que apagar o reiniciar manualmente cada equipo.

Por ejemplo, para realizar una actualización de red, es posible que tenga que apagar todos los equipos que se ejecutan en un segmento de red determinado. Para forzar una actualización de directiva de grupo, debe cerrar la sesión de los usuarios en sus equipos. Si un virus informático está presente en cualquier parte de su organización, es posible que desee apagar tantos equipos como sea posible, antes de que el virus tenga la oportunidad de propagarse. La capacidad de apagar y reiniciar los equipos y de cerrar la sesión de los usuarios mediante programación en lugar de hacerlo manualmente puede ser un ahorro de tiempo enorme.

El proceso de llamada debe tener el privilegio de **\_ \_ nombre de cierre de se** .

El método [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) proporciona el mismo conjunto de opciones de cierre admitido por el método **Win32Shutdown** en el [**\_ OperatingSystem de Win32**](win32-operatingsystem.md) , pero también permite especificar comentarios, un motivo para el apagado o un tiempo de espera.

El método Win32Shutdown no tiene un parámetro para bloquear una estación de trabajo, lo que hace que el usuario inicie sesión. Sin embargo, las estaciones de trabajo se pueden bloquear desde la línea de comandos mediante el comando siguiente:

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a>Ejemplos

En el ejemplo de VBScript [Cerrar sesión, reiniciar o apagar varios equipos](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) de la galería de TechNet se usa Win32Shutdown para cerrar la sesión, apagar, reiniciar o desconectar (dependiendo de la selección) los equipos que aparecen en la matriz de servidores.

El ejemplo de [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell en la galería de TechNet incluye un método que llama a Win32Shutdown en un equipo remoto.

En el siguiente ejemplo de PowerShell se usa el método Win32Shutdown para apagar el equipo especificado.


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



En el siguiente ejemplo de código de PowerShell se usa el cmdlet EnableAllPrivileges desde Get-WMIObject para obtener los privilegios adecuados.


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



El siguiente código de ejemplo de VB.NET usa el método shutdown para reiniciar o cerrar la sesión de un sistema.


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
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

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[**OperatingSystem de Win32 \_**](win32-operatingsystem.md)
</dt> <dt>

[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[Tareas WMI: administración de escritorio](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[Ejecutar operaciones con privilegios mediante VBScript](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
