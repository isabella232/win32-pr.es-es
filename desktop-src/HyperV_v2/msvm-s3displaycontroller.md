---
description: Representa el estado del controlador S3 emulado que se encuentra en cada configuración de máquina virtual.
ms.assetid: 194E0195-1AFF-4298-8000-2249495818C2
title: Clase Msvm_S3DisplayController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_S3DisplayController
- Msvm_S3DisplayController.SetPowerState
- Msvm_S3DisplayController.EnableDevice
- Msvm_S3DisplayController.OnlineDevice
- Msvm_S3DisplayController.QuiesceDevice
- Msvm_S3DisplayController.SaveProperties
- Msvm_S3DisplayController.RestoreProperties
- Msvm_S3DisplayController.InstanceID
- Msvm_S3DisplayController.Caption
- Msvm_S3DisplayController.Description
- Msvm_S3DisplayController.ElementName
- Msvm_S3DisplayController.InstallDate
- Msvm_S3DisplayController.Name
- Msvm_S3DisplayController.OperationalStatus
- Msvm_S3DisplayController.StatusDescriptions
- Msvm_S3DisplayController.Status
- Msvm_S3DisplayController.HealthState
- Msvm_S3DisplayController.CommunicationStatus
- Msvm_S3DisplayController.DetailedStatus
- Msvm_S3DisplayController.OperatingStatus
- Msvm_S3DisplayController.PrimaryStatus
- Msvm_S3DisplayController.EnabledState
- Msvm_S3DisplayController.OtherEnabledState
- Msvm_S3DisplayController.RequestedState
- Msvm_S3DisplayController.EnabledDefault
- Msvm_S3DisplayController.TimeOfLastStateChange
- Msvm_S3DisplayController.AvailableRequestedStates
- Msvm_S3DisplayController.TransitioningToState
- Msvm_S3DisplayController.SystemCreationClassName
- Msvm_S3DisplayController.SystemName
- Msvm_S3DisplayController.CreationClassName
- Msvm_S3DisplayController.DeviceID
- Msvm_S3DisplayController.PowerManagementSupported
- Msvm_S3DisplayController.PowerManagementCapabilities
- Msvm_S3DisplayController.Availability
- Msvm_S3DisplayController.StatusInfo
- Msvm_S3DisplayController.LastErrorCode
- Msvm_S3DisplayController.ErrorDescription
- Msvm_S3DisplayController.ErrorCleared
- Msvm_S3DisplayController.OtherIdentifyingInfo
- Msvm_S3DisplayController.PowerOnHours
- Msvm_S3DisplayController.TotalPowerOnHours
- Msvm_S3DisplayController.IdentifyingDescriptions
- Msvm_S3DisplayController.AdditionalAvailability
- Msvm_S3DisplayController.MaxQuiesceTime
- Msvm_S3DisplayController.TimeOfLastReset
- Msvm_S3DisplayController.ProtocolSupported
- Msvm_S3DisplayController.MaxNumberControlled
- Msvm_S3DisplayController.ProtocolDescription
- Msvm_S3DisplayController.VideoProcessor
- Msvm_S3DisplayController.VideoMemoryType
- Msvm_S3DisplayController.OtherVideoMemoryType
- Msvm_S3DisplayController.NumberOfVideoPages
- Msvm_S3DisplayController.MaxMemorySupported
- Msvm_S3DisplayController.AcceleratorCapabilities
- Msvm_S3DisplayController.CapabilityDescriptions
- Msvm_S3DisplayController.OtherVideoArchitecture
- Msvm_S3DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a4195ff8947bf92d8e4af3a95df320ed950ab21e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156944"
---
# <a name="msvm_s3displaycontroller-class"></a>MSVM \_ S3DisplayController (clase)

Representa el estado del controlador S3 emulado que se encuentra en cada configuración de máquina virtual. Solo un controlador de pantalla puede estar activo en una máquina virtual en cualquier momento.

> [!Note]  
> Esta clase solo se aplica a las máquinas virtuales de generación 1.

 

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_S3DisplayController : CIM_DisplayController
{
  string   InstanceID;
  string   Caption = "Display Controller";
  string   Description = "Microsoft Emulated Display Controller";
  string   ElementName = "Display Controller";
  datetime InstallDate;
  string   Name = "Display Controller";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 3;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  uint16   CreationClassName = "Msvm_S3DisplayController";
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability = 6;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[] = {6};
  uint64   MaxQuiesceTime;
  datetime TimeOfLastReset;
  uint16   ProtocolSupported = 1;
  uint32   MaxNumberControlled = 1;
  string   ProtocolDescription = "Video";
  string   VideoProcessor = "Virtual S3 Video Processor";
  uint16   VideoMemoryType = 2;
  string   OtherVideoMemoryType;
  uint32   NumberOfVideoPages = 32768;
  uint32   MaxMemorySupported = 134217728;
  uint16   AcceleratorCapabilities[] = { 2 };
  string   CapabilityDescriptions[] = { "Graphics Accelerator" };
  string   OtherVideoArchitecture;
  uint16   VideoArchitecture;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ S3DisplayController** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSVM \_ S3DisplayController** tiene estos métodos.



| Método                                                                    | Descripción                              |
|:--------------------------------------------------------------------------|:-----------------------------------------|
| **EnableDevice**                                                          | No se admite este método.<br/> |
| **OnlineDevice**                                                          | No se admite este método.<br/> |
| **QuiesceDevice**                                                         | No se admite este método.<br/> |
| [**RequestStateChange**](msvm-s3displaycontroller-requeststatechange.md) | Solicita un cambio de estado. <br/>     |
| [**Reset**](msvm-s3displaycontroller-reset.md)                           | Restablece el dispositivo virtual.<br/>    |
| **RestoreProperties**                                                     | No se admite este método.<br/> |
| **SaveProperties**                                                        | No se admite este método.<br/> |
| **SetPowerState**                                                         | No se admite este método.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **MSVM \_ S3DisplayController** tiene estas propiedades.

<dl> <dt>

**AcceleratorCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Las capacidades de gráficos y 3D del controlador de pantalla. Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

</dd> <dt>

**AdditionalAvailability**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cualquier disponibilidad adicional y estado del dispositivo. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**Disponibilidad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La disponibilidad y el estado principales del dispositivo. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).



| Value                                                                        | Significado                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>6</dt> </dl> | No es aplicable<br/> |



 

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** . Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una matriz de cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de las características del acelerador de vídeo indicadas en la matriz **AcceleratorCapabilities** . Cada entrada de esta matriz está relacionada con la entrada de la matriz **AcceleratorCapabilities** que se encuentra en el mismo índice. Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

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

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000... )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de una instancia de. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en "MSVM \_ S3DisplayController".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000... )
</dt> </dl>

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).



| Value                                                                        | Significado             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <dt>2</dt> </dl> | habilitado<br/>  |
| <dl> <dt>3</dt> </dl> | Disabled<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitado y deshabilitado de un elemento. También puede indicar las transiciones entre estos Estados solicitados. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada) o 3 (deshabilitada).



| Value                                                                        | Significado             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <dt>2</dt> </dl> | habilitado<br/>  |
| <dl> <dt>3</dt> </dl> | Disabled<br/> |



 

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el error comunicado en **LastErrorCode** se ha borrado. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes. Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).



| Value                                                                        | Significado       |
|------------------------------------------------------------------------------|---------------|
| <dl> <dt>5</dt> </dl> | Aceptar<br/> |



 

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** . Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.

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

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último código de error indicado por el dispositivo lógico. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.

</dd> <dt>

**MaxMemorySupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad máxima de memoria admitida, en bytes. Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

</dd> <dt>

**MaxNumberControlled**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número máximo de entidades directamente direccionables admitidas por este controlador. Se debe utilizar un valor de 0 si el número es desconocido o ilimitado. Protocolo usado por el controlador para tener acceso a los dispositivos controlados. Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).

</dd> <dt>

**MaxQuiesceTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad está en desuso. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NumberOfVideoPages**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible. Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** . Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)
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

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000... )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados actuales del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro). Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)y siempre se establece en **null**.

</dd> <dt>

**OtherVideoArchitecture**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el tipo de arquitectura de vídeo cuando la propiedad **videoarchitecture** es 1 ("Other"). Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

</dd> <dt>

**OtherVideoMemoryType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de memoria de vídeo cuando la propiedad **VideoMemoryType** de la instancia es 1 (otra). Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Las capacidades de administración de energía del dispositivo. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el dispositivo puede administrarse con energía. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.

</dd> <dt>

**PowerOnHours**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000... )
</dt> </dl>

</dd> <dt>

**ProtocolDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que proporciona más información relacionada con el protocolo compatible con el controlador. Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).

</dd> <dt>

**ProtocolSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Protocolo usado por el controlador para tener acceso a los dispositivos controlados. Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último estado solicitado o deseado del elemento. El estado real del elemento se representa mediante **EnabledState**. Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).



| Value                                                                         | Significado                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>12</dt> </dl> | No es aplicable<br/> |



 

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadenas que describen los distintos valores de la matriz **OperationalStatus** . Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del dispositivo lógico. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase de creación del sistema de ámbito. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único de la máquina virtual de ámbito. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La última vez que se encendió la máquina virtual. Esta propiedad se hereda del [**\_ controlador CIM**](/windows/desktop/CIMWin32Prov/cim-controller).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha u hora en que se cambió por última vez el estado habilitado del elemento. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TotalPowerOnHours**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número total de horas que se ha alimentado este dispositivo. Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el estado de destino al que la instancia está cambiando. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.

</dd> <dt>

**Videoarquitectura**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la arquitectura de vídeo del controlador de pantalla utilizada para generar la señal de vídeo. Normalmente, un procesador de vídeo dedicado genera la señal de vídeo de acuerdo con la arquitectura especificada. Es un indicador de la capacidad de resolución máxima del controlador de pantalla. Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="CGA"></span><span id="cga"></span>**CGA** (2)
</dt> <dt>

<span id="EGA"></span><span id="ega"></span>**EGA** (3)
</dt> <dt>

<span id="VGA"></span><span id="vga"></span>**VGA** (4)
</dt> <dt>

<span id="SVGA"></span><span id="svga"></span>**SVGA** (5)
</dt> <dt>

<span id="MDA"></span><span id="mda"></span>**MDA** (6)
</dt> <dt>

<span id="HGC"></span><span id="hgc"></span>**HGC** (7)
</dt> <dt>

<span id="MCGA"></span><span id="mcga"></span>**MCGA** (8)
</dt> <dt>

<span id="8514A"></span><span id="8514a"></span>**8514A** (9)
</dt> <dt>

<span id="XGA"></span><span id="xga"></span>**XGA** (10)
</dt> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>**Búfer de trama lineal** (11)
</dt> <dt>

<span id="PC-98"></span><span id="pc-98"></span>**PC-98** (160)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000... )
</dt> </dl>

</dd> <dt>

**VideoMemoryType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de memoria de vídeo. Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

</dd> <dt>

**Videoprocesador**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el procesador o controlador de vídeo. Esta propiedad se hereda de [**\_ DisplayController CIM**](/previous-versions//cc136810(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ S3DisplayController** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_DISPLAYCONTROLLER CIM**](cim-displaycontroller.md)
</dt> <dt>

[**\_DISPLAYCONTROLLER CIM**](/previous-versions//cc136810(v=vs.85))
</dt> <dt>

[Clases de vídeo](video-classes.md)
</dt> </dl>

 

