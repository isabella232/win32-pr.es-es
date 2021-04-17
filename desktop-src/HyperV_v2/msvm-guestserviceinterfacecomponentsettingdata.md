---
description: Representa el estado configurado del componente de la interfaz de servicio de invitado.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Msvm_GuestServiceInterfaceComponentSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666335"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a>MSVM \_ GuestServiceInterfaceComponentSettingData (clase)

Representa el estado configurado del componente de la interfaz de servicio de invitado. Esta clase se deriva de la [**clase \_ ResourceAllocationSettingData de CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) .

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
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
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ GuestServiceInterfaceComponentSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ GuestServiceInterfaceComponentSettingData** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del recurso. Por ejemplo, la dirección MAC de un puerto Ethernet.

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica las unidades de asignación utilizadas por las propiedades de reserva y límite. Por ejemplo, si ResourceType = processor, AllocationUnits se puede establecer en MHz. Cuando ResourceType = Memory, AllocationUnits se puede establecer en MB

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica si el recurso se asignará automáticamente. Por ejemplo, si se establece en true, cuando se enciende el sistema de equipo virtual de consumo, se asignará este recurso. Un valor de False indica que el recurso debe asignarse explícitamente. Por ejemplo, la configuración puede representar un medio extraíble (es decir, un CDROM o disquete) en el momento en que se enciende el tiempo, el medio no está presente. Se requiere una operación explícita para asignar el recurso.

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica si el recurso se desasignará automáticamente. Por ejemplo, cuando se establece en true, cuando el sistema de equipo virtual de consumo está apagado, se desasignará este recurso. Cuando se establece en false, el recurso permanecerá asignado y debe desasignarse explícitamente.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento al que está conectado este recurso. Por ejemplo, una red con nombre o un puerto de conmutador.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la visibilidad de los consumidores para el recurso asignado.



| Value                                                                                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                                            | Desconocido.<br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <dt>**Paso a través**</dt> <dt>2</dt> </dl>                | El recurso de host o subyacente se utiliza y pasa al consumidor, posiblemente mediante el uso de particiones. Al menos un elemento debe estar presente en la propiedad DeviceID.<br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <dt>**Virtualizado**</dt> <dt>3</dt> </dl>                            | El recurso está virtualizado y no se puede asignar directamente a un recurso de host o subyacente. Algunas implementaciones pueden admitir la asignación específica de recursos virtualizados, en cuyo caso los recursos del host se exponen mediante la propiedad DeviceID.<br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <dt>**No se representa**</dt> <dt>4</dt> </dl>            | Una representación del recurso no existe en el contexto del consumidor del recurso.<br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>..</dt> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> El <dt>**proveedor ha reservado**</dt> <dt>32767.. 65535</dt> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

**DefaultEnabledStatePolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los Estados habilitado y deshabilitado de los servicios de comunicación de invitados de forma predeterminada.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

> [!Note]  
> Agregado en Windows 10.

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar de esta instancia de SettingData. Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o una consulta. (Nota: el nombre no tiene que ser único dentro de un espacio de nombres).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitado y deshabilitado de un elemento.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (o [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) en Windows 10 o posterior) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

Los valores válidos son:

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad expone una asignación específica a recursos de host o subyacentes. Las instancias incrustadas solo contendrán propiedades clave y se tratarán como rutas de acceso de objeto. Si el recurso virtual se puede programar en varios recursos subyacentes, esta propiedad debe ser **null**. En ese caso, las asociaciones de DeviceAllocatedFromPool o ResourceAllocationFromPool se pueden usar para determinar el grupo de recursos de host en el que se puede programar este recurso virtual. Si se utiliza una asignación específica, todos los recursos subyacentes que usa este recurso virtual se enumerarán en esta matriz. Normalmente, la matriz contendrá un elemento, pero para las asignaciones de agregado, como varios procesadores, se pueden especificar varios recursos de host.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Dentro del ámbito del espacio de nombres de la creación de instancias, InstanceID identifica de forma opaca y única una instancia de esta clase. Para garantizar la unicidad dentro del espacio de nombres, el valor de InstanceID debe construirse con el siguiente algoritmo "preferido": *OrgID*:*LocalID* donde *orgid* y *LocalID* se separan mediante dos puntos (:), y donde *OrgID* debe incluir un nombre con copyright, marca comercial o de otro tipo que sea propiedad de la entidad empresarial que está creando o definiendo el InstanceID o que es un ID (Este requisito es similar al de *SchemaName* \_ Estructura *className* de los nombres de clase de esquema.) Además, para garantizar la exclusividad, *OrgID* no debe contener dos puntos (:). Al usar este algoritmo, el primer signo de dos puntos que aparece en InstanceID debe aparecer entre *OrgID* y *LocalID*. La entidad empresarial elige *LocalID* y no se debe volver a usar para identificar distintos elementos subyacentes (del mundo real). Si no se usa el algoritmo "preferido" anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceIDs generado por este u otros proveedores para el espacio de nombres de esta instancia. En el caso de las instancias definidas por DMTF, el algoritmo "preferido" se debe usar con el valor de *OrgID* establecido en CIM.

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica el límite superior o la cantidad máxima de recursos que se concederán para esta asignación. Por ejemplo, un sistema que admita la paginación de memoria puede admitir el establecimiento del límite de una asignación de memoria por debajo de la de VirtualQuantity, lo que obliga a que se produzca la paginación para esta asignación.

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica cómo se asigna este recurso a los recursos subyacentes. Si la matriz HostResource contiene entradas, esta propiedad refleja el modo en que el recurso se asigna a esos recursos específicos.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)
</dt> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (2)
</dt> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Afinidad de software** (3)
</dt> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Afinidad fuerte** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32767.. 65535)
</dt> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y ResourceType tiene el valor "Other".

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario del recurso. Por ejemplo, un controlador para la asignación actual.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica a qué ResourcePool se asigna actualmente el recurso, o a qué ResourcePool se asignará el recurso cuando se produzca la asignación.

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica la cantidad de recursos que se garantiza que estarán disponibles para esta asignación. En el sistema que admiten el compromiso excesivo de recursos, este valor se utiliza normalmente para el control de admisión con el fin de evitar que se acepte una asignación, lo que impide el agotamiento de los recursos.

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de implementación para este recurso. Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que esta configuración de asignación representa.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controladora IDE** (5)
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**HBA de FC** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de e/s** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de e/s** (13)
</dt> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Unidad de disquete** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (17)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (18)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controladora USB** (19)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controladora de gráficos** (20)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de almacenamiento** (21)
</dt> <dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)
</dt> <dt>

<span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Cinta** (23)
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (24)
</dt> <dt>

<span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Controlador Firewire** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base con particiones** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fuente de alimentación** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de refrigeración** (29)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32767.. 65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica la cantidad de recursos que se presentan al consumidor. Por ejemplo, si ResourceType = procesador, esta propiedad reflejará el número de procesadores discretos que se presentan al sistema del equipo virtual. Cuando ResourceType = Memory, esta propiedad podría reflejar el número de MB que se ha comunicado al sistema del equipo virtual.

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica una prioridad relativa para esta asignación en relación con otras asignaciones de la misma ResourcePool. Esta propiedad no tiene ninguna unidad de medida y solo es relevante en comparación con otras asignaciones que compiten por los mismos recursos de host.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                                 |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

