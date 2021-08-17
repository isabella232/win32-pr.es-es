---
title: source (atributo)
description: El atributo \ source\ indica que un miembro de una coclase, propiedad o método es un origen de eventos. Para un miembro de una coclase, este atributo significa que se llama al miembro en lugar de implementarse.
ms.assetid: fbd5411a-e614-4643-810a-f3765e7ec16d
keywords:
- MIDL del atributo de origen
topic_type:
- apiref
api_name:
- source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f7039505846d7a35bbd0e077456905c0d29ad13be398fe673ca5c1f8da25e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066685"
---
# <a name="source-attribute"></a>source (atributo)

El **\[ atributo \]** source indica que un miembro de una [**coclase**](coclass.md), propiedad o método es un origen de eventos. Para un miembro de una **coclase**, este atributo significa que se llama al miembro en lugar de implementarse.

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

Puede ser [**interface**](interface.md) o [**dispinterface**](dispinterface.md).

</dd> <dt>

*statement-name* 
</dt> <dd>

Nombre de la [**interfaz o**](interface.md) [**dispinterface**](dispinterface.md).

</dd> <dt>

*object-type* 
</dt> <dd>

Tipo del objeto que devuelve el método. Este objeto es un origen de eventos.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre de un método en una [**interfaz o**](interface.md) [**dispinterface**](dispinterface.md).

</dd> <dt>

*optional-parameter-list* 
</dt> <dd>

Cero o más parámetros de método.

</dd> </dl>

## <a name="remarks"></a>Comentarios

En una propiedad o método, el atributo **\[ de \]** origen indica que el miembro devuelve un objeto o VARIANT que es un origen de eventos. El objeto implementa **IConnectionPointContainer**.

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

 

 