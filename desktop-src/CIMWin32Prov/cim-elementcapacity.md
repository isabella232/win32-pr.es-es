---
description: La clase \_ ElementCapacity de CIM asocia un objeto PhysicalCapacity de CIM a uno o varios elementos \_ físicos. Asocia una descripción de los requisitos de hardware mínimos y máximos (o funcionalidades) a los elementos físicos que se describen.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974188"
---
# <a name="cim_elementcapacity-class"></a>Cim \_ ElementCapacity (clase)

La **clase \_ ElementCapacity de CIM** asocia un objeto [**\_ PhysicalCapacity**](cim-physicalcapacity.md) de CIM a uno o varios elementos físicos. Asocia una descripción de los requisitos de hardware mínimos y máximos (o funcionalidades) a los elementos físicos que se describen.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

## <a name="members"></a>Members

La **clase \_ ElementCapacity de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ElementCapacity de CIM** tiene estas propiedades.

<dl> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim PhysicalCapacity**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la [**clase \_ PhysicalCapacity**](cim-physicalcapacity.md) de CIM que describe los requisitos mínimos y máximos y la capacidad de admitir distintos tipos de hardware para un elemento físico.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mínimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia al elemento físico que se describe.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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



 

