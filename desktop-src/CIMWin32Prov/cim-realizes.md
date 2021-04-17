---
description: La \_ clase CIM Observations representa la asociación que define la asignación entre un dispositivo lógico y el componente físico que implementa el dispositivo.
ms.assetid: 3bddb0c8-dca5-4877-9e30-322516a8d388
ms.tgt_platform: multiple
title: CIM_Realizes (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Realizes
- CIM_Realizes.Dependent
- CIM_Realizes.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b37b2f5f3fe9cfce78e16530df8b94e4333e9a33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659521"
---
# <a name="cim_realizes-class"></a>CIM ( \_ clase)

La clase **CIM \_ Observations** representa la asociación que define la asignación entre un dispositivo lógico y el componente físico que implementa el dispositivo.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B62-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Realizes : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_PhysicalElement REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM** impones tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ Observations** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ PhysicalElement de CIM**](cim-physicalelement.md) que describe el componente físico que implementa el dispositivo.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ LogicalDevice de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ CIM** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).

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

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 

