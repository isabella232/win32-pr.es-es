---
description: La \_ Asociación FileStorage de CIM vincula el sistema de archivos y los archivos lógicos que se dirigen a través del sistema de archivos.
ms.assetid: 1d0b698b-4c57-4a1c-8b00-0a6079be8dcc
ms.tgt_platform: multiple
title: CIM_FileStorage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileStorage
- CIM_FileStorage.PartComponent
- CIM_FileStorage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3630bdf3250ce93765809df17e9318d3cd44f393
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659599"
---
# <a name="cim_filestorage-class"></a>\_Clase FileStorage de CIM

La **Asociación \_ FileStorage de CIM** vincula el sistema de archivos y los archivos lógicos que se dirigen a través del sistema de archivos.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{4A626026-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FileStorage : CIM_Component
{
  CIM_LogicalFile REF PartComponent;
  CIM_FileSystem  REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ FileStorage** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ FileStorage** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ sistema de archivos CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un sistema de archivos [**CIM \_**](cim-filesystem.md) que describe el sistema de archivos.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalFile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**\_ LogicalFile de CIM**](cim-logicalfile.md) que describe el archivo lógico almacenado en el contexto del sistema de archivos.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

