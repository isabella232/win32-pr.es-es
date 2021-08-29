---
description: La clase LogicalIdentity de CIM es una asociación abstracta y genérica que indica que dos elementos lógicos representan aspectos diferentes \_ de la misma entidad subyacente.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: CIM_LogicalIdentity clase (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b390e0aab0a95ce7eccd7f819fd1f1bd24940760802e342f189f06fde57a8af7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923015"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a>CIM_LogicalIdentity clase (proveedores WMI CIMWin32)

La **clase \_ LogicalIdentity de CIM** es una asociación abstracta y genérica que indica que dos elementos lógicos representan aspectos diferentes de la misma entidad subyacente. La asociación transmite lo que se puede definir con herencia múltiple y está restringida a los aspectos lógicos de un elemento del sistema administrado. En la mayoría de los escenarios, la relación de identidad viene determinada por la equivalencia de claves u otras propiedades de identificación de los elementos relacionados.

La asociación solo debe usarse en escenarios que se entiendan bien, lo que permite una definición y una aclaración más concretas en subclases. Un escenario en el que la relación es razonable, por ejemplo, representa un dispositivo que es una entidad de bus y una entidad funcional donde el dispositivo es una entidad USB (bus) y teclado (funcional).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Miembros

La **clase \_ LogicalIdentity de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ LogicalIdentity de CIM** tiene estas propiedades.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ CIM LogicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a un aspecto alternativo de la entidad del sistema.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ CIM LogicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a un aspecto del elemento lógico.

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase. Para las clases derivadas de **\_ CIM LogicalIdentity,** vea [Clases win32.](win32-provider.md)

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




