---
title: atributo de solo lectura
description: El atributo \ readonly\ prohíbe la asignación a una variable.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- MIDL de atributo de solo lectura
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159404"
---
# <a name="readonly-attribute"></a>atributo de solo lectura

El **\[ atributo \] readonly** prohíbe la asignación a una variable.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*optional-attributes* 
</dt> <dd>

Cero o más atributos MIDL.

</dd> <dt>

*tipo de datos* 
</dt> <dd>

Tipo de los datos contenidos por el *identificador*.

</dd> <dt>

*identifier* 
</dt> <dd>

Nombre por el que el software puede hacer referencia a la ubicación de almacenamiento de datos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo \] readonly** prohíbe la asignación a una variable. **\[ Readonly \]** solo se admite en el nivel de parámetro, no en el nivel de método.

### <a name="flags"></a>Marcas

VARFLAG \_ FREADONLY

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 