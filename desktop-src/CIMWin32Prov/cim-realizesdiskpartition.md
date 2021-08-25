---
description: La clase CIM RealizesDiskPartition representa una partición de disco en un medio físico que modela la creación de particiones en una \_ unidad SCSI o IDE sin procesar.
ms.assetid: cc317f7d-06cd-4126-8123-6a3eb32f792e
ms.tgt_platform: multiple
title: CIM_RealizesDiskPartition clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesDiskPartition
- CIM_RealizesDiskPartition.Dependent
- CIM_RealizesDiskPartition.Antecedent
- CIM_RealizesDiskPartition.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9e81cd96906cd7981ea7fdc7da54a728cb0efb22f0bed8269c735c642ad79cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920885"
---
# <a name="cim_realizesdiskpartition-class"></a>CIM \_ RealizesDiskPartition (clase)

La **clase CIM \_ RealizesDiskPartition** representa una partición de disco en un medio físico que modela la creación de particiones en una unidad SCSI o IDE sin procesar.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B80-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesDiskPartition : CIM_Realizes
{
  CIM_DiskPartition REF Dependent;
  CIM_PhysicalMedia REF Antecedent;
  uint64                StartingAddress;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ RealizesDiskPartition** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ RealizesDiskPartition** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalMedia**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Cim [**\_ PhysicalMedia que**](cim-physicalmedia.md) describe los medios físicos en los que se realiza la extensión.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DiskPartition**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Una [**partición de \_ disco CIM**](cim-diskpartition.md) que describe la partición de disco que se encuentra en el medio.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección inicial en el medio físico donde comienza la partición de disco. La dirección final de la partición se determina mediante las propiedades **NumberOfBlocks** y **BlockSize** del [**objeto \_ DiskPartition de CIM.**](cim-diskpartition.md)

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase CIM \_ RealizesDiskPartition** se deriva de [**CIM \_ Realizes**](cim-realizes.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ se da cuenta**](cim-realizes.md)
</dt> </dl>

 

