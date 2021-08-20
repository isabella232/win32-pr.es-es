---
description: Representa el estado configurado del componente de interfaz de servicio invitado.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Msvm_GuestServiceInterfaceComponentSettingData clase
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
ms.openlocfilehash: 6e1171e5f303d5b122f0d2202978415206a26e94c15e69f09af73b811c33dcb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147811"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a>Clase \_ GuestServiceInterfaceComponentSettingData de Msvm

Representa el estado configurado del componente de interfaz de servicio invitado. Esta clase se deriva de la [**\_ clase ResourceAllocationSettingData de CIM.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

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

La **clase Msvm \_ GuestServiceInterfaceComponentSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ GuestServiceInterfaceComponentSettingData** tiene estas propiedades.

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

Esta propiedad especifica las unidades de asignación utilizadas por las propiedades Reservation y Limit. Por ejemplo, cuando ResourceType=Processor, AllocationUnits puede establecerse en MHz. Cuando ResourceType=Memory, AllocationUnits puede establecerse en MB

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica si el recurso se asignará automáticamente. Por ejemplo, cuando se establece en true, cuando el sistema de equipo virtual de consumo está encendido, se asignaría este recurso. Un valor de false indica que el recurso debe asignarse explícitamente. Por ejemplo, la configuración puede representar medios extraíbles (es decir, cdrom o disquete) en los que, a tiempo, el medio no está presente. Se requiere una operación explícita para asignar el recurso.

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica si el recurso se desasignará automáticamente. Por ejemplo, cuando se establece en true, cuando se apaga el sistema de equipo virtual de consumo, este recurso se desasignaría. Cuando se establece en false, el recurso permanecerá asignado y se debe desasignar explícitamente.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El elemento al que está conectado este recurso. Por ejemplo, una red con nombre o un puerto de conmutador.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la visibilidad de los consumidores para el recurso asignado.



| Valor                                                                                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                                            | Desconocido.<br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <dt>**Paso a través**</dt> <dt>2</dt> </dl>                | El recurso subyacente o host se utiliza y se pasa al consumidor, posiblemente mediante la creación de particiones. Al menos un elemento debe estar presente en la propiedad DeviceID.<br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <dt>**Virtualizado**</dt> <dt>3</dt> </dl>                            | El recurso está virtualizado y es posible que no se asigne directamente a un recurso subyacente o host. Algunas implementaciones pueden admitir una asignación específica para los recursos virtualizados, en cuyo caso los recursos host se exponen mediante la propiedad DeviceID.<br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <dt>**No representado**</dt> <dt>4</dt> </dl>            | Una representación del recurso no existe en el contexto del consumidor de recursos.<br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>.</dt> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Vendor Reserved**</dt> <dt>32767..65535</dt> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

**DefaultEnabledStatePolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los estados habilitados y deshabilitados de los servicios de comunicación de invitado de forma predeterminada.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

> [!Note]  
> Se ha agregado en Windows 10.

 

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

Nombre para mostrar de esta instancia de SettingData. Además, el nombre para mostrar se puede usar como una propiedad de índice para una búsqueda o consulta. (Nota: El nombre no tiene que ser único dentro de un espacio de nombres).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitados y deshabilitados de un elemento.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyVirtualSystemResources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (o [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) en Windows 10 o posterior) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

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

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad expone una asignación específica al host o a los recursos subyacentes. Las instancias incrustadas solo deben contener propiedades clave y tratarse como rutas de acceso de objeto. Si el recurso virtual se puede programar en varios recursos subyacentes, esta propiedad debe seguir siendo **NULL.** En ese caso, se pueden usar las asociaciones DeviceAllocatedFromPool o ResourceAllocationFromPool para determinar el grupo de recursos de host en el que se puede programar este recurso virtual. Si se utiliza una asignación específica, todos los recursos subyacentes utilizados por este recurso virtual se mostrarán en esta matriz. Normalmente, la matriz contendrá un elemento; sin embargo, para las asignaciones agregadas, como varios procesadores, se pueden especificar varios recursos de host.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Dentro del ámbito del espacio de nombres de creación de instancias, InstanceID identifica de forma opaca e inequívoca una instancia de esta clase. Para garantizar la unidad dentro del Espacio de nombres, el valor de InstanceID debe construirse mediante el siguiente algoritmo *"preferido": OrgID:**LocalID,* donde *OrgID* y *LocalID* están separados por dos puntos (:), y donde *OrgID* debe incluir un nombre con derechos de autor, marca comercial o único que sea propiedad de la entidad empresarial que crea o define instanceID o que es un identificador registrado asignado a la entidad empresarial por una autoridad global reconocida. (Este requisito es similar a *SchemaName* \_ *Estructura ClassName* de nombres de clase de esquema). Además, para garantizar la unidad, *OrgID* no debe contener dos puntos (:). Cuando se usa este algoritmo, los primeros dos puntos que aparecen en InstanceID deben aparecer entre *OrgID* y *LocalID.* La entidad empresarial elige *LocalID* y no debe reutilizarse para identificar diferentes elementos subyacentes (reales). Si no se usa el algoritmo "preferido" anterior, la entidad de definición debe asegurarse de que el InstanceID resultante no se reutiliza en ningún InstanceID generado por este u otros proveedores para nameSpace de esta instancia. En el caso de las instancias definidas por DMTF, el algoritmo "preferido" debe usarse con *orgID* establecido en CIM.

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica el límite superior o la cantidad máxima de recursos que se concederán para esta asignación. Por ejemplo, un sistema que admite la paginación de memoria puede admitir establecer el límite de una asignación de memoria por debajo del de VirtualQuantity, lo que obliga a que se produzca la paginación para esta asignación.

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica cómo se asigna este recurso a los recursos subyacentes. Si la matriz HostResource contiene entradas, esta propiedad refleja cómo se asigna el recurso a esos recursos específicos.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)
</dt> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (2)
</dt> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Afinidad flexible** (3)
</dt> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Afinidad dura** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)
</dt> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y ResourceType tiene el valor "Other".

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

Esta propiedad especifica desde qué ResourcePool se asigna actualmente el recurso o desde qué ResourcePool se asignará el recurso cuando se produzca la asignación.

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica la cantidad de recurso que se garantiza que estará disponible para esta asignación. En el sistema que admite el exceso de compromiso de los recursos, este valor se usa normalmente para el control de admisión a fin de evitar que se acepte una asignación, lo que impide el agotamiento de recursos.

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de implementación para este recurso. Por ejemplo, esto se puede usar para distinguir diferentes modelos del mismo tipo de recurso.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que representa esta configuración de asignación.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de E/S** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de E/S** (13)
</dt> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Disquete** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (17)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (18)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (19)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (20)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage extensión** (21)
</dt> <dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Disco** (22)
</dt> <dt>

<span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Cinta** (23)
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (24)
</dt> <dt>

<span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base particionable** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fuente de alimentación** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de refrigeración** (29)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32767..65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica la cantidad de recursos presentados al consumidor. Por ejemplo, cuando ResourceType=Processor, esta propiedad reflejaría el número de procesadores discretos presentados al sistema de equipo virtual. Cuando ResourceType=Memory, esta propiedad podría reflejar el número de MB notificado al sistema de equipo virtual.

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad especifica una prioridad relativa para esta asignación en relación con otras asignaciones del mismo ResourcePool. Esta propiedad no tiene ninguna unidad de medida y solo es relevante en comparación con otras asignaciones que compiten por los mismos recursos de host.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

