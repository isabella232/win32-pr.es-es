---
description: La \_ clase CIM ProductProductDependency representa una asociación entre dos productos, lo que indica que se debe instalar o ausente un para que el otro funcione. Es conceptualmente equivalente a la \_ Asociación ServiceServiceDependency de CIM.
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: CIM_ProductProductDependency (clase)
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
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080141"
---
# <a name="cim_productproductdependency-class"></a>\_Clase ProductProductDependency de CIM

La clase **CIM \_ ProductProductDependency** representa una asociación entre dos productos, lo que indica que se debe instalar o ausente un para que el otro funcione. Es conceptualmente equivalente a la Asociación [**\_ ServiceServiceDependency de CIM**](cim-serviceservicedependency.md) .

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

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

## <a name="members"></a>Miembros

La clase **CIM \_ ProductProductDependency** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ProductProductDependency** tiene estas propiedades.

<dl> <dt>

**DependentProduct**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ Product**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto que depende de otro producto.

</dd> <dt>

**RequiredProduct**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ Product**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al producto requerido.

</dd> <dt>

**TypeOfDependency**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
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

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>El **producto debe estar instalado** (2)


</dt> <dd>

El producto debe estar instalado.

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>El **producto no debe estar instalado** (3)


</dt> <dd>

El producto no debe estar instalado.

</dd> </dl>

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



 

 




