---
description: Representa un servicio en un equipo que ejecuta Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Win32_Service (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080117"
---
# <a name="win32_service-class"></a>\_Clase de servicio Win32

La [clase WMI](../wmisdk/retrieving-a-class.md) del **\_ servicio Win32** representa un servicio en un equipo que ejecuta Windows.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a>Miembros

La clase de **\_ servicio Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ servicio Win32** tiene estos métodos.



| Método                                                                               | Descripción                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Cambio**](change-method-in-class-win32-service.md)                               | Modifica un servicio.<br/>                                                                       |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-service.md)             | Modifica el modo de inicio de un servicio.<br/>                                                     |
| [**A**](create-method-in-class-win32-service.md)                               | Crea un nuevo servicio.<br/>                                                                    |
| [**Elimínelos**](delete-method-in-class-win32-service.md)                               | Elimina un servicio existente.<br/>                                                              |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-service.md) | Devuelve el descriptor de seguridad que controla el acceso al servicio.<br/>                      |
| [**InterrogateService**](interrogateservice-method-in-class-win32-service.md)       | Solicita que un servicio actualice su estado al administrador de servicios.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Intenta poner un servicio en estado de pausa.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Intenta poner un servicio en estado reanudado.<br/>                                         |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-service.md) | Escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.<br/> |
| [**StartService**](startservice-method-in-class-win32-service.md)                   | Intenta colocar un servicio en el estado de inicio.<br/>                                       |
| [**StopService**](stopservice-method-in-class-win32-service.md)                     | Coloca un servicio en estado detenido.<br/>                                                    |
| [**UserControlService**](usercontrolservice-method-in-class-win32-service.md)       | Intenta enviar un código de control definido por el usuario a un servicio.<br/>                                |



 

### <a name="properties"></a>Propiedades

La clase de **\_ servicio Win32** tiene estas propiedades.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| Service \_ Accept \_ PAUSE \_ Continue"), [**displayName**](../wmisdk/standard-qualifiers.md) ("el servicio acepta la pausa")
</dt> </dl>

Indica si se puede pausar el servicio.

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures Service \| [**\_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status)servicio \| dwControlsAccepted \| \_ \_ Stop"), [**displayName**](../wmisdk/standard-qualifiers.md) ("el servicio acepta la detención")
</dt> </dl>

Indica si se puede detener el servicio.

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción del servicio: una cadena de una línea.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**SnapSure**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")
</dt> </dl>

Valor que el servicio incrementa periódicamente para informar sobre su progreso durante una operación larga de inicio, detención, pausa o continuación. Por ejemplo, el servicio incrementa este valor a medida que completa cada paso de su inicialización cuando se inicia. El programa de interfaz de usuario que invoca la operación en el servicio usa este valor para realizar el seguimiento del progreso del servicio durante una operación larga. Este valor no es válido y debe ser cero cuando el servicio no tiene pendiente una operación de inicio, detención, pausa o continuación.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")
</dt> </dl>

Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia. Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.

Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api Service \| Structures \| [**\_ retardo \_ auto \_ Start \_ info**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Inicio automático retrasado")
</dt> </dl>

Si es **true**, el servicio se inicia después de que se inicien otros servicios de inicio automático más un breve retraso.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| Service \_ Interactive \_ Process"), [**displayName**](../wmisdk/standard-qualifiers.md) ("interactúa con Desktop")
</dt> </dl>

Indica si el servicio puede crear o comunicarse con Windows en el escritorio y, por tanto, interactuar de algún modo con un usuario. Los servicios interactivos deben ejecutarse en la cuenta de sistema local. La mayoría de los servicios no son interactivos; es decir, no se comunican con el usuario de ningún modo.

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpDisplayName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre para mostrar")
</dt> </dl>

Nombre del servicio tal como se ve en el complemento Servicios. Esta cadena tiene una longitud máxima de 256 caracteres. Tenga en cuenta que el nombre para mostrar y el nombre del servicio (que se almacena en el registro) no son siempre los mismos. Por ejemplo, el servicio de cliente DHCP tiene el nombre de servicio DHCP, pero el cliente DHCP de nombre para mostrar. El nombre se conserva en las mayúsculas y minúsculas en el administrador de control de servicios. Sin embargo, las comparaciones de **displayName** siempre distinguen entre mayúsculas y minúsculas.

Constraint: acepta el mismo valor que la propiedad **Name** .

Ejemplo: "Endisco"

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**displayName**](../wmisdk/standard-qualifiers.md) ("gravedad del error de inicio")
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

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**displayName**](../wmisdk/standard-qualifiers.md) ("código de salida")
</dt> </dl>

Código de error de Windows que define los errores detectados al iniciar o detener el servicio. Esta propiedad se establece en **\_ \_ \_ error específico del servicio de error** (1066) cuando el error es exclusivo del servicio representado por esta clase, y la información sobre el error está disponible en la propiedad **ServiceSpecificExitCode** . El servicio establece este valor en **ningún \_ error** cuando se ejecuta y de nuevo tras la terminación normal.

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")
</dt> </dl>

El objeto de fecha está instalado. Esta propiedad no requiere un valor para indicar que el objeto está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](../wmisdk/key-qualifier.md)
</dt> </dl>

Identificador único del servicio que proporciona una indicación de la funcionalidad que se administra. Esta funcionalidad se describe en la propiedad **Description** del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("File path name")
</dt> </dl>

Ruta de acceso completa al archivo binario del servicio que implementa el servicio.

Ejemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Process ID")
</dt> </dl>

Identificador de proceso del servicio.

Ejemplo: 324

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**displayName**](../wmisdk/standard-qualifiers.md) ("código de salida específico del servidor")
</dt> </dl>

Código de error específico del servicio para los errores que se producen mientras el servicio se está iniciando o deteniendo. Los códigos de salida se definen mediante el servicio representado por esta clase. Este valor solo se establece cuando el valor de la propiedad **ExitCode** es **\_ \_ \_ error específico del servicio de error** (1066).

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Service Type")
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

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("iniciado")
</dt> </dl>

Indica si se ha iniciado o no el servicio.

Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("modo de inicio")
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

Servicio que el administrador de control de servicios iniciará cuando un proceso llame al método [**StartService**](startservice-method-in-class-win32-service.md) . Estos servicios no se inician a menos que un usuario inicie sesión y los inicie.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("deshabilitado")


</dt> <dd>

Servicio que no se puede iniciar hasta que su StartMode se cambie a automático o manual.

</dd> </dl>

Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de la cuenta de inicio")
</dt> </dl>

Nombre de cuenta con la que se ejecuta un servicio. Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato "nombreDeDominio \\ nombreDeUsuario" o el formato UPN (" *Username@DomainName* "). El proceso de servicio se registra con una de estas dos formas cuando se ejecuta. Si la cuenta pertenece al dominio integrado, ". \\ Se puede especificar username. En el caso de los controladores de kernel o de nivel de sistema, **StartName** contiene el nombre de objeto del controlador (es decir, " \\ filesystem \\ RDR" o " \\ controlador \\ XNS") que usa el sistema de e/s para cargar el controlador de dispositivo. Además, si se especifica **null** , el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de e/s basado en el nombre del servicio.

Ejemplo: "DWDOM \\ admin"

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**displayName**](../wmisdk/standard-qualifiers.md) ("State")
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

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios Estados operativos y no operativos. Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo). Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio". El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

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

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" System Class name ")
</dt> </dl>

Nombre de tipo del sistema que hospeda este servicio.

Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema ")
</dt> </dl>

Nombre del sistema que hospeda este servicio.

Esta propiedad se hereda del [**\_ servicio CIM**](cim-service.md).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**query \_ Service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("ID. de etiqueta")
</dt> </dl>

Valor de etiqueta único para este servicio en el grupo. Un valor de 0 (cero) indica que el servicio no tiene una etiqueta. Se puede usar una etiqueta para ordenar el inicio del servicio en un grupo de orden de carga mediante la especificación de un vector de orden de etiquetas en el registro ubicado en:

**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local GroupOrderList    

Las etiquetas solo se evalúan para el controlador de kernel y los servicios de tipo de inicio de controlador del sistema de archivos que tienen modos de inicio o de inicio del sistema.

Esta propiedad se hereda de [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Service Structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**displayName**](../wmisdk/standard-qualifiers.md) ("tiempo de espera estimado")
</dt> </dl>

Tiempo estimado necesario, en milisegundos, para una operación pendiente de inicio, detención, pausa o continuación. Una vez transcurrido el tiempo especificado, el servicio realiza su siguiente llamada al método **SetServiceStatus** con un valor de punto de **comprobación** incrementado o un cambio en **CurrentState**. Si la cantidad de tiempo especificada por **WaitHint** pasa y el **punto de comprobación** no se ha incrementado o **CurrentState** no ha cambiado, el administrador de control de servicios o el programa de control de servicio supone que se ha producido un error.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ servicio Win32** se deriva de [**Win32 \_ BaseService**](win32-baseservice.md).

La forma en que se administra un equipo específico depende en gran medida del rol que desempeña el equipo. Por ejemplo, en general, se supervisan distintos aspectos de un servidor DNS que un servidor DHCP. Aunque ninguna propiedad puede indicar si un equipo determinado es un servidor de base de datos, un servidor de correo electrónico o un servidor multimedia, a menudo puede identificar el rol que reproduce un equipo mediante la identificación de los servicios instalados en él.

En organizaciones de gran tamaño, es probable que solo uno de los servicios principales (como el correo electrónico) esté instalado en un solo equipo. Es poco habitual que un servidor de correo también funcione como servidor de Microsoft® archivos del reproductor de Windows Media® Technologies. Debido a esto, la identificación de un servicio instalado en un equipo puede ayudar a identificar el rol del equipo en la red. Si el servicio Microsoft® Exchange Server está instalado y en ejecución en un equipo, por lo general es seguro suponer que este equipo funciona como un servidor de correo.

Puede utilizar la clase de **\_ servicio Win32** de WMI para enumerar los servicios instalados en un equipo. Además, puede usar esta clase para determinar si esos servicios se están ejecutando actualmente y para devolver cualquier otra información necesaria sobre el servicio y cómo se ha configurado.

Una aplicación de servicio se ajusta a las reglas de la interfaz del administrador de control de servicios (SCM) y un usuario puede iniciarla automáticamente en el inicio del sistema a través de la utilidad servicios del panel de control, o bien mediante una aplicación que usa las funciones de servicio incluidas en la API de Windows. Los servicios pueden iniciarse cuando no haya usuarios con sesión iniciada en el equipo.

Un usuario que se conecta desde un equipo remoto debe tener el privilegio de **\_ \_ conexión SC Manager** habilitado para poder enumerar esta clase. Para obtener más información, consulte [seguridad del servicio y derechos de acceso](../services/service-security-and-access-rights.md).

## <a name="examples"></a>Ejemplos

La [consulta PS-WMI que devuelve el servicio "estado" en un grupo de dispositivos ejemplo de](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell en la galería de TechNet usa el **\_ servicio Win32** para crear una lista de dispositivos a partir de Active Directory y, a continuación, consultar cada dispositivo que responde con pingfor un servicio específico en ejecución.

El ejemplo de PowerShell para [informes de servidor](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) en la galería de TechNet utiliza el **\_ servicio Win32** para recopilar información del servidor y publicar en un documento de Word.

En el siguiente ejemplo de código de VBScript se muestran todos los servicios instalados actualmente.


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



El siguiente ejemplo de código de VBScript describe los servicios en pausa, en ejecución y detenido en el equipo especificado.


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



El siguiente script Perl muestra cómo recuperar una lista de los servicios en ejecución de las instancias del **\_ servicio de Win32**.


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



En el siguiente \# ejemplo de c se usa [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) para recuperar todos los servicios que se están ejecutando en el equipo local.


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



El siguiente \# ejemplo de código C usa el espacio de nombres [System. Management](/dotnet/api/system.management) para recuperar todos los servicios en ejecución en el equipo local.

> [!Note]  
> [System. Management](/dotnet/api/system.management) contiene las clases originales utilizadas para tener acceso a WMI. sin embargo, se consideran más lentos y, por lo general, no se escalan, así como sus homólogos [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


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

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Tareas WMI: servicios](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
