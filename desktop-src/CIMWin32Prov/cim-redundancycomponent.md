---
description: La \_ clase CIM RedundancyComponent asocia un grupo de redundancia compuesto por elementos del sistema administrados e indica que, juntos, los elementos proporcionan redundancia.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: CIM_RedundancyComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906989"
---
# <a name="cim_redundancycomponent-class"></a>\_Clase RedundancyComponent de CIM

La clase **CIM \_ RedundancyComponent** asocia un grupo de redundancia compuesto por elementos del sistema administrados e indica que, juntos, los elementos proporcionan redundancia. Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ RedundancyComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ RedundancyComponent** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ RedundancyGroup**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

La **Asociación \_ RedundancyComponent de CIM** indica que "este conjunto de aficionados" o "estas extensiones físicas" participan en un solo grupo de redundancia.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ManagedSystemElement de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Un [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) que describe el elemento secundario de la asociación.

Esta propiedad se hereda del [**\_ componente CIM**](cim-component.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

**CIM \_ RedundancyComponent** se deriva del [**\_ componente CIM**](cim-component.md).

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

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

