---
description: La \_ asociación FromDirectoryAction de CIM identifica el directorio de origen para la acción de archivo.
ms.assetid: 25d06dad-ae39-4cfc-9331-4be7ef02d87c
ms.tgt_platform: multiple
title: CIM_FromDirectoryAction clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectoryAction
- CIM_FromDirectoryAction.FileName
- CIM_FromDirectoryAction.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f485fa32561e746afa16a899a1392b4fddc18f1f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974575"
---
# <a name="cim_fromdirectoryaction-class"></a>Cim \_ FromDirectoryAction (clase)

La **\_ asociación FromDirectoryAction de CIM** identifica el directorio de origen para la acción de archivo. Cuando se usa esta asociación, se supone que una acción anterior creó el directorio de origen. Esta asociación no puede existir con una [**asociación \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) de CIM; una acción de archivo solo puede implicar un único directorio de origen.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{55D5B446-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectoryAction
{
  CIM_FileAction      REF FileName;
  CIM_DirectoryAction REF SourceDirectory;
};
```

## <a name="members"></a>Members

La **clase \_ FromDirectoryAction de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ FromDirectoryAction de CIM** tiene estas propiedades.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ CIM FileAction**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Mínimo**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia al nombre de archivo.

</dd> <dt>

**SourceDirectory**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DirectoryAction**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Máximo**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Mínimo**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia al directorio de origen.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

