---
title: Clase Win32_TerminalService
description: Subclase de la clase De \_ servicio Win32. TerminalService de Win32 representa la propiedad Element de la asociación \_ \_ TerminalServiceToSetting de Win32.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService clase Servicios de Escritorio remoto
- Win32_TerminalService clase Servicios de Escritorio remoto , descrita
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
ms.openlocfilehash: 735b033017958816e8e9a40caea935847104fdcbe3e9acf3128890d88685d09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867855"
---
# <a name="win32_terminalservice-class"></a>Clase TerminalService de Win32 \_

La **clase WMI \_ TerminalService de Win32** es una subclase de la [**clase \_ Servicio Win32.**](/windows/desktop/CIMWin32Prov/win32-service) **Win32 \_ TerminalService** representa la **propiedad Element** de la [**asociación \_ TerminalServiceToSetting de Win32.**](win32-terminalservicetosetting.md)

La sintaxis siguiente se simplifica a partir del código MOF e incluye todas las propiedades definidas y heredadas, en orden alfabético.

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

La **clase \_ TerminalService de Win32** tiene estos métodos.



| Método                                                                       | Descripción                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Change**](win32-terminalservice-change.md)                               | Modifica un servicio.<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | Modifica el modo de inicio de un servicio.<br/>                                                     |
| [**Crear**](win32-terminalservice-create.md)                               | Crea un nuevo servicio.<br/>                                                                    |
| [**Eliminar**](win32-terminalservice-delete.md)                               | Elimina un servicio existente.<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | Devuelve el descriptor de seguridad que controla el acceso al servicio.<br/>                      |
| [**InterrogateService**](win32-terminalservice-interrogateservice.md)       | Solicita que un servicio actualice su estado al administrador de servicios.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Intenta colocar un servicio en estado de pausa.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Intenta colocar un servicio en el estado reanudado.<br/>                                         |
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

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")
</dt> </dl>

Indica si el servicio se puede pausar.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")
</dt> </dl>

Indica si se puede detener el servicio.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descripción del servicio de una cadena de una línea.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Checkpoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")
</dt> </dl>

Valor que el servicio incrementa periódicamente para informar de su progreso durante una operación larga de inicio, detenerse, pausar o continuar. Por ejemplo, el servicio incrementa este valor a medida que completa cada paso de su inicialización cuando se inicia. El programa de interfaz de usuario que invoca la operación en el servicio usa este valor para realizar un seguimiento del progreso del servicio durante una operación larga. Este valor no es válido y debe ser cero cuando el servicio no tenga pendiente una operación de inicio, detenerse, pausar o continuar.

Esta propiedad se hereda del [**servicio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre de clase")
</dt> </dl>

Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de . Cuando se usa con las otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de esta clase y sus subclases.

Esta propiedad se hereda del [**servicio CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")
</dt> </dl>

Si **es True**, el servicio se inicia después de que se inicien otros servicios de inicio automático más un breve retraso.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.

Esta propiedad se hereda del [**servicio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")
</dt> </dl>

Indica si el servicio puede crear o comunicarse con ventanas en el escritorio y, por tanto, interactuar de alguna manera con un usuario. Los servicios interactivos deben ejecutarse en la cuenta de sistema local. La mayoría de los servicios no son interactivos; es decir, no se comunican con el usuario de ninguna manera.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**DisconnectedSessions**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de sesiones desconectadas en el servidor actual. Estas sesiones pueden seguir consumiendo activamente recursos de servidor, pero actualmente no tienen conexión de red con un cliente.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre para mostrar")
</dt> </dl>

Nombre del servicio tal como se ve en el complemento Servicios. Esta cadena tiene una longitud máxima de 256 caracteres. Tenga en cuenta que el nombre para mostrar y el nombre del servicio (que se almacena en el Registro) no siempre son iguales. Por ejemplo, el servicio cliente DHCP tiene el nombre de servicio Dhcp, pero el nombre para mostrar cliente DHCP. El nombre se conserva en el Administrador de control de servicios. Sin embargo, [**las comparaciones de DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) siempre no tienen en cuenta mayúsculas de minúsculas.

Restricción: acepta el mismo valor que la [**propiedad Name.**](/windows/desktop/CIMWin32Prov/win32-service)

Ejemplo: "Atdisk"

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Gravedad del error de inicio")
</dt> </dl>

Gravedad del error si este servicio no se inicia durante el inicio. El valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** ("Omitir")


</dt> <dd>

No se notifica al usuario.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")


</dt> <dd>

Se notifica al usuario. Normalmente, se trata de una pantalla de cuadro de mensaje que notifica al usuario el problema.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("Grave")


</dt> <dd>

El sistema se reinicia con la última configuración válida conocida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("Crítico")


</dt> <dd>

El sistema intenta reiniciarse con una configuración válida. Si el servicio no se inicia una segunda vez, se produce un error de inicio.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")


</dt> <dd>

Se desconoce la gravedad del error.

</dd> </dl>

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Código de salida")
</dt> </dl>

Windows código de error que define los errores detectados al iniciar o detener el servicio. Esta propiedad se establece en **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) cuando el error es único para el servicio representado por esta clase y la información sobre el error está disponible en la [**propiedad ServiceSpecificExitCode.**](/windows/desktop/CIMWin32Prov/win32-service) El servicio establece este valor en **NO \_ ERROR cuando se** ejecuta y, de nuevo, en la finalización normal.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Fecha de instalación")
</dt> </dl>

El objeto Date está instalado. Esta propiedad no requiere un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador único del servicio que proporciona una indicación de la funcionalidad que se administra. Esta funcionalidad se describe en la [**propiedad Description**](/windows/desktop/CIMWin32Prov/win32-service) del objeto .

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nombre de ruta de acceso del archivo")
</dt> </dl>

Ruta de acceso completa al archivo binario de servicio que implementa el servicio.

Ejemplo: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys"

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE STATUS \| [**\_ \_ PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Id. de proceso")
</dt> </dl>

Identificador de proceso del servicio.

Ejemplo: 324

Esta propiedad se hereda del [**servicio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Código de salida específico del servidor")
</dt> </dl>

Código de error específico del servicio para los errores que se producen mientras el servicio se está iniciando o deteniendo. El servicio representado por esta clase define los códigos de salida. Este valor solo se establece cuando el valor [**de la propiedad ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) es **ERROR SERVICE SPECIFIC \_ \_ \_ ERROR** (1066).

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")
</dt> </dl>

Tipo de servicio proporcionado a los procesos de llamada.

Los valores son:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Kernel Driver** ("Kernel Driver")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Controlador del sistema de archivos** ("controlador del sistema de archivos")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Adaptador** ("Adaptador")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Recognizer Driver** ("Recognizer Driver")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Proceso propio** ("Proceso propio")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Proceso de uso compartido** ("Proceso de uso compartido")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Proceso interactivo** ("proceso interactivo")


</dt> <dd></dd> </dl>

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Comenzó**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Indica si se ha iniciado o no el servicio.

Esta propiedad se hereda del [**servicio CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Modo de inicio")
</dt> </dl>

Modo de inicio del Windows base.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque** ("Arranque")


</dt> <dd>

Controlador de dispositivo iniciado por el cargador de sistema operativo (válido solo para los servicios de controladores).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


</dt> <dd>

Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")


</dt> <dd>

Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema. Los servicios automáticos se inician incluso si un usuario no inicia sesión.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")


</dt> <dd>

Servicio que debe iniciar el Administrador de control de servicios cuando un proceso llame al [**método StartService.**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) Estos servicios no se inician a menos que un usuario inicie sesión e inicie estos servicios.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("Deshabilitado")


</dt> <dd>

Servicio que no se puede iniciar hasta que startMode cambie a Auto o Manual.

</dd> </dl>

Esta propiedad se hereda del [**servicio CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**Startname**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")
</dt> </dl>

Nombre de cuenta con el que se ejecuta un servicio. Según el tipo de servicio, el nombre de la cuenta puede tener el formato "NombredeUsuario de nombreDe DomainName" o \\ Formato UPN (" *Username@DomainName* "). El proceso de servicio se registra mediante uno de estos dos formularios cuando se ejecuta. Si la cuenta pertenece al dominio integrado, ". \\ Nombre de usuario" se puede especificar. En el caso de los controladores de nivel de sistema o kernel, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contiene el nombre del objeto de controlador (es decir, \\ "FileSystem \\ Rdr" o \\ "Driver Xns") que el sistema de E/S usa para cargar el controlador de \\ dispositivo. Además, si **se especifica NULL,** el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de E/S basado en el nombre del servicio.

Ejemplo: "DWDOM \\ Admin"

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")
</dt> </dl>

Estado actual del servicio base.

Los valores son:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Detenido** ("Detenido")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Iniciar pendiente** ("Iniciar pendiente")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Detener pendiente** ("Detener pendiente")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**En** ejecución ("En ejecución")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Continuar pendiente** ("Continuar pendiente")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Pausa pendiente** ("Pausa pendiente")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**En pausa** ("En pausa")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("Desconocido")


</dt> <dd></dd> </dl>

**Windows Server 2008 y Windows Vista:** Esta propiedad es de solo lectura antes Windows 7 y Windows Server 2008 R2.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Los estados no operativo incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "correcto" ni está en uno de los demás estados.

Los valores son:

<dt>

<span id="OK"></span><span id="ok"></span>

**Ok** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Error** ("Error")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** ("Desconocido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**A partir** de ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Deteniendo")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servicio** ("Servicio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Estresado** ("estresado")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sin contacto** ("Sin contacto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comm perdido** ("Comm perdido")


</dt> <dd></dd> </dl>

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")
</dt> </dl>

Escriba el nombre del sistema que hospeda este servicio.

Esta propiedad se hereda del [**servicio CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system). Name"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")
</dt> </dl>

Nombre del sistema que hospeda este servicio.

Esta propiedad se hereda del [**servicio CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Id. de etiqueta")
</dt> </dl>

Valor de etiqueta único para este servicio del grupo. Un valor de 0 (cero) indica que el servicio no tiene una etiqueta. Una etiqueta se puede usar para ordenar el inicio del servicio dentro de un grupo de pedidos de carga especificando un vector de orden de etiquetas en el registro ubicado en:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **GroupOrderList**    

Las etiquetas solo se evalúan para los servicios de tipo de inicio del controlador kernel y del controlador del sistema de archivos que tienen modos de inicio de arranque o del sistema.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**TotalSessions**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de sesiones en el servidor actual. Esto incluye las sesiones conectadas y desconectadas.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")
</dt> </dl>

Tiempo estimado necesario, en milisegundos, para una operación pendiente de inicio, detenerse, pausar o continuar. Una vez transcurrido el tiempo especificado, el servicio realiza su siguiente llamada al método **SetServiceStatus** con un valor [**de CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) incrementado o un cambio en **CurrentState**. Si se supera la cantidad de tiempo especificada por **WaitHint** y **CheckPoint** no se ha incrementado o **CurrentState** no ha cambiado, el administrador de control de servicios o el programa de control de servicios asumen que se ha producido un error.

Esta propiedad se hereda del [**servicio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Puesto que **la clase \_ TerminalService de Win32** es una subclase de la clase [**Servicio Win32, \_**](/windows/desktop/CIMWin32Prov/win32-service) la clase hereda todas las propiedades y métodos del **servicio Win32. \_**

[**Win32 \_ TerminalServiceSetting está**](win32-terminalservicesetting.md) asociado a **\_ TerminalService de Win32** como la **propiedad Setting** de la asociación [**\_ TerminalServiceToSetting de Win32.**](win32-terminalservicetosetting.md)

[**Win32 \_ TSSessionDirectory está**](win32-tssessiondirectory.md) asociado a **\_ TerminalService de Win32** como la **propiedad Setting** de la asociación [**\_ TSSessionDirectorySetting de Win32.**](win32-tssessiondirectorysetting.md)

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Servicio \_ Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**Terminal De \_ Win32ServiceToSetting**](win32-terminalservicetosetting.md)
</dt> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> <dt>

[**BaseService de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**Servicio \_ CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

