---
description: Representa el servicio de migración del sistema virtual. Se usa para migrar un sistema virtual o para migrar el almacenamiento de un sistema virtual de una plataforma de virtualización a otra.
ms.assetid: af25e405-4498-40a8-ba8e-4b3873c56097
title: Msvm_VirtualSystemMigrationService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService
- Msvm_VirtualSystemMigrationService.InstanceID
- Msvm_VirtualSystemMigrationService.Caption
- Msvm_VirtualSystemMigrationService.Description
- Msvm_VirtualSystemMigrationService.ElementName
- Msvm_VirtualSystemMigrationService.InstallDate
- Msvm_VirtualSystemMigrationService.OperationalStatus
- Msvm_VirtualSystemMigrationService.StatusDescriptions
- Msvm_VirtualSystemMigrationService.Status
- Msvm_VirtualSystemMigrationService.HealthState
- Msvm_VirtualSystemMigrationService.CommunicationStatus
- Msvm_VirtualSystemMigrationService.DetailedStatus
- Msvm_VirtualSystemMigrationService.OperatingStatus
- Msvm_VirtualSystemMigrationService.PrimaryStatus
- Msvm_VirtualSystemMigrationService.EnabledState
- Msvm_VirtualSystemMigrationService.OtherEnabledState
- Msvm_VirtualSystemMigrationService.RequestedState
- Msvm_VirtualSystemMigrationService.EnabledDefault
- Msvm_VirtualSystemMigrationService.TimeOfLastStateChange
- Msvm_VirtualSystemMigrationService.AvailableRequestedStates
- Msvm_VirtualSystemMigrationService.TransitioningToState
- Msvm_VirtualSystemMigrationService.SystemCreationClassName
- Msvm_VirtualSystemMigrationService.SystemName
- Msvm_VirtualSystemMigrationService.Name
- Msvm_VirtualSystemMigrationService.CreationClassName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerName
- Msvm_VirtualSystemMigrationService.PrimaryOwnerContact
- Msvm_VirtualSystemMigrationService.StartMode
- Msvm_VirtualSystemMigrationService.Started
- Msvm_VirtualSystemMigrationService.ActiveVirtualSystemMigrationCount
- Msvm_VirtualSystemMigrationService.ActiveStorageMigrationCount
- Msvm_VirtualSystemMigrationService.MigrationServiceListenerIPAddressList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1e80cb12e6e6767b49670a1aff68c9791f224068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808767"
---
# <a name="msvm_virtualsystemmigrationservice-class"></a>MSVM \_ VirtualSystemMigrationService (clase)

Representa el servicio de migración del sistema virtual. Se usa para migrar un sistema virtual o para migrar el almacenamiento de un sistema virtual de una plataforma de virtualización a otra.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationService : CIM_VirtualSystemMigrationService
{
  string   InstanceID;
  string   Caption = "Hyper-V Migration Service";
  string   Description = "Hyper-V Migration Service";
  string   ElementName = "Hyper-V Migration Service";
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
  string   Name = "migrationwmi";
  string   CreationClassName = "Msvm_VirtualSystemMigrationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started;
  uint32   ActiveVirtualSystemMigrationCount;
  uint32   ActiveStorageMigrationCount;
  string   MigrationServiceListenerIPAddressList[];
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualSystemMigrationService** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSVM \_ VirtualSystemMigrationService** tiene estos métodos.



| Método                                                                                                                  | Descripción                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddNetworkSettings**](addnetworksettings-msvm-virtualsystemmigrationservice.md)                                     | Agrega subredes de red de migración para el servicio de migración del sistema virtual.<br/>                                                                                          |
| [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                 | Comprueba la información de compatibilidad para la compatibilidad con el sistema del equipo host.<br/>                                                                          |
| [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md)             | Método para migrar un sistema virtual o el almacenamiento de un sistema virtual a un host de destino especificado por un nombre de host.<br/>                                              |
| [**CheckVirtualSystemIsMigratableToHost**](checkvirtualsystemismigratabletohost-msvm-virtualsystemmigrationservice.md) | Determina si el sistema virtual especificado se puede migrar a un host de destino especificado por un nombre de red o una dirección IP.<br/>                                       |
| [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md)                     | Genera un BLOB opaco de datos que contiene información de compatibilidad del sistema especificado.<br/>                                                                |
| [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md)               | Obtiene vectores de compatibilidad para una máquina virtual o un host.<br/> **Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.<br/> |
| [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)                     | Migra un sistema virtual o el almacenamiento de un sistema virtual a un host de destino especificado por un nombre de host.<br/>                                                       |
| [**MigrateVirtualSystemToSystem**](migratevirtualsystemtosystem-msvm-virtualsystemmigrationservice.md)                 | Mueve, migra o reubica un sistema virtual en un sistema de destino.<br/>                                                                                                |
| [**ModifyNetworkSettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)                               | Modifica las subredes de la red de migración del servicio de migración del sistema virtual.<br/>                                                                                       |
| [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md)                               | Modifica los datos de configuración para el servicio de migración.<br/>                                                                                                              |
| [**RemoveNetworkSettings**](removenetworksettings-msvm-virtualsystemmigrationservice.md)                               | Quita las subredes de la red de migración del servicio de migración del sistema virtual.<br/>                                                                                      |
| [**RequestStateChange**](msvm-virtualsystemmigrationservice-requeststatechange.md)                                     | Solicita un cambio de estado<br/>                                                                                                                                           |
| [**StartService**](msvm-virtualsystemmigrationservice-startservice.md)                                                 | inicia el servicio.<br/>                                                                                                                                               |
| [**StopService**](msvm-virtualsystemmigrationservice-stopservice.md)                                                   | detiene el servicio.<br/>                                                                                                                                                |



 

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualSystemMigrationService** tiene estas propiedades.

<dl> <dt>

**ActiveStorageMigrationCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de migraciones de almacenamiento actuales en curso.

</dd> <dt>

**ActiveVirtualSystemMigrationCount**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de migraciones actuales del sistema virtual en curso.

</dd> <dt>

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

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de migración de Hyper-V".

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

Nombre de la clase o subclase utilizada en la creación de una instancia de. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "MSVM \_ VirtualSystemMigrationService".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de migración de Hyper-V".

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

Nombre para mostrar del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "servicio de migración de Hyper-V".

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

**MigrationServiceListenerIPAddressList**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La lista de direcciones IP de host que se pueden usar para la migración del sistema virtual.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)y siempre se establece en "migrationwmi".

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



 

