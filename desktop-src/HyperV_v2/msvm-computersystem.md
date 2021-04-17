---
description: Representa un sistema de equipo físico o una máquina virtual.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Msvm_ComputerSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem
- Msvm_ComputerSystem.SetPowerState
- Msvm_ComputerSystem.InstanceID
- Msvm_ComputerSystem.Caption
- Msvm_ComputerSystem.Description
- Msvm_ComputerSystem.ElementName
- Msvm_ComputerSystem.InstallDate
- Msvm_ComputerSystem.OperationalStatus
- Msvm_ComputerSystem.StatusDescriptions
- Msvm_ComputerSystem.Status
- Msvm_ComputerSystem.HealthState
- Msvm_ComputerSystem.CommunicationStatus
- Msvm_ComputerSystem.DetailedStatus
- Msvm_ComputerSystem.OperatingStatus
- Msvm_ComputerSystem.PrimaryStatus
- Msvm_ComputerSystem.EnabledState
- Msvm_ComputerSystem.OtherEnabledState
- Msvm_ComputerSystem.RequestedState
- Msvm_ComputerSystem.EnabledDefault
- Msvm_ComputerSystem.TimeOfLastStateChange
- Msvm_ComputerSystem.AvailableRequestedStates
- Msvm_ComputerSystem.TransitioningToState
- Msvm_ComputerSystem.CreationClassName
- Msvm_ComputerSystem.Name
- Msvm_ComputerSystem.PrimaryOwnerName
- Msvm_ComputerSystem.PrimaryOwnerContact
- Msvm_ComputerSystem.Roles
- Msvm_ComputerSystem.NameFormat
- Msvm_ComputerSystem.OtherIdentifyingInfo
- Msvm_ComputerSystem.IdentifyingDescriptions
- Msvm_ComputerSystem.Dedicated
- Msvm_ComputerSystem.OtherDedicatedDescriptions
- Msvm_ComputerSystem.ResetCapability
- Msvm_ComputerSystem.PowerManagementCapabilities
- Msvm_ComputerSystem.OnTimeInMilliseconds
- Msvm_ComputerSystem.ProcessID
- Msvm_ComputerSystem.TimeOfLastConfigurationChange
- Msvm_ComputerSystem.NumberOfNumaNodes
- Msvm_ComputerSystem.ReplicationState
- Msvm_ComputerSystem.ReplicationHealth
- Msvm_ComputerSystem.ReplicationMode
- Msvm_ComputerSystem.FailedOverReplicationType
- Msvm_ComputerSystem.LastReplicationType
- Msvm_ComputerSystem.LastApplicationConsistentReplicationTime
- Msvm_ComputerSystem.LastReplicationTime
- Msvm_ComputerSystem.LastSuccessfulBackupTime
- Msvm_ComputerSystem.EnhancedSessionModeState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae36179e14b584bad4e68350e27d485cdc10c42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551875"
---
# <a name="msvm_computersystem-class"></a>MSVM \_ clase ComputerSystem

Representa un sistema de equipo físico o una máquina virtual.

Para recuperar información de VMMS, use la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   CreationClassName;
  string   Name = "GUID";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   NameFormat;
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability = 1;
  uint16   PowerManagementCapabilities[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
  uint16   NumberOfNumaNodes;
  uint16   ReplicationState;
  uint16   ReplicationHealth;
  uint16   ReplicationMode;
  uint16   FailedOverReplicationType;
  uint16   LastReplicationType;
  DateTime LastApplicationConsistentReplicationTime;
  DateTime LastReplicationTime;
  DateTime LastSuccessfulBackupTime;
  uint16   EnhancedSessionModeState;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ComputerSystem** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ ComputerSystem de MSVM** tiene estos métodos.



| Método                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)           | Inserta una interrupción no enmascarable en la máquina virtual. Este método solo se admite para las instancias de la clase **MSVM \_ ComputerSystem** que representan una máquina virtual.<br/> **Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.<br/>                                    |
| [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md)     | Solicita que el estado de replicación de la máquina virtual se cambie al valor especificado. Este método solo se admite para las instancias de la clase **MSVM \_ ComputerSystem** que representan una máquina virtual.<br/>                                                                                                        |
| [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) | Solicita que el estado de replicación de la máquina virtual se cambie al valor especificado. Este método solo se admite para las instancias de la clase **MSVM \_ ComputerSystem** que representan una máquina virtual.<br/> **Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.<br/> |
| [**RequestStateChange**](requeststatechange-msvm-computersystem.md)                           | Solicita que se cambie el estado de la máquina virtual. Este método solo se admite para las instancias de la clase **MSVM \_ ComputerSystem** que representan una máquina virtual.<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | No se admite este método.<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>Propiedades

La **clase \_ ComputerSystem de MSVM** tiene estas propiedades.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado. Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) . Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual. Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.

Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (.. )
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y contendrá uno de los valores siguientes.



| Value                                                                                                | Significado                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Máquina virtual"</dt> </dl>         | La instancia representa una máquina virtual.<br/>    |
| <dl> <dt>"Sistema del equipo host"</dt> </dl> | La instancia representa el equipo host.<br/> |



 

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase o subclase que se usa en la creación de una instancia de. Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre se establece en "MSVM \_ ComputerSystem".

</dd> <dt>

**Dedicado**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el sistema informático es un sistema especial (dedicado a un uso determinado), en lugar de un sistema de uso general. Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en 0 (no dedicado).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y contendrá uno de los valores siguientes.



| Value                                                                                                          | Significado                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Sistema de equipo virtual de Microsoft"</dt> </dl> | La instancia representa una máquina virtual.<br/>    |
| <dl> <dt>"Sistema de equipo de hospedaje de Microsoft"</dt> </dl> | La instancia representa el equipo host.<br/> |



 

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en el nombre para mostrar del equipo de una máquina virtual o el nombre NetBIOS del sistema operativo de administración.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitado y deshabilitado de un elemento. Esta propiedad también puede indicar las transiciones entre estos Estados solicitados. Esta propiedad se hereda de la clase [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y está establecida en 2 (habilitado) para un equipo físico o uno de los siguientes valores para una máquina virtual. Para obtener una vista gráfica de estos Estados, consulte la sección Comentarios.



| Value                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                                                 | No se pudo determinar el estado del elemento.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Otro**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Habilitado**</dt> <dt>2</dt> </dl>                                                 | El elemento se está ejecutando.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deshabilitado**</dt> <dt>3</dt> </dl>                                             | El elemento está desactivado.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Cerrando**</dt> <dt>4</dt> </dl>                         | El elemento está en el proceso de pasar a un Estado deshabilitado.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**No aplicable**</dt> <dt>5</dt> </dl>                     | El elemento no admite la habilitación o deshabilitación.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Habilitada pero sin conexión**</dt> <dt>6</dt> </dl> | Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**En la prueba**</dt> <dt>7</dt> </dl>                                                 | El elemento está en un estado de prueba.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Aplazado**</dt> <dt>8</dt> </dl>                                             | Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> Modo <dt>**inactivo**</dt> <dt>9</dt> </dl>                                                 | El elemento está habilitado pero en modo restringido. El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos. Todas las demás solicitudes se ponen en cola.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Inicio**</dt> <dt>10</dt> </dl>                                            | El elemento está en proceso de pasar a un estado habilitado (2). Las nuevas solicitudes se ponen en cola.<br/>                                                                                                             |



 

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el estado actual del modo de sesión mejorada en la máquina virtual.

El proveedor WMI de Hyper-V genera una [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) cada vez que cambia el **EnhancedSessionModeState** de la clase **MSVM \_ ComputerSystem** . Si una sesión de vmconnection activa recibe un **\_ \_ InstanceModificationEvent**, intenta cambiar al modo de sesión mejorada si el usuario habilita esa configuración.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

**EnhancedSessionModeState** puede tener uno de estos valores:

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Permitido y disponible** (2)


</dt> <dd>

Se permite el modo mejorado y está disponible en la máquina virtual.

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**No permitido** (3)


</dt> <dd>

El modo mejorado no se permite en la máquina virtual.

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Permitido pero no disponible** (6)


</dt> <dd>

Se permite el modo mejorado, pero no está disponible actualmente en la máquina virtual.

</dd> </dl>

</dd> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**FailedOverReplicationType**")
</dt> </dl>

El tipo de punto de datos de recuperación que se aplicó durante la operación de conmutación por error.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

Los valores posibles son:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coherente** con la aplicación (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planeada** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.

Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información. La propiedad **EnabledState** también puede contener más información. Por ejemplo, si el espacio en disco es muy bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Value                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**Aceptar**</dt> <dt>5</dt> </dl>                                                                               | La máquina virtual es totalmente funcional y funciona en parámetros operativos normales y sin errores.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Error principal**</dt> <dt>20</dt> </dl>             | Se produjo un error importante en la máquina virtual. Este valor se usa cuando uno o varios discos que contienen los VHD de la máquina virtual tienen poco espacio en disco y la máquina virtual se ha puesto en pausa.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Error crítico**</dt> <dt>25</dt> </dl> | El elemento no es funcional y es posible que la recuperación no sea posible. Esto puede indicar que el proceso de trabajo de la máquina virtual (Vmwp.exe) no responde a las solicitudes de control o información, o que uno o varios discos que contienen los discos duros virtuales de la máquina virtual tienen poco espacio en disco.<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración de la máquina virtual para una máquina virtual, o **null**, para un sistema operativo de administración. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

En Windows 8, hay una única instancia de [**ReplicationSettingData**](msvm-replicationsettingdata.md) para cada sistema de equipo o máquina virtual. Por Windows 8.1, una máquina virtual de recuperación tiene dos instancias de **ReplicationSettingData**. Este cambio distingue y asocia los datos de configuración con la relación de replicación.



| Nombre de propiedad  | Valor de Windows 8               | Windows 8.1 valor                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft: <vmguid> \\ HVR | Microsoft: <vmguid> \\ HVR \\<0/1> |



 

En el valor Windows 8.1, 0 indica principal y 1 indica replicación extendida. Para obtener más información acerca de la replicación extendida, consulte [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")
</dt> </dl>

La hora a la que se recibió la última replicación coherente con la aplicación para la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationTime**")
</dt> </dl>

La hora a la que se recibió la última replicación durante la recuperación de la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**LastReplicationType**")
</dt> </dl>

El tipo de la última replicación que se recibió para la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

Los valores posibles son:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coherente** con la aplicación (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planeada** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastSuccessfulBackupTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora a la que se completó la última copia de seguridad correcta de la máquina virtual.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en "*GUID*".

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que identifica el modo en que se generó el nombre del sistema mediante la heurística de subclases. Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.

</dd> <dt>

**NumberOfNumaNodes**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de nodos de acceso a memoria no uniforme (NUMA) del equipo. Cuando **MSVM \_ ComputerSystem** representa el sistema del equipo host, esta propiedad contiene el recuento de nodos Numa físicos. Cuando **MSVM \_ ComputerSystem** representa una máquina virtual, esta propiedad contiene el número de nodos Numa virtuales que se presentan al sistema operativo invitado a través de la tabla de afinidad de recursos del sistema ACPI (SRAT).

</dd> <dt>

**OnTimeInMilliseconds**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milisegundos")
</dt> </dl>

Para la máquina virtual, esta propiedad indica el tiempo, en milisegundos, desde la última vez que se activó, restableció o restauró el equipo. Esta vez excluye la hora en que la máquina virtual estaba en estado de pausa. En el sistema operativo de administración, esta propiedad se establece en **null**.

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

Una matriz que contiene los Estados actuales del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). El valor en el índice cero (0) es uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**Aceptar**</dt> <dt>2</dt> </dl>                                                                                      | La máquina virtual es funcional y funciona con normalidad.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degradado**</dt> <dt>3</dt> </dl>                                         | La máquina virtual solo es parcialmente funcional. Esto indica que no se puede tener acceso al almacenamiento que contiene la configuración. Una máquina virtual en este estado solo se puede desactivar o eliminar. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Error predictivo**</dt> <dt>5</dt> </dl> | La máquina virtual es funcional, pero puede producir un error en el futuro. Esto indica que el almacenamiento que contiene el disco duro virtual de la máquina virtual tiene poco espacio disponible. La máquina virtual se pausará si no hay más espacio disponible en disco.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Detenido**</dt> <dt>10</dt> </dl>                                            | Este valor no se admite. Si se detiene la máquina virtual, la propiedad **EnabledState** tendrá un valor de 3 (deshabilitado).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**En el servicio**</dt> <dt>11</dt> </dl>                                | La máquina virtual está procesando una solicitud.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Inactivo**</dt> <dt>15</dt> </dl>                                            | Este valor no se admite. Si la máquina virtual está suspendida o en pausa, la propiedad **EnabledState** tendrá un valor de 32769 (suspendido) o 32768 (en pausa).<br/>                                                                                    |



 

El valor en el índice uno (1) es opcional y contiene información de estado secundaria. Un cliente debe usar el estado principal del índice cero (0) para determinar si se puede emitir una nueva solicitud a la máquina virtual. Si **OperationalStatus** \[ 0 \] es 2 (OK),  \[ \] se puede interrumpir la operación indicada por OperationalStatus 1.

El valor de **OperationalStatus** \[ 1 \] es uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                                   | Significado                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Creando instantánea**</dt> <dt>32768</dt> </dl>                                 | Se está creando una instantánea en el proceso de creación de la máquina virtual.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Aplicando la instantánea**</dt> <dt>32769</dt> </dl>                                 | Una instantánea está en proceso de aplicarse a la máquina virtual.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Eliminando instantánea**</dt> <dt>32770</dt> </dl>                                 | Se está eliminando una instantánea de la máquina virtual.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Esperando a iniciar**</dt> <dt>32771</dt> </dl>                                     | La máquina virtual se iniciará después de que haya transcurrido el retraso de inicio automático.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Combinación de discos**</dt> <dt>32772</dt> </dl>                                                 | Se están combinando los discos duros virtuales de las instantáneas eliminadas previamente.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportando Máquina Virtual**</dt> <dt>32773</dt> </dl> | La máquina virtual se está exportando.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migrando la máquina Virtual**</dt> <dt>32774</dt> </dl> | La máquina virtual se está migrando en directo desde un equipo físico a otro.<br/>  |



 

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que describe cómo o por qué el sistema está dedicado cuando la matriz **dedicada** incluye el valor 2 (otro). Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El estado habilitado o deshabilitado de la máquina virtual cuando la propiedad **EnabledState** está establecida en 1 (otro). Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de la de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en **null**.

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**un \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem), pero no se usa.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que indica cómo se puede alcanzar el propietario del sistema principal (por ejemplo, un número de teléfono o una dirección de correo electrónico). Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del propietario del sistema principal. Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El identificador del proceso en el que se está ejecutando esta máquina virtual. Este valor se puede usar para identificar de forma única la instancia de Vmwp.exe en el sistema que ejecuta la máquina virtual.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationHealth**")
</dt> </dl>

Mantenimiento de la replicación de la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

Los valores posibles son:

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**Aceptar** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**ADVERTENCIA** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el modo de replicación para la máquina virtual. Será uno de los valores siguientes.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Principal** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>**Réplica** (2)


</dt> <dd>

Recuperación

</dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>**Réplica de prueba** (3)


</dt> <dd>

Réplica

</dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>**Réplica extendida** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md).**ReplicationState**")
</dt> </dl>

El estado de replicación de la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

Los valores posibles son:

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Listo para la replicación** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**Esperando para completar la replicación inicial** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Replicando** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Replicación sincronizada completa** (4)


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

Volver a **sincronizar** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Resincronización suspendida** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Conmutación por error en curso** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

**Conmutación por recuperación en curso** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

**Conmutación por recuperación completada** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último estado solicitado o deseado de la máquina virtual tal como se pasó al método [**RequestStateChange**](requeststatechange-msvm-computersystem.md) , o 12 (no aplicable) si no hay ningún cambio de estado en curso. El estado real del elemento se representa mediante **EnabledState**. Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**un \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre está establecida en 1 (otro).

</dd> <dt>

**Roles**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que describen los roles que el sistema desempeña en el entorno de tecnología de la información. Esta propiedad se hereda del [**\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre está establecida en **null**.

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
</dt> <dt>

Calificadores: **ArrayType** ("indexado")
</dt> </dl>

Una matriz que contiene cadenas que describen los valores correspondientes de la matriz **OperationalStatus** . Por ejemplo, si 11 (en servicio) es el valor asignado a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] puede incluir una explicación sobre el motivo por el que la máquina virtual está procesando una solicitud. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**TimeOfLastConfigurationChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se modificó por última vez el archivo de configuración de la máquina virtual. El archivo de configuración se modifica durante ciertas operaciones de máquina virtual, así como cuando se agrega, modifica o quita cualquiera de las configuraciones de dispositivo o máquina virtual.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se cambió por última vez el estado habilitado del elemento. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el estado de destino al que la instancia está cambiando. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), pero no se usa.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En la ilustración siguiente se muestran los valores **EnabledState** .

![diagrama de estado de los valores enabledstate para Windows Server 2008 R2](images/msvm-computersystem-enabledstate-win2008r2.png)

Cuando cambia una propiedad de la clase **MSVM \_ ComputerSystem** , el proveedor WMI indica un evento [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) que describe los cambios. El estado anterior se encuentra en la propiedad **PreviousInstance** y el nuevo estado se incluye en la propiedad **TargetInstance** . Este evento es asincrónico; en el momento en que se procesa el evento **\_ \_ InstanceModificationEvent** , es posible que la propiedad **TargetInstance** no refleje el estado actual.

El acceso a la clase **MSVM \_ ComputerSystem** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Ejemplos

Consulte [consultar objetos de red](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ComputerSystem de CIM \_**](cim-computersystem.md)
</dt> <dt>

[**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**ComputerSystem de CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**MSVM \_ ComputerSystem (V1)**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[Clases de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

