---
description: La \_ clase CIM PhysicalCapacity es una clase abstracta que representa los requisitos mínimo y máximo de un elemento físico y su capacidad para admitir distintos tipos de hardware.
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: CIM_PhysicalCapacity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f928f69d34600c0f90865a4df44a5d7697fc89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000660"
---
# <a name="cim_physicalcapacity-class"></a>\_Clase PhysicalCapacity de CIM

La clase **CIM \_ PhysicalCapacity** es una clase abstracta que representa los requisitos mínimo y máximo de un elemento físico y su capacidad para admitir distintos tipos de hardware. Por ejemplo, los requisitos de memoria mínima y máxima se pueden modelar como una subclase de **\_ PhysicalCapacity de CIM**.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ PhysicalCapacity** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ PhysicalCapacity** tiene estas propiedades.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descripción textual del objeto.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Etiqueta por la que se conoce el objeto. Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.

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



 

