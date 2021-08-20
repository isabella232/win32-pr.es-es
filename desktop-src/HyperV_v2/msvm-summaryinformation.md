---
description: Se usa en los métodos GetSummaryInformation y GetDefinitionFileSummaryInformation de la clase Msvm VirtualSystemManagementService para recuperar rápidamente información común relacionada con una máquina virtual o \_ instantánea.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Msvm_SummaryInformation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4af759cf621f5afbaef90924351ad24a232889b1d81048f0e1372630c74f98f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950094"
---
# <a name="msvm_summaryinformation-class"></a>Clase Msvm \_ SummaryInformation

Se usa en los [**métodos GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) y [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para recuperar rápidamente información común relacionada con una máquina virtual o instantánea.

La sintaxis siguiente se simplifica Managed Object Format (MOF).

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a>Miembros

La **clase \_ SummaryInformation de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SummaryInformation de Msvm** tiene estas propiedades.

<dl> <dt>

**AllocatedGPU**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de la unidad de procesamiento de gráficos físicos (GPU) asignada a esta máquina virtual. Esta propiedad solo se aplica a las máquinas virtuales que usan RemoteFX.

</dd> <dt>

**ApplicationHealth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual de mantenimiento de la aplicación para la máquina virtual. Esta propiedad no es válida para las instancias de **\_ SummaryInformation de Msvm** que representan una instantánea de máquina virtual.

<dt>

<span id="OK"></span><span id="ok"></span>

**Aceptar** (2)


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

**Crítico para la** aplicación (32782)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (32896)


</dt> <dd></dd> </dl>

</dd> <dt>

**AsynchronousTasks**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ ConcreteJob array**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de [**instancias de \_ Msvm ConcreteJob**](msvm-concretejob.md) que representan cualquier operación asincrónica relacionada con la máquina virtual que se está ejecutando actualmente. Esta propiedad no es válida para las instancias de **\_ SummaryInformation de Msvm** que representan una instantánea de máquina virtual.

</dd> <dt>

**AvailableMemoryBuffer**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Porcentaje de búfer de memoria disponible para la máquina virtual. Cuando la memoria dinámica está habilitada para una máquina virtual, esta propiedad representa la proporción del búfer de memoria disponible con el búfer de memoria ideal para la máquina virtual. El tamaño de búfer de memoria ideal se configura mediante la **propiedad TargetMemoryBuffer** de la [**clase \_ MemorySettingData de Msvm.**](msvm-memorysettingdata.md)

Esta propiedad no es válida para las instancias de la clase **\_ SummaryInformation de Msvm** que representan máquinas virtuales para las que no está habilitada la memoria dinámica.

Esta propiedad no es válida para las instancias de la clase **\_ SummaryInformation de Msvm** que representan una instantánea de máquina virtual.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se creó la máquina virtual o la instantánea.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar de la máquina virtual o instantánea.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual de la máquina virtual o instantánea. Vea la **propiedad EnabledState** de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) para ver los valores posibles.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el host permite las conexiones en modo mejorado y, si se permiten, si están disponibles para la máquina virtual.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Permitido y disponible** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**No permitido** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Permitido pero no disponible** (6 )


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del sistema operativo invitado, si está disponible. Si esta información no está disponible, el valor de esta propiedad es **Null.** Esta propiedad no es válida para las instancias de **\_ SummaryInformation de Msvm** que representan una instantánea de máquina virtual.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado de mantenimiento actual de la máquina virtual. Esta propiedad no es válida para las instancias de **\_ SummaryInformation de Msvm** que representan una instantánea de máquina virtual.

</dd> <dt>

**Heartbeat**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del latido de la máquina virtual. Para obtener más información, vea la documentación de la [**propiedad StatusDescriptions**](msvm-heartbeatcomponent.md) de la **clase \_ HeartbeatComponent de Msvm.** Esta propiedad no es válida para las instancias de **\_ SummaryInformation de Msvm** que representan una instantánea de máquina virtual.

<dl> <dt>

<span id="OK"></span><span id="ok"></span>**Aceptar** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (6)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (12)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (13)
</dt> </dl>

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo que hospeda esta máquina virtual.

> [!Note]  
> Se ha agregado en Windows 10.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ManagedElement.InstanceID"), [**Clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID es una propiedad opcional que se puede usar para identificar de forma opaca e inequívoca una instancia de esta clase dentro del ámbito del espacio de nombres de creación de instancias. Varias subclases de esta clase pueden invalidar esta propiedad para que sea necesaria o una clave. Estas subclases también pueden modificar los algoritmos preferidos para garantizar la unidad que se definen a continuación.

Para garantizar la unidad dentro del Espacio de nombres, el valor de InstanceID debe construirse mediante el siguiente algoritmo "preferido":

<OrgID>:<LocalID>

Donde y están separados por dos puntos (:), y donde deben incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial que crea o define el InstanceID o que es un identificador registrado asignado a la entidad empresarial por una autoridad <OrgID> <LocalID> global <OrgID> reconocida. (Este requisito es similar al <Schema Name> \_ <Class Name> estructura de nombres de clase de esquema). Además, para garantizar la unidad, <OrgID> no debe contener dos puntos (:). Cuando se usa este algoritmo, los primeros dos puntos que aparecen en InstanceID deben aparecer entre <OrgID> y <LocalID> .

<LocalID> la entidad empresarial elige y no debe reutilizarse para identificar diferentes elementos subyacentes (reales). Si no es NULL y no se usa el algoritmo "preferido" anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún instanceID generado por este u otros proveedores para el Espacio de nombres de esta instancia.

Si no se establece en null para las instancias definidas por DMTF, el algoritmo "preferido" debe usarse con <OrgID> el establecido en CIM.

> [!Note]  
> Se ha agregado en Windows 10.

 

</dd> <dt>

**IntegrationServicesVersionState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si los servicios de integración instalados en la máquina virtual están actualizados.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

**UpToDate** (1)


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

**Error de coincidencia** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**MemoryAvailable**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Porcentaje de la memoria actual disponible para la máquina virtual. Cuando la memoria dinámica está habilitada para una máquina virtual, esta propiedad representa la proporción de memoria disponible de la máquina virtual con la memoria física total asignada a la máquina virtual. Cuando una máquina virtual no tiene memoria disponible, esta propiedad será negativa y contendrá la proporción de memoria necesaria para la máquina virtual con la memoria física total asignada a la máquina virtual.

Esta propiedad no es válida para las instancias de la clase **\_ Msvm SummaryInformation** que representan máquinas virtuales para las que no está habilitada la memoria dinámica.

Esta propiedad no es válida para las instancias de la clase **Msvm \_ SummaryInformation** que representan una instantánea de máquina virtual.

</dd> <dt>

**MemorySpansPhysicalNumaNodes**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la memoria de uno o varios de los nodos de acceso a memoria virtual no uniforme (NUMA) de la máquina virtual abarca varios nodos NUMA físicos del sistema de equipo host. Contiene **True si** la memoria abarca varios nodos NUMA físicos o **False** en caso contrario.

</dd> <dt>

**MemoryUsage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El uso actual de memoria, en megabytes, de la máquina virtual. Esta propiedad no es válida para las instancias de **Msvm \_ SummaryInformation** que representan una instantánea de máquina virtual.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre único de la máquina virtual o instantánea.

</dd> <dt>

**Notas**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Notas asociadas a la máquina virtual o instantánea.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de procesadores virtuales asignados a la máquina virtual o instantánea.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Los estados operativos actuales de la máquina virtual. Vea la **propiedad OperationalStatus** de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) para ver los valores posibles.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el estado habilitado o deshabilitado del elemento cuando la **propiedad EnabledState** está establecida en 1. Esta propiedad se establecerá en **Null cuando** **EnabledState** sea cualquier valor distinto de 1.

</dd> <dt>

**ProcessorLoad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El uso actual del procesador de la máquina virtual, en porcentaje. Esta propiedad no es válida para las instancias de **Msvm \_ SummaryInformation** que representan una instantánea de máquina virtual.

</dd> <dt>

**ProcessorLoadHistory**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de los 100 ejemplos anteriores del uso del procesador, en porcentaje, para la máquina virtual. Esta propiedad no es válida para las instancias de **Msvm \_ SummaryInformation** que representan una instantánea de máquina virtual.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationHealthEx**")
</dt> </dl>

El estado de replicación de la máquina virtual. Vea la **propiedad ReplicationHealth** de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) para ver los valores posibles.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use **ReplicationHealthEx**.

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**Ok** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Advertencia** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationHealthEx**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de valores de mantenimiento de replicación para las distintas relaciones de replicación de la máquina virtual. Vea la **propiedad ReplicationHealth** de la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para ver los valores posibles.

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**Ok** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Advertencia** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de replicación de la máquina virtual. Vea la **propiedad ReplicationMode** de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) para ver los valores posibles.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**Principal** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**Réplica** (2)


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**Réplica de prueba** (3)


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

**Réplica extendida** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationProviderId**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Para la máquina virtual de réplica principal o extendida, este es el identificador del proveedor de replicación principal. Para una máquina virtual de réplica y si la replicación extendida está habilitada, este es el identificador del proveedor para la relación extendida.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationStateEx**")
</dt> </dl>

Estado de replicación de la máquina virtual. Vea la **propiedad ReplicationState** de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) para ver los valores posibles.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use **ReplicationStateEx.**

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Listo para replicación** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**Esperando a completar la replicación inicial** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Replicación** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Replicación sincronizada completada** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Recuperado** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Confirmado** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Suspendido** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**Esperando para iniciar la resincronización** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Resincronización** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Resincronización suspendida** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Conmutación por error en curso** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationStateEx**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de valores de estado de replicación para las distintas relaciones de replicación de la máquina virtual. Vea la **propiedad ReplicationState** de la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para ver los valores posibles.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Listo para replicación** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Esperando a completar la replicación inicial** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicación** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicación sincronizada completada** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recuperado** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Confirmado** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Esperando para iniciar la resincronización** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Resincronización** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Resincronización suspendida** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Conmutación por error en curso** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Conmutación por recuperación en curso** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Conmutación por recuperación completada** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Actualización de disco en curso** (15)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Actualización de disco crítica** (16)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (17)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Reasignación de la replicación en curso** (18)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparado para la replicación de sincronización** (19)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparado para la replicación inversa de grupos** (20)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill en curso** (21)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**Blindada**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el blindaje está configurado o no para la máquina virtual.

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

**Instantáneas**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz \_ CIM VirtualSystemSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Matriz de [**instancias de Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representan las instantáneas de la máquina virtual. Esta propiedad no es válida para las instancias de **\_ SummaryInformation de Msvm** que representan una instantánea de máquina virtual.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Cadenas que describen los valores de **matriz OperationalStatus** correspondientes. Esto corresponde a la **propiedad StatusDescriptions** de la [**clase \_ ComputerSystem de Msvm.**](msvm-computersystem.md)

</dd> <dt>

**SwapFilesInUse**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si la paginación de segundo nivel está activa. Contiene **True si** la paginación de segundo nivel está activa o False en **caso** contrario.

</dd> <dt>

**TestReplicaSystem**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una [**instancia \_ de ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual de réplica de prueba para la máquina virtual. Esta propiedad no es válida para las instancias de **\_ SummaryInformation de Msvm** que representan una instantánea de máquina virtual.

</dd> <dt>

**ThumbnailImage**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImageWidth**", "**Msvm \_ SummaryInformation**.**ThumbnailImageHeight**")
</dt> </dl>

Matriz que contiene una imagen pequeña de tamaño miniatura del escritorio para la máquina virtual o la instantánea en formato RGB565.

</dd> <dt>

**ThumbnailImageHeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

Alto en píxeles de la imagen en la propiedad ThumbnailImage.

> [!Note]  
> Se ha agregado en Windows 10.

 

</dd> <dt>

**ThumbnailImageWidth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

Ancho en píxeles de la imagen en la propiedad ThumbnailImage.

> [!Note]  
> Se ha agregado en Windows 10.

 

</dd> <dt>

**Uptime**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La cantidad de tiempo desde que la máquina virtual se arranque por última vez. Esta propiedad no es válida para las instancias de **Msvm \_ SummaryInformation** que representan una instantánea de máquina virtual.

</dd> <dt>

**Versión**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión del sistema virtual en un formato de "major.minor", por ejemplo, "2.0".

> [!Note]  
> Se ha agregado en Windows 10.

 

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Cadenas que especifican los nombres descriptivos de los conmutadores virtuales a los que está conectada la máquina virtual.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Subtipo del sistema virtual.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft:Hyper-V:SubType:1** ()


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft:Hyper-V:SubType:2** ()


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ SummaryInformation de Msvm** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
</dt> <dt>

[Clases de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

