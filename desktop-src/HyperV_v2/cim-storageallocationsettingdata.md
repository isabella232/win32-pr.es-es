---
description: Representa la configuración para la asignación de almacenamiento virtual.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: Clase CIM_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe380b03daced6ca98a44c189c52b5842862aa2e033bf66a04f8dd1466968449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899675"
---
# <a name="cim_storageallocationsettingdata-class"></a>Cim \_ StorageAllocationSettingData (clase)

Representa la configuración para la asignación de almacenamiento virtual.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a>Miembros

La **clase \_ Cim StorageAllocationSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Cim StorageAllocationSettingData** tiene estas propiedades.

<dl> <dt>

**Acceder**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Access**")
</dt> </dl>

Compatibilidad de lectura y escritura de la asignación de almacenamiento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Legible** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Escritura** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Lectura y escritura admitidas** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**Cim \_ StorageExtent**](cim-storageextent.md).**Name**")
</dt> </dl>

Identificador único de la extensión de almacenamiento del host.

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**", "**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**")
</dt> </dl>

Formato del valor de **la propiedad HostExtentName.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)


</dt> <dd>

Número de serie/Proveedor/Modelo (SNVM) SNVM es 3 cadenas que representan el nombre del proveedor, el nombre del producto dentro del espacio de nombres del proveedor y el número de serie dentro del espacio de nombres del modelo. Las cadenas se delimitan con "+". Los espacios se pueden incluir y son significativos. El número de serie es la representación de texto del número de serie en mayúsculas hexadecimales. Representa el proveedor y el identificador de modelo de los datos de consulta SCSI; el campo proveedor DEBE tener 8 caracteres de ancho y el campo de producto DEBE tener 16 caracteres de ancho. Por ejemplo,

'ACME \_ \_ \_ \_ +SUPER DISK \_ \_ \_ \_ \_ \_ +124437458' ( \_ es un carácter de espacio)

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span id="NAA"></span><span id="naa"></span>**NAA** (9)


</dt> <dd>

9 = NAA como formato genérico. Vea

https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html. Con formato de 16 o 32 caracteres hexadecimales sin separar en mayúsculas (2 por byte binario).

Por ejemplo, "21000020372D3C73"

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)


</dt> <dd>

EUI como formato genérico (EUI64) Consulte

https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)


</dt> <dd>

Formato de identificador de proveedor T10 devuelto por la página 83 de vpd de consulta SCSI, tipo de identificador 1. Consulte especificación T10 SPC-3. Este es el identificador de proveedor ASCII de 8 bytes del registro T10 seguido de un identificador ASCII específico del proveedor. se permiten espacios. En el caso de los volúmenes no SCSI, "SNVM" puede ser la opción más adecuada.

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nombre del dispositivo del sistema operativo** (12)


</dt> <dd>

Nombre del dispositivo del sistema operativo (para LogicalDisks). Consulte Descripción del nombre del disco lógico para obtener más información.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**", "**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM \_ StorageExtent**](cim-storageextent.md).**Espacio de** nombres ")
</dt> </dl>

Formato de nomenclatura de la **propiedad Name.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

**VPD83Type3** (2)


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (3)


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (4)


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

**VPD80** (5)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Espacio de nombres de dispositivo del** sistema operativo (8)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**", "[**Cim \_ BasedOn**](cim-basedon.md).**StartingAddress**")
</dt> </dl>

Dirección inicial en la extensión de almacenamiento del host. Un valor NULL val;ue indica que no hay ninguna asignación directa entre la extensión de almacenamiento virtual y la extensión de almacenamiento del host.

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")
</dt> </dl>

Tamaño, en bytes, de los bloques asignados en el host para la asignación de almacenamiento. Si el tamaño del bloque es variable, se debe especificar el tamaño máximo del bloque en bytes. Si se desconoce el tamaño del bloque o si no se aplica un concepto de bloque, se debe usar el valor "1" (desconocido).

</dd> <dt>

**Límite**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

Cantidad máxima de bloques que se concederán para la asignación de recursos de almacenamiento en el host. La propiedad **HostResourceBlockSize** especifica el tamaño del bloque.

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")
</dt> </dl>

Formato de la **propiedad HostExtentName** si la propiedad está establecida en "1" (otro).

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")
</dt> </dl>

Cadena que describe el espacio de nombres de la propiedad **HostExtentName** si el valor de la propiedad **HostExtentNameNamespace** es "1" (otro).

</dd> <dt>

**Reserva**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

Cantidad de bloques que se garantiza que estarán disponibles para la asignación de recursos de almacenamiento en el host. La propiedad **HostResourceBlockSize** especifica el tamaño del bloque.

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**")
</dt> </dl>

Número de bloques que la asignación de almacenamiento presenta al consumidor.

> [!Note]  
> La **propiedad VirtualQuantity** puede especificar un tamaño de bloque de "1", incluso si **VirtualResourceBlockSize** es desconocido.

 

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**
</dt> </dl>

Unidades usadas por **la propiedad VirtualQuantity.** Este valor debe establecerse en "count(fixed size block)" o "byte". El valor predeterminado, "count(bloque de tamaño fijo)" debe usarse para un tamaño de bloque fijo y "byte" debe usarse para un tamaño de bloque desconocido o variable.

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")
</dt> </dl>

Tamaño, en bytes, de los bloques que forman la solicitud de asignación de almacenamiento. Si el tamaño del bloque es variable, se debe especificar el tamaño máximo del bloque. Si se desconoce el tamaño del bloque o si no se aplica un concepto de bloque, el tamaño del bloque debe ser "1" (desconocido).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

