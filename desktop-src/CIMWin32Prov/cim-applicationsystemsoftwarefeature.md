---
description: La \_ clase CIM ApplicationSystemSoftwareFeature representa una asociación que identifica las características de software que componen un sistema de aplicación determinado. Las características de software se pueden incluir en diferentes productos.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: CIM_ApplicationSystemSoftwareFeature (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907378"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a>\_Clase ApplicationSystemSoftwareFeature de CIM

La clase **CIM \_ ApplicationSystemSoftwareFeature** representa una asociación que identifica las características de software que componen un sistema de aplicación determinado. Las características de software se pueden incluir en diferentes productos.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ApplicationSystemSoftwareFeature** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ApplicationSystemSoftwareFeature** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ApplicationSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

[**\_ ApplicationSystem CIM**](cim-applicationsystem.md) que contiene el sistema primario de la asociación.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) que contiene el elemento secundario que es un componente de un sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ ApplicationSystemSoftwareFeature** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> </dl>

 

