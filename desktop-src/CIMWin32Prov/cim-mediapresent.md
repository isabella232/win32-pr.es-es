---
description: La \_ Asociación MediaPresent de CIM describe una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso a medios.
ms.assetid: 84c4931c-1dc6-4fc1-b3b9-8252ecb627f5
ms.tgt_platform: multiple
title: CIM_MediaPresent (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaPresent
- CIM_MediaPresent.Dependent
- CIM_MediaPresent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d033871a77a0433292c4a2ca1fae185df6aa5015
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914158"
---
# <a name="cim_mediapresent-class-cimwin32-wmi-providers"></a>CIM_MediaPresent (clase) (proveedores WMI de CIMWin32)

La **Asociación \_ MediaPresent de CIM** describe una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso a medios.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{8502C540-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MediaPresent : CIM_Dependency
{
  CIM_StorageExtent     REF Dependent;
  CIM_MediaAccessDevice REF Antecedent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ MediaPresent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ MediaPresent** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ MediaAccessDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ MediaAccessDevice de CIM**](cim-mediaaccessdevice.md) que describe el dispositivo de acceso a medios.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Un [**\_ StorageExtent de CIM**](cim-storageextent.md) que describe la extensión de almacenamiento a la que se tiene acceso mediante el dispositivo de acceso a medios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **CIM \_ MediaPresent** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).

WMI no implementa esta clase. Para las clases derivadas de **CIM \_ MediaPresent**, vea [clases Win32](win32-provider.md).

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

 

