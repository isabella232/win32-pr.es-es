---
description: Define los medios por los que un cliente puede detectar el intervalo válido de configuración predeterminada para un recurso virtual.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Msvm_AllocationCapabilities clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfdbb9dc884bd84e15e02e004af3cef296ae7723733f572a4525542747449e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149325"
---
# <a name="msvm_allocationcapabilities-class"></a>Clase AllocationCapabilities de Msvm \_

Define los medios por los que un cliente puede detectar el intervalo válido de configuración predeterminada para un recurso virtual. Un **objeto \_ AllocationCapabilities de Msvm** está asociado a cada grupo de recursos. Hay cuatro objetos [**\_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) de **Msvm asociados al objeto \_ AllocationCapabilities de Msvm** para describir los valores mínimo, máximo, predeterminado e incremental de la asignación del recurso especificado. Juntas, estas clases describen la gama general de funcionalidades admitidas.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a>Miembros

La **clase \_ AllocationCapabilities de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ AllocationCapabilities de Msvm** tiene estas propiedades.

<dl> <dt>

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

Nombre para mostrar del objeto. Esta propiedad permite a cada instancia definir un nombre para mostrar además de sus propiedades clave, datos de identidad e información de descripción. La [**propiedad Name**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) de la clase **\_ ManagedSystemElement de CIM** también se define como un nombre para mostrar. Sin embargo, a menudo se subclasifica para ser una clave. No es razonable que la misma propiedad pueda transmitir la identidad y un nombre para mostrar, sin incoherencias. Donde [**Name**](msvm-keyboard.md) existe y no es una clave (por ejemplo, para las instancias de un dispositivo lógico), la misma información puede estar presente en las propiedades **Name** y **ElementName.** Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único para este grupo de recursos. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **ResourceType** tiene el valor "Other". Esta propiedad se hereda de [**Cim \_ AllocationCapabilities.**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)

</dd> <dt>

**RequestTypesSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se admite la solicitud de un recurso específico. Esta propiedad se hereda de [**Cim \_ AllocationCapabilities.**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)



| Valor                                                                                                                                                                                                                           | Significado                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>     | Unknown<br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <dt>**Específico**</dt> <dt>2</dt> </dl> | La solicitud puede incluir una solicitud para un recurso específico.<br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <dt>**General**</dt> <dt>3</dt> </dl>     | La solicitud no incluye una solicitud para un recurso específico.<br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <dt>**Ambos**</dt> <dt>4</dt> </dl>                 | Se admiten solicitudes específicas y generales.<br/>               |



 

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de implementación para este recurso. Por ejemplo, esto se puede usar para distinguir diferentes modelos del mismo tipo de recurso. Esta propiedad se hereda de [**Cim \_ AllocationCapabilities.**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que representa esta configuración de asignación. Esta propiedad se hereda de [**Cim \_ AllocationCapabilities.**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)

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

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidad de disco** (17)
</dt> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidad de** cinta (18)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage extensión** (19)
</dt> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otros Storage dispositivo** (20)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (21)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (22)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (23)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (24)
</dt> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controlador** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base particionable** (27)
</dt> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energía** (28)
</dt> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacidad de refrigeración** (29)
</dt> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Puerto de conmutador Ethernet** (30)
</dt> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)
</dt> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage volumen** (32)
</dt> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexión Ethernet** (33)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000.. 0xFFFF )
</dt> </dl>

</dd> <dt>

**SharingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica cómo se concede acceso a un recurso subyacente. Esta propiedad se hereda de [**Cim \_ AllocationCapabilities.**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)



| Valor                                                                                                                                                                                                                               | Significado                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>         | Unknown<br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <dt>**Dedicado**</dt> <dt>2</dt> </dl> | Acceso exclusivo a un recurso subyacente.<br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <dt>**Compartido**</dt> <dt>3</dt> </dl>             | Uso compartido de un recurso subyacente.<br/>       |



 

</dd> <dt>

**SupportedAddStates**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los estados en los que puede estar el sistema al que se asociará el recurso cuando se crea un nuevo recurso. Esta propiedad se hereda de [**Cim \_ AllocationCapabilities.**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Apagar** (4)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (5)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado pero sin conexión** (6)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En prueba** (7)
</dt> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Aplazado** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A partir** de (10)
</dt> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**En pausa** (11)
</dt> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (12)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000.. 0xFFFF )
</dt> </dl>

</dd> <dt>

**SupportedRemoveStates**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los estados en los que puede estar el sistema al que está asociado el recurso cuando se quita el recurso. Esta propiedad se hereda de [**Cim \_ AllocationCapabilities.**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Apagar** (4)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (5)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitado pero sin conexión** (6)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En prueba** (7)
</dt> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Aplazado** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**A partir** de (10)
</dt> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**En pausa** (11)
</dt> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspendido** (12)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000.. 0xFFFF )
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a la **clase \_ AllocationCapabilities de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Asignación \_ de CIMCapabilities**](cim-allocationcapabilities.md)
</dt> <dt>

[**Asignación \_ de CIMCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[**Msvm \_ AllocationCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[Clases de administración de recursos](resource-management-classes.md)
</dt> </dl>

 

