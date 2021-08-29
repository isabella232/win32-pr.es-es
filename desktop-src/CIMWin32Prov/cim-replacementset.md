---
description: La clase CIM \_ ReplacementSet agrega elementos físicos que se deben reemplazar juntos.
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: CIM_ReplacementSet clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9fc82a4e710eb3b76d526b1efd254596018610280e214b2b13fc00c9c4055916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920345"
---
# <a name="cim_replacementset-class"></a>Clase \_ ReplacementSet de CIM

La **clase CIM \_ ReplacementSet** agrega elementos físicos que se deben reemplazar juntos. Por ejemplo, al reemplazar una tarjeta de memoria, también se pueden quitar y reemplazar los chips de memoria del componente. O bien, esta asociación se puede usar para reemplazar o actualizar un conjunto de chips de memoria.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM ReplacementSet** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM ReplacementSet** tiene estas propiedades.

<dl> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena de forma libre que especifica información relacionada con esta clase. La finalidad del conjunto, o información relacionada con cómo se reemplazan los elementos del componente, se puede incluir en esta propiedad.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadena de forma libre que define una etiqueta para esta propiedad. Esta propiedad es la clave del objeto .

</dd> </dl>

## <a name="remarks"></a>Comentarios

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



 

