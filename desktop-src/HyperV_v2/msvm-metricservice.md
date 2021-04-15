---
description: Proporciona la capacidad de administrar las métricas.
ms.assetid: 39dee432-995d-472a-84c3-eede95dccb43
title: Msvm_MetricService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService
- Msvm_MetricService.InstanceID
- Msvm_MetricService.Caption
- Msvm_MetricService.Description
- Msvm_MetricService.ElementName
- Msvm_MetricService.InstallDate
- Msvm_MetricService.OperationalStatus
- Msvm_MetricService.StatusDescriptions
- Msvm_MetricService.Status
- Msvm_MetricService.HealthState
- Msvm_MetricService.CommunicationStatus
- Msvm_MetricService.DetailedStatus
- Msvm_MetricService.OperatingStatus
- Msvm_MetricService.PrimaryStatus
- Msvm_MetricService.EnabledState
- Msvm_MetricService.OtherEnabledState
- Msvm_MetricService.RequestedState
- Msvm_MetricService.EnabledDefault
- Msvm_MetricService.TimeOfLastStateChange
- Msvm_MetricService.AvailableRequestedStates
- Msvm_MetricService.TransitioningToState
- Msvm_MetricService.SystemCreationClassName
- Msvm_MetricService.SystemName
- Msvm_MetricService.Name
- Msvm_MetricService.CreationClassName
- Msvm_MetricService.PrimaryOwnerName
- Msvm_MetricService.PrimaryOwnerContact
- Msvm_MetricService.StartMode
- Msvm_MetricService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c4117e3adf3db5a2b0073615ae999b9f85bb9b18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688564"
---
# <a name="msvm_metricservice-class"></a>MSVM \_ MetricService (clase)

Proporciona la capacidad de administrar las métricas.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricService : CIM_MetricService
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service";
  string   Description = "Provides Hyper-V Metric WMI management";
  string   ElementName = "Hyper-V Metric Service";
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   Name = "metricsvc";
  string   CreationClassName = "Msvm_MetricService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ MetricService** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSVM \_ MetricService** tiene estos métodos.



| Método                                                                    | Descripción                                                                             |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**ControlMetrics**](controlmetrics-msvm-metricservice.md)               | Se utiliza para controlar la colección de métricas de un elemento o elementos administrados.<br/> |
| [**ControlMetricsByClass**](msvm-metricservice-controlmetricsbyclass.md) | Controla las métricas por clase.<br/>                                               |
| [**ControlSampleTimes**](msvm-metricservice-controlsampletimes.md)       | Establece las horas de muestra del control.<br/>                                               |
| [**GetMetricValues**](msvm-metricservice-getmetricvalues.md)             | Recupera los valores de la métrica.<br/>                                                 |
| [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) | Modifica los datos de configuración para el servicio.<br/>                                   |
| [**RequestStateChange**](msvm-metricservice-requeststatechange.md)       | Solicita un cambio de estado.<br/>                                                     |
| [**ShowMetrics**](msvm-metricservice-showmetrics.md)                     | Muestra las métricas especificadas.<br/>                                                 |
| [**ShowMetricsByClass**](msvm-metricservice-showmetricsbyclass.md)       | Muestra las métricas por clase.<br/>                                                  |
| [**StartService**](msvm-metricservice-startservice.md)                   | inicia el servicio.<br/>                                                          |
| [**StopService**](msvm-metricservice-stopservice.md)                     | detiene el servicio.<br/>                                                           |



 

### <a name="properties"></a>Propiedades

La clase **MSVM \_ MetricService** tiene estas propiedades.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** . Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de métricas de Hyper-V".

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

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de una instancia de. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ MetricService".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "proporciona administración WMI de métricas de Hyper-V".

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

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de métricas de Hyper-V".

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitado y deshabilitado de un elemento. Esta propiedad también puede indicar las transiciones entre estos Estados solicitados. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes. Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).

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

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "metricsvc".

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

Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro). Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Valor que proporciona información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.). Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del propietario principal del servicio, si se ha definido uno. El propietario principal es el contacto de soporte inicial para el servicio. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.

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

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último estado solicitado o deseado del elemento. El estado real del elemento se representa mediante **EnabledState**. Esta propiedad se proporciona para comparar los Estados actual y habilitado o deshabilitado en último lugar. Una instancia concreta de [**\_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir el método **RequestStateChange** . Si esto ocurre, se usa el valor 12 (no aplicable). Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servicio se está ejecutando actualmente. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en "OK".

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadenas que describen los distintos valores de la matriz **OperationalStatus** . Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y las cadenas siempre se establecen en "OK".

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase de creación del sistema de ámbito. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del sistema del equipo host. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha u hora en que se cambió por última vez el estado habilitado del elemento. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el estado de destino al que la instancia está cambiando. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

