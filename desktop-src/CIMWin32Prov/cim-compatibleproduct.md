---
description: La clase CIM CompatibleProduct representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, como si se pueden instalar juntos, o si uno puede ser el contenedor físico para el otro, y así \_ sucesivamente.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: CIM_CompatibleProduct clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d0d4721d8554723bb9ab808ff55884bb896f59e6050103cf127cc4df77109f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080879"
---
# <a name="cim_compatibleproduct-class"></a>Cim \_ CompatibleProduct (clase)

La **clase CIM \_ CompatibleProduct** representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, como si se pueden instalar juntos, o si uno puede ser el contenedor físico para el otro, y así sucesivamente.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ CompatibleProduct** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM CompatibleProduct** tiene estas propiedades.

<dl> <dt>

**CompatibilityDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que define cómo los dos productos a los que se hace referencia son interoperables, compatibles y si existen limitaciones de compatibilidad.

</dd> <dt>

**CompatibleProduct**
</dt> <dd> <dl> <dt>

Tipo de datos: **Producto \_ CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto compatible.

</dd> <dt>

**Producto**
</dt> <dd> <dl> <dt>

Tipo de datos: **Producto \_ CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto para el que se definen ofertas compatibles.

</dd> </dl>

## <a name="remarks"></a>Comentarios

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



 

 




