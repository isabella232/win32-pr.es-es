---
description: Representa el controlador del sistema para un servicio base.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Win32_SystemDriver clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061455"
---
# <a name="win32_systemdriver-class"></a>Clase SystemDriver de Win32 \_

La **clase \_ WMI SystemDriver** [de](../wmisdk/retrieving-a-class.md) Win32 representa el controlador del sistema para un servicio base.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a>Members

La **clase \_ SystemDriver de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ SystemDriver de Win32** tiene estos métodos.



| Método                                                                              | Descripción                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Change**](change-method-in-class-win32-systemdriver.md)                         | Método de clase que modifica un servicio.<br/>                                                |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-systemdriver.md)       | Método de clase que modifica el modo de inicio de un servicio.<br/>                              |
| [**Crear**](create-method-in-class-win32-systemdriver.md)                         | Método de clase que crea un nuevo servicio.<br/>                                             |
| [**Eliminar**](delete-method-in-class-win32-systemdriver.md)                         | Método de clase que elimina un servicio existente.<br/>                                       |
| [**InterrogateService**](interrogateservice-method-in-class-win32-systemdriver.md) | Método de clase que solicita que el servicio actualice su estado al administrador de servicios.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md)             | Método de clase que intenta colocar el servicio en estado en pausa.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-systemdriver.md)           | Método de clase que intenta colocar el servicio en el estado reanudado.<br/>                |
| [**StartService**](startservice-method-in-class-win32-systemdriver.md)             | Método de clase que intenta colocar el servicio en su estado de inicio.<br/>              |
| [**StopService**](stopservice-method-in-class-win32-systemdriver.md)               | Método de clase que coloca el servicio en estado detenido.<br/>                           |
| [**UserControlService**](usercontrolservice-method-in-class-win32-systemdriver.md) | Método de clase que intenta enviar un código de control definido por el usuario a un servicio.<br/>         |



 

### <a name="properties"></a>Propiedades

La **clase \_ SystemDriver de Win32** tiene estas propiedades.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")
</dt> </dl>

El servicio se puede pausar.

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

El servicio se puede detener.

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

Breve descripción del objeto.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

Este servicio puede crear o comunicarse con ventanas en el escritorio.

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

Nombre para mostrar del servicio. Esta cadena tiene una longitud máxima de 256 caracteres. El nombre se conserva en el Administrador de control de servicios. **Las comparaciones** de DisplayName siempre no tienen en cuenta las mayúsculas y minúsculas.

Restricciones: acepta el mismo valor que la **propiedad Name.**

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

Gravedad del error si este servicio no se puede iniciar durante el inicio. Este valor indica la acción realizada por el programa de inicio si se produce un error. El sistema registra todos los errores.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Omitir** ("Omitir")


</dt> <dd>

No se notifica al usuario.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")


</dt> <dd>

Se notifica al usuario.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("Grave")


</dt> <dd>

El sistema se reinicia con la última configuración válida conocida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("Crítico")


</dt> <dd>

El sistema intenta reiniciarse con una configuración válida.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")


</dt> <dd>

Se desconoce la causa del error.

</dd> </dl>

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Código de salida")
</dt> </dl>

Windows código de error que define los problemas detectados al iniciar o detener el servicio. Esta propiedad se establece en **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) cuando el error es único para el servicio representado por esta clase y la información sobre el error está disponible en la **propiedad ServiceSpecificExitCode.** El servicio establece este valor en **NO \_ ERROR cuando se** ejecuta y, de nuevo, en la finalización normal.

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

Se instaló el objeto . Esta propiedad no necesita un valor para indicar que el objeto está instalado.

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

Identificador único para el servicio que proporciona una indicación de la funcionalidad que se administra. Esta funcionalidad se describe con más detalle en la propiedad **Descripción del** objeto.

Esta propiedad se hereda del [**servicio CIM. \_**](cim-service.md)

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

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

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

</dd> <dt>

**Comenzó**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")
</dt> </dl>

Se ha iniciado el servicio.

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

Modo de inicio del controlador del sistema.

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Arranque** ("Arranque")


</dt> <dd>

Controlador de dispositivo iniciado por el cargador del sistema operativo (válido solo para los servicios de controlador).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")


</dt> <dd>

Controlador de dispositivo iniciado por el proceso de inicialización del sistema operativo. Este valor solamente es válido para servicios de controladores.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")


</dt> <dd>

Servicio que el administrador de control de servicios iniciará automáticamente durante el inicio del sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")


</dt> <dd>

Servicio que va a iniciar el administrador de control de servicios cuando un proceso llame al [**método StartService.**](startservice-method-in-class-win32-systemdriver.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** ("Deshabilitado")


</dt> <dd>

Servicio que ya no se puede iniciar.

</dd> </dl>

</dd> <dt>

**Startname**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures QUERY SERVICE \| [**\_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")
</dt> </dl>

Nombre de cuenta con el que se ejecuta el servicio. Dependiendo del tipo de servicio, el nombre de la cuenta puede tener el formato nombreDeNombreDe \\ DomainName. El proceso de servicio se registrará mediante uno de estos dos formularios cuando se ejecute. Si la cuenta pertenece al dominio integrado, . \\ Se puede especificar el nombre de usuario. Si se especifica **NULL,** el servicio se inicia sesión como la cuenta LocalSystem. En el caso de los controladores de kernel o de nivel de sistema, **StartName** contiene el nombre del objeto de controlador (es decir, FileSystem Rdr o Driver Xns) que el sistema de entrada y salida \\ \\ \\ (E/S) usa para cargar el controlador de \\ dispositivo. Además, si **se especifica NULL,** el controlador se ejecuta con un nombre de objeto predeterminado creado por el sistema de E/S basado en el nombre del servicio.

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

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

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

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Estado actual del objeto. Se pueden definir varios estados operativos y no operativos. Los estados operativos incluyen: "Ok", "Degraded" y "Pred Fail" (un elemento, como una unidad de disco duro habilitada para SMART, puede funcionar correctamente pero predecir un error en un futuro próximo). Entre los estados no operativo se incluyen: "Error", "Starting", "Stopping" y "Service". El último, "Servicio", podría aplicarse durante la resilvering de reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo. No todo este trabajo está en línea, pero el elemento administrado no es "Correcto" ni está en uno de los demás estados.

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

Valor de etiqueta único para este servicio en el grupo. Un valor de 0 (cero) indica que no se ha asignado una etiqueta al servicio. Una etiqueta se puede usar para ordenar el inicio del servicio dentro de un grupo de pedidos de carga especificando un vector de orden de etiquetas en el registro ubicado en:

Esta propiedad se hereda de [**\_ BaseService de Win32.**](win32-baseservice.md)

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ GroupOrderList**.

Las etiquetas solo se evalúan para los servicios de tipo de inicio del controlador de kernel y del controlador del sistema de archivos que tienen modos de inicio de arranque o del sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SystemDriver de Win32** se deriva de [**\_ BaseService de Win32.**](win32-baseservice.md)

## <a name="examples"></a>Ejemplos

El [ejemplo de VBScript Enumerar](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) controladores del sistema muestra los controladores del sistema instalados en un archivo HTML.

En el siguiente ejemplo de PowerShell se recuperan varias propiedades de los controladores del sistema en ejecución en un equipo.


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
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

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
