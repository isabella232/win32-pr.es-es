---
description: Proporciona información de estado para una imagen de disco duro virtual existente.
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Msvm_VirtualHardDiskState clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5896e8b19d2897084997bd01b65bbb0d6e80e0ca15f662fff38871bdc0b6755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426315"
---
# <a name="msvm_virtualharddiskstate-class"></a>Clase VirtualHardDiskState de Msvm \_

Proporciona información de estado para una imagen de disco duro virtual existente.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a>Miembros

La **clase \_ VirtualHardDiskState de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ VirtualHardDiskState de Msvm** tiene estas propiedades.

<dl> <dt>

**Alineación**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de alineación del disco duro virtual. Este será uno de los siguientes valores.



| Value                                                                        | Significado                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>0</dt> </dl> | Alineación de 512 bytes.<br/> |
| <dl> <dt>1</dt> </dl> | Alineación de 4 KB.<br/>     |



 

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño del archivo de disco duro virtual (la cantidad real de almacenamiento que consume el archivo), en bytes.

</dd> <dt>

**FragmentaciónPercentage**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Aproximación del porcentaje de bloques de disco virtual que se fragmentan en el archivo de disco duro virtual.

</dd> <dt>

**Uso inuso**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad está reservada para un uso futuro.

</dd> <dt>

**MinInternalSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño mínimo al que se puede reducido el disco duro virtual, en bytes. Este tamaño se redondea al siguiente múltiplo más grande del tamaño del sector.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tamaño del sector físico utilizado por el disco físico subyacente, en bytes.

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo de datos: **DATETIME**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marca de tiempo del disco duro virtual

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




