---
description: La \_ asociación Cim LogicalDiskBasedOnVolumeSet relaciona los discos lógicos con el volumen en el que se encuentran. Los discos lógicos se pueden basar en un único volumen (por ejemplo, expuesto por un administrador de volúmenes de software) o en una partición de disco.
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnVolumeSet clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38ecbcf35ed46cb22a254289d617f9086780c087d932ba17a4cbd60bc1782f52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923145"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a>\_Clase LogicalDiskBasedOnVolumeSet de CIM

La **\_ asociación Cim LogicalDiskBasedOnVolumeSet** relaciona los discos lógicos con el volumen en el que se encuentran. Los discos lógicos se pueden basar en un único volumen (por ejemplo, expuesto por un administrador de volúmenes de software) o en una partición de disco.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ LogicalDiskBasedOnVolumeSet** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ LogicalDiskBasedOnVolumeSet** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ VolumeSet**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Conjunto [**de \_ volúmenes CIM**](cim-volumeset.md) que describe el conjunto de volúmenes.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ LogicalDisk**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Disco [**lógico CIM \_**](cim-logicaldisk.md) que describe el disco lógico que se basa en el conjunto de volúmenes.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el final de la extensión de alto nivel en el almacenamiento de nivel inferior. Esta propiedad es útil al asignar extensiones no contiguas a una agrupación de nivel superior.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Esta propiedad se hereda de [**CIM \_ BasedOn.**](cim-basedon.md)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el principio de la extensión de alto nivel en el almacenamiento de nivel inferior.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

Esta propiedad se hereda de [**CIM \_ BasedOn.**](cim-basedon.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ LogicalDiskBasedOnVolumeSet** de CIM se deriva de [**CIM \_ BasedOn**](cim-basedon.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ BasedOn**](cim-basedon.md)
</dt> </dl>

 

