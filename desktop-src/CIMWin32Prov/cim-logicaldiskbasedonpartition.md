---
description: La \_ clase LogicalDiskBasedOnPartition de CIM asocia un disco lógico a la partición de disco en la que reside.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnPartition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538505"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a>\_Clase LogicalDiskBasedOnPartition de CIM

La **clase \_ LogicalDiskBasedOnPartition de CIM** asocia un disco lógico a la partición de disco en la que reside.

Por ejemplo, la unidad C de un equipo puede encontrarse en una partición en un medio físico local, lo que indica que un disco lógico no puede abarcar más de una partición. Sin embargo, cuando un disco lógico puede abarcar más de una partición, el disco lógico se basa en la configuración de RAID (por ejemplo, un conjunto de espejos o de bandas). En ese caso, el disco lógico se basa en el volumen de almacenamiento. Para evitar el uso incorrecto de la Asociación **\_ LogicalDiskBasedOnPartition de CIM** , se colocó el calificador **Max (1)** en la referencia **antecedente** a la partición de disco.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ LogicalDiskBasedOnPartition** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ LogicalDiskBasedOnPartition** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DiskPartition**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**\_ DiskPartition de CIM**](cim-diskpartition.md) que describe la partición del disco.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalDisk**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Un [**\_ LogicalDisk de CIM**](cim-logicaldisk.md) que describe el disco lógico que se basa en la partición.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el final de la extensión de alto nivel en el almacenamiento de nivel inferior. Esta propiedad es útil cuando se asignan extensiones no contiguas a una agrupación de nivel superior.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda de [**\_ BasedOn CIM**](cim-basedon.md).

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el principio de la extensión de alto nivel en el almacenamiento de nivel inferior.

Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Esta propiedad se hereda de [**\_ BasedOn CIM**](cim-basedon.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ LogicalDiskBasedOnPartition** se deriva de [**la \_ BasedOn CIM**](cim-basedon.md).

WMI no implementa esta clase. Para las clases derivadas de **CIM \_ LogicalDiskBasedOnPartition**, vea [clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_BasedOn CIM**](cim-basedon.md)
</dt> </dl>

 

