---
description: La \_ clase CIM ProductSupport representa una asociación entre el producto y el acceso de soporte que muestra cómo se obtiene la compatibilidad con el producto.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: CIM_ProductSupport (clase)
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
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659446"
---
# <a name="cim_productsupport-class"></a>\_Clase ProductSupport de CIM

La clase **CIM \_ ProductSupport** representa una asociación entre el producto y el acceso de soporte que muestra cómo se obtiene la compatibilidad con el producto. Hay varios tipos de soporte técnico disponibles para un producto; el mismo objeto de soporte técnico puede proporcionar asistencia para varios productos.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

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

La clase **CIM \_ ProductSupport** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ProductSupport** tiene estas propiedades.

<dl> <dt>

**Producto**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ Product**
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



 

 




