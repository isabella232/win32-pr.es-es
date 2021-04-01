---
description: La \_ clase CIM CompatibleProduct representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, por ejemplo, si se pueden instalar juntos o si puede ser el contenedor físico del otro, etc.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: CIM_CompatibleProduct (clase)
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
ms.openlocfilehash: 94969b1f2e45a27e402e132a0b9593de413a653b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907335"
---
# <a name="cim_compatibleproduct-class"></a>\_Clase CompatibleProduct de CIM

La clase **CIM \_ CompatibleProduct** representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, por ejemplo, si se pueden instalar juntos o si puede ser el contenedor físico del otro, etc.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

La clase **CIM \_ CompatibleProduct** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ CompatibleProduct** tiene estas propiedades.

<dl> <dt>

**CompatibilityDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que define el modo en que los dos productos a los que se hace referencia son interoperables, compatibles y si existen limitaciones de compatibilidad.

</dd> <dt>

**CompatibleProduct**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ Product**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto compatible.

</dd> <dt>

**Producto**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ Product**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto para el que se definen las ofertas compatibles.

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



 

 




