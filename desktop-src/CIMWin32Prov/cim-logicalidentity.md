---
description: La \_ clase CIM LogicalIdentity es una asociación abstracta y genérica que indica que dos elementos lógicos representan distintos aspectos de la misma entidad subyacente.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: CIM_LogicalIdentity (clase) (proveedores WMI de CIMWin32)
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
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998171"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a>CIM_LogicalIdentity (clase) (proveedores WMI de CIMWin32)

La clase **CIM \_ LogicalIdentity** es una asociación abstracta y genérica que indica que dos elementos lógicos representan distintos aspectos de la misma entidad subyacente. La Asociación transmite lo que se puede definir con varias herencia y está restringido a los aspectos lógicos de un elemento del sistema administrado. En la mayoría de los escenarios, la relación de identidad viene determinada por la equivalencia de claves u otras propiedades de identificación de los elementos relacionados.

La Asociación solo se debe usar en escenarios que se hayan entendido bien, lo que permite una mayor definición y aclaración concretas en las subclases. Un escenario en el que la relación es razonable, por ejemplo, representa un dispositivo que es una entidad de bus y una entidad funcional en la que el dispositivo es una entidad USB (bus) y de teclado (funcional).

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

La clase **CIM \_ LogicalIdentity** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ LogicalIdentity** tiene estas propiedades.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a un aspecto alternativo de la entidad del sistema.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a un aspecto del elemento lógico.

</dd> </dl>

## <a name="remarks"></a>Observaciones

WMI no implementa esta clase. Para las clases derivadas de **CIM \_ LogicalIdentity**, vea [clases Win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




