---
Description: El proceso de Win32 \_&\# 32; La clase WMI representa un proceso en un sistema operativo.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Clase Win32_Process
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660479"
---
# <a name="win32_process-class"></a>\_Clase de proceso Win32

La [clase WMI](../wmisdk/retrieving-a-class.md) de **\_ proceso de Win32** representa un proceso en un sistema operativo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

> [!NOTE]
> Para obtener una explicación general sobre los procesos y subprocesos de Windows, vea el tema [procesos y subprocesos](/ProcThread/processes-and-threads.md).

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a>Miembros

La clase de **\_ proceso de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ proceso de Win32** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachDebugger**](attachdebugger-method-in-class-win32-process.md)   | Inicia el depurador registrado actualmente para un proceso.<br/>                                                                                                                                                                                                                      |
| [**A**](create-method-in-class-win32-process.md)                   | Crea un nuevo proceso.<br/>                                                                                                                                                                                                                                                         |
| [**GetAvailableVirtualSize**](getavailablevirtualsize-win32-process.md) | Recupera el tamaño actual, en bytes, del espacio de direcciones virtuales libre disponible para el proceso.<br/> **Windows server 2012, Windows 8, Windows 7, Windows server 2008 y Windows Vista:** Este método no se admite antes de Windows 8.1 y Windows Server 2012 R2.<br/> |
| [**GetOwner**](getowner-method-in-class-win32-process.md)               | Recupera el nombre de usuario y el nombre de dominio en el que se está ejecutando el proceso.<br/>                                                                                                                                                                                                    |
| [**GetOwnerSid**](getownersid-method-in-class-win32-process.md)         | Recupera el identificador de seguridad (SID) del propietario de un proceso.<br/>                                                                                                                                                                                                            |
| [**SetPriority**](setpriority-method-in-class-win32-process.md)         | Cambia la prioridad de ejecución de un proceso.<br/>                                                                                                                                                                                                                                   |
| [**Terminate**](terminate-method-in-class-win32-process.md)             | Finaliza un proceso y todos sus subprocesos.<br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propiedades

La clase de **\_ proceso de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción de un objeto: una cadena de una línea.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**CommandLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("línea de comandos para iniciar proceso")
</dt> </dl>

Línea de comandos que se usa para iniciar un proceso específico, si procede.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) ("nombre de clase")
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de una instancia de. Cuando se usa con otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de la clase y sus subclases se identifiquen de forma única.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**displayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")
</dt> </dl>

Fecha en que comienza la ejecución del proceso.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) (" Computer System Class name ")
</dt> </dl>

Nombre de la clase de creación del sistema de ámbito del equipo.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) (" Computer System Name ")
</dt> </dl>

Nombre del sistema de ámbito del equipo.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")
</dt> </dl>

Descripción de un objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**ExecutablePath _s**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tool Help Structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| SzExePath"), [**displayName**](../wmisdk/standard-qualifiers.md) ("ruta de acceso del archivo ejecutable")
</dt> </dl>

Ruta de acceso al archivo ejecutable del proceso.

Ejemplo: "C: \\ Windows \\ System \\Explorer.Exe"

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("estado de ejecución")
</dt> </dl>

Condición de funcionamiento actual del proceso.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Unknown

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

Otros

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Listo** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqueado** (4)


</dt> <dd>

Bloqueado

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Suspendido bloqueado** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspendido preparado** (6)


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminada** (7)


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (8)


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>En **aumento** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) ("Handle")
</dt> </dl>

Identificador del proceso.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| HandleCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de identificadores")
</dt> </dl>

Número total de identificadores abiertos propiedad del proceso. **HandleCount** es la suma de los identificadores abiertos actualmente por cada subproceso de este proceso. Un identificador se utiliza para examinar o modificar los recursos del sistema. Cada controlador tiene una entrada en una tabla que se mantiene internamente. Las entradas contienen las direcciones de los recursos y los datos para identificar el tipo de recurso.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")
</dt> </dl>

Fecha en que se instala un objeto. El objeto se puede instalar sin que se escriba un valor en esta propiedad.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**unidades**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")
</dt> </dl>

Tiempo en modo kernel, en milisegundos. Si esta información no está disponible, utilice un valor de 0 (cero).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**MaximumWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| \_ límites \| de cuota MaximumWorkingSetSize "), [**displayName**](../wmisdk/standard-qualifiers.md) (" tamaño máximo del espacio de trabajo "), [**unidades**](../wmisdk/standard-qualifiers.md) (" kilobytes ")
</dt> </dl>

Tamaño máximo del espacio de trabajo del proceso. El espacio de trabajo de un proceso es el conjunto de páginas de memoria visibles para el proceso en la RAM física. Estas páginas son residentes y están disponibles para que una aplicación las use sin desencadenar un error de página.

Ejemplo: 1413120

</dd> <dt>

**MinimumWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| \_ límites \| de cuota MinimumWorkingSetSize "), [**displayName**](../wmisdk/standard-qualifiers.md) (" tamaño mínimo del espacio de trabajo "), [**unidades**](../wmisdk/standard-qualifiers.md) (" kilobytes ")
</dt> </dl>

Tamaño mínimo del espacio de trabajo del proceso. El espacio de trabajo de un proceso es el conjunto de páginas de memoria visibles para el proceso en la RAM física. Estas páginas son residentes y están disponibles para que una aplicación las use sin desencadenar un error de página.

Ejemplo: 20480

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Nombre del archivo ejecutable responsable del proceso, equivalente a la propiedad nombre de imagen del administrador de tareas.

Cuando se hereda mediante una subclase, la propiedad se puede invalidar para ser una propiedad de clave. El nombre se codifica de forma rígida en la propia aplicación y no se ve afectado por el cambio del nombre de archivo. Por ejemplo, incluso si cambia el nombre de Calc.exe, el nombre Calc.exe seguirá apareciendo en el administrador de tareas y en cualquier script de WMI que recupere el nombre del proceso.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre de clase del sistema operativo ")
</dt> </dl>

Nombre de la clase de creación del sistema operativo de ámbito.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Nombre**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**displayName**](../wmisdk/standard-qualifiers.md) (" nombre del sistema operativo ")
</dt> </dl>

Nombre del sistema operativo de ámbito.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**OtherOperationCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| información de proceso del sistema \_ \_ \| OtherOperationCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("otro recuento de operaciones")
</dt> </dl>

Número de operaciones de e/s realizadas que no son operaciones de lectura o escritura.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**OtherTransferCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| información de proceso del sistema \_ \_ \| OtherTransferCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("otro recuento de transferencias"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad de datos transferidos durante las operaciones que no son operaciones de lectura o escritura.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PageFaults**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| \_ información de proceso del sistema de estado de proceso inesperados win32api \_ \| PageFaultCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de errores de página")
</dt> </dl>

Número de errores de página que genera un proceso.

Ejemplo: 10

</dd> <dt>

**PageFileUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| PagefileUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("uso del archivo de paginación"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Cantidad de espacio del archivo de paginación que un proceso está usando actualmente. Este valor es coherente con el valor de **VMSize** en TaskMgr.exe.

Ejemplo: 102435

</dd> <dt>

**ParentProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status Process \| System \_ \_ Information \| InheritedFromUniqueProcessId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Parent Process ID")
</dt> </dl>

Identificador único del proceso que crea un proceso. Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso. Es posible que el proceso identificado por **ParentProcessId** termine, de modo que **ParentProcessId** no puede hacer referencia a un proceso en ejecución. También es posible que **ParentProcessId** haga referencia incorrectamente a un proceso que reutiliza un identificador de proceso. Puede usar la propiedad **CreationDate** para determinar si se ha creado el elemento primario especificado después de que se haya creado el proceso representado por esta instancia de **\_ proceso de Win32** .

</dd> <dt>

**PeakPageFileUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| \_ Process System \_ Information Information \| PeakPagefileUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("uso máximo de archivo de paginación"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Cantidad máxima de espacio de archivo de paginación utilizada durante la vida de un proceso.

Ejemplo: 102367

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| \_ Process System \_ Information Information \| PeakVirtualSize"), [**displayName**](../wmisdk/standard-qualifiers.md) ("pico de uso de espacio de direcciones de virtual"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Espacio de direcciones virtuales máximo que utiliza un proceso en un momento dado. El uso del espacio de direcciones virtuales no implica necesariamente el uso correspondiente del disco o las páginas de memoria principal. Sin embargo, el espacio virtual es finito y, si se usa demasiado, es posible que el proceso no pueda cargar bibliotecas.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| \_ Process System \_ Information Information \| PeakWorkingSetSize"), [**displayName**](../wmisdk/standard-qualifiers.md) ("tamaño máximo del espacio de trabajo"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Tamaño máximo del espacio de trabajo de un proceso.

Ejemplo: 1413120

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| Process System \_ \_ Information \| BasePriority"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Priority")
</dt> </dl>

La prioridad de programación de un proceso dentro de un sistema operativo. Cuanto mayor sea el valor, más prioridad recibirá un proceso. Los valores de prioridad pueden oscilar entre 0 (cero), que es la prioridad más baja a 31, que es la prioridad más alta.

Ejemplo: 7

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| información de proceso del sistema de estado de proceso inesperados win32api \| \_ \_ \| PrivatePageCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de páginas privadas")
</dt> </dl>

Número actual de páginas asignadas que solo son accesibles para el proceso representado por esta instancia de **\_ proceso de Win32** .

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**Process \_ Information**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| DwProcessId"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Process ID")
</dt> </dl>

Identificador numérico que se usa para distinguir un proceso de otro. Los ProcessIDs son válidos desde el momento de creación del proceso para la terminación del proceso. Tras la finalización, se puede aplicar el mismo identificador numérico a un nuevo proceso.

Esto significa que no puede usar ProcessID solo para supervisar un proceso determinado. Por ejemplo, una aplicación podría tener un ProcessID de 7 y, a continuación, producir un error. Cuando se inicia un nuevo proceso, se puede asignar el ID. de proceso 7 al nuevo proceso. Por lo tanto, un script que solo comprobó un ProcessID especificado podría "engañarse" para pensar que la aplicación original todavía se estaba ejecutando.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| QuotaNonPagedPoolUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cuota de uso de bloque no paginado")
</dt> </dl>

Cuota de uso de bloque no paginado para un proceso.

Ejemplo: 15

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| QuotaPagedPoolUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cuota de uso del grupo paginado")
</dt> </dl>

Cuota de uso del grupo paginado para un proceso.

Ejemplo: 22

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| QuotaPeakNonPagedPoolUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cuota máxima de uso de bloque no paginado")
</dt> </dl>

Cantidad máxima de cuota de uso de bloque no paginado para un proceso.

Ejemplo: 31

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| QuotaPeakPagedPoolUsage"), [**displayName**](../wmisdk/standard-qualifiers.md) ("cuota máxima de uso del grupo paginado")
</dt> </dl>

Cantidad máxima de cuota de uso del grupo paginado para un proceso.

Ejemplo: 31

</dd> <dt>

**ReadOperationCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| de proceso y estructuras de subprocesos \| información de proceso del sistema \_ \_ \| ReadOperationCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de operaciones de lectura")
</dt> </dl>

Número de operaciones de lectura realizadas.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ReadTransferCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| información de proceso del sistema \_ \_ \| ReadTransferCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de transferencias de lectura"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad de datos leídos.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| System \_ Process \_ Information \| SessionID"), [**displayName**](../wmisdk/standard-qualifiers.md) ("ID. de sesión")
</dt> </dl>

Identificador único que genera un sistema operativo cuando se crea una sesión. Una sesión abarca un período de tiempo desde el inicio de sesión hasta el cierre de sesión desde un sistema específico.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Esta propiedad no está implementada y no se rellena para ninguna instancia de esta clase. Siempre es **null**.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

Los valores son los siguientes:

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

**TerminationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("fecha de finalización")
</dt> </dl>

El proceso se detuvo o finalizó. Para obtener el tiempo de finalización, se debe mantener abierto un identificador del proceso. De lo contrario, esta propiedad devuelve **null**.

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**ThreadCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process status \| \_ Process System \_ Information \| NumberOfThreads"), [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de subprocesos")
</dt> </dl>

Número de subprocesos activos en un proceso. Una instrucción es la unidad básica de ejecución en un procesador y un subproceso es el objeto que ejecuta una instrucción. Cada proceso en ejecución tiene al menos un subproceso.

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**unidades**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")
</dt> </dl>

Tiempo en modo de usuario, en unidades de 100 nanosegundos. Si esta información no está disponible, utilice un valor de 0 (cero).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \| información de proceso del sistema de estado de proceso inesperados win32api \_ \_ \| VirtualSize"), [**displayName**](../wmisdk/standard-qualifiers.md) ("uso del espacio de direcciones virtuales"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño actual del espacio de direcciones virtuales que usa un proceso, no de la memoria física o virtual usada realmente por el proceso. El uso del espacio de direcciones virtuales no implica necesariamente el uso correspondiente del disco o las páginas de memoria principal. El espacio virtual es finito y, si se usa demasiado, es posible que el proceso no pueda cargar bibliotecas. Este valor es coherente con lo que se ve en Perfmon.exe.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WindowsVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Functions \| GetProcessVersion"), [**displayName**](../wmisdk/standard-qualifiers.md) ("Windows version")
</dt> </dl>

Versión de Windows en la que se está ejecutando el proceso.

Ejemplo: 4,0

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("tamaño del espacio de trabajo"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad de memoria en bytes que un proceso necesita ejecutar de forma eficaz — para un sistema operativo que usa la administración de memoria basada en páginas. Si el sistema no tiene suficiente memoria (menos que el tamaño del espacio de trabajo), se produce la paginación excesiva. Si no se conoce el tamaño del espacio de trabajo, utilice **null** o 0 (cero). Si se proporcionan datos del espacio de trabajo, puede supervisar la información para comprender los requisitos de memoria variables de un proceso.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

Esta propiedad se hereda del [**\_ proceso CIM**](cim-process.md).

</dd> <dt>

**WriteOperationCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| de proceso y estructuras de subprocesos \| información de proceso del sistema \_ \_ \| WriteOperationCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("número de operaciones de escritura")
</dt> </dl>

Número de operaciones de escritura realizadas.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WriteTransferCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| información de proceso del sistema \_ \_ \| WriteTransferCount"), [**displayName**](../wmisdk/standard-qualifiers.md) ("recuento de transferencias de escritura"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad de datos escritos.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ proceso de Win32** se deriva del [**\_ proceso CIM**](cim-process.md). El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro. Para obtener más información, vea [ejecutar operaciones con privilegios](../wmisdk/executing-privileged-operations.md).

### <a name="overview"></a>Información general

Los procesos subyacen casi todo lo que ocurre en un equipo. De hecho, se puede realizar un seguimiento de la causa principal de la mayoría de los problemas del equipo con los procesos; por ejemplo, se podrían estar ejecutando demasiados procesos en un equipo (y se está consiguiendo un conjunto finito de recursos), o bien un único proceso podría estar usando más de su recurso compartido de recursos. Estos factores hacen que sea importante mantener una observación cercana en los procesos que se ejecutan en un equipo. La supervisión de procesos, la actividad principal en la administración de procesos, permite determinar lo que realmente hace un equipo, qué aplicaciones ejecuta el equipo y cómo se ven afectadas por los cambios en el entorno informático.

### <a name="monitoring-a-process"></a>Supervisión de un proceso

La supervisión de procesos de forma periódica le ayuda a garantizar que un equipo se ejecute con una eficacia máxima y que lleve a cabo sus tareas designadas según lo previsto. Por ejemplo, mediante la supervisión de procesos se puede recibir una notificación inmediata de cualquier aplicación que haya dejado de responder y, a continuación, realizar los pasos necesarios para finalizar el proceso. Además, la supervisión de procesos permite identificar problemas antes de que se produzcan. Por ejemplo, al comprobar repetidamente la cantidad de memoria usada por un proceso, puede identificar una fuga de memoria. Después, puede detener el proceso antes de que la aplicación errante utilice toda la memoria disponible y el equipo se detenga.

La supervisión de procesos también ayuda a minimizar las interrupciones causadas por las interrupciones planeadas para las actualizaciones y el mantenimiento. Por ejemplo, al comprobar el estado de una aplicación de base de datos que se ejecuta en los equipos cliente, puede determinar el impacto de dejar la base de datos sin conexión para actualizar el software.

Supervisión de la disponibilidad del proceso. Mide el porcentaje de tiempo que un proceso está disponible. La disponibilidad normalmente se supervisa mediante el uso de un sondeo simple, que indica si el proceso sigue en ejecución. Al realizar un seguimiento de los resultados de cada sondeo, puede calcular la disponibilidad del proceso. Por ejemplo, un proceso que se sondea 100 veces y responde en 95 de esas ocasiones tiene una disponibilidad del 95 por ciento. Este tipo de supervisión normalmente se reserva para las bases de datos, programas de correo y otras aplicaciones que se espera que se ejecuten en todo momento. No es adecuado para programas de procesamiento de texto, hojas de cálculo u otras aplicaciones que se inician de forma rutinaria y se detienen varias veces al día.

Puede crear una instancia de la clase [**Win32 \_ ProcessStartup**](win32-processstartup.md) para configurar el proceso.

Puede supervisar el rendimiento de los procesos con la clase de [**proceso de Win32 \_ PerfFormattedData \_ PerfProc \_**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) y un objeto de actualizador de WMI, como [**SWbemRefresher**](../wmisdk/swbemrefresher.md). Para obtener más información, vea [supervisar datos de rendimiento](../wmisdk/monitoring-performance-data.md).

## <a name="examples"></a>Ejemplos

En el ejemplo [de código de PowerShell de las propiedades de las clases WMI](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) de la galería de TechNet se describe la clase de **\_ proceso de Win32** y se muestran los resultados en formato de Excel.

El [proceso de finalización en ejecución en varios servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) finaliza un proceso que se ejecuta en uno o varios equipos.

En el tema [ejemplo: llamar a un método de proveedor](../wmisdk/example--calling-a-provider-method.md) , el código usa C++ para llamar al **\_ proceso de Win32** para crear un proceso.

La disponibilidad es la forma más sencilla de supervisión de procesos: con este enfoque, solo tiene que asegurarse de que el proceso se está ejecutando. Al supervisar la disponibilidad de los procesos, normalmente se recupera una lista de procesos que se ejecutan en un equipo y, a continuación, se comprueba que un proceso determinado todavía está activo. Si el proceso está activo, se considera que está disponible. Si el proceso no está activo, no está disponible. El siguiente ejemplo de VBScript supervisa la disponibilidad del proceso mediante la comprobación de la lista de procesos que se ejecutan en un equipo y la emisión de una notificación si no se encuentra el proceso de Database.exe.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



El siguiente ejemplo de VBScript supervisa la creación de procesos mediante un consumidor de eventos temporal.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



El siguiente VBScript supervisa la información de rendimiento del proceso.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



En el ejemplo de código de VBScript siguiente se muestra cómo obtener el propietario de cada proceso en un equipo local. Puede usar este script para obtener datos de un equipo remoto, por ejemplo, para determinar qué usuarios tienen procesos que ejecutan Terminal Server, sustituya el nombre del equipo remoto por "." en la primera línea. También debe ser administrador en el equipo remoto.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



En el ejemplo de código de VBScript siguiente se muestra cómo obtener la sesión de inicio de sesión asociada a un proceso en ejecución. Un proceso debe estar en ejecución Notepad.exe antes de que se inicie el script. En el ejemplo se buscan las instancias de [**Win32 \_ LogonSession**](win32-logonsession.md) asociadas al **\_ proceso de Win32** que representa Notepad.exe. [**Win32 \_ SessionProcess**](win32-sessionprocess.md) se especifica como la clase Association. Para obtener más información, vea [ASSOCIATORS OF Statement.](../wmisdk/associators-of-statement.md)


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
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

[**\_Proceso CIM**](cim-process.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Tareas de WMI: procesos](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
