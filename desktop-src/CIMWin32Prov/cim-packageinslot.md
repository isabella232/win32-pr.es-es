---
description: La \_ Asociación PackageInSlot de CIM representa la relación entre las tarjetas de dispositivo y el chasis en el que se montan.
ms.assetid: 439f28a8-24fd-4a53-9d42-48fabb58e84a
ms.tgt_platform: multiple
title: CIM_PackageInSlot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInSlot
- CIM_PackageInSlot.Dependent
- CIM_PackageInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a17e133f16f838d6353b6d74ee2054bd5ec52cd0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152876"
---
# <a name="cim_packageinslot-class"></a>\_Clase PackageInSlot de CIM

La **Asociación \_ PackageInSlot de CIM** representa la relación entre las tarjetas de dispositivo y el chasis en el que se montan.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B89-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInSlot : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_Slot            REF Antecedent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ PackageInSlot** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ PackageInSlot** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ ranura CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Una [**\_ ranura CIM**](cim-slot.md) que describe la ranura en la que se inserta el paquete físico.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ PhysicalPackage**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete en la ranura.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**CIM \_ PackageInSlot** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).

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

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 

