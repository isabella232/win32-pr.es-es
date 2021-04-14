---
description: La \_ clase ElementCapacity de CIM asocia un \_ objeto PHYSICALCAPACITY de CIM con uno o más elementos físicos. Asocia una descripción de los requisitos de hardware mínimos y máximos (o las capacidades) a los elementos físicos que se describen.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496283"
---
# <a name="cim_elementcapacity-class"></a>\_Clase ElementCapacity de CIM

La **clase \_ ElementCapacity de CIM** asocia un objeto [**\_ PhysicalCapacity de CIM**](cim-physicalcapacity.md) con uno o más elementos físicos. Asocia una descripción de los requisitos de hardware mínimos y máximos (o las capacidades) a los elementos físicos que se describen.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ElementCapacity** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ElementCapacity** tiene estas propiedades.

<dl> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalCapacity**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la [**clase \_ PhysicalCapacity de CIM**](cim-physicalcapacity.md) que describe los requisitos mínimo y máximo, así como la capacidad de admitir distintos tipos de hardware para un elemento físico.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Referencia al elemento físico que se describe.

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



 

