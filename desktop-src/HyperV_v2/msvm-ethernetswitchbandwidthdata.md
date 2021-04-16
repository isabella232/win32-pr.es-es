---
description: Representa el estado del recurso de ancho de banda del conmutador.
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Msvm_EthernetSwitchBandwidthData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d238b8ddc40506a3eae8a6c7c089de2ebd87db5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686742"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a>MSVM \_ EthernetSwitchBandwidthData (clase)

Representa el estado del recurso de ancho de banda del conmutador.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ EthernetSwitchBandwidthData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ EthernetSwitchBandwidthData** tiene estas propiedades.

<dl> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Ancho de banda máximo disponible en el conmutador.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de esta instancia.

</dd> <dt>

**DefaultFlowReservation**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Ancho de banda absoluto actual reservado en el conmutador para el flujo predeterminado.

</dd> <dt>

**DefaultFlowReservationPercentage**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Porcentaje actual de ancho de banda reservado en el conmutador para el flujo predeterminado.

</dd> <dt>

**DefaultFlowWeight**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Peso actual del flujo predeterminado en el modificador.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

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

Calificadores: **clave**, **invalidación**, **MaxLen** (256)
</dt> </dl>

Nombre único del recurso.

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Ancho de banda actual reservado en el conmutador.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Nombre de la clase de creación del sistema de hospedaje. Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

El nombre del conmutador virtual al que está enlazada la instancia de recurso asociada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

