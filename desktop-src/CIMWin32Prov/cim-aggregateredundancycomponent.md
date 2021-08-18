---
description: La clase AggregateRedundancyComponent de CIM describe la extensión física agregada \_ en un grupo de redundancia de almacenamiento.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: CIM_AggregateRedundancyComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dec68f7c5464774f6b9aa8ef91ec427857dd09cb73bf709c207f0e8bfb4d319c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322785"
---
# <a name="cim_aggregateredundancycomponent-class"></a>Clase \_ AggregateRedundancyComponent de CIM

La **clase \_ AggregateRedundancyComponent de CIM** describe la extensión física agregada en un grupo de redundancia de almacenamiento.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ AggregateRedundancyComponent de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ AggregateRedundancyComponent de CIM** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StorageRedundancyGroup**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**\_ storageRedundancyGroup**](cim-storageredundancygroup.md) de CIM que contiene el grupo de redundancia de almacenamiento.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ AggregatePExtent de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ AggregatePExtent**](cim-aggregatepextent.md) de CIM que contiene la extensión física agregada que participa en el grupo de redundancia.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ AggregateRedundancyComponent de CIM** se deriva de Redundancia de [**\_ CIMComponent.**](cim-redundancycomponent.md)

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

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

[**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)
</dt> </dl>

 

