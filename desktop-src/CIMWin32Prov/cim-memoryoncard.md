---
description: La \_ clase MemoryOnCard de CIM asocia la memoria física que se encuentra en los paneles de hospedaje, las tarjetas de adaptador, etc. Esta asociación define explícitamente la relación de memoria con las tarjetas.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: CIM_MemoryOnCard (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659618"
---
# <a name="cim_memoryoncard-class"></a>\_Clase MemoryOnCard de CIM

La **clase \_ MemoryOnCard de CIM** asocia la memoria física que se encuentra en los paneles de hospedaje, las tarjetas de adaptador, etc. Esta asociación define explícitamente la relación de memoria con las tarjetas.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ MemoryOnCard** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ MemoryOnCard** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ tarjeta CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Una [**\_ tarjeta CIM**](cim-card.md) que describe la tarjeta que incluye o "contiene" memoria.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que representa la posición del elemento físico en el paquete físico. La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad. Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .

Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalMemory**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ PhysicalMemory de CIM**](cim-physicalmemory.md) que describe la memoria física que se encuentra en la tarjeta.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ MemoryOnCard** se deriva de [**\_ PackagedComponent de CIM**](cim-packagedcomponent.md).

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

[**\_PACKAGEDCOMPONENT CIM**](cim-packagedcomponent.md)
</dt> </dl>

 

