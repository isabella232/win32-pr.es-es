---
description: Representa la configuración relacionada específicamente con la asignación de almacenamiento virtual.
ms.assetid: de6787c0-9998-4f1d-9715-f0dfa0ff70c6
title: Msvm_StorageAllocationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageAllocationSettingData
- Msvm_StorageAllocationSettingData.InstanceID
- Msvm_StorageAllocationSettingData.Caption
- Msvm_StorageAllocationSettingData.Description
- Msvm_StorageAllocationSettingData.ElementName
- Msvm_StorageAllocationSettingData.ResourceType
- Msvm_StorageAllocationSettingData.OtherResourceType
- Msvm_StorageAllocationSettingData.ResourceSubType
- Msvm_StorageAllocationSettingData.PoolID
- Msvm_StorageAllocationSettingData.ConsumerVisibility
- Msvm_StorageAllocationSettingData.HostResource
- Msvm_StorageAllocationSettingData.AllocationUnits
- Msvm_StorageAllocationSettingData.VirtualQuantity
- Msvm_StorageAllocationSettingData.Limit
- Msvm_StorageAllocationSettingData.Weight
- Msvm_StorageAllocationSettingData.StorageQoSPolicyID
- Msvm_StorageAllocationSettingData.AutomaticAllocation
- Msvm_StorageAllocationSettingData.AutomaticDeallocation
- Msvm_StorageAllocationSettingData.Parent
- Msvm_StorageAllocationSettingData.Connection
- Msvm_StorageAllocationSettingData.Address
- Msvm_StorageAllocationSettingData.MappingBehavior
- Msvm_StorageAllocationSettingData.AddressOnParent
- Msvm_StorageAllocationSettingData.VirtualResourceBlockSize
- Msvm_StorageAllocationSettingData.VirtualQuantityUnits
- Msvm_StorageAllocationSettingData.Access
- Msvm_StorageAllocationSettingData.HostResourceBlockSize
- Msvm_StorageAllocationSettingData.Reservation
- Msvm_StorageAllocationSettingData.HostExtentStartingAddress
- Msvm_StorageAllocationSettingData.HostExtentName
- Msvm_StorageAllocationSettingData.HostExtentNameFormat
- Msvm_StorageAllocationSettingData.OtherHostExtentNameFormat
- Msvm_StorageAllocationSettingData.HostExtentNameNamespace
- Msvm_StorageAllocationSettingData.OtherHostExtentNameNamespace
- Msvm_StorageAllocationSettingData.IOPSLimit
- Msvm_StorageAllocationSettingData.IOPSReservation
- Msvm_StorageAllocationSettingData.IOPSAllocationUnits
- Msvm_StorageAllocationSettingData.PersistentReservationsSupported
- Msvm_StorageAllocationSettingData.CachingMode
- Msvm_StorageAllocationSettingData.SnapshotId
- Msvm_StorageAllocationSettingData.IgnoreFlushes
- Msvm_StorageAllocationSettingData.WriteHardeningMethod
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d889c262eee9d827a02547ddbfdff2cb121cb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277567"
---
# <a name="msvm_storageallocationsettingdata-class"></a>MSVM \_ StorageAllocationSettingData (clase)

Representa la configuración relacionada específicamente con la asignación de almacenamiento virtual.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageAllocationSettingData : CIM_StorageAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Hard Disk Image Default Settings";
  string  Description = "Describes the default settings for the hard disk image resources";
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Limit = 1;
  uint32  Weight;
  string  StorageQoSPolicyID;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  uint64  VirtualResourceBlockSize;
  string  VirtualQuantityUnits = "count(fixed size block)";
  uint16  Access;
  uint64  HostResourceBlockSize;
  uint64  Reservation;
  uint64  HostExtentStartingAddress;
  string  HostExtentName;
  uint16  HostExtentNameFormat;
  string  OtherHostExtentNameFormat;
  uint16  HostExtentNameNamespace;
  string  OtherHostExtentNameNamespace;
  uint64  IOPSLimit;
  uint64  IOPSReservation;
  string  IOPSAllocationUnits;
  boolean PersistentReservationsSupported;
  uint16  CachingMode;
  string  SnapshotId = "";
  boolean IgnoreFlushes;
  uint16  WriteHardeningMethod;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ StorageAllocationSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ StorageAllocationSettingData** tiene estas propiedades.

<dl> <dt>

**Acceder**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el acceso de almacenamiento. Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legible** (1)
</dt> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Grabable** (2)
</dt> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Compatible con lectura y escritura** (3)
</dt> </dl>

</dd> <dt>

**Dirección**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección del recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe la dirección de este recurso en el contexto del elemento primario. Las propiedades **Parent** y **AddressOnParent** se usan para describir la relación del controlador, así como el orden de los dispositivos en un controlador. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Las unidades de asignación utilizadas por las propiedades de **límite** y **reserva** . Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se asignará automáticamente. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el recurso se desasignará automáticamente. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**CachingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si se debe usar el almacenamiento en caché de archivos en memoria para este VHD. La directiva predeterminada se establece en el campo **DefaultVirtualHardDiskCachingMode** de la clase [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .

> [!Note]  
> Agregado en Windows 10.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Predeterminado** (2)


</dt> <dd></dd> <dt>

<span id="No_Caching"></span><span id="no_caching"></span><span id="NO_CACHING"></span>

**Sin almacenamiento en caché** (3)


</dt> <dd></dd> <dt>

<span id="Cache_Sharable_Parents"></span><span id="cache_sharable_parents"></span><span id="CACHE_SHARABLE_PARENTS"></span>

**Elementos primarios que se pueda compartir en caché** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración predeterminada de la imagen de disco duro".

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El dispositivo al que está conectado este recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Visibilidad del consumidor en el recurso asignado. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span>**Pass-through** (2)
</dt> <dt>

<span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span>**Virtualizado** (3)
</dt> <dt>

<span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span>**No se representa** (4)
</dt> </dl>

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "describe la configuración predeterminada para los recursos de imagen de disco duro".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador único para la extensión del host. La extensión de host identificada se usa para la asignación de recursos de almacenamiento. Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica el formato que se usa para la propiedad **HostExtentName** . Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)
</dt> <dt>

<span id="NAA"></span><span id="naa"></span>**NAA** (9)
</dt> <dt>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)
</dt> <dt>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)
</dt> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nombre del dispositivo de SO** (12)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (.. )
</dt> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si la extensión del host es un volumen SCSI, el origen preferido para los nombres de los volúmenes SCSI es la página de VPD 83 de las respuestas. Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>**VPD83Type3** (2)
</dt> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>**VPD83Type2** (3)
</dt> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>**VPD83Type1** (4)
</dt> <dt>

<span id="VPD80"></span><span id="vpd80"></span>**VPD80** (5)
</dt> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>**NodeWWN** (6)
</dt> <dt>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)
</dt> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>**Espacio de nombres de dispositivo de SO** (8)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (.. )
</dt> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identifica la dirección de inicio en la extensión de almacenamiento de host, identificada por la propiedad **HostExtentName** , que se usa para la asignación de la extensión de almacenamiento virtual. Un valor **null** indica que no hay ninguna asignación directa de la extensión de almacenamiento virtual a la extensión de almacenamiento de host al que se hace referencia. Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Solo se puede asignar un recurso de host a cada dispositivo de la máquina virtual, por lo que solo se puede establecer el primer elemento de esta matriz. En el caso de los dispositivos que admiten esta característica, establezca el primer elemento de la matriz **HostResource** para que contenga una referencia al recurso de host subyacente que se va a asignar. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Se trata de una propiedad de solo lectura. Pero si la propiedad **resourcetype** es 31 (disco lógico) y la propiedad **subtipo** es "Microsoft: Hyper-v: disco duro virtual", "Microsoft: Hyper-v: disco de CD/DVD virtual" o "Microsoft: Hyper-v: disquete virtual", se puede cambiar la propiedad **HostResource** mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño, en bytes, de los bloques que se asignan en el host como resultado de la asignación de recursos de almacenamiento o la solicitud de asignación de recursos de almacenamiento. Si el tamaño de bloque es variable, se especificará el tamaño máximo de bloque, en bytes. Si el tamaño de bloque es desconocido o si no se aplica un concepto de bloque, se usará el valor 1. Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**IgnoreFlushes**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si se establece en true, Hyper-V omitirá el vaciado de escritura de la máquina virtual en cuestión. Si se establece en false, Hyper-V seguirá reescribiendo en el disco en cada vaciado. False es la configuración predeterminada.

**Windows 10:** Este valor no se admite hasta Windows 10.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**IOPSAllocationUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica las unidades de asignación utilizadas por las propiedades **IOPSLimit** y **IOPSReservation** . Esta propiedad siempre tiene el valor:

"recuento (e/s normalizado)/segundo"

El rendimiento se mide en operaciones de e/s normalizadas por segundo (IOPS) en lugar de IOPS sin procesar. Cuando se usa la IOPS normalizada, cada solicitud de e/s se cuenta como 1 e/s normalizada si el tamaño de la solicitud es menor o igual que un tamaño base predefinido (8 KB). Las solicitudes que son mayores que el tamaño base se tienen en cuenta como operaciones de e/s de N, donde N es el valor redondeado del tamaño de la solicitud dividido por el tamaño base. Por ejemplo, si el tamaño base es de 8 KB, una solicitud de 16 KB se cuenta como dos operaciones de e/s normalizadas, una solicitud de 32 KB como 4 operaciones de e/s normalizadas, etc.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**IOPSLimit**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 mil millones)
</dt> </dl>

Número máximo de operaciones de e/s por segundo (IOPS) que se van a atender para esta extensión de almacenamiento virtual. Si el valor no está definido o es cero, no hay ningún límite en el número de IOPS que el dispositivo puede emitir.

> [!Note]  
> Puede usar el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar el valor de esta propiedad. Esta propiedad solo es significativa para las instancias de **MSVM \_ StorageAllocationSettingData** que solicitan asignaciones de recursos para máquinas virtuales. Se omite cuando se asignan recursos a un grupo secundario.

 

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**IOPSReservation**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1 mil millones)
</dt> </dl>

El número mínimo de operaciones de e/s por segundo (IOPS) que se van a atender para esta extensión de almacenamiento virtual.

Si se definen tanto **IOPSLimit** como **IOPSReservation** , el valor de **IOPSLimit** debe ser mayor o igual que el valor de **IOPSReservation**.

> [!Note]  
> Puede usar el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para modificar el valor de esta propiedad. Esta propiedad solo es significativa para las instancias de **MSVM \_ StorageAllocationSettingData** que solicitan asignaciones de recursos para máquinas virtuales. Se omite cuando se asignan recursos a un grupo secundario.

 

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número máximo de bloques que se concederán para esta asignación de recursos de almacenamiento en el host. El tamaño de bloque se especifica mediante la propiedad **HostResourceBlockSize** . Normalmente, el valor de esta propiedad reflejará un tamaño máximo para la extensión de host asignada que coincida con el tamaño de la extensión de almacenamiento virtual presentada al consumidor. Un valor menor que esto indicaría una situación en la que se espera una extensión de almacenamiento virtual parcialmente rellenada, donde la velocidad de relleno está limitada por el valor de la propiedad Limit. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica cómo se asigna este recurso a los recursos subyacentes. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el formato de la propiedad **HostExtentName** si la propiedad **HostExtentNameFormat** es 1 (otra). Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que describe el espacio de nombres de la propiedad **HostExtentName** si la propiedad **HostExtentNameNamespace** contiene 1 (otro). Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y [**resourcetype**](msvm-processorsettingdata.md) tiene el valor 1 (otro). Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario del recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**PersistentReservationsSupported**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el disco duro virtual admite reservas persistentes SCSI-3.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador del grupo de recursos desde el que se asignó este recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **override** ("reserva"), **ModelCorrespondence** ("CIM \_ StorageAllocationSettingData. HostResourceBlockSize")
</dt> </dl>

El número de bloques que se garantiza que estarán disponibles para esta asignación de recursos de almacenamiento en el host. El tamaño de bloque se especifica mediante la propiedad **HostResourceBlockSize** . Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**Subtipo de recurso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe un subtipo específico de la implementación para este recurso. Por ejemplo, se puede usar para distinguir los diferentes modelos del mismo tipo de recurso. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de recurso que esta configuración de asignación representa. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

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

<span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Unidad de disquete** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)
</dt> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidad de disco** (17)
</dt> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidad de cinta** (18)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de almacenamiento** (19)
</dt> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (20)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (21)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (22)
</dt> <dt>

<span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controladora USB** (23)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controladora de gráficos** (24)
</dt> <dt>

<span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**Controlador IEEE 1394** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base con particiones** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Fuente de alimentación** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Dispositivo de refrigeración** (29)
</dt> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Puerto de conmutador Ethernet** (30)
</dt> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)
</dt> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volumen de almacenamiento** (32)
</dt> <dt>

<span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexión Ethernet** (33)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (30 32767)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (32768 65535)
</dt> </dl>

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un GUID que representa qué instantánea del archivo del conjunto de VHD se va a adjuntar.

> [!Note]  
> Agregado en Windows 10.

 

</dd> <dt>

**StorageQoSPolicyID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el identificador único de la Directiva de QoS de almacenamiento que se va a aplicar a esta extensión de almacenamiento virtual.

> [!Note]  
> Agregado en Windows 10.

 

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El número de bloques que se presentan al consumidor. El tamaño de bloque se especifica mediante la propiedad **VirtualResourceBlockSize** . Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica las unidades utilizadas por la propiedad **VirtualQuantity** . Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.



| Value                                                                                                | Significado                                                                                    |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>"recuento (bloque de tamaño fijo)"</dt> </dl> | El tamaño de bloque fijo está contenido en la propiedad **VirtualResourceBlockSize** .<br/> |
| <dl> <dt>bytes</dt> </dl>                    | La propiedad **VirtualQuantity** se mide en bytes.<br/>                          |



 

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño, en bytes, de los bloques que se presentan al consumidor como resultado de la asignación de recursos de almacenamiento o la solicitud de asignación de recursos de almacenamiento. Si el tamaño de bloque es variable, se especificará el tamaño máximo de bloque, en bytes. Si el tamaño de bloque es desconocido o si no se aplica un concepto de bloque, se usará el valor 1. Esta propiedad se hereda de **\_ StorageAllocationSettingData CIM**.

</dd> <dt>

**Peso**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("peso"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (10000)
</dt> </dl>

Especifica una prioridad relativa para esta asignación en relación con otras asignaciones del mismo grupo de recursos de sitio. Esta propiedad no tiene ninguna unidad de medida y solo es relevante en comparación con otras asignaciones vying para los mismos recursos de host. Esta propiedad se hereda de [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

Intervalo: 1 10000

</dd> <dt>

**WriteHardeningMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica qué método de protección de escritura es compatible con el disco.

> [!Note]  
> Esta propiedad se agregó en la versión 1703 de Windows 10.

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valor predeterminado** (0)


</dt> <dd></dd> <dt>

<span id="WriteCacheEnabled"></span><span id="writecacheenabled"></span><span id="WRITECACHEENABLED"></span>

**WriteCacheEnabled** (1)


</dt> <dd></dd> <dt>

<span id="WriteCacheandFUAEnabled"></span><span id="writecacheandfuaenabled"></span><span id="WRITECACHEANDFUAENABLED"></span>

**WriteCacheandFUAEnabled** (2)


</dt> <dd></dd> <dt>

<span id="WriteCacheDisabled"></span><span id="writecachedisabled"></span><span id="WRITECACHEDISABLED"></span>

**WriteCacheDisabled** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

