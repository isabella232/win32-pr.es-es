---
description: Servicio para crear, aplicar y destruir instantáneas de máquinas virtuales.
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Msvm_VirtualSystemSnapshotService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be84d70dd9478012e747626a9a566464d7587789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907691"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a>MSVM \_ VirtualSystemSnapshotService (clase)

Servicio para crear, aplicar y destruir instantáneas de máquinas virtuales.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualSystemSnapshotService** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSVM \_ VirtualSystemSnapshotService** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></td>
<td style="text-align: left;">Aplica una instantánea de máquina virtual a la máquina virtual desde la que se creó.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></td>
<td style="text-align: left;">Borra el estado de guardado de una instantánea existente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></td>
<td style="text-align: left;">Convertir una instantánea del sistema virtual existente en un punto de referencia. La instantánea se elimina como un efecto secundario. Solo las instantáneas de recuperación se pueden convertir en puntos de referencia.<br/>
<blockquote>
[!Note]<br />
La compatibilidad con este método se agregó en Windows 10.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></td>
<td style="text-align: left;">Crea una instantánea de una máquina virtual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></td>
<td style="text-align: left;">Destruya una instantánea de máquina virtual existente. Este método puede, como efecto secundario, destruir otras instantáneas que dependen de la instantánea afectada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></td>
<td style="text-align: left;">Quita una instantánea existente, y todos sus elementos secundarios, de una máquina virtual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></td>
<td style="text-align: left;">Solicita un cambio de estado para el elemento.<br/>
<blockquote>
[!Note]<br />
La compatibilidad con este método se agregó en Windows 10.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><strong>StartService</strong></td>
<td style="text-align: left;">No se admite este método.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><strong>StopService</strong></td>
<td style="text-align: left;">No se admite este método.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualSystemSnapshotService** tiene estas propiedades.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** usado para iniciar un cambio de estado. Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual del objeto [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) . Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual. Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.

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

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "servicio de instantánea de sistema virtual de Hyper-V".

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
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de una instancia de. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ VirtualSystemSnapshotService".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio para crear, destruir y aplicar instantáneas de máquina virtual".

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

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).



| Value                                                                        | Significado            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | habilitado<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitado y deshabilitado de un elemento. También puede indicar las transiciones entre estos Estados solicitados. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).



| Value                                                                        | Significado            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | habilitado<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del elemento. Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes. Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).



| Value                                                                        | Significado                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | El estado de mantenimiento es normal.<br/> |



 

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

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en "vssnapsvc".

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
</dt> <dt>

Calificadores: **MaxLen** (256)
</dt> </dl>

Cualquier información sobre cómo se puede alcanzar el propietario principal del servicio (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.). Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
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

Último estado solicitado o deseado del elemento. El estado real del elemento se representa mediante **EnabledState**. Esta propiedad se proporciona para comparar el último estado solicitado y el actual para un elemento. Una instancia concreta de la [**clase \_ EnabledLogicalElement de CIM**](/previous-versions//cc136818(v=vs.85)) podría no admitir la propiedad **RequestedState** . Si esto ocurre, se usa el valor 12 (no aplicable). Esta propiedad se hereda de **\_ EnabledLogicalElement CIM** y siempre está establecida en 12 (no aplicable).



| Value                                                                         | Significado                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | No es aplicable.<br/> |



 

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el servicio se está ejecutando actualmente. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **true**.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (10)
</dt> </dl>

Un valor de cadena que indica si el servicio se inicia automáticamente por un sistema, un sistema operativo o se inicia solo después de la solicitud. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en **null**.

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

Cadenas que describen los distintos valores de la matriz **OperationalStatus** . Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "el servicio se está ejecutando normalmente".

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Nombre de la clase de creación del sistema de ámbito. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ ComputerSystem".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Nombre NetBIOS del sistema del equipo host. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

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



| Value                                                                                                                                                                                                                                                     | Significado                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Habilitado**</dt> <dt>2</dt> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deshabilitado**</dt> <dt>3</dt> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <dt>**Apagar**</dt> <dt>4</dt> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <dt>**Sin cambio**</dt> <dt>5</dt> </dl>                       | No hay ninguna transición en curso.<br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <dt>**Sin conexión**</dt> <dt>6</dt> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <dt>**Prueba**</dt> <dt>7</dt> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <dt>**Aplazar**</dt> <dt>8</dt> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> Modo <dt>**inactivo**</dt> <dt>9</dt> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <dt>**Reiniciar**</dt> <dt>10</dt> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <dt>**Restablecer**</dt> <dt>11</dt> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**No aplicable**</dt> <dt>12</dt> </dl>  | La implementación de no admite la representación de transiciones en curso.<br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt> **DMTF reservado**</dt> <dt>..</dt> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

