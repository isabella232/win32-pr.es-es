---
description: La \_ clase CIM ConnectorOnPackage representa una asociación que hace explícita la relación de contención entre los conectores y los paquetes. Los paquetes físicos contienen conectores y otros elementos físicos.
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: CIM_ConnectorOnPackage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9dfac5cf2daa19f1d3c073ac65d30fa859d2523b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907332"
---
# <a name="cim_connectoronpackage-class"></a>\_Clase ConnectorOnPackage de CIM

La clase **CIM \_ ConnectorOnPackage** representa una asociación que hace explícita la relación de contención entre los conectores y los paquetes. Los paquetes físicos contienen conectores y otros elementos físicos.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ConnectorOnPackage** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ConnectorOnPackage** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete físico que tiene un conector.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que representa la posición del elemento físico en el paquete físico. La información relativa a los elementos estacionarios del contenedor (por ejemplo, "segunda Bahía de unidad de la parte superior"), ángulos, altitudes y otros datos se puede grabar en esta propiedad. Esta cadena se puede complementar o utilizar en lugar de crear una instancia del objeto de [**\_ Ubicación CIM**](cim-location.md) .

Esta propiedad se hereda del [**\_ contenedor CIM**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalConnector**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ PhysicalConnector de CIM**](cim-physicalconnector.md) que describe el conector físico.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ ConnectorOnPackage** se deriva del [**\_ contenedor CIM**](cim-container.md).

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

[**\_Contenedor CIM**](cim-container.md)
</dt> </dl>

 

