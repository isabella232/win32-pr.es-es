---
description: Representa el servicio de virtualización presente en un único sistema host.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0dab3dc9b530ca565e78ecc1f5a6e50a26bc3f630f5c60491b01c253e09aa97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147998"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a>Clase \_ VirtualSystemManagementService de Msvm

Representa el servicio de virtualización presente en un único sistema host. **Msvm \_ VirtualSystemManagementService** se usa para controlar la definición, modificación y eliminación de máquinas virtuales. También tiene métodos para realizar operaciones en máquinas virtuales, como la clonación, la instantánea y la importación o exportación de máquinas virtuales. Para recuperar información por máquina virtual, use [**Msvm \_ ComputerSystem**](msvm-computersystem.md).

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>Miembros

La **clase \_ VirtualSystemManagementService de Msvm** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase Msvm \_ VirtualSystemManagementService** tiene estos métodos.



| Método                                                                                                                 | Descripción                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | Agrega orígenes de arranque a una configuración del sistema virtual cuando se aplica a una configuración del sistema virtual de "estado".<br/>                                                                                                                             |
| [**AddFeatureSettings**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | Agrega la configuración de características Ethernet a la configuración de una conexión Ethernet de máquina virtual.<br/>                                                                                                                                           |
| [**AddFibreChannelChap**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | Agrega parámetros DH-CHAP a un puerto Canal de fibra sintético en una máquina virtual.<br/>                                                                                                                                                         |
| [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | Agrega la configuración del servicio invitado a una configuración del sistema virtual.<br/> Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden modificar los servicios invitados del sistema virtual activo.<br/>              |
| [**AddKvpItems**](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | Agrega pares clave-valor a una máquina virtual.<br/>                                                                                                                                                                                              |
| [**AddResourceSettings**](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | Agrega recursos a una configuración de máquina virtual.<br/>                                                                                                                                                                                      |
| [**AddSystemComponentSettings**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | Agrega valores genéricos a una configuración del sistema virtual.<br/>                                                                                                                                                                                |
| [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | Define un sistema virtual planeado.<br/> La entrada que no se especifica completamente se puede rellenar con valores predeterminados.<br/>                                                                                                              |
| [**DefineSystem**](definesystem-msvm-virtualsystemmanagementservice.md)                                               | Crea una nueva definición de máquina virtual.<br/>                                                                                                                                                                                               |
| [**DestroySystem**](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | Elimina una definición de máquina virtual existente.<br/>                                                                                                                                                                                         |
| [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | Diagnostica la conectividad de red de una máquina virtual en un Windows Network Virtualization Environment.<br/>                                                                                                                                             |
| [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | Exporta una máquina virtual, o una instantánea de una máquina virtual, a un archivo.<br/>                                                                                                                                                               |
| [**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | Devuelve una cadena de mensaje de error con formato para la matriz especificada de instancias de [**\_ error de Msvm**](msvm-error.md) insertadas.<br/>                                                                                                               |
| [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | Genera un conjunto de nombres de puertos world wide (WWPN).<br/>                                                                                                                                                                                       |
| [**GetCurrentWwpnFromGenerator**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | Proporciona la capacidad de obtener una vista previa del nombre de puerto world wide (WWPN) actual sin que el WWPN esté reservado.<br/>                                                                                                                                |
| [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | Devuelve información de resumen de la máquina virtual para los archivos de definición de máquina virtual especificados.<br/>                                                                                                                                         |
| [**GetSizeOfSystemFiles**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | Recupera el tamaño total de los archivos del sistema de la máquina virtual.<br/>                                                                                                                                                                        |
| [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | Devuelve información de resumen de la máquina virtual.<br/>                                                                                                                                                                                            |
| [**GetVirtualSystemThumbnailImage**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | Recupera una imagen en miniatura de una máquina virtual existente.<br/>                                                                                                                                                                             |
| [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | Busca en la carpeta especificada los archivos de definición de instantánea asociados al sistema de equipo planeado especificado y crea una nueva instantánea en el sistema del equipo planeado para cada archivo de definición asociado en esta ubicación.<br/> |
| [**ImportSystemDefinition**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | Crea un nuevo sistema informático planeado basado en la definición de máquina virtual especificada.<br/>                                                                                                                                                |
| [**ModifyDiskMergeSettings**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | Modifica los datos de configuración de mezcla de disco.<br/>                                                                                                                                                                                                   |
| [**ModifyFeatureSettings**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | Modifica la configuración de características actual de una conexión Ethernet de máquina virtual.<br/>                                                                                                                                                         |
| [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | Modifica la configuración del servicio de invitado.<br/> Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden modificar los servicios invitados del sistema virtual activo.<br/>                                            |
| [**ModifyKvpItems**](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | Modifica los pares clave-valor existentes en una máquina virtual.<br/>                                                                                                                                                                                 |
| [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | Modifica la configuración de recursos virtuales.<br/>                                                                                                                                                                                                     |
| [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | Modifica los datos de configuración del servicio.<br/>                                                                                                                                                                                                    |
| [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | Modifica la configuración de componentes genéricos del sistema.<br/>                                                                                                                                                                                             |
| [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | Modifica la configuración de la máquina virtual.<br/>                                                                                                                                                                                                      |
| [**RealizePlannedSystem**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | Valida la configuración de una máquina virtual planeada y la convierte en una máquina virtual realizada.<br/>                                                                                                                                 |
| [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | Quita la configuración de recursos virtuales de una configuración del sistema virtual.<br/> Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden quitar los recursos del sistema virtual activo.<br/>            |
| [**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | Quita la configuración de características de una conexión Ethernet de máquina virtual.<br/>                                                                                                                                                                    |
| [**RemoveFibreChannelChap**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | Quita los parámetros DH-CHAP de un puerto Canal de fibra sintético en una máquina virtual.<br/>                                                                                                                                                    |
| [**RemoveGuestServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | Quita la configuración del servicio invitado de una configuración del sistema virtual.<br/> Cuando se aplica a partes de una configuración del sistema virtual "actual", como efecto secundario se pueden modificar los servicios invitados del sistema virtual activo.<br/>         |
| [**RemoveKvpItems**](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | Quita los pares clave-valor existentes de una máquina virtual.<br/>                                                                                                                                                                                |
| [**RemoveResourceSettings**](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | Quita la configuración de recursos virtuales de una configuración de máquina virtual.<br/>                                                                                                                                                                 |
| [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | Quita la configuración de componentes genéricos de una configuración del sistema virtual.<br/>                                                                                                                                                                 |
| [**RequestStateChange**](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | No se admite este método.<br/>                                                                                                                                                                                                           |
| [**SetGuestNetworkAdapterConfiguration**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | Configura los adaptadores de red dentro del sistema operativo invitado.<br/>                                                                                                                                                                      |
| [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | Establece los datos de configuración iniciales de la máquina virtual.<br/>                                                                                                                                                                                         |
| [**StartService**](msvm-virtualsystemmanagementservice-startservice.md)                                               | No se admite este método.<br/>                                                                                                                                                                                                           |
| [**StopService**](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | No se admite este método.<br/>                                                                                                                                                                                                           |
| [**TestNetworkConnection**](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | Prueba la conectividad de red de una máquina virtual en un entorno Windows Virtualización de red.<br/>                                                                                                                                                 |
| [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | Actualiza el sistema virtual.<br/> Cuando se aplica a la configuración del sistema de una configuración del sistema virtual "actual".<br/>                                                                                                                 |
| [**ValidatePlannedSystem**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | Valida el sistema planeado especificado.<br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a>Propiedades

La **clase \_ VirtualSystemManagementService de Msvm** tiene estas propiedades.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los valores posibles para el *parámetro RequestedState* del **método RequestStateChange.** Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre se establece en **Null.**

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Servicio de administración de sistemas virtuales de Hyper-V".

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la capacidad de la instrumentación para comunicarse con el elemento administrado subyacente. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000.. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de una instancia de . Esta propiedad se hereda del [**servicio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "Msvm \_ VirtualSystemManagementService".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Servicio para crear, manipular y administrar máquinas virtuales".

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la **propiedad PrimaryStatus con** detalles de estado adicionales. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Sin información adicional** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Estresado** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad de compatibilidad con error** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000.. )
</dt> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Servicio de administración de sistemas virtuales de Hyper-V".

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre se establece en 2 (Habilitado).



| Value                                                                        | Significado            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | habilitado<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitados y deshabilitados de un elemento. Esta propiedad también puede indicar las transiciones entre estos estados solicitados. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre se establece en 2 (Habilitado).



| Value                                                                        | Significado            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | habilitado<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes. Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento es completamente no funcional. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en 5 (correcto).



| Value                                                                        | Significado                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | El estado de mantenimiento es normal.<br/> |



 

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración de la máquina virtual. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

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

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda de [**Cim \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en "vmms".

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado actual para la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la **propiedad EnabledState.** Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A partir** de (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detener** (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Contrabando** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantáneas** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Apagar** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En prueba** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados actuales del objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de matriz siempre se establece en 2 (correcto).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el estado habilitado o deshabilitado del elemento cuando la **propiedad EnabledState** está establecida en 1 ("Other"). Esta propiedad debe establecerse en **Null cuando** **EnabledState** es cualquier valor distinto de 1. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre se establece en **Null.**

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** ( 256 )
</dt> </dl>

Cualquier información sobre cómo se puede acceder al propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, entre otros). Esta propiedad se hereda del [**servicio \_ CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **Null.**

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** ( 64 )
</dt> </dl>

Nombre del propietario principal del servicio, si se define uno. El propietario principal es el contacto inicial de soporte técnico para el servicio. Esta propiedad se hereda del [**servicio \_ CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **Null.**

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe usarse junto con la propiedad **DetailedStatus** para proporcionar un estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**Aceptar** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000.. )
</dt> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último estado solicitado o deseado para el elemento. El estado real del elemento se representa mediante **EnabledState**. Esta propiedad se proporciona para comparar los últimos estados solicitados y actuales de un elemento. Es posible que una instancia determinada [**de la clase CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) no admita la **propiedad RequestedState.** Si esto ocurre, se usa el valor 12 ("No aplicable"). Esta propiedad se hereda de **CIM \_ EnabledLogicalElement** y siempre se establece en 12 (no aplicable).



| Value                                                                         | Significado                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | No es aplicable.<br/> |



 

</dd> <dt>

**Comenzó**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servicio se está ejecutando actualmente. Esta propiedad se hereda del servicio [**\_ CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **True.**

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** ( 10 )
</dt> </dl>

Valor de cadena que indica si un sistema, un sistema operativo o un sistema operativo inician automáticamente el servicio solo a petición. Esta propiedad se hereda del [**servicio \_ CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **Null.**

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ManagedSystemElement,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)pero no se usa.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadenas que describen los distintos **valores de la matriz OperationalStatus.** Esta propiedad se hereda de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de matriz siempre se establece en "El servicio se ejecuta con normalidad".

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Nombre de clase de creación del sistema de ámbito. Esta propiedad se hereda del servicio [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "Msvm \_ ComputerSystem".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Key**, **MaxLen** ( 256 )
</dt> </dl>

Nombre NetBIOS del sistema del equipo host. Esta propiedad se hereda del [**servicio CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha u hora en que cambió por última vez el estado habilitado del elemento. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el estado de destino al que la instancia está transfiriendo. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre se establece en **Null.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a la **clase \_ VirtualSystemManagementService de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))
</dt> <dt>

[Clases de administración de sistemas virtuales](virtual-system-management-classes.md)
</dt> </dl>

 

