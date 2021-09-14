---
description: La asociación Cim DirectorySpecificationFile representa el directorio que contiene el archivo especificado haciendo referencia a \_ la clase \_ DirectorySpecification de CIM.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: CIM_DirectorySpecificationFile clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974214"
---
# <a name="cim_directoryspecificationfile-class"></a>Cim \_ DirectorySpecificationFile (clase)

La **\_ asociación Cim DirectorySpecificationFile** representa el directorio que contiene el archivo especificado haciendo referencia a la [**clase \_ DirectorySpecification de CIM.**](cim-directoryspecification.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

## <a name="members"></a>Members

La **clase CIM \_ DirectorySpecificationFile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Cim \_ DirectorySpecificationFile** tiene estas propiedades.

<dl> <dt>

**DirectorySpecification**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ DirectorySpecification**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Máximo**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Mínimo**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia a la especificación del directorio.

</dd> <dt>

**FileSpecification**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ FileSpecification**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referencia a la especificación de archivo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

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



 

