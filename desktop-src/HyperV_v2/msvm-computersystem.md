---
description: Representa un sistema de equipo físico o una máquina virtual.
ms.assetid: 1db9e169-1466-4898-ab95-e9d622fe43cb
title: Msvm_ComputerSystem clase
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
ms.openlocfilehash: 7e35ebd6000dfae5e99c4b589f4c0a62e84f1e1d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880912"
---
# <a name="msvm_computersystem-class"></a>Clase ComputerSystem de Msvm \_

Representa un sistema de equipo físico o una máquina virtual.

Para recuperar información de VMMS, use la [**clase \_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

La sintaxis siguiente se Managed Object Format código MOF e incluye todas las propiedades heredadas.

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

La **clase \_ ComputerSystem de Msvm** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ ComputerSystem de Msvm** tiene estos métodos.



| Método                                                                                         | Descripción                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md)           | Inserta una interrupción no enmascarable en la máquina virtual. Este método solo se admite para instancias de la clase **\_ ComputerSystem de Msvm** que representan una máquina virtual.<br/> **Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.<br/>                                    |
| [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md)     | Solicita que el estado de replicación de la máquina virtual cambie al valor especificado. Este método solo se admite para instancias de la clase **\_ ComputerSystem de Msvm** que representan una máquina virtual.<br/>                                                                                                        |
| [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) | Solicita que el estado de replicación de la máquina virtual cambie al valor especificado. Este método solo se admite para instancias de la clase **\_ ComputerSystem de Msvm** que representan una máquina virtual.<br/> **Windows 8.1:** Este método no se admite hasta Windows 8.1 y Windows Server 2012 R2.<br/> |
| [**RequestStateChange**](requeststatechange-msvm-computersystem.md)                           | Solicita que se cambie el estado de la máquina virtual. Este método solo se admite para instancias de la clase **\_ ComputerSystem de Msvm** que representan una máquina virtual.<br/>                                                                                                                                           |
| **SetPowerState**                                                                              | No se admite este método.<br/>                                                                                                                                                                                                                                                                                            |



 

### <a name="properties"></a>Propiedades

La **clase \_ ComputerSystem de Msvm** tiene estas propiedades.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los valores posibles para el parámetro *RequestedState* del [**método RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado. Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities,** donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85)) Esta propiedad puede ser no **NULL** si una implementación puede anunciar el conjunto de valores posibles como una función del estado actual. Esta propiedad será **Null si** una implementación no puede determinar el conjunto de valores posibles como una función del estado actual.

Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin** conexión (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Aplazar** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)
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

Breve descripción del objeto. Esta propiedad se hereda de la [**clase \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y contendrá uno de los siguientes valores.



| Valor                                                                                                | Significado                                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Máquina virtual"</dt> </dl>         | La instancia representa una máquina virtual.<br/>    |
| <dl> <dt>"Sistema de hospedaje del equipo"</dt> </dl> | La instancia de representa el equipo host.<br/> |



 

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la capacidad de la instrumentación para comunicarse con el elemento administrado subyacente. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase o subclase que se usa en la creación de una instancia de . Esta propiedad se hereda del sistema [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-system)y siempre se establece en "Msvm \_ ComputerSystem".

</dd> <dt>

**Dedicado**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el sistema informático es un sistema de propósito especial (dedicado a un uso determinado), en lugar de ser un sistema de uso general. Esta propiedad se hereda de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre se establece en 0 (No dedicado).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y contendrá uno de los siguientes valores.



| Valor                                                                                                          | Significado                                                  |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>"Microsoft Virtual Computer System"</dt> </dl> | La instancia representa una máquina virtual.<br/>    |
| <dl> <dt>"Sistema de equipos de hospedaje de Microsoft"</dt> </dl> | La instancia de representa el equipo host.<br/> |



 

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la propiedad **PrimaryStatus con** detalles de estado adicionales. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ MANAGEDElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en el nombre para mostrar del equipo de una máquina virtual o el nombre NetBIOS del sistema operativo de administración.

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y será uno de los siguientes valores.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado pero sin conexión** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitados y deshabilitados de un elemento. Esta propiedad también puede indicar las transiciones entre estos estados solicitados. Esta propiedad se hereda de la clase [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y se establece en 2 (Habilitado) para un equipo físico o uno de los valores siguientes para una máquina virtual. Para obtener una vista gráfica de estos estados, vea Comentarios.



| Valor                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                                                 | No se pudo determinar el estado del elemento.<br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Otros**</dt> <dt>1</dt> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Habilitado**</dt> <dt>2</dt> </dl>                                                 | El elemento se está ejecutando.<br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deshabilitado**</dt> <dt>3</dt> </dl>                                             | El elemento está desactivado.<br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Apagar**</dt> <dt>4</dt> </dl>                         | El elemento está en proceso de pasar a un estado Deshabilitado.<br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**No aplicable**</dt> <dt>5</dt> </dl>                     | El elemento no admite la habilitación o deshabilitación.<br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Habilitado pero sin conexión**</dt> <dt>6</dt> </dl> | El elemento podría estar completando comandos y quitará las solicitudes nuevas.<br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**En la prueba**</dt> <dt>7</dt> </dl>                                                 | El elemento está en estado de prueba.<br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <dt>**Aplazado**</dt> <dt>8</dt> </dl>                                             | El elemento podría estar completando comandos, pero pondrá en cola las nuevas solicitudes.<br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <dt>**Quiesce**</dt> <dt>9</dt> </dl>                                                 | El elemento está habilitado, pero en modo restringido. El comportamiento del elemento es similar al estado Habilitado (2), pero procesa solo un conjunto restringido de comandos. Todas las demás solicitudes se ponen en cola.<br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**A partir**</dt> <dt>de 10</dt> </dl>                                            | El elemento está en proceso de pasar a un estado Habilitado (2). Las nuevas solicitudes se ponen en cola.<br/>                                                                                                             |



 

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el estado actual del modo de sesión mejorado en la máquina virtual.

El proveedor WMI de Hyper-V genera [**\_ \_ un instanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) cada vez que **cambia el Elemento EnhancedSessionModeState** de la clase **\_ ComputerSystem de Msvm.** Si una sesión de vmconnection activa recibe **\_ \_ un instanceModificationEvent**, intenta cambiar al modo de sesión mejorada si el usuario ha habilitado esa configuración.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

**EnhancedSessionModeState** puede ser uno de estos valores:

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>**Permitido y disponible** (2)


</dt> <dd>

El modo mejorado está permitido y disponible en la máquina virtual.

</dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**No permitido** (3)


</dt> <dd>

No se permite el modo mejorado en la máquina virtual.

</dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>**Permitido pero no disponible** (6)


</dt> <dd>

Se permite el modo mejorado, pero no está disponible actualmente en la máquina virtual.

</dd> </dl>

</dd> <dt>

**FailedOverReplicationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).**FailedOverReplicationType**")
</dt> </dl>

Tipo de punto de datos de recuperación que se aplicó durante la operación de conmutación por error.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

Los valores posibles son:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coherente con la** aplicación (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planeado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.

Cuando se produzca un error crítico, compruebe el registro de eventos para obtener más información. La **propiedad EnabledState** también puede contener más información. Por ejemplo, cuando el espacio en disco es críticamente bajo, **HealthState** se establece en 25, la máquina virtual se pausa y **EnabledState** se establece en 32768 (en pausa).

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)



| Valor                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**Ok**</dt> <dt>5</dt> </dl>                                                                               | La máquina virtual es totalmente funcional y funciona con parámetros operativos normales y sin errores.<br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <dt>**Error principal**</dt> <dt>20</dt> </dl>             | La máquina virtual ha sufrido un error importante. Este valor se usa cuando uno o varios discos que contienen los VHD de la máquina virtual tienen poco espacio en disco y la máquina virtual se ha pausado.<br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <dt>**Error crítico**</dt> <dt>25</dt> </dl> | El elemento no es funcional y es posible que la recuperación no sea posible. Esto puede indicar que el proceso de trabajo de la máquina virtual (Vmwp.exe) no responde a las solicitudes de control o de información, o que uno o varios discos que contienen los VHD de la máquina virtual tienen poco espacio en disco.<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre se establece en **Null.**

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración de la máquina virtual para una máquina virtual, o **Null,** para un sistema operativo de administración. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

En Windows 8, hay una única instancia de [**ReplicationSettingData**](msvm-replicationsettingdata.md) para cada sistema de equipo o máquina virtual. Por Windows 8.1, una máquina virtual de recuperación tiene dos instancias de **ReplicationSettingData**. Este cambio diferencia y asocia los datos de configuración con la relación de replicación.



| Nombre de propiedad  | Windows 8 valor               | Windows 8.1 valor                          |
|----------------|-------------------------------|--------------------------------------------|
| **InstanceID** | Microsoft: &lt; vmguid &gt; \\ HVR | Microsoft: &lt; vmguid &gt; \\ HVR \\<0/1> |



 

En el Windows 8.1, 0 indica principal y 1 indica replicación extendida. Para obtener más información sobre la replicación extendida, [**vea Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).

</dd> <dt>

**LastApplicationConsistentReplicationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).**LastApplicationConsistentReplicationTime**")
</dt> </dl>

Hora a la que se recibió la última replicación coherente con la aplicación para la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

</dd> <dt>

**LastReplicationTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).**LastReplicationTime**")
</dt> </dl>

Hora a la que se recibe la última replicación en la recuperación de la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

</dd> <dt>

**LastReplicationType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).**LastReplicationType**")
</dt> </dl>

Tipo de la última replicación que se recibió para la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

Los valores posibles son:

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

**Normal** (1)


</dt> <dd></dd> <dt>

<span id="Application_consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

**Coherente con la** aplicación (2)


</dt> <dd></dd> <dt>

<span id="Planned"></span><span id="planned"></span><span id="PLANNED"></span>

**Planeado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastSuccessfulBackupTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora a la que se completó la última copia de seguridad correcta para la máquina virtual.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda del sistema CIM y siempre se establece en "*GUID*". [**\_**](/windows/desktop/CIMWin32Prov/cim-system)

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que identifica cómo se generó el nombre del sistema mediante la subclase heurística. Esta propiedad se hereda de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre se establece en **Null.**

</dd> <dt>

**NumberOfNumaNodes**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de nodos de acceso a memoria no uniforme (NUMA) del sistema informático. Cuando **Msvm \_ ComputerSystem representa** el sistema del equipo host, esta propiedad contiene el recuento de nodos NUMA físicos. Cuando **Msvm \_ ComputerSystem** representa una máquina virtual, esta propiedad contiene el número de nodos NUMA virtuales que se presentan al sistema operativo invitado a través de la tabla de afinidad de recursos del sistema ACPI (SRAT).

</dd> <dt>

**OnTimeInMilliseconds**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Milegundos")
</dt> </dl>

En el caso de la máquina virtual, esta propiedad indica el tiempo, en milisegundos, desde la última vez que la máquina se ha activado, restablecido o restaurado. Esta hora excluye la hora en que la máquina virtual estaba en estado de pausa. Para el sistema operativo de administración, esta propiedad se establece en **Null.**

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado actual para la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la **propiedad EnabledState.** Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que contiene los estados actuales del objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) El valor del índice cero (0) es uno de los siguientes valores.



| Valor                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**Ok**</dt> <dt>2</dt> </dl>                                                                                      | La máquina virtual es funcional y funciona con normalidad.<br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Degradado**</dt> <dt>3</dt> </dl>                                         | La máquina virtual solo es parcialmente funcional. Esto indica que no se puede acceder al almacenamiento que contiene la configuración. Una máquina virtual en este estado solo se puede desactivar o eliminar. <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <dt>**Error predictivo**</dt> <dt>5</dt> </dl> | La máquina virtual es funcional, pero puede producir un error en el futuro. Esto indica que el almacenamiento que contiene el disco duro virtual de la máquina virtual tiene poco espacio libre. La máquina virtual se pausará si no hay más espacio disponible en disco.<br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <dt>**Detenido**</dt> <dt>10</dt> </dl>                                            | Este valor no se admite. Si se detiene la máquina virtual, la **propiedad EnabledState** tendrá un valor de 3 (Deshabilitado).<br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <dt>**En el servicio**</dt> <dt>11</dt> </dl>                                | La máquina virtual está procesando una solicitud.<br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <dt>**Inactivo**</dt> <dt>15</dt> </dl>                                            | Este valor no se admite. Si la máquina virtual está suspendida o en pausa, la propiedad **EnabledState** tendrá un valor de 32769 (suspendido) o 32768 (en pausa).<br/>                                                                                    |



 

El valor del índice uno (1) es opcional y contiene información de estado secundaria. Un cliente debe usar el estado principal del índice cero (0) para determinar si se puede emitir una nueva solicitud a la máquina virtual. Si **OperationalStatus** \[ 0 es 2 (correcto), se puede interrumpir la operación indicada por \] **OperationalStatus** \[ 1. \]

El valor de **OperationalStatus** \[ 1 \] es uno de los siguientes valores.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <dt>**Creación de la**</dt> <dt>instantánea 32768</dt> </dl>                                 | Una instantánea está en proceso de creación para la máquina virtual.<br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <dt>**Aplicación de la instantánea**</dt> <dt>32769</dt> </dl>                                 | Una instantánea está en proceso de aplicarse a la máquina virtual.<br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <dt>**Eliminación de la instantánea**</dt> <dt>32770</dt> </dl>                                 | Una instantánea está en proceso de eliminación de la máquina virtual.<br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <dt>**Waiting to Start**</dt> <dt>32771</dt> </dl>                                     | La máquina virtual se inicia una vez transcurrido el retraso de inicio automático.<br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <dt>**Combinar discos**</dt> <dt>32772</dt> </dl>                                                 | Se combinan discos duros virtuales de instantáneas eliminadas previamente.<br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <dt>**Exportación de la máquina virtual**</dt> <dt>32773</dt> </dl> | La máquina virtual se está exportando.<br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <dt>**Migración de la máquina virtual**</dt> <dt>32774</dt> </dl> | La máquina virtual se está migrando en vivo de un equipo físico a otro.<br/>  |



 

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe cómo o por qué se dedica el sistema cuando la **matriz Dedicada** incluye el valor 2 (Otros). Esta propiedad se hereda de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre se establece en **Null.**

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado habilitado o deshabilitado de la máquina virtual cuando la **propiedad EnabledState** está establecida en 1 (Otros). Esta propiedad debe establecerse en **Null cuando** **EnabledState** es cualquier valor distinto de 1. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre se establece en **Null.**

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre se establece en **Null.**

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem), pero no se usa.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que indica cómo se puede acceder al propietario del sistema principal (por ejemplo, un número de teléfono o una dirección de correo electrónico). Esta propiedad se hereda del [**sistema \_ CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre se establece en **Null.**

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del propietario del sistema principal. Esta propiedad se hereda del [**sistema \_ CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre se establece en **Null.**

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe usarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ProcessID**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del proceso en el que se ejecuta esta máquina virtual. Este valor se puede usar para identificar de forma única la instancia de Vmwp.exe en el sistema que ejecuta la máquina virtual.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).**ReplicationHealth**")
</dt> </dl>

Estado de replicación de la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

Los valores posibles son:

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**Correcto** (1)


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

Especifica el modo de replicación de la máquina virtual. Este será uno de los siguientes valores.

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

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**Replicación de MsvmRelationship \_**](msvm-replicationrelationship.md).**ReplicationState**")
</dt> </dl>

Estado de replicación de la máquina virtual.

> [!Note]  
> Esta propiedad está en desuso a partir de Windows 8.1; en su lugar, use la propiedad del mismo nombre en la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) para obtener el valor de la relación principal o extendida.

 

Los valores posibles son:

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

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último estado solicitado o deseado para la máquina virtual tal como se pasa al método [**RequestStateChange,**](requeststatechange-msvm-computersystem.md) o 12 (No aplicable) si no hay ningún cambio de estado en curso. El estado real del elemento se representa mediante **EnabledState**. Esta propiedad se proporciona para comparar los últimos estados solicitados y los estados habilitados o deshabilitados actuales. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**ResetCapability**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)y siempre se establece en 1 (Otros).

</dd> <dt>

**Roles**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas que describen los roles que desempeña el sistema en el entorno de tecnología de la información. Esta propiedad se hereda del [**sistema \_ CIM**](/windows/desktop/CIMWin32Prov/cim-system)y siempre se establece en **Null.**

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**\_ MANAGEDSystemElement de CIM,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)pero no se usa.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **ArrayType** ("Indexed")
</dt> </dl>

Matriz que contiene cadenas que describen los valores de **matriz OperationalStatus** correspondientes. Por ejemplo, si 11 (En servicio) es el valor asignado a **OperationalStatus** \[ \] 0, **StatusDescriptions** 0 puede contener una explicación de por qué la máquina virtual está procesando \[ una \] solicitud. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**TimeOfLastConfigurationChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se modificó por última vez el archivo de configuración de la máquina virtual. El archivo de configuración se modifica durante determinadas operaciones de máquina virtual, así como cuando se agrega, modifica o quita cualquiera de las configuraciones de máquina virtual o dispositivo.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que cambió por última vez el estado habilitado del elemento. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el estado de destino al que se está transfiriendo la instancia. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement,**](/previous-versions//cc136818(v=vs.85))pero no se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

En la ilustración siguiente se muestran los **valores de EnabledState.**

![diagrama de estado de los valores enabledstate para Windows Server 2008 r2](images/msvm-computersystem-enabledstate-win2008r2.png)

Cuando cambia una propiedad de la clase **\_ ComputerSystem de Msvm,** el proveedor WMI indica un evento [**\_ \_ InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent) que describe los cambios. El estado anterior se encuentra en la **propiedad PreviousInstance** y el nuevo estado se encuentra en la **propiedad TargetInstance.** Este evento es asincrónico; en el momento en que se procesa el evento **\_ \_ InstanceModificationEvent,** es posible que la propiedad **TargetInstance** no refleje el estado actual.

El acceso a **la clase \_ ComputerSystem de Msvm** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

Consulte [Consulta de objetos de red.](querying-networking-objects.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> <dt>

[**\_\_InstanceModificationEvent**](/windows/desktop/WmiSdk/--instancemodificationevent)
</dt> <dt>

[**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)
</dt> <dt>

[**Msvm \_ ComputerSystem (V1)**](/previous-versions/windows/desktop/virtual/msvm-computersystem)
</dt> <dt>

[Clases de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

