---
title: source (atributo)
description: El atributo \ Source \ indica que un miembro de una coclase, propiedad o método es un origen de eventos. Para un miembro de una coclase, este atributo significa que se llama al miembro en lugar de implementarlo.
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
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995130"
---
# <a name="source-attribute"></a>source (atributo)

El atributo de **\[ origen \]** indica que un miembro de una [**coclase**](coclass.md), propiedad o método es un origen de eventos. Para un miembro de una **coclase**, este atributo significa que se llama al miembro en lugar de implementarlo.

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

*coclase: atributos* 
</dt> <dd>

Cero o más atributos que se aplicarán a la [**coclase**](coclass.md).

</dd> <dt>

*nombre de coclase* 
</dt> <dd>

Identificador de nombre de la [**coclase**](coclass.md).

</dd> <dt>

*opcional: atributos* 
</dt> <dd>

Cero o más atributos de MIDL.

</dd> <dt>

*tipo de instrucción* 
</dt> <dd>

Puede ser [**interface**](interface.md) o [**dispinterface**](dispinterface.md).

</dd> <dt>

*nombre de instrucción* 
</dt> <dd>

Nombre de la [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).

</dd> <dt>

*tipo de objeto* 
</dt> <dd>

Tipo del objeto que devuelve el método. Este objeto es un origen de eventos.

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Nombre de un método en una [**interfaz**](interface.md) o [**dispinterface**](dispinterface.md).

</dd> <dt>

*opcional-parameter-list* 
</dt> <dd>

Cero o más parámetros de método.

</dd> </dl>

## <a name="remarks"></a>Observaciones

En una propiedad o método, el atributo de **\[ origen \]** indica que el miembro devuelve un objeto o una variante que es un origen de eventos. El objeto implementa **IConnectionPointContainer**.

### <a name="flags"></a>Marcas

IMPLTYPEFLAG \_ FSOURCE, VARFLAG \_ source, FUNCFLAG \_ source

## <a name="examples"></a>Ejemplos

``` syntax
[default, source] dispinterface DIMyFaceAdviseSink;
[source]interface IMyFaceAdviseSink;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**coclase**](coclass.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**interfaz**](interface.md)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 