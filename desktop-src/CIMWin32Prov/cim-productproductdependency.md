---
description: La clase CIM ProductProductDependency representa una asociación entre dos productos, lo que indica que uno debe estar instalado o ausente para que el otro \_ funcione. Esto es conceptualmente equivalente a la \_ asociación ServiceServiceDependency de CIM.
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: CIM_ProductProductDependency clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductProductDependency
- CIM_ProductProductDependency.DependentProduct
- CIM_ProductProductDependency.RequiredProduct
- CIM_ProductProductDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 094800b3a2d50d7be4039d5850f9ac1d3f236a40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970296"
---
# <a name="cim_productproductdependency-class"></a>Cim \_ ProductProductDependency (clase)

La **clase \_ CIM ProductProductDependency** representa una asociación entre dos productos, lo que indica que uno debe estar instalado o ausente para que el otro funcione. Esto es conceptualmente equivalente a la [**\_ asociación ServiceServiceDependency**](cim-serviceservicedependency.md) de CIM.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{65878E68-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductProductDependency
{
  CIM_Product REF DependentProduct;
  CIM_Product REF RequiredProduct;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a>Members

La **clase \_ ProductProductDependency** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM ProductProductDependency** tiene estas propiedades.

<dl> <dt>

**DependentProduct**
</dt> <dd> <dl> <dt>

Tipo de datos: **Producto \_ CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto que depende de otro producto.

</dd> <dt>

**RequiredProduct**
</dt> <dd> <dl> <dt>

Tipo de datos: **Producto \_ CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto necesario.

</dd> <dt>

**TypeOfDependency**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Naturaleza de la dependencia del producto.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**El producto debe estar instalado** (2)


</dt> <dd>

El producto debe estar instalado.

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**No se debe instalar el producto** (3)


</dt> <dd>

No se debe instalar el producto.

</dd> </dl>

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



 

 




