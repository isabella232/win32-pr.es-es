---
description: La asociación PackagedComponent de CIM representa una relación explícita en la que un componente suele estar contenido por un paquete físico, como un \_ chasis o una tarjeta.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: CIM_PackagedComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: deda43cc153baf320f5c927438314114edf3ec2d92d9e96af95707d1b7805e56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422035"
---
# <a name="cim_packagedcomponent-class"></a>Cim \_ PackagedComponent (clase)

La **\_ asociación PackagedComponent** de CIM representa una relación explícita en la que un componente normalmente está contenido por un paquete físico, como un chasis o una tarjeta.

**Nota**  Un componente se puede quitar de su paquete de contenido (es decir, la propiedad **booleana** extraíble es TRUE o no insertarse **aún en él).** Por lo tanto, es posible que un componente no siempre esté asociado a un contenedor.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ PackagedComponent** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PackagedComponent de CIM** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ CIM PhysicalPackage**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**\_ paquete físico CIM**](cim-physicalpackage.md) que describe el paquete físico que contiene componentes.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que representa el posicionamiento del elemento físico dentro del paquete físico. En esta propiedad se puede registrar información relativa a los elementos stationary del contenedor (por ejemplo, "second drive bay from the top"), ángulos, altitudes y otros datos. Esta cadena podría complementar o usarse en lugar de crear instancias del [**objeto Cim \_ Location.**](cim-location.md)

Esta propiedad se hereda del [**contenedor CIM \_**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalComponent**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**elemento \_ PhysicalComponent de CIM**](cim-physicalcomponent.md) que describe el componente físico que se encuentra en el paquete.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ Cim PackagedComponent** se deriva del [**contenedor CIM \_**](cim-container.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Contenedor \_ CIM**](cim-container.md)
</dt> </dl>

 

