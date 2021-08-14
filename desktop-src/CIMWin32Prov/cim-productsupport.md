---
description: La clase CIM ProductSupport representa una asociación entre el producto y el acceso de soporte técnico que transmite cómo se obtiene \_ el soporte técnico para el producto.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: CIM_ProductSupport clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a33efc39481ebe94b6aa8802d469e218d026aba34ab8da6cddf3f136b45a6d3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421452"
---
# <a name="cim_productsupport-class"></a>\_Cim ProductSupport (clase)

La **clase \_ CIM ProductSupport** representa una asociación entre el producto y el acceso de soporte técnico que transmite cómo se obtiene el soporte técnico para el producto. Hay varios tipos de soporte técnico disponibles para un producto; el mismo objeto de soporte técnico puede proporcionar asistencia para varios productos.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. ACTUALMENTE, WMI solo admite los [esquemas de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM ProductSupport** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM ProductSupport** tiene estas propiedades.

<dl> <dt>

**Producto**
</dt> <dd> <dl> <dt>

Tipo de datos: **Producto CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto.

</dd> <dt>

**Soporte técnico**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SupportAccess**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al soporte técnico del producto.

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



 

 




