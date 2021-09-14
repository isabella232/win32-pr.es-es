---
title: source (atributo)
description: El atributo \ source\ indica que un miembro de una coclase, propiedad o método es un origen de eventos. Para un miembro de una coclase, este atributo significa que se llama al miembro en lugar de implementarse.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- atributo de origen MIDL
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621e97fd20b6b96d275044dc7cbe701faee29712
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159379"
---
# <a name="source-attribute"></a>source (atributo)

El **\[ atributo \]** source indica que un miembro de una [**clase ,**](coclass.md)propiedad o método es un origen de eventos. Para un miembro de una **coclase**, este atributo significa que se llama al miembro en lugar de implementarse.

``` syntax
[
    coclass-attributes
]
coclass coclass-name
{
    [source [, optional-attributes] ] statement-type statement-name; 
  [, ...]
}

[source] object-type function-name(optional-parameter-list);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*coclass-attributes* 
</dt> <dd>

Cero o más atributos que se aplicarán a la [**coclase**](coclass.md).

</dd> <dt>

*coclass-name* 
</dt> <dd>

Identificador de nombre de la [**coclase**](coclass.md).

</dd> <dt>

*optional-attributes* 
</dt> <dd>

Cero o más atributos MIDL.

</dd> <dt>

*statement-type* 
</dt> <dd>

Puede ser [**interface**](interface.md) o [**dispinterface.**](dispinterface.md)

</dd> <dt>

*statement-name* 
</dt> <dd>

Nombre de la [**interfaz o**](interface.md) [**dispinterface**](dispinterface.md).

</dd> <dt>

*object-type* 
</dt> <dd>

Tipo del objeto que devuelve el método. Este objeto es un origen de eventos.

</dd> <dt>

*function-name* 
</dt> <dd>

Nombre de un método en una [**interfaz o**](interface.md) [**dispinterface**](dispinterface.md).

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Cero o más parámetros de método.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En una propiedad o método, el atributo **\[ de \]** origen indica que el miembro devuelve un objeto o VARIANT que es un origen de eventos. El objeto implementa **IConnectionPointContainer.**

### <a name="flags"></a>Marcas

IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ SOURCE, FUNCFLAG \_ SOURCE

## <a name="examples"></a>Ejemplos

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[**Dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**Interfaz**](interface.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 