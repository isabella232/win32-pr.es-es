---
description: La clase CIM BIOSLoadedInNV asocia un elemento BIOS y el almacenamiento no volátil en \_ el que se carga.
ms.assetid: 11641616-e11d-49ff-bfe4-f95fe27f00b8
ms.tgt_platform: multiple
title: CIM_BIOSLoadedInNV clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSLoadedInNV
- CIM_BIOSLoadedInNV.Dependent
- CIM_BIOSLoadedInNV.Antecedent
- CIM_BIOSLoadedInNV.EndingAddress
- CIM_BIOSLoadedInNV.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b38e05be817a388a8edf7a8407a0ada90999cc4e779a5270d0d2271af169aaf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119284585"
---
# <a name="cim_biosloadedinnv-class"></a>CIM \_ BIOSLoadedInNV (clase)

La **clase \_ CIM BIOSLoadedInNV** asocia un elemento BIOS y el almacenamiento no volátil en el que se carga.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{524ED194-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BIOSLoadedInNV : CIM_Dependency
{
  CIM_BIOSElement        REF Dependent;
  CIM_NonVolatileStorage REF Antecedent;
  uint64                     EndingAddress;
  uint64                     StartingAddress;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM BIOSLoadedInNV** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM BIOSLoadedInNV** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ NonVolatileStorage**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Cim [**\_ NonVolatileStorage**](cim-nonvolatilestorage.md) que describe el almacenamiento no volátil.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ BIOSElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**ELEMENTO \_ BIOSElement de CIM**](cim-bioselement.md) que describe el BIOS almacenado en la extensión no volátil.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección final donde el BIOS se encuentra en un almacenamiento no volátil.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dirección inicial donde el BIOS se encuentra en un almacenamiento no volátil.

Para obtener más información sobre el **uso de valores uint64** en scripts, vea [Scripting en WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ CIM BIOSLoadedInNV** se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

