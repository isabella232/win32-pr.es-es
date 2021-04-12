---
title: Clase Win32_TerminalService
description: Una subclase de la clase de servicio de Win32 \_ . Win32 \_ TerminalService representa la propiedad de elemento de la \_ Asociación TerminalServiceToSetting de Win32.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TerminalService de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492736"
---
# <a name="win32_terminalservice-class"></a>\_Clase Win32 TerminalService

La clase WMI **\_ TerminalService de Win32** es una subclase de la clase de [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) . **Win32 \_ TerminalService** representa la propiedad de **elemento** de la Asociación [**\_ TerminalServiceToSetting de Win32**](win32-terminalservicetosetting.md) .

La siguiente sintaxis se simplifica desde el código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a>Miembros

La **clase \_ TerminalService de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TerminalService** tiene estos métodos.



| Método                                                                       | Descripción                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Cambio**](win32-terminalservice-change.md)                               | Modifica un servicio.<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | Modifica el modo de inicio de un servicio.<br/>                                                     |
| [**A**](win32-terminalservice-create.md)                               | Crea un nuevo servicio.<br/>                                                                    |
| [**Elimínelos**](win32-terminalservice-delete.md)                               | Elimina un servicio existente.<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | Devuelve el descriptor de seguridad que controla el acceso al servicio.<br/>                      |
| [**InterrogateService**](win32-terminalservice-interrogateservice.md)       | Solicita que un servicio actualice su estado al administrador de servicios.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Intenta poner un servicio en estado de pausa.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Intenta poner un servicio en estado reanudado.<br/>                                         |
| [**SetSecurityDescriptor**](win32-terminalservice-setsecuritydescriptor.md) | Escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.<br/> |
| [**StartService**](win32-terminalservice-startservice.md)                   | Intenta colocar un servicio en el estado de inicio.<br/>                                       |
| [**StopService**](win32-terminalservice-stopservice.md)                     | Coloca un servicio en estado detenido.<br/>                                                    |
| [**UserControlService**](win32-terminalservice-usercontrolservice.md)       | Intenta enviar un código de control definido por el usuario a un servicio.<br/>                                |



 

### <a name="properties"></a>Propiedades

La **clase \_ TerminalService de Win32** tiene estas propiedades.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ PAUSE \_ Continue"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("el servicio acepta la pausa")
</dt> </dl>

Indica si se puede pausar el servicio.

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status)servicio \| dwControlsAccepted \| \_ \_ Stop"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("el servicio acepta la detención")
</dt> </dl>

Indica si se puede detener el servicio.

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción del servicio: una cadena de una línea.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**SnapSure**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")
</dt> </dl>

Valor que el servicio incrementa periódicamente para informar sobre su progreso durante una operación larga de inicio, detención, pausa o continuación. Por ejemplo, el servicio incrementa este valor a medida que completa cada paso de su inicialización cuando se inicia. El programa de interfaz de usuario que invoca la operación en el servicio usa este valor para realizar el seguimiento del progreso del servicio durante una operación larga. Este valor no es válido y debe ser cero cuando el servicio no tiene pendiente una operación de inicio, detención, pausa o continuación.

Esta propiedad se hereda del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de clase")
</dt> </dl>

Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia. Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.

Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api Service \| Structures \| [**\_ retardo \_ auto \_ Start \_ info**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Inicio automático retrasado")
</dt> </dl>

Si es **true**, el servicio se inicia después de que se inicien otros servicios de inicio automático más un breve retraso.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.

Esta propiedad se hereda del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descripción")
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ Process"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("interactúa con Desktop")
</dt> </dl>

Indica si el servicio puede crear o comunicarse con Windows en el escritorio y, por tanto, interactuar de algún modo con un usuario. Los servicios interactivos deben ejecutarse en la cuenta de sistema local. La mayoría de los servicios no son interactivos; es decir, no se comunican con el usuario de ningún modo.

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**DisconnectedSessions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de sesiones desconectadas en el servidor actual. Estas sesiones pueden seguir consumiendo activamente recursos del servidor, pero actualmente no tienen ninguna conexión de red con un cliente.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre para mostrar")
</dt> </dl>

Nombre del servicio tal como se ve en el complemento Servicios. Esta cadena tiene una longitud máxima de 256 caracteres. Tenga en cuenta que el nombre para mostrar y el nombre del servicio (que se almacena en el registro) no son siempre los mismos. Por ejemplo, el servicio de cliente DHCP tiene el nombre de servicio DHCP, pero el cliente DHCP de nombre para mostrar. El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios. Sin embargo, las comparaciones de [**displayName**](/windows/desktop/CIMWin32Prov/win32-service) siempre distinguen entre mayúsculas y minúsculas.

Constraint: acepta el mismo valor que la propiedad [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .

Ejemplo: "Endisco"

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("gravedad del error de inicio")
</dt> </dl>

Gravedad del error si este servicio no se inicia durante el inicio. El valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** ("omitir")


</dt> <dd>

No se notifica al usuario.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")


</dt> <dd>

Se notifica al usuario. Normalmente, se trata de un cuadro de mensaje que informa al usuario del problema.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")


</dt> <dd>

El sistema se reinicia con la última configuración válida conocida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")


</dt> <dd>

El sistema intenta reiniciarse con una configuración válida. Si el servicio no se inicia por segunda vez, se produce un error de inicio.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** ("desconocido")


</dt> <dd>

Se desconoce la gravedad del error.

</dd> </dl>

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de salida")
</dt> </dl>

Código de error de Windows que define los errores detectados al iniciar o detener el servicio. Esta propiedad se establece en **\_ \_ \_ error específico del servicio de error** (1066) cuando el error es exclusivo del servicio representado por esta clase, y la información sobre el error está disponible en la propiedad [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) . El servicio establece este valor en **ningún \_ error** cuando se ejecuta y de nuevo tras la terminación normal.

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" instalación de fecha ")
</dt> </dl>

El objeto de fecha está instalado. Esta propiedad no requiere un valor para indicar que el objeto está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador único del servicio que proporciona una indicación de la funcionalidad que se administra. Esta funcionalidad se describe en la propiedad [**Description**](/windows/desktop/CIMWin32Prov/win32-service) del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File path name")
</dt> </dl>

Ruta de acceso completa al archivo binario del servicio que implementa el servicio.

Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process ID")
</dt> </dl>

Identificador de proceso del servicio.

Ejemplo: 324

Esta propiedad se hereda del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("código de salida específico del servidor")
</dt> </dl>

Código de error específico del servicio para los errores que se producen mientras el servicio se está iniciando o deteniendo. Los códigos de salida se definen mediante el servicio representado por esta clase. Este valor solo se establece cuando el valor de la propiedad [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) es **\_ \_ \_ error específico del servicio de error** (1066).

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")
</dt> </dl>

Tipo de servicio proporcionado a los procesos de llamada.

Los valores son:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Controlador de kernel** ("controlador de kernel")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Controlador del sistema de archivos** ("controlador del sistema de archivos")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Adaptador** ("adaptador")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Controlador del reconocedor** ("controlador del reconocedor")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Proceso propio** ("propio proceso")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Proceso de recurso compartido** ("proceso de recurso compartido")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Proceso interactivo** ("proceso interactivo")


</dt> <dd></dd> </dl>

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("iniciado")
</dt> </dl>

Indica si se ha iniciado o no el servicio.

Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("modo de inicio")
</dt> </dl>

Modo de inicio del servicio base de Windows.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque** ("arranque")


</dt> <dd>

Controlador de dispositivo Iniciado por el cargador del sistema operativo (válido solo para los servicios de controlador).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("System")


</dt> <dd>

Controlador de dispositivo Iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("auto")


</dt> <dd>

Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema. Los servicios automáticos se inician incluso si un usuario no inicia sesión.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")


</dt> <dd>

Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Estos servicios no se inician a menos que un usuario inicie sesión y los inicie.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")


</dt> <dd>

Servicio que no se puede iniciar hasta que su StartMode se cambie a automático o manual.

</dd> </dl>

Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre de la cuenta de inicio")
</dt> </dl>

Nombre de cuenta con la que se ejecuta un servicio. Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato "nombreDeDominio \\ nombreDeUsuario" o el formato UPN (" *Username@DomainName* "). El proceso de servicio se registra con una de estas dos formas cuando se ejecuta. Si la cuenta pertenece al dominio integrado, ". \\ Se puede especificar username. En el caso de los controladores de kernel o de nivel de sistema, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contiene el nombre de objeto del controlador (es decir, " \\ filesystem \\ RDR" o " \\ controlador \\ XNS") que usa el sistema de e/s para cargar el controlador de dispositivo. Además, si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.

Ejemplo: "DWDOM \\ admin"

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")
</dt> </dl>

Estado actual del servicio base.

Los valores son:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Detenido** ("detenido")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Inicio pendiente** ("Inicio pendiente")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Detención pendiente** ("detención pendiente")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

En **ejecución** ("en ejecución")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Continuar pendiente** ("continuar pendiente")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Pausar pendiente** ("pausa pendiente")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

En **pausa** ("en pausa")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("desconocido")


</dt> <dd></dd> </dl>

**Windows Server 2008 y Windows Vista:** Esta propiedad es de solo lectura antes de Windows 7 y Windows Server 2008 R2.

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios Estados operativos y no operativos. Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo). Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio". El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.

Los valores son:

<dt>

<span id="OK"></span><span id="ok"></span>

**Aceptar** ("Aceptar")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred FAIL** ("Pred FAIL")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detener** ("detener")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

Con **estrés** ("acentuado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Recover** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicación perdida** ("pérdida de comunicación")


</dt> <dd></dd> </dl>

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class name ")
</dt> </dl>

Nombre de tipo del sistema que hospeda este servicio.

Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system). Nombre "), [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nombre del sistema ")
</dt> </dl>

Nombre del sistema que hospeda este servicio.

Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID. de etiqueta")
</dt> </dl>

Valor de etiqueta único para este servicio en el grupo. Un valor de 0 (cero) indica que el servicio no tiene una etiqueta. Se puede usar una etiqueta para ordenar el inicio del servicio en un grupo de orden de carga mediante la especificación de un vector de orden de etiquetas en el registro ubicado en:

**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local GroupOrderList    

Las etiquetas solo se evalúan para el controlador de kernel y los servicios de tipo de inicio de controlador del sistema de archivos que tienen modos de inicio o de inicio del sistema.

Esta propiedad se hereda de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**TotalSessions**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de sesiones en el servidor actual. Esto incluye las sesiones conectadas y desconectadas.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**displayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tiempo de espera estimado")
</dt> </dl>

Tiempo estimado necesario, en milisegundos, para una operación pendiente de inicio, detención, pausa o continuación. Una vez transcurrido el tiempo especificado, el servicio realiza su siguiente llamada al método **SetServiceStatus** con un valor de punto de [**comprobación**](/windows/desktop/CIMWin32Prov/win32-service) incrementado o un cambio en **CurrentState**. Si la cantidad de tiempo especificada por **WaitHint** pasa y el **punto de comprobación** no se ha incrementado o **CurrentState** no ha cambiado, el administrador de control de servicios o el programa de control de servicio supone que se ha producido un error.

Esta propiedad se hereda del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Dado que la clase **Win32 \_ TerminalService** es una subclase de la clase de [**\_ servicio de Win32**](/windows/desktop/CIMWin32Prov/win32-service) , la clase hereda todas las propiedades y los métodos del **\_ servicio Win32**.

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) está asociado a **Win32 \_ TerminalService** como la propiedad **Setting** de la [**Asociación \_ TerminalServiceToSetting de Win32**](win32-terminalservicetosetting.md) .

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) está asociado a **Win32 \_ TerminalService** como la propiedad **Setting** de la [**Asociación \_ TSSessionDirectorySetting de Win32**](win32-tssessiondirectorysetting.md) .

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dt>

[**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**\_Servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

