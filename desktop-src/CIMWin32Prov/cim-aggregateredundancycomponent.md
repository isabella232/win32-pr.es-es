---
description: La \_ clase CIM AggregateRedundancyComponent describe la extensión física agregada en un grupo de redundancia de almacenamiento.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: CIM_AggregateRedundancyComponent (clase)
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
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807687"
---
# <a name="cim_aggregateredundancycomponent-class"></a>\_Clase AggregateRedundancyComponent de CIM

La clase **CIM \_ AggregateRedundancyComponent** describe la extensión física agregada en un grupo de redundancia de almacenamiento.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

La clase **CIM \_ AggregateRedundancyComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ AggregateRedundancyComponent** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StorageRedundancyGroup**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**\_ StorageRedundancyGroup de CIM**](cim-storageredundancygroup.md) que contiene el grupo de redundancia de almacenamiento.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ AggregatePExtent**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ AggregatePExtent de CIM**](cim-aggregatepextent.md) que contiene la extensión física agregada que participa en el grupo de redundancia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ AggregateRedundancyComponent** se deriva de [**\_ RedundancyComponent de CIM**](cim-redundancycomponent.md).

WMI no implementa esta clase.

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

[**\_REDUNDANCYCOMPONENT CIM**](cim-redundancycomponent.md)
</dt> </dl>

 

