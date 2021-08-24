---
description: La \_ asociación CIM AdjacentSlots describe el diseño de ranuras en una tarjeta de hospedaje o adaptador.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: CIM_AdjacentSlots clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a219c2bbe95d8ccf3f89c029b4cb9f417ef8e2f0633a058c736b1339a41d7571
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701305"
---
# <a name="cim_adjacentslots-class"></a>\_Cim AdjacentSlots (clase)

La **\_ asociación CIM AdjacentSlots** describe el diseño de ranuras en una tarjeta de hospedaje o adaptador. La información, como la distancia entre las ranuras y si se "comparten" (si se rellena una, no se puede usar la otra ranura), se transmite como propiedades de asociación.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM AdjacentSlots** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM AdjacentSlots** tiene estas propiedades.

<dl> <dt>

**DistanceBetweenSlots**
</dt> <dd> <dl> <dt>

Tipo de datos: **real32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")
</dt> </dl>

Distancia, en pulgadas, entre ranuras adyacentes.

</dd> <dt>

**SharedSlots**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si **es TRUE,** una de las ranuras se rellena mediante una tarjeta adaptadora; La otra ranura se debe dejar vacía.

</dd> <dt>

**Slota**
</dt> <dd> <dl> <dt>

Tipo de datos: **Ranura CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una de las ranuras adyacentes.

</dd> <dt>

**SlotB**
</dt> <dd> <dl> <dt>

Tipo de datos: **Ranura CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la "otra" ranura adyacente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

