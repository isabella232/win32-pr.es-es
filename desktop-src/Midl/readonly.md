---
title: atributo de solo lectura
description: El atributo \ ReadOnly \ prohíbe la asignación a una variable.
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- atributo de solo lectura MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995206"
---
# <a name="readonly-attribute"></a>atributo de solo lectura

El atributo **\[ ReadOnly \]** prohíbe la asignación a una variable.

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*opcional: atributos* 
</dt> <dd>

Cero o más atributos de MIDL.

</dd> <dt>

*tipo de datos* 
</dt> <dd>

Tipo de los datos contenidos en el *identificador*.

</dd> <dt>

*identifier* 
</dt> <dd>

Un nombre por el que el software puede hacer referencia a la ubicación de almacenamiento de datos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ ReadOnly \]** prohíbe la asignación a una variable. solo se admite **\[ ReadOnly \]** en el nivel de parámetro, no en el nivel de método.

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

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 