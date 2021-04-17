---
description: Esta clase representa un trabajo de operación de migración creado para el almacenamiento o la migración del sistema virtual por el servicio de migración del sistema virtual.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Msvm_MigrationJob (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ddecf34148e3ef07dc78af9b4f2dd45950644cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687268"
---
# <a name="msvm_migrationjob-class"></a>MSVM \_ MigrationJob (clase)

Esta clase representa un trabajo de operación de migración creado para el almacenamiento o la migración del sistema virtual por el servicio de migración del sistema virtual.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ MigrationJob** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSVM \_ MigrationJob** tiene estos métodos.



| Método                                                             | Descripción                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetError**](geterror-msvm-migrationjob.md)                     | Recupera el objeto de error para el trabajo de migración, si existe uno.<br/>                |
| [**GetErrorEx**](geterrorex-msvm-migrationjob.md)                 | Recupera los objetos de error para el trabajo de migración, si existe alguno.<br/>                |
| **KillJob**                                                        | No se admite este método.<br/>                                                   |
| [**RequestStateChange**](requeststatechange-msvm-migrationjob.md) | Solicita que el estado del trabajo de migración se cambie al estado especificado.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **MSVM \_ MigrationJob** tiene estas propiedades.

<dl> <dt>

**Cancelable**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se puede cancelar el trabajo. El valor de esta propiedad no garantiza que una solicitud para cancelar el trabajo se realizará correctamente.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si el trabajo debe eliminarse automáticamente al finalizar. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DestinationHost**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El nombre de host de la plataforma de virtualización de destino a la que está migrando el sistema virtual. Será **null** para la migración de almacenamiento.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El intervalo de tiempo en el que se ha estado ejecutando el trabajo o el tiempo total de ejecución si el trabajo ha finalizado. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un código de error específico del proveedor. El valor debe establecerse en cero si el trabajo se completó sin errores. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que contiene la descripción del error del proveedor. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabajo de CIM**](cim-job.md).**ErrorCode**")
</dt> </dl>

Descripción breve del error, si está presente.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes. Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración de la máquina virtual. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de veces que se debe ejecutar el trabajo. Un valor de 1 indica que el trabajo no se repite, mientras que cualquier valor distinto de cero indica un límite del número de veces que se repetirá el trabajo. Cero indica que no hay ningún límite en el número de veces que se puede procesar el trabajo, pero se terminará después de que se haya alcanzado el **UntilTime** o cuando el trabajo finalice manualmente. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**JobState** es una enumeración de enteros que indica el estado operativo de un trabajo. También puede indicar transiciones entre estos Estados, por ejemplo, "apagar" e "iniciando". Esta propiedad se hereda de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).



| Value                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**Nuevo**</dt> <dt>2</dt> </dl>                                                           | Nunca se ha iniciado el trabajo.<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Inicio**</dt> <dt>3</dt> </dl>                                       | El trabajo se mueve de los Estados 2 (nuevo), 5 (suspendido) u 11 (servicio) al estado 4 (en ejecución).<br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**Ejecución**</dt> <dt>4</dt> </dl>                                           | El trabajo se está ejecutando.<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <dt>**Suspendido**</dt> <dt>5</dt> </dl>                                   | El trabajo se ha detenido, pero se puede reiniciar sin problemas.<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Cerrando**</dt> <dt>6</dt> </dl>                   | El trabajo se está cambiando a un estado 7 (completado), 8 (finalizado) o 9 (con terminación).<br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**Completado**</dt> <dt>7</dt> </dl>                                   | El trabajo se ha completado con normalidad.<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**Terminó**</dt> <dt>8</dt> </dl>                               | El trabajo se ha detenido mediante una solicitud de cambio de estado "finalizar". El trabajo y todos sus procesos subyacentes finalizan y solo se pueden reiniciar como un nuevo trabajo. El requisito de que el trabajo se reinicie solo como un nuevo trabajo es específico del trabajo.<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <dt>**Eliminado**</dt> <dt>9</dt> </dl>                                               | La solicitud de cambio de estado "Kill" detuvo el trabajo. Es posible que los procesos subyacentes sigan en ejecución y que sea necesario realizar una limpieza para liberar recursos.<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**Excepción**</dt> <dt>10</dt> </dl>                                  | El trabajo está en un estado anómalo que podría ser indicativo de una condición de error. El estado real del trabajo podría estar disponible a través de objetos específicos del trabajo.<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**Servicio**</dt> <dt>11</dt> </dl>                                          | El trabajo está en un estado específico del proveedor que admite la detección de problemas, la resolución o ambos.<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>12 32767</dt> </dl>            | Reservado.<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Proveedor reservado**</dt> <dt>32768 65535</dt> </dl> | Reservado.<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**Estado del trabajo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que representa el estado del trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el tipo de trabajo del que este objeto realiza el seguimiento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

**Creación de una máquina virtual remota** (300)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

**Comprobando la compatibilidad de las máquinas virtuales** (301)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

**Comprobando la compatibilidad de la máquina virtual y el almacenamiento** (302)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

**Comprobando la compatibilidad de almacenamiento** (303)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

**Comprobando la migración de almacenamiento** (304)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

**Mover la máquina virtual** (305)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

**Traslado de máquinas virtuales y almacenamiento** (306)


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

**Mover almacenamiento** (307)


</dt> <dd></dd> </dl>

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

Indica si las horas representadas en las propiedades **RunStartInterval** y **UntilTime** representan las horas locales o las horas UTC.

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Hora local** (1)
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Hora UTC** (2)
</dt> </dl>

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")
</dt> </dl>

El tipo de migración representado por este objeto de trabajo. Será uno de los valores definidos para la propiedad **MigrationType** de la clase [**\_ VirtualSystemMigrationSettingData de MSVM**](msvm-virtualsystemmigrationsettingdata.md) .

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Nombre para mostrar de esta instancia de un trabajo. Además, el nombre para mostrar se puede usar como una propiedad para una búsqueda o una consulta. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NewResourceSettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

En el caso de una migración en vivo, siempre se establecerá en **null**.

En el caso de una migración de almacenamiento, si es **null**, no se mueve ninguno de los discos duros virtuales (VHD) de la máquina virtual. De lo contrario, contendrá una matriz de instancias incrustadas de la clase [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) que representan los VHD que se van a deshacer. La propiedad de **conexión** de estas instancias especificará la ubicación de destino del VHD.

</dd> <dt>

**NewSystemSettingData**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

En el caso de una migración en vivo, siempre se establecerá en **null**.

En el caso de una migración de almacenamiento, si es **null**, las raíces de datos de la máquina virtual no se mueven. De lo contrario, contendrá una instancia incrustada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) , donde las propiedades **ExternalDataRoot**, **SnapshotDataRoot** y **SwapFileDataRoot** especificarán las nuevas raíces de datos.

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Usuario al que se notifica el error o la finalización del trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** . Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados actuales del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que describe la acción de recuperación cuando la propiedad **RecoveryAction** de la instancia es 1 (otra). Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El usuario que envió el trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MinValue** (0), **MaxValue** (100), **unidades** ("porcentaje")
</dt> </dl>

Porcentaje de finalización del trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La importancia de la ejecución de un trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la acción de recuperación que se va a realizar para un trabajo que no se ejecuta correctamente. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**No continuar** (2)
</dt> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar con el trabajo siguiente** (3)
</dt> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Volver a ejecutar el trabajo** (4)
</dt> <dt>

<span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Ejecutar trabajo de recuperación** (5)
</dt> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MinValue** (-31), **MaxValue** (31)
</dt> </dl>

Día del mes en el que se debe procesar el trabajo. Hay distintas interpretaciones para esta propiedad, dependiendo del valor de **RunDayOfWeek**.

Cuando **RunDayOfWeek** es 0 y **RunDay** es positivo, **RunDay** define el día del mes en el que se procesa el trabajo. Por ejemplo, si **RunDayOfWeek** es 0 y **RunDay** es 12, el trabajo se procesará <sup>el día 12</sup> del mes.

Cuando **RunDayOfWeek** es 0 y **RunDay** es negativo, **RunDay** define el número de días antes del último día del mes en el que se procesa el trabajo.  1 indica el último día del mes, 2 indica un día antes del último día del mes, y así sucesivamente. Por ejemplo, si **RunDayOfWeek** es 0 y **RunDay** es 1, el trabajo se procesará el último día del mes.

Cuando **RunDayOfWeek** no es 0, **RunDayOfWeek** es el día de la semana en el que se procesará el trabajo, en relación con **RunDay**. Por ejemplo, si **RunDay** es 15 y **RunDayOfWeek** es 7 (+ sábado), el trabajo se procesará el primer sábado en o después <sup>del día 15</sup> del mes. Si el **RunDay** es 20 y el de **RunDayOfWeek** es 7 (sábado), el trabajo se procesará el primer sábado en <sup>el día del</sup> mes o antes del mismo. Si **RunDay** es 1 y **RunDayOfWeek** es 1 (domingo), el trabajo se procesará el último domingo del mes.

Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Entero positivo o negativo que se usa junto con **RunDay** para indicar el día de la semana o el mes en el que se procesa el trabajo. Vea la descripción de la propiedad **RunDay** para obtener más información. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Sábado** (7)
</dt> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Viernes** (6)
</dt> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Jueves** (5)
</dt> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Miércoles** (4)
</dt> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Martes** (3)
</dt> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Lunes** (2)
</dt> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** (1)
</dt> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)
</dt> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domingo** (1)
</dt> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Lunes** (2)
</dt> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Martes** (3)
</dt> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Miércoles** (4)
</dt> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Jueves** (5)
</dt> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Viernes** (6)
</dt> <dt>

<span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sábado** (7)
</dt> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mes en el que se debe procesar el trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

<dl> <dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Enero** (0)
</dt> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Febrero** (1)
</dt> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>**Marzo** (2)
</dt> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>**Abril** (3)
</dt> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>**Mayo** (4)
</dt> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>**Junio** (5)
</dt> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>**Julio** (6)
</dt> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)
</dt> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Septiembre** (8)
</dt> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Octubre** (9)
</dt> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Noviembre** (10)
</dt> <dt>

<span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Diciembre** (11)
</dt> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El intervalo de tiempo después de medianoche en el momento en que se debe procesar el trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora de inicio programada para el trabajo, si procede. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora a la que comenzó el trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadenas que describen los distintos valores de la matriz **OperationalStatus** . Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad de tiempo, en minutos, que el trabajo se conserva una vez finalizada la ejecución, ya sea correctamente o con errores en esa ejecución. El trabajo debe permanecer en vigor durante un período de tiempo, independientemente del valor de la propiedad **DeleteOnCompletion** . El valor predeterminado es cinco minutos. Esta propiedad se hereda de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))y siempre está establecida en 00000000000500.000000:000.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha u hora en que cambió por última vez el estado del trabajo. Si el estado del trabajo no ha cambiado y se rellena esta propiedad, debe establecerse en un valor de intervalo 0. Si se solicitó un cambio de estado, pero se rechazó o no se procesó todavía, la propiedad no se debe actualizar. Esta propiedad se hereda de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora a la que se envió el trabajo. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que el trabajo no es válido o se debe detener. Esta propiedad se hereda del [**\_ trabajo CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**VirtualSystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre único del sistema virtual afectado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

