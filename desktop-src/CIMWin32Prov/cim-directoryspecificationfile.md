---
description: La \_ Asociación DirectorySpecificationFile de CIM representa el directorio que contiene el archivo especificado al hacer referencia a la \_ clase DIRECTORYSPECIFICATION de CIM.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: CIM_DirectorySpecificationFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153279"
---
# <a name="cim_directoryspecificationfile-class"></a>\_Clase DirectorySpecificationFile de CIM

La **Asociación \_ DirectorySpecificationFile de CIM** representa el directorio que contiene el archivo especificado al hacer referencia a la clase [**\_ DirectorySpecification de CIM**](cim-directoryspecification.md) .

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ DirectorySpecificationFile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ DirectorySpecificationFile** tiene estas propiedades.

<dl> <dt>

**DirectorySpecification**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DirectorySpecification**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia a la especificación del directorio.

</dd> <dt>

**FileSpecification**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ FileSpecification**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)
</dt> </dl>

Referencia a la especificación del archivo.

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



 

