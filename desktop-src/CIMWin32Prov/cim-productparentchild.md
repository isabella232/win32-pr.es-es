---
description: La \_ Asociación ProductParentChild de CIM define una jerarquía de elementos primarios y secundarios entre productos. Por ejemplo, un producto puede estar incluido en otros productos.
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: CIM_ProductParentChild (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538560"
---
# <a name="cim_productparentchild-class"></a>\_Clase ProductParentChild de CIM

La **Asociación \_ ProductParentChild de CIM** define una jerarquía de elementos primarios y secundarios entre productos. Por ejemplo, un producto puede estar incluido en otros productos.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ProductParentChild** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ProductParentChild** tiene estas propiedades.

<dl> <dt>

**Elemento secundario**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ Product**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto secundario en la asociación.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ Product**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia al producto primario de la asociación.

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



 

