---
description: La \_ Asociación AdjacentSlots de CIM describe el diseño de las ranuras en una placa de hospedaje o en una tarjeta de adaptador.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: CIM_AdjacentSlots (clase)
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
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153298"
---
# <a name="cim_adjacentslots-class"></a>\_Clase AdjacentSlots de CIM

La **Asociación \_ AdjacentSlots de CIM** describe el diseño de las ranuras en una placa de hospedaje o en una tarjeta de adaptador. La información, como la distancia entre las ranuras y si están "compartidas" (si se ha rellenado una, no se puede usar la otra ranura), se transmite como propiedades de asociación.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

La clase **CIM \_ AdjacentSlots** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ AdjacentSlots** tiene estas propiedades.

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

Si es **true**, una tarjeta adaptador rellena una de las ranuras; la otra ranura debe dejarse vacía.

</dd> <dt>

**Ranuraa**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ranura CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una de las ranuras adyacentes.

</dd> <dt>

**SlotB**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ranura CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la ranura adyacente "otros".

</dd> </dl>

## <a name="remarks"></a>Observaciones

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

[Clases CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

