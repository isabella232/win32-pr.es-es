---
description: Representa un servicio en un sistema informático que ejecuta Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Win32_Service clase
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
ms.openlocfilehash: a33265b3dfc3b114d55b381a229b717e291bbd258716e8305d9995282d29b3f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759265"
---
# <a name="win32_service-class"></a>Clase de servicio Win32 \_

La **clase \_ WMI de servicio Win32** [representa](../wmisdk/retrieving-a-class.md) un servicio en un sistema informático que ejecuta Windows.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

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

La **clase \_ Servicio Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ Servicio Win32** tiene estos métodos.



| Método                                                                               | Descripción                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Change**](change-method-in-class-win32-service.md)                               | Modifica un servicio.<br/>                                                                       |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-service.md)             | Modifica el modo de inicio de un servicio.<br/>                                                     |
| [**Creación**](create-method-in-class-win32-service.md)                               | Crea un nuevo servicio.<br/>                                                                    |
| [**Eliminar**](delete-method-in-class-win32-service.md)                               | Elimina un servicio existente.<br/>                                                              |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-service.md) | Devuelve el descriptor de seguridad que controla el acceso al servicio.<br/>                      |
| [**InterrogateService**](interrogateservice-method-in-class-win32-service.md)       | Solicita que un servicio actualice su estado al administrador de servicios.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Intenta colocar un servicio en estado en pausa.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Intenta colocar un servicio en el estado reanudado.<br/>                                         |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-service.md) | Escribe una versión actualizada del descriptor de seguridad que controla el acceso al servicio.<br/> |
| [**StartService**](startservice-method-in-class-win32-service.md)                   | Intenta colocar un servicio en el estado de inicio.<br/>                                       |
| [**StopService**](stopservice-method-in-class-win32-service.md)                     | Coloca un servicio en estado detenido.<br/>                                                    |
| [**UserControlService**](usercontrolservice-method-in-class-win32-service.md)       | Intenta enviar un código de control definido por el usuario a un servicio.<br/>                                |



 

### <a name="properties"></a>Propiedades

La **clase \_ Servicio Win32** tiene estas propiedades.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")
</dt> </dl>

Indica si el servicio se puede pausar.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")
</dt> </dl>

Indica si se puede detener el servicio.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Descripción breve del servicio: una cadena de una línea.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Checkpoint**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")
</dt> </dl>

Valor que el servicio incrementa periódicamente para informar de su progreso durante una operación larga de inicio, detenerse, pausar o continuar. Por ejemplo, el servicio incrementa este valor a medida que completa cada paso de su inicialización cuando se inicia. El programa de interfaz de usuario que invoca la operación en el servicio usa este valor para realizar un seguimiento del progreso del servicio durante una operación larga. Este valor no es válido y debe ser cero cuando el servicio no tiene una operación de inicio, detenerse, pausar o continuar pendiente.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre de clase")
</dt> </dl>

Nombre de la primera clase concreta que aparece en la cadena de herencia utilizada en la creación de una instancia de . Cuando se usa con las otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de esta clase y sus subclases.

Esta propiedad se hereda del [**servicio CIM. \_**](cim-service.md)

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")
</dt> </dl>

Si **es True,** el servicio se inicia después de que se inicien otros servicios de inicio automático más un breve retraso.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 y Windows Vista:** Esta propiedad no se admite antes de Windows Server 2016 y Windows 10.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")
</dt> </dl>

Indica si el servicio puede crear o comunicarse con ventanas en el escritorio y, por tanto, interactuar de alguna manera con un usuario. Los servicios interactivos deben ejecutarse en la cuenta de sistema local. La mayoría de los servicios no son interactivos; es decir, no se comunican con el usuario de ninguna manera.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre para mostrar")
</dt> </dl>

Nombre del servicio tal como se ve en el complemento Servicios. Esta cadena tiene una longitud máxima de 256 caracteres. Tenga en cuenta que el nombre para mostrar y el nombre del servicio (que se almacena en el Registro) no siempre son iguales. Por ejemplo, el servicio cliente DHCP tiene el nombre de servicio Dhcp, pero el nombre para mostrar cliente DHCP. El nombre se conserva en el Administrador de control de servicios. Sin embargo, **las comparaciones de DisplayName** siempre no tienen en cuenta mayúsculas de minúsculas.

Restricción: acepta el mismo valor que la **propiedad Name.**

Ejemplo: "Atdisk"

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Gravedad del error de inicio")
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

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Código de salida")
</dt> </dl>

Windows código de error que define los errores detectados al iniciar o detener el servicio. Esta propiedad se establece en **\_ ERROR SERVICE SPECIFIC \_ \_ ERROR** (1066) cuando el error es único para el servicio representado por esta clase y la información sobre el error está disponible en la **propiedad ServiceSpecificExitCode.** El servicio establece este valor en **NO \_ ERROR cuando se** ejecuta y, de nuevo, en la finalización normal.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

El objeto Date está instalado. Esta propiedad no requiere un valor para indicar que el objeto está instalado.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **Clave**](../wmisdk/key-qualifier.md)
</dt> </dl>

Identificador único del servicio que proporciona una indicación de la funcionalidad que se administra. Esta funcionalidad se describe en la **propiedad Description** del objeto .

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre de ruta de acceso del archivo")
</dt> </dl>

Ruta de acceso completa al archivo binario de servicio que implementa el servicio.

Ejemplo: \\ "SystemRoot \\ System32 \\ drivers \\afd.sys"

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE STATUS \| [**\_ \_ PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Id. de proceso")
</dt> </dl>

Identificador de proceso del servicio.

Ejemplo: 324

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Código de salida específico del servidor")
</dt> </dl>

Código de error específico del servicio para los errores que se producen mientras el servicio se está iniciando o deteniendo. El servicio representado por esta clase define los códigos de salida. Este valor solo se establece cuando el valor **de la propiedad ExitCode** es **ERROR SERVICE SPECIFIC \_ \_ \_ ERROR** (1066).

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")
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

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**Comenzó**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Indica si se ha iniciado o no el servicio.

Esta propiedad se hereda del [**servicio CIM. \_**](cim-service.md)

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Modo de inicio")
</dt> </dl>

Modo de inicio del Windows base de datos.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque** ("Arranque")


</dt> <dd>

Controlador de dispositivo iniciado por el cargador del sistema operativo (válido solo para los servicios de controlador).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("Sistema")


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

Servicio que debe iniciar el Administrador de control de servicios cuando un proceso llame al [**método StartService.**](startservice-method-in-class-win32-service.md) Estos servicios no se inician a menos que un usuario inicie sesión y los inicie.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("Deshabilitado")


</dt> <dd>

Servicio que no se puede iniciar hasta que startMode cambia a Automático o Manual.

</dd> </dl>

Esta propiedad se hereda del [**servicio CIM. \_**](cim-service.md)

</dd> <dt>

**Startname**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")
</dt> </dl>

Nombre de cuenta con el que se ejecuta un servicio. Según el tipo de servicio, el nombre de la cuenta puede tener el formato "NombreDeUsuario DeNombreDe DomainName" o \\ Formato UPN (" *Username@DomainName* "). El proceso de servicio se registra mediante uno de estos dos formularios cuando se ejecuta. Si la cuenta pertenece al dominio integrado, ". \\ Nombre de usuario" se puede especificar. En el caso de los controladores de kernel o de nivel de sistema, **StartName** contiene el nombre del objeto de controlador (es decir, \\ "FileSystem \\ Rdr" o \\ "Driver Xns") que el sistema de E/S usa para cargar el controlador de \\ dispositivo. Además, si **se especifica NULL,** el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de E/S basado en el nombre del servicio.

Ejemplo: "DWDOM \\ Admin"

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")
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

**Ejecución** ("En ejecución")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Continuar pendiente** ("Continuar pendiente")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Pausa pendiente** ("Pausa pendiente")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**En pausa** ("en pausa")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unknown** ("Unknown")


</dt> <dd></dd> </dl>

**Windows Server 2008 y Windows Vista:** Esta propiedad es de solo lectura antes de Windows 7 y Windows Server 2008 R2.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Los estados no de operación incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los demás estados.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

**Unknown** ("Unknown")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Error de pred** ("error previo")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Starting** ("Starting")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Detención** ("Detención")


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

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")
</dt> </dl>

Nombre de tipo del sistema que hospeda este servicio.

Esta propiedad se hereda del [**servicio CIM. \_**](cim-service.md)

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")
</dt> </dl>

Nombre del sistema que hospeda este servicio.

Esta propiedad se hereda del [**servicio CIM. \_**](cim-service.md)

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Id. de etiqueta")
</dt> </dl>

Valor de etiqueta único para este servicio en el grupo. Un valor de 0 (cero) indica que el servicio no tiene una etiqueta. Una etiqueta se puede usar para ordenar el inicio del servicio dentro de un grupo de pedidos de carga especificando un vector de orden de etiquetas en el registro ubicado en:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **GroupOrderList**    

Las etiquetas solo se evalúan para los servicios de tipo de inicio Controlador de kernel y Controlador del sistema de archivos que tienen modos de inicio de arranque o sistema.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estimated Wait Time")
</dt> </dl>

Tiempo estimado necesario, en milisegundos, para una operación pendiente de inicio, detenerse, pausar o continuar. Una vez transcurrido el tiempo especificado, el servicio realiza su siguiente llamada al método **SetServiceStatus** con un valor **de CheckPoint** incrementado o un cambio en **CurrentState**. Si la cantidad de tiempo especificada por **WaitHint** pasa y **CheckPoint** no se ha incrementado o **CurrentState** no ha cambiado, el administrador de control de servicios o el programa de control de servicios asumen que se ha producido un error.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase De servicio \_ win32** se deriva de [**\_ BaseService de Win32.**](win32-baseservice.md)

La forma en que administra un equipo específico depende en gran medida del rol que desempeña ese equipo. Por ejemplo, generalmente supervisa distintos aspectos de un servidor DNS que un servidor DHCP. Aunque ninguna propiedad individual puede saber si un equipo determinado es un servidor de bases de datos, un servidor de correo electrónico o un servidor multimedia, a menudo puede identificar el rol que desempeña un equipo mediante la identificación de los servicios instalados en él.

En organizaciones grandes, es probable que solo uno de los principales servicios (como el correo electrónico) esté instalado en un solo equipo. No sería habitual que un servidor de correo también actuara como servidor para los archivos de reproductor de microsoft® Windows Media® technologies. Por este problema, identificar un servicio instalado en un equipo puede ayudar a identificar el rol del equipo en la red. Si el servicio microsoft® Exchange Server está instalado y ejecutándose en un equipo, por lo general es seguro suponer que este equipo funciona como un servidor de correo.

Puede usar la clase de **servicio Win32 \_ de** WMI para enumerar los servicios instalados en un equipo. Además, puede usar esta clase para determinar si esos servicios se están ejecutando actualmente y devolver cualquier otra información necesaria sobre ese servicio y cómo se ha configurado.

Una aplicación de servicio se ajusta a las reglas de interfaz del Administrador de control de servicios (SCM) y un usuario puede iniciarla automáticamente al iniciar el sistema a través de la utilidad del panel de control Servicios o mediante una aplicación que usa las funciones de servicio incluidas en la API de Windows. Los servicios se pueden iniciar cuando no hay usuarios que hayan iniciado sesión en el equipo.

Un usuario que se conecta desde un equipo remoto debe tener habilitado el privilegio **SC \_ MANAGER \_ CONNECT** para poder enumerar esta clase. Para obtener más información, vea [Derechos de acceso y seguridad del servicio.](../services/service-security-and-access-rights.md)

## <a name="examples"></a>Ejemplos

La consulta PS- WMI que devuelve el servicio ["Estado"](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) en un grupo de dispositivos Ejemplo de PowerShell en la Galería de TechNet usa el servicio **\_ Win32** para crear una lista de dispositivos de Active Directory y, a continuación, consultar cada dispositivo que responde con ping para un servicio específico en ejecución.

El [ejemplo de](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell del informe del servidor en la Galería de TechNet usa el servicio **\_ Win32** para recopilar información del servidor y publicar en el documento de Word.

El siguiente ejemplo de código VBScript muestra todos los servicios instalados actualmente.


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



En el siguiente ejemplo de código VBScript se describen los servicios en pausa, en ejecución y detenidos en el equipo especificado.


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



El siguiente script de Perl muestra cómo recuperar una lista de servicios en ejecución de instancias del **servicio Win32 \_**.


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



En el ejemplo \# c siguiente se usa [Microsoft.Management.Infrastructure para](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) recuperar todos los servicios en ejecución en el equipo local.


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



En el ejemplo \# de código C siguiente se usa el espacio de nombres [System.Management](/dotnet/api/system.management) para recuperar todos los servicios en ejecución en el equipo local.

> [!Note]  
> [System.Management contiene](/dotnet/api/system.management) las clases originales usadas para tener acceso a WMI; sin embargo, se consideran más lentos y, por lo general, no se escalan, así como sus homólogos [de Microsoft.Management.Infrastructure.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))

 


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BaseService de Win32 \_**](win32-baseservice.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Tareas wmi: servicios](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
