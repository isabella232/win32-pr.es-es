---
description: La clase CIM \_ DirectoryContainsFile representa una asociación entre un directorio y los archivos contenidos en ese directorio.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: CIM_DirectoryContainsFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974222"
---
# <a name="cim_directorycontainsfile-class"></a>Clase \_ Cim DirectoryContainsFile

La **clase CIM \_ DirectoryContainsFile** representa una asociación entre un directorio y los archivos contenidos en ese directorio.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a>Members

La **clase \_ Cim DirectoryContainsFile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Cim DirectoryContainsFile** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Directorio CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Directorio [**CIM \_ que**](cim-directory.md) describe el directorio.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DataFile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Un [**archivo de datos \_ CIM**](cim-datafile.md) que describe el archivo lógico contenido en el directorio .

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI implementa la clase **\_ Cim DirectoryContainsFile,** que es una clase dinámica.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

