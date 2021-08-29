---
description: Representa la configuración de un recurso asignado que está fuera del ámbito de la clase CIM utilizada normalmente para representar el propio recurso.
ms.assetid: 6261bab9-aa51-479e-bd6a-43c4a9b294a6
title: CIM_ResourceAllocationSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationSettingData
- CIM_ResourceAllocationSettingData.ResourceType
- CIM_ResourceAllocationSettingData.OtherResourceType
- CIM_ResourceAllocationSettingData.ResourceSubType
- CIM_ResourceAllocationSettingData.PoolID
- CIM_ResourceAllocationSettingData.ConsumerVisibility
- CIM_ResourceAllocationSettingData.HostResource
- CIM_ResourceAllocationSettingData.AllocationUnits
- CIM_ResourceAllocationSettingData.VirtualQuantity
- CIM_ResourceAllocationSettingData.Reservation
- CIM_ResourceAllocationSettingData.Limit
- CIM_ResourceAllocationSettingData.Weight
- CIM_ResourceAllocationSettingData.AutomaticAllocation
- CIM_ResourceAllocationSettingData.AutomaticDeallocation
- CIM_ResourceAllocationSettingData.Parent
- CIM_ResourceAllocationSettingData.Connection
- CIM_ResourceAllocationSettingData.Address
- CIM_ResourceAllocationSettingData.MappingBehavior
- CIM_ResourceAllocationSettingData.AddressOnParent
- CIM_ResourceAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b84ebb7c95b192f5461fe0f4abb99a6f1d17ead74960ff8058629c81fd9a8771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981045"
---
# <a name="cim_resourceallocationsettingdata-class"></a>Clase \_ ResourceAllocationSettingData de CIM

Representa la configuración de un recurso asignado que está fuera del ámbito de la clase CIM utilizada normalmente para representar el propio recurso. Esta configuración incluye información específica de la asignación que puede no ser visible para el consumidor del recurso.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourceAllocationSettingData : CIM_SettingData
{
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
};
```

## <a name="members"></a>Miembros

La **clase \_ ResourceAllocationSettingData** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ResourceAllocationSettingData** de CIM tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La dirección del recurso, por ejemplo, la dirección MAC de un puerto Ethernet.

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección de este recurso del contexto del elemento primario. Esta propiedad se usa para describir una relación de controlador y el orden de los dispositivos en un controlador. Por ejemplo, si el elemento primario es un controlador PCI, esta propiedad especificaría la ranura PCI de este dispositivo secundario.

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**Reservation**", "**CIM \_ ResourceAllocationSettingData**.**Limit**"), **IsPUnit**
</dt> </dl>

Unidades de asignación utilizadas por las **propiedades Reservation** **y Limit.**

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**true** para asignar automáticamente el recurso; de lo contrario, **false**.

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**true** para desasignar automáticamente el recurso; de lo contrario, **false**.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz que indica los objetos conectados al recurso, como una red con nombre o un puerto de conmutador.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Visibilidad de los consumidores para el recurso asignado.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>

**Paso a través** (2)


</dt> <dd></dd> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>

**Virtualizado** (3)


</dt> <dd></dd> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>

**No representado** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (32767..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ConsumerVisibility**", "**\_ CIM ResourceAllocationSettingData**.**MappingBehavior**")
</dt> </dl>

Matriz que contiene la asignación de los recursos asignados. Cada valor distinto de NULL de esta propiedad debe tener el formato DE UN URI basado en RFC3986. Si se modela el recurso, el valor debe ser un URI WBEM.

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")
</dt> </dl>

Cantidad máxima de recursos que se concederá a la asignación. La propiedad **AllocationUnits** especifica el tipo de unidad de esta propiedad.

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se asigna el recurso a los recursos subyacentes.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**No compatible** (2)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

**Dedicado** (3)


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

**Afinidad flexible** (4)


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

**Afinidad fuerte** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (32767..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")
</dt> </dl>

Descripción del tipo de recurso cuando la **propiedad ResourceType** se establece en 1 (otro).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El elemento primario del recurso, por ejemplo, un controlador para la asignación actual.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolId**")
</dt> </dl>

Identificador del grupo de recursos que generó el recurso.

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**AllocationUnits**")
</dt> </dl>

Número de recursos que se garantiza que estarán disponibles para esta asignación. En los sistemas que admiten el exceso de compromiso de los recursos, este valor se usa normalmente para el control de admisión.

La propiedad **AllocationUnits** especifica el tipo de unidad de esta propiedad.

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**ResourceType**")
</dt> </dl>

Subtipo específico de implementación para este recurso. Por ejemplo, esto se puede usar para distinguir distintos modelos del mismo tipo de recurso.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**OtherResourceType**", "**CIM \_ ResourceAllocationSettingData**.**ResourceSubType**")
</dt> </dl>

Tipo de recurso representado por la configuración de asignación.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

**Sistema informático** (2)


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

**Procesador** (3)


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

**Memoria** (4)


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

**Controlador IDE** (5)


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

**HBA SCSI paralelo** (6)


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

**FC HBA** (7)


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

**HBA iSCSI** (8)


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

**IB HCA** (9)


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

**Adaptador Ethernet** (10)


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

**Otro adaptador de** red (11)


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

**Ranura de E/S** (12)


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

**Dispositivo de E/S** (13)


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

**Disquete** (14)


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

**Unidad de CD** (15)


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

**Unidad de DVD** (16)


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Unidad de disco** (17)


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

**Unidad de cinta** (18)


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

**Storage extensión** (19)


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

**Otro dispositivo de almacenamiento** (20)


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

**Puerto serie** (21)


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

**Puerto paralelo** (22)


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

**Controlador USB** (23)


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

**Controlador de gráficos** (24)


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

**IEEE 1394 controlador** (25)


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

**Unidad particionable** (26)


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

**Unidad base particionable** (27)


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

**Potencia** (28)


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

**Capacidad de refrigeración** (29)


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

**Puerto de conmutador Ethernet** (30)


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

**Disco lógico** (31)


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

**Storage volumen** (32)


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

**Conexión Ethernet** (33)


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Proveedor reservado** (0x8000.. 0xFFFF)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantityUnits**")
</dt> </dl>

Número de recursos presentados al consumidor del recurso.

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourceAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**
</dt> </dl>

Unidades usadas por la **propiedad VirtualQuantity.**

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Prioridad relativa para esta asignación en relación con otras asignaciones del mismo grupo de recursos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

