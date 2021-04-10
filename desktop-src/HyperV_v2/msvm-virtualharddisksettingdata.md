---
description: Proporciona datos de configuración para un disco duro virtual.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Msvm_VirtualHardDiskSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e13efbb068d15ca4051995e7d9f317eb2ccacab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153892"
---
# <a name="msvm_virtualharddisksettingdata-class"></a>MSVM \_ VirtualHardDiskSettingData (clase)

Proporciona datos de configuración para un disco duro virtual.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualHardDiskSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualHardDiskSettingData** tiene estas propiedades.

<dl> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tamaño de bloque usado por el disco duro virtual, en bytes.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "datos de configuración de disco duro virtual".

</dd> <dt>

**Alineación de los mismos**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica la alineación deseada, en bytes, para la carga de datos del disco virtual.

> [!Note]  
> Agregado en Windows 10, versión 1709.

 

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "establecer datos para un disco duro virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Format**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El formato del disco duro virtual. Será uno de los valores siguientes.

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span id="VHD"></span><span id="vhd"></span>**VHD** (2)


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)


</dt> <dd>

> [!Note]  
> Agregado en Windows 10 y Windows Server 2016.

 

</dd> </dl>

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

**IsPmemCompatible**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Especifica si el disco virtual se puede usar como memoria auxiliar para un dispositivo de memoria persistente.

> [!Note]  
> Agregado en Windows 10, versión 1709.

 

</dd> <dt>

**LogicalSectorSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tamaño del sector lógico usado por el disco duro virtual, en bytes.

</dd> <dt>

**MaxInternalSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El tamaño máximo del disco duro virtual tal como lo ve la máquina virtual, en bytes. Este tamaño se redondeará al siguiente múltiplo más grande del tamaño del sector.

</dd> <dt>

**ParentIdentifier**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID que se usa para identificar de forma única el elemento primario del disco duro virtual. Si el disco duro virtual no tiene un elemento primario, este campo estará vacío.

> [!Note]  
> Agregado en Windows 10 y Windows Server 2016.

 

</dd> <dt>

**ParentPath**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El elemento primario del disco duro virtual. Si el disco duro virtual no tiene un elemento primario, esta propiedad está vacía.

</dd> <dt>

**ParentTimestamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo del elemento primario del disco duro virtual. Si el disco duro virtual no tiene un elemento primario, este campo estará vacío.

> [!Note]  
> Agregado en Windows 10 y Windows Server 2016.

 

</dd> <dt>

**Ruta de acceso**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Ruta de acceso completa del disco duro virtual.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tamaño de sector físico utilizado por el disco duro virtual, en bytes.

</dd> <dt>

**PmemAddressAbstractionType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Método de abstracción de dirección de memoria persistente que se va a usar con este disco virtual.

> [!Note]  
> Agregado en Windows 10, versión 1709.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

**BTT** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El tipo de disco duro virtual. Será uno de los valores siguientes.

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Fijo** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

**Dinámico** (3)


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

**Diferenciación** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualDiskId**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

GUID que se usa para identificar de forma única el disco virtual.

Cuando el método [**MSVM \_ ImageManagementService. GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) devuelve una instancia de **MSVM \_ VirtualHardDiskSettingData**, el cliente puede usar esta propiedad para obtener el identificador de disco único del VHD.

En la detección de conflictos o de lo contrario, un cliente puede establecer el valor de **VirtualDiskId** en un nuevo GUID y pasar esta instancia de **MSVM \_ VirtualHardDiskSettingData** al método [**MSVM \_ ImageManagementService. SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) para cambiar el identificador de disco del VHD. Si el disco duro virtual no es un VHD VHDX o si el VHD está conectado, se produce un error en la operación. También se produce un error en la operación si el valor pasado tiene un formato incorrecto, es decir, no un GUID o tiene todos 0. La operación se realiza de forma silenciosa si el valor pasado es igual que el identificador de disco actual.

Los errores generados por la función [**SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) se propagan a través de esta propiedad. Un cliente también puede usar el mismo mecanismo para proporcionar el valor de **VirtualDiskId** en el VHD que se crea mediante el método [**MSVM \_ ImageManagementService. CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) en el mismo espacio de nombres. Se puede usar para crear VHD de VHD1 o VHD2.

**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SettingData de CIM \_**](cim-settingdata.md)
</dt> <dt>

[**GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

