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
ms.openlocfilehash: e52ae224aee9db09ffa42cf19b3550a5ff6362326b0058d87e4d2a8b2da1851e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759415"
---
# <a name="win32_process-class"></a>Win32 \_ Process (clase)

La **clase WMI De \_ proceso win32** representa un proceso en un sistema operativo. [](../wmisdk/retrieving-a-class.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

> [!NOTE]
> Para obtener una explicación general sobre los procesos y subprocesos Windows, vea el tema [Procesos y subprocesos](/ProcThread/processes-and-threads.md).

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

La **clase Win32 \_ Process** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase Win32 \_ Process** tiene estos métodos.



| Método                                                                   | Descripción                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachDebugger**](attachdebugger-method-in-class-win32-process.md)   | Inicia el depurador registrado actualmente para un proceso.<br/>                                                                                                                                                                                                                      |
| [**Crear**](create-method-in-class-win32-process.md)                   | Crea un nuevo proceso.<br/>                                                                                                                                                                                                                                                         |
| [**GetAvailableVirtualSize**](getavailablevirtualsize-win32-process.md) | Recupera el tamaño actual, en bytes, del espacio de direcciones virtuales disponible para el proceso.<br/> **Windows Server 2012, Windows 8, Windows 7, Windows Server 2008 y Windows Vista:** Este método no se admite antes de Windows 8.1 y Windows Server 2012 R2.<br/> |
| [**GetOwner**](getowner-method-in-class-win32-process.md)               | Recupera el nombre de usuario y el nombre de dominio con los que se ejecuta el proceso.<br/>                                                                                                                                                                                                    |
| [**GetOwnerSid**](getownersid-method-in-class-win32-process.md)         | Recupera el identificador de seguridad (SID) del propietario de un proceso.<br/>                                                                                                                                                                                                            |
| [**SetPriority**](setpriority-method-in-class-win32-process.md)         | Cambia la prioridad de ejecución de un proceso.<br/>                                                                                                                                                                                                                                   |
| [**Terminate**](terminate-method-in-class-win32-process.md)             | Finaliza un proceso y todos sus subprocesos.<br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propiedades

La **clase Win32 \_ Process** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Descripción breve de un objeto: una cadena de una línea.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CommandLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Línea de comandos para iniciar el proceso")
</dt> </dl>

Línea de comandos que se usa para iniciar un proceso específico, si procede.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ Clave CIM,**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre de clase")
</dt> </dl>

Nombre de la clase o subclase usada en la creación de una instancia de . Cuando se usa con otras propiedades clave de la clase , esta propiedad permite identificar de forma única todas las instancias de la clase y sus subclases.

Esta propiedad se hereda del proceso [**\_ CIM**](cim-process.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")
</dt> </dl>

Fecha en que comienza a ejecutarse el proceso.

Esta propiedad se hereda del proceso [**\_ CIM**](cim-process.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSCreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Computer System Class Name")
</dt> </dl>

Nombre de clase de creación del sistema de equipo de ámbito.

Esta propiedad se hereda del proceso [**\_ CIM**](cim-process.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CSName**"), [**Clave CIM, \_**](../wmisdk/standard-wmi-qualifiers.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre del sistema del equipo")
</dt> </dl>

Nombre del sistema de equipo de ámbito.

Esta propiedad se hereda del proceso [**\_ CIM**](cim-process.md).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descripción de un objeto .

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ExecutablePath _s**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Tool Help Structures \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Ruta de acceso ejecutable")
</dt> </dl>

Ruta de acceso al archivo ejecutable del proceso.

Ejemplo: "C: \\ Windows \\ System \\Explorer.Exe"

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estado de ejecución")
</dt> </dl>

Condición de funcionamiento actual del proceso.

Esta propiedad se hereda del proceso [**\_ CIM**](cim-process.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Unknown

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Listo** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**En** ejecución (3)


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

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Suspendido listo** (6)


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Finalizado** (7)


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (8)


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Crecimiento** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")
</dt> </dl>

Identificador del proceso.

Esta propiedad se hereda del proceso [**\_ CIM.**](cim-process.md)

</dd> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle Count")
</dt> </dl>

Número total de identificadores abiertos propiedad del proceso. **HandleCount** es la suma de los identificadores abiertos actualmente por cada subproceso de este proceso. Se usa un identificador para examinar o modificar los recursos del sistema. Cada identificador tiene una entrada en una tabla que se mantiene internamente. Las entradas contienen las direcciones de los recursos y los datos para identificar el tipo de recurso.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de instalación")
</dt> </dl>

Fecha en que se instala un objeto. El objeto se puede instalar sin escribir un valor en esta propiedad.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")
</dt> </dl>

Tiempo en modo kernel, en milisegundos. Si esta información no está disponible, use un valor de 0 (cero).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> <dt>

**MaximumWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| WINNT. H \| QUOTA \_ LIMITS \| MaximumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tamaño máximo del espacio de trabajo"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Tamaño máximo del conjunto de trabajo del proceso. El espacio de trabajo de un proceso es el conjunto de páginas de memoria visibles para el proceso en la RAM física. Estas páginas son residentes y están disponibles para que una aplicación las use sin desencadenar un error de página.

Ejemplo: 1413120

</dd> <dt>

**MinimumWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| WINNT. H \| QUOTA \_ LIMITS \| MinimumWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tamaño mínimo del espacio de trabajo"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
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

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre")
</dt> </dl>

Nombre del archivo ejecutable responsable del proceso, equivalente a la propiedad Image Name de Administrador de tareas.

Cuando se hereda mediante una subclase, la propiedad se puede invalidar para que sea una propiedad de clave. El nombre está codificado de forma hard-code en la propia aplicación y no se ve afectado por el cambio del nombre de archivo. Por ejemplo, incluso si cambia el nombre Calc.exe, el nombre Calc.exe seguirá apareciendo en Administrador de tareas y en cualquier script WMI que recupere el nombre del proceso.

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**CreationClassName**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nombre de clase de sistema operativo")
</dt> </dl>

Nombre de clase de creación del sistema operativo de ámbito.

Esta propiedad se hereda del proceso [**\_ CIM.**](cim-process.md)

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Operating System Name")
</dt> </dl>

Nombre del sistema operativo de ámbito.

Esta propiedad se hereda del proceso [**\_ CIM.**](cim-process.md)

</dd> <dt>

**OtherOperationCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures SYSTEM PROCESS INFORMATION \| \_ \_ \| OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Operation Count")
</dt> </dl>

Número de operaciones de E/S realizadas que no son operaciones de lectura o escritura.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> <dt>

**OtherTransferCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures SYSTEM PROCESS INFORMATION \| \_ \_ \| OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Other Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad de datos transferidos durante las operaciones que no son operaciones de lectura o escritura.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](../wmisdk/creating-a-wmi-script.md)

</dd> <dt>

**PageFaults**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Number Of Page Faults")
</dt> </dl>

Número de errores de página que genera un proceso.

Ejemplo: 10

</dd> <dt>

**PageFileUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Cantidad de espacio de archivo de página que un proceso usa actualmente. Este valor es coherente con el **valor VMSize** de TaskMgr.exe.

Ejemplo: 102435

</dd> <dt>

**ParentProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Parent Process Id")
</dt> </dl>

Identificador único del proceso que crea un proceso. Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso. Es posible que el proceso identificado por **ParentProcessId** finalice, por lo que **ParentProcessId** puede no hacer referencia a un proceso en ejecución. También es posible que **ParentProcessId hace referencia** incorrectamente a un proceso que reutiliza un identificador de proceso. Puede usar la propiedad **CreationDate** para determinar si el elemento primario especificado se creó después de que se creara el proceso representado por esta instancia del proceso **Win32. \_**

</dd> <dt>

**PeakPageFileUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Page File Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Cantidad máxima de espacio de archivo de página utilizado durante la vida de un proceso.

Ejemplo: 102367

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Virual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Espacio máximo de direcciones virtuales que un proceso usa en cualquier momento. El uso de espacio de direcciones virtuales no implica necesariamente el uso correspondiente de páginas de memoria principal o de disco. Sin embargo, el espacio virtual es finito y, al usar demasiado, es posible que el proceso no pueda cargar bibliotecas.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Working Set Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Tamaño máximo del conjunto de trabajo de un proceso.

Ejemplo: 1413120

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")
</dt> </dl>

Prioridad de programación de un proceso dentro de un sistema operativo. Cuanto mayor sea el valor, mayor será la prioridad que recibe un proceso. Los valores de prioridad pueden oscilar entre 0 (cero), que es la prioridad más baja a 31, que es la prioridad más alta.

Ejemplo: 7

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Private Page Count")
</dt> </dl>

Número actual de páginas asignadas que solo son accesibles para el proceso representado por esta **instancia de Win32 \_ Process.**

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures PROCESS \| [**\_ INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Id. de proceso")
</dt> </dl>

Identificador numérico utilizado para distinguir un proceso de otro. Los processID son válidos desde el momento de creación del proceso hasta la finalización del proceso. Tras la finalización, ese mismo identificador numérico se puede aplicar a un nuevo proceso.

Esto significa que no puede usar ProcessID solo para supervisar un proceso determinado. Por ejemplo, una aplicación podría tener un ProcessID de 7 y, a continuación, producir un error. Cuando se inicia un nuevo proceso, se podría asignar el ProcessID 7 al nuevo proceso. Por lo tanto, un script que solo ha comprobado un ProcessID especificado podría estar "desaprobado" al pensar que la aplicación original todavía se estaba ejecutando.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Non-Paged Pool Usage Quota")
</dt> </dl>

Cantidad de cuota de uso de grupo sin página para un proceso.

Ejemplo: 15

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Paged Pool Usage Quota")
</dt> </dl>

Cantidad de cuota de uso de grupo paginado para un proceso.

Ejemplo: 22

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Non-Paged Pool Usage Quota")
</dt> </dl>

Cantidad máxima de cuota de uso de grupo sin página para un proceso.

Ejemplo: 31

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Peak Paged Pool Usage Quota")
</dt> </dl>

Cantidad máxima de cuota de uso de grupo paginado para un proceso.

Ejemplo: 31

</dd> <dt>

**ReadOperationCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures SYSTEM PROCESS INFORMATION \| \_ \_ \| ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Operation Count")
</dt> </dl>

Número de operaciones de lectura realizadas.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ReadTransferCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures SYSTEM PROCESS INFORMATION \| \_ \_ \| ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Read Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad de datos leídos.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| SessionId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Id. de sesión")
</dt> </dl>

Identificador único que genera un sistema operativo cuando se crea una sesión. Una sesión abarca un período de tiempo desde el inicio de sesión hasta el cierre de sesión desde un sistema específico.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Esta propiedad no se implementa y no se rellena para ninguna instancia de esta clase. Siempre es **NULL.**

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Los valores son los siguientes:

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

**TerminationDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Fecha de finalización")
</dt> </dl>

El proceso se detuvo o finalizó. Para obtener el tiempo de finalización, se debe mantener abierto un identificador para el proceso. De lo contrario, esta propiedad devuelve **NULL.**

Esta propiedad se hereda del proceso [**\_ CIM**](cim-process.md).

</dd> <dt>

**ThreadCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Thread Count")
</dt> </dl>

Número de subprocesos activos en un proceso. Una instrucción es la unidad básica de ejecución en un procesador y un subproceso es el objeto que ejecuta una instrucción. Cada proceso en ejecución tiene al menos un subproceso.

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanoseconds")
</dt> </dl>

Tiempo en modo de usuario, en unidades de 100 nanosegundos. Si esta información no está disponible, use un valor de 0 (cero).

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process Status SYSTEM PROCESS INFORMATION \| \_ \_ \| VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Virtual Address Space Usage"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamaño actual del espacio de direcciones virtuales que usa un proceso, no la memoria física o virtual usada realmente por el proceso. El uso de espacio de direcciones virtuales no implica necesariamente el uso correspondiente de páginas de memoria principal o de disco. El espacio virtual es finito y, al usar demasiado, es posible que el proceso no pueda cargar bibliotecas. Este valor es coherente con lo que se ve en Perfmon.exe.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WindowsVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Functions \| GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Windows Version")
</dt> </dl>

Versión de Windows en la que se ejecuta el proceso.

Ejemplo: 4.0

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tamaño del espacio de trabajo"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad de memoria en bytes que un proceso debe ejecutar de forma eficaz, para un sistema operativo que usa la administración de memoria basada en páginas. Si el sistema no tiene suficiente memoria (menor que el tamaño del espacio de trabajo), se produce la thrashing. Si no se conoce el tamaño del conjunto de trabajo, use **NULL** o 0 (cero). Si se proporcionan datos de espacio de trabajo, puede supervisar la información para comprender los requisitos de memoria cambiantes de un proceso.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

Esta propiedad se hereda del proceso [**\_ CIM**](cim-process.md).

</dd> <dt>

**WriteOperationCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures SYSTEM PROCESS INFORMATION \| \_ \_ \| WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Operation Count")
</dt> </dl>

Número de operaciones de escritura realizadas.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WriteTransferCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures SYSTEM PROCESS INFORMATION \| \_ \_ \| WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Write Transfer Count"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Cantidad de datos escritos.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase Win32 \_ Process** se deriva del [**proceso CIM \_**](cim-process.md). El proceso de llamada que usa esta clase debe tener el **SE \_ restore \_ NAME** en el equipo en el que reside el Registro. Para obtener más información, [vea Ejecutar operaciones con privilegios.](../wmisdk/executing-privileged-operations.md)

### <a name="overview"></a>Información general

Los procesos subyacen a casi todo lo que sucede en un equipo. De hecho, la causa principal de la mayoría de los problemas del equipo se puede realizar en los procesos. Por ejemplo, es posible que se ejecuten demasiados procesos en un equipo (y que se contenda por un conjunto finito de recursos), o que un único proceso esté usando más de su parte de recursos. Estos factores hacen que sea importante mantener una estrecha atención sobre los procesos que se ejecutan en un equipo. La supervisión de procesos, la actividad principal en la administración de procesos, le permite determinar qué hace realmente un equipo, qué aplicaciones ejecuta el equipo y cómo se ven afectadas esas aplicaciones por los cambios en el entorno informático.

### <a name="monitoring-a-process"></a>Supervisión de un proceso

La supervisión de los procesos de forma periódica le ayuda a garantizar que un equipo se ejecuta con la máxima eficacia y que lleva a cabo sus tareas designadas según lo previsto. Por ejemplo, mediante la supervisión de procesos, se le puede notificar inmediatamente de cualquier aplicación que haya dejado de responder y, a continuación, realizar los pasos necesarios para finalizar ese proceso. Además, la supervisión de procesos permite identificar problemas antes de que se produzcan. Por ejemplo, al comprobar repetidamente la cantidad de memoria usada por un proceso, puede identificar una pérdida de memoria. A continuación, puede detener el proceso antes de que la aplicación errant use toda la memoria disponible y detenga el equipo.

La supervisión de procesos también ayuda a minimizar las interrupciones causadas por interrupciones planeadas para las actualizaciones y el mantenimiento. Por ejemplo, al comprobar el estado de una aplicación de base de datos que se ejecuta en equipos cliente, puede determinar el impacto de desconectar la base de datos para actualizar el software.

Supervisión de la disponibilidad del proceso. Mide el porcentaje de tiempo que un proceso está disponible. Normalmente, la disponibilidad se supervisa mediante un sondeo simple, que informa de si el proceso todavía se está ejecutando. Al realizar un seguimiento de los resultados de cada sondeo, puede calcular la disponibilidad del proceso. Por ejemplo, un proceso que se sondea 100 veces y responde en 95 de esas ocasiones tiene una disponibilidad del 95 %. Este tipo de supervisión se reserva normalmente para bases de datos, programas de correo y otras aplicaciones que se espera que se ejecuten en todo momento. No es adecuado para programas de procesamiento de texto, hojas de cálculo u otras aplicaciones que se inician y detienen de forma rutinaria varias veces al día.

Puede crear una instancia de la clase [**\_ ProcessStartup de Win32**](win32-processstartup.md) para configurar el proceso.

Puede supervisar el rendimiento de los procesos con la clase [**\_ PerfFormattedData \_ PerfProc \_ Process de Win32**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) y un objeto de actualizador WMI, [**como SWbemRefresher.**](../wmisdk/swbemrefresher.md) Para obtener más información, vea [Supervisión de datos de rendimiento.](../wmisdk/monitoring-performance-data.md)

## <a name="examples"></a>Ejemplos

El [ejemplo de](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) código de PowerShell Enumerar las propiedades de las clases WMI en la Galería de TechNet describe la clase Proceso **\_ win32** y genera los resultados en Excel formato.

El [proceso De finalizar en ejecución en varios servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) finaliza un proceso que se ejecuta en uno o varios equipos.

En el [tema Ejemplo: Llamar a un método de](../wmisdk/example--calling-a-provider-method.md) proveedor, el código usa C++ para llamar a Proceso **win32 \_** para crear un proceso.

La disponibilidad es la forma más sencilla de supervisión de procesos: con este enfoque, simplemente se asegura de que el proceso se está ejecutando. Al supervisar la disponibilidad del proceso, normalmente se recupera una lista de procesos que se ejecutan en un equipo y, a continuación, se comprueba que un proceso determinado sigue activo. Si el proceso está activo, se considera disponible. Si el proceso no está activo, no está disponible. En el ejemplo de VBScript siguiente se supervisa la disponibilidad de los procesos comprobando la lista de procesos que se ejecutan en un equipo y emitiendo una notificación si no se encuentra Database.exe proceso.


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



En el ejemplo de VBScript siguiente se supervisa la creación de procesos mediante un consumidor de eventos temporal.


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



En el siguiente ejemplo de código de VBScript se muestra cómo obtener el propietario de cada proceso en un equipo local. Puede usar este script para obtener datos de un equipo remoto, por ejemplo, para determinar qué usuarios tienen procesos que ejecutan terminal server y sustituya el nombre del equipo remoto por "." en la primera línea. También debe ser administrador en el equipo remoto.


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



En el siguiente ejemplo de código de VBScript se muestra cómo obtener la sesión de inicio de sesión asociada a un proceso en ejecución. Un proceso debe ejecutarse Notepad.exe antes de que se inicie el script. En el ejemplo se localizan las instancias de [**\_ LogonSession de Win32**](win32-logonsession.md) asociadas al proceso **de Win32 \_** que representa Notepad.exe. [**Win32 \_ SessionProcess**](win32-sessionprocess.md) se especifica como clase de asociación. Para obtener más información, [vea ASSOCIATORS OF (Instrucción).](../wmisdk/associators-of-statement.md)


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
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Proceso \_ CIM**](cim-process.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> <dt>

[Tareas wmi: procesos](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
