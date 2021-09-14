---
description: La \_ asociación CIM ProductSoftwareFeatures identifica las características de software de un producto determinado.
ms.assetid: cd6190f8-d86e-44c8-b506-48016a7c22e1
ms.tgt_platform: multiple
title: CIM_ProductSoftwareFeatures clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSoftwareFeatures
- CIM_ProductSoftwareFeatures.Component
- CIM_ProductSoftwareFeatures.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d891d9465688d92c016217cecd8324588026535
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254589"
---
# <a name="cim_productsoftwarefeatures-class"></a>Cim \_ ProductSoftwareFeatures (clase)

La **\_ asociación CIM ProductSoftwareFeatures** identifica las características de software de un producto determinado.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{7C39D12A-DB2B-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_ProductSoftwareFeatures
{
  CIM_SoftwareFeature REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a>Members

La **clase \_ ProductSoftwareFeatures** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ProductSoftwareFeatures** de CIM tiene estas propiedades.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia al componente.

</dd> <dt>

**Producto**
</dt> <dd> <dl> <dt>

Tipo de datos: **Producto CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia al producto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Para las clases WMI derivadas de **CIM \_ ProductSoftwareFeatures**, vea [Clases win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

