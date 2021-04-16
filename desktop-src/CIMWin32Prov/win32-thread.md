---
description: El \_ subproceso de Win32&\# 8194; La clase WMI representa un subproceso de ejecución.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Win32_Thread (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6e9f6a8c821aa327e8b810b634c85bb06459910f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652347"
---
# <a name="win32_thread-class"></a>\_Clase de subproceso Win32

La  [clase WMI](../wmisdk/retrieving-a-class.md) de **\_ subproceso Win32** representa un subproceso de ejecución. Mientras que un proceso debe tener un subproceso de ejecución, el proceso puede crear otros subprocesos para ejecutar tareas en paralelo. Los subprocesos comparten el entorno de proceso, por lo que varios subprocesos del mismo proceso usan menos memoria que el mismo número de procesos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a>Miembros

La clase de **\_ subproceso de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ subproceso de Win32** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descripción del objeto.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia. Cuando se usa con las otras propiedades de clave de la clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.

Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**CSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de la clase de creación del sistema de ámbito del equipo.

Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**CSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre del sistema de ámbito del equipo.

Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).

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

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| performance Data Structures \| [**Perf \_ Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("Milliseconds")
</dt> </dl>

Tiempo de ejecución total, en milisegundos, dado a este subproceso desde su creación.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Condición de funcionamiento actual del subproceso.

Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

**Listo** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

En **ejecución** (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

**Bloqueado** (4)


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

**Suspendido bloqueado** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

**Suspendido preparado** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")
</dt> </dl>

Identificador de un subproceso. De forma predeterminada, el identificador tiene derechos de acceso completo. Con el acceso de seguridad correcto, el identificador se puede utilizar en cualquier función que acepte un identificador de subproceso. Dependiendo de la marca de herencia especificada al crearse, este identificador puede ser heredado por procesos secundarios.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")
</dt> </dl>

Objeto instalado. Esta propiedad no necesita un valor para indicar que el objeto está instalado.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| performance Data Structures \| [**Perf \_ Object \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PrivilegedTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")
</dt> </dl>

Tiempo en modo kernel, en unidades de 100 nanosegundos. Si esta información no está disponible, se debe usar un valor de 0 (cero).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**OSCreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre de la clase de creación del sistema operativo de ámbito.

Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**OSName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nombre del sistema operativo de ámbito.

Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri")
</dt> </dl>

Prioridad dinámica del subproceso. Cada subproceso tiene una prioridad dinámica que el programador usa para determinar qué subproceso se debe ejecutar. Inicialmente, la prioridad dinámica de un subproceso es igual que su prioridad base. El sistema puede aumentar y disminuir la prioridad dinámica para garantizar que responde (lo que garantiza que ningún subproceso se queda sin tiempo de procesador). El sistema no aumenta la prioridad de los subprocesos con un nivel de prioridad base entre 16 y 31. Solo los subprocesos con una prioridad base entre 0 y 15 reciben aumentos de prioridad dinámica. Los números más altos indican prioridades más altas.

</dd> <dt>

**PriorityBase**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| performance Data Structures \| [**Perf \_ Object \_ Type**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| PerfPriorityBase")
</dt> </dl>

Prioridad base actual de un subproceso. El sistema operativo puede aumentar la prioridad dinámica del subproceso por encima de la prioridad base si el subproceso está controlando los datos proporcionados por el usuario o reducirlo hacia la prioridad base si el subproceso se convierte en un enlace de proceso. La propiedad **PriorityBase** puede tener un valor entre 0 y 31.

</dd> <dt>

**ProcessCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ proceso de CIM**](cim-process.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Valor de la propiedad de proceso de ámbito de **CreationClassName** .

Esta propiedad se hereda del [**\_ subproceso CIM**](cim-thread.md).

</dd> <dt>

**ProcessHandle**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**invalidar**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**propagado**](../wmisdk/standard-qualifiers.md) ("[**\_ proceso de CIM**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" inesperados win32api \| Tool Help Structures \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ")
</dt> </dl>

Proceso que creó el subproceso. Los elementos de la interfaz de programación de aplicaciones (API) de Windows pueden usar el contenido de esta propiedad.

</dd> <dt>

**StartAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| objeto inesperados win32api Thread \| LPTHREAD \_ Start \_ rutina \| lpStartAddress")
</dt> </dl>

Dirección inicial del subproceso. Dado que cualquier aplicación con el acceso adecuado al subproceso puede cambiar el contexto del subproceso, este valor solo puede ser una aproximación de la dirección de inicio del subproceso.

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

**ThreadState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Thread State")
</dt> </dl>

Estado de ejecución actual del subproceso.

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Inicializado** (0)


</dt> <dd>

Initialized: el microkernel lo reconoce.

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Listo** (1)


</dt> <dd>

Listo: está preparado para ejecutarse en el siguiente procesador disponible.

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>En **ejecución** (2)


</dt> <dd>

En ejecución: se está ejecutando.

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>En **espera** (3)


</dt> <dd>

Standby: está a punto de ejecutarse, solo un subproceso puede estar en este estado a la vez.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Terminada** (4)


</dt> <dd>

Terminada: ha terminado de ejecutarse.

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>En **espera** (5)


</dt> <dd>

Esperando: no está listo para el procesador, cuando esté listo, se volverá a programar.

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transición** (6)


</dt> <dd>

Transición: el subproceso está esperando recursos distintos del procesador,

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (7)


</dt> <dd>

Desconocido: se desconoce el estado del subproceso.

</dd> </dl>

</dd> <dt>

**ThreadWaitReason**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| razón de espera del subproceso de inesperados win32api")
</dt> </dl>

Motivo por el que el subproceso está esperando. Este valor solo es válido si el miembro **ThreadState** está establecido en Transition (6). Los pares de eventos permiten la comunicación con subsistemas protegidos.

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Ejecutivo** (0)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)


</dt> <dd>

FreePage

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Buscapersonas** (2)


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Buscapersonas** (6)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Ejecutivo** (7)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Buscapersonas** (9)


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Buscapersonas** (13)


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**Pageout.** (19)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (20)


</dt> <dd></dd> </dl>

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| performance Data Structures \| [**Perf \_ Object \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| UserTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanosegundos")
</dt> </dl>

Tiempo en modo de usuario, en unidades de 100 nanosegundos. Si esta información no está disponible, se debe usar un valor de 0 (cero).

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ subproceso de Win32** se deriva del [**\_ subproceso CIM**](cim-thread.md).

**Información general**

En el caso de la supervisión diaria rutinaria, normalmente hay poca razón para tener una lista detallada de subprocesos y sus propiedades asociadas. Los equipos crean y eliminan miles de subprocesos durante el transcurso del día y algunas de estas creaciones o eliminaciones son significativas para cualquier persona, pero el desarrollador que escribió el software.

Sin embargo, cuando se están solucionando problemas con una aplicación, el seguimiento de los subprocesos individuales de un proceso permite identificar cuándo se crean los subprocesos y cuándo (o si) se destruyen. Dado que los subprocesos que se crean pero no se destruyen producen fugas de memoria, el seguimiento de subprocesos individuales puede ser información útil para los técnicos de soporte. Del mismo modo, identificar las prioridades de subprocesos puede ayudar a identificar los subprocesos que, al ejecutarse con una prioridad anómalamente alta, son los ciclos de CPU que necesitan otros subprocesos y otros procesos.

**Usar el \_ subproceso Win32**

Como se ha implícito en el bloque de sintaxis anterior, la clase de **\_ subproceso de Win32** no informa del nombre del proceso en el que se ejecuta cada subproceso. En su lugar, notifica el identificador del proceso en el que se ejecuta el subproceso. Para devolver el nombre de un proceso y una lista de todos los subprocesos, el script debe:

1.  Conéctese a la clase de [**\_ proceso de Win32**](win32-process.md) y devuelva la lista de procesos y sus identificadores de proceso.
2.  Almacene temporalmente esta información en un objeto de matriz o de diccionario.
3.  Para cada ID. de proceso, devuelve la lista de subprocesos para ese proceso y, a continuación, muestra el nombre del proceso y la lista de subprocesos.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de VBScript se supervisan los subprocesos que se ejecutan en un equipo.


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
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

[**Subproceso CIM \_**](cim-thread.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
