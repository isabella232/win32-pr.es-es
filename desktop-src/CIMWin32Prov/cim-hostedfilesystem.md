---
description: La asociación Cim HostedFileSystem representa un vínculo entre el sistema de equipos y el sistema \_ de archivos hospedado en el sistema de equipos.
ms.assetid: 1027fc6b-588b-4da8-8b3f-0c4c3328534a
ms.tgt_platform: multiple
title: CIM_HostedFileSystem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedFileSystem
- CIM_HostedFileSystem.PartComponent
- CIM_HostedFileSystem.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 544dd18f5d8ea3bd0afb166fac3b692bacfe47b67777fdcc65678a418111775a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921675"
---
# <a name="cim_hostedfilesystem-class"></a>Cim \_ HostedFileSystem (clase)

La **\_ asociación CIM HostedFileSystem** representa un vínculo entre el sistema de equipos y el sistema de archivos hospedado en el sistema de equipos.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{A2EFC898-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_HostedFileSystem : CIM_SystemComponent
{
  CIM_FileSystem     REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ HostedFileSystem de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ HostedFileSystem de CIM** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Un [**sistema de equipos \_ CIM**](cim-computersystem.md) que describe el sistema del equipo.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ FileSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**sistema de \_ archivos CIM**](cim-filesystem.md) que describe el sistema de archivos propiedad del sistema de equipos.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase CIM \_ HostedFileSystem** se deriva de [**CIM \_ SystemComponent**](cim-systemcomponent.md).

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> </dl>

 

