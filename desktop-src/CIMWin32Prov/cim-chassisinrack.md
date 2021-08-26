---
description: La asociación CIM ChassisInRack representa la relación \_ &\# 0034; que contiene&0034; entre un bastidor y un chasis que \# contiene.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: CIM_ChassisInRack clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 765b5e36fcb5f2cfe400d9dec9ba86d37cd29af8c756ae8416f7aece803f9052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065215"
---
# <a name="cim_chassisinrack-class"></a>Cim \_ ChassisInRack (clase)

La **\_ asociación CIM ChassisInRack** representa la relación "que contiene" entre un bastidor y un chasis que contiene.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM ChassisInRack** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ ChassisInRack** tiene estas propiedades.

<dl> <dt>

**BottomU**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")
</dt> </dl>

Entero que indica la "U" más baja o inferior en la que está montado el chasis. Una "U" es una unidad de medida estándar para la altura de un bastidor, o componente montable en bastidor, y es igual a 1,75 pulgadas o 4,445 cm.

</dd> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Bastidor CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Bastidor [**CIM \_ que**](cim-rack.md) describe el bastidor que contiene el chasis.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que representa el posicionamiento del elemento físico dentro del paquete físico. La información relativa a los elementos estacionados del contenedor (por ejemplo, "segunda unidad desde la parte superior"), los ángulos, las altitudes y otros datos se pueden registrar en esta propiedad. Esta cadena podría complementar o usarse en lugar de crear instancias del [**objeto Cim \_ Location.**](cim-location.md)

Esta propiedad se hereda del [**contenedor CIM \_**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Chasis CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Chasis [**CIM \_ que**](cim-chassis.md) describe el chasis montado en el bastidor.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ CIM ChassisInRack** se deriva del [**contenedor CIM \_**](cim-container.md).

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

[**Contenedor \_ CIM**](cim-container.md)
</dt> </dl>

 

