---
description: Representa el estado configurado de un puerto de Canal de fibra sintético o un Canal de fibra de conmutador.
ms.assetid: 680badc4-8dba-47e8-859a-0ed472a15eda
title: Msvm_FcPortAllocationSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcPortAllocationSettingData
- Msvm_FcPortAllocationSettingData.InstanceID
- Msvm_FcPortAllocationSettingData.Caption
- Msvm_FcPortAllocationSettingData.Description
- Msvm_FcPortAllocationSettingData.ElementName
- Msvm_FcPortAllocationSettingData.ResourceType
- Msvm_FcPortAllocationSettingData.OtherResourceType
- Msvm_FcPortAllocationSettingData.ResourceSubType
- Msvm_FcPortAllocationSettingData.PoolID
- Msvm_FcPortAllocationSettingData.ConsumerVisibility
- Msvm_FcPortAllocationSettingData.HostResource
- Msvm_FcPortAllocationSettingData.AllocationUnits
- Msvm_FcPortAllocationSettingData.VirtualQuantity
- Msvm_FcPortAllocationSettingData.Reservation
- Msvm_FcPortAllocationSettingData.Limit
- Msvm_FcPortAllocationSettingData.Weight
- Msvm_FcPortAllocationSettingData.AutomaticAllocation
- Msvm_FcPortAllocationSettingData.AutomaticDeallocation
- Msvm_FcPortAllocationSettingData.Parent
- Msvm_FcPortAllocationSettingData.Connection
- Msvm_FcPortAllocationSettingData.Address
- Msvm_FcPortAllocationSettingData.MappingBehavior
- Msvm_FcPortAllocationSettingData.AddressOnParent
- Msvm_FcPortAllocationSettingData.VirtualQuantityUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cae27c18aa83878152ac006bf57911258d8d8980befd72becff19c7e2343e797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681365"
---
# <a name="msvm_fcportallocationsettingdata-class"></a>Clase Msvm \_ FcPortAllocationSettingData

Representa el estado configurado de un puerto de Canal de fibra sintético o un Canal de fibra de conmutador.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Virtual Fibre Channel VDev Default Settings";
  string  Description = "The default settings for the virtual Fibre Channel connection pool.";
  string  ElementName;
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

La **clase \_ FcPortAllocationSettingData de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ FcPortAllocationSettingData de Msvm** tiene estas propiedades.

<dl> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la dirección de este recurso en el contexto del elemento primario. Las **propiedades Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Unidades de asignación utilizadas por las **propiedades Reservation** **y Limit.** Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se asignará automáticamente. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se desasignará automáticamente. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dispositivo al que está conectado este recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Visibilidad del consumidor para el recurso asignado. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)). Al cambiar esta propiedad, se cambiará el nombre del elemento derivado del dispositivo lógico asociado.

Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**Msvm \_ VirtualSystemManagementService.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Solo se puede asignar un recurso host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz. Para los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso host subyacente que se va a asignar. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

Se trata de una propiedad de solo lectura, pero si la propiedad **ResourceType** es 22 (Disco) y la propiedad **ResourceSubType** es "Unidad de disco físico de Microsoft", se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**\_ VirtualSystemManagementService de Msvm.**](msvm-virtualsystemmanagementservice.md)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad máxima de recursos que se concederá para esta asignación. La propiedad **VirtualQuantityUnits** especifica la unidad de medida de esta propiedad. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica cómo se asigna este recurso a los recursos subyacentes. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**ResourceType**](msvm-processorsettingdata.md) tiene el valor 1(Other). Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario del recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del grupo de recursos desde el que se asignó este recurso. En el caso de las instancias asociadas a una máquina virtual, será "Microsoft:*datos* \\ *específicos del dispositivo GUID".* En el caso de las instancias que definen la configuración potencial de una máquina virtual, será "Microsoft:Definition GUID Type", donde Type puede ser \\  \\ "Maximum", "Minimum", "Default" o "Increment".  Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cantidad de recursos que se garantiza que estará disponible para esta asignación. La propiedad **VirtualQuantityUnits** especifica la unidad de medida de esta propiedad. Se garantiza que estos recursos estarán disponibles para su consumo por parte de la máquina virtual. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de implementación para este recurso. Por ejemplo, esto se puede usar para distinguir distintos modelos del mismo tipo de recurso. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que representa esta configuración de asignación. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

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

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de** red (11)
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

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768 65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la cantidad de recursos presentados al consumidor. La propiedad **VirtualQuantityUnits** especifica la unidad de medida de esta propiedad. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la unidad de medida para esta asignación de recursos. El valor de esta propiedad debe ser un valor legal del calificador Unidades de programación tal como se define en el anexo C.1 de DSP0004 V2.5 o posterior. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Entero que define el peso relativo de cada procesador de máquina virtual. Una vez que se hayan cumplido todas las reservas, la capacidad restante del procesador físico de la plataforma de hospedaje se asignará a las máquinas virtuales en función de sus pesos relativos. Esta propiedad se hereda de [**\_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

Intervalo: 0 1000

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

