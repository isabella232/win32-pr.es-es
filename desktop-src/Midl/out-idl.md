---
title: out (atributo)
description: El atributo \ out \ identifica los parámetros de puntero devueltos por el procedimiento llamado al procedimiento que realiza la llamada (desde el servidor al cliente).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- out (atributo) MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b590cadeb12a77cff859991efb6356393072823
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665808"
---
# <a name="out-attribute"></a>out (atributo)

El \[  \] atributo out identifica los parámetros de puntero devueltos por el procedimiento llamado al procedimiento que realiza la llamada (desde el servidor al cliente).

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son \[ [**callback**](callback.md) \] , \[ [**local**](local.md) \] ; el atributo de puntero \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] o \[ [**ptr**](ptr.md) \] ; y los atributos de uso \[ [**cadena**](string.md) \] , \[ [**omitir**](ignore.md) \] y \[ [**\_ identificador de contexto**](context-handle.md) \] .

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [tipo \_ base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador de puntero* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Especifica cero o más atributos adecuados para un tipo de parámetro especificado. Los atributos de parámetro con el \[ atributo **out** \] también pueden sacar el atributo direccional \[  \] ; los atributos de campo \[ [**primero \_ son**](first-is.md) \] , \[ [**Last \_ es**](last-is.md) \] , \[ [**length \_**](length-is.md)es \] , \[ [**Max \_ is**](max-is.md) \] , \[ [**size \_ is**](size-is.md) \] y \[ [**Switch \_ Type**](switch-type.md) \] ; el atributo de puntero \[ [**ref**](ref.md) \] , \[ [**Unique**](unique.md) \] o \[ [**ptr**](ptr.md) \] ; y el \[ [**\_ identificador de contexto**](context-handle.md) y la \] \[ [**cadena**](string.md) \] de atributos de uso. El atributo de uso \[ [**Ignore**](ignore.md) \] no se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> <dt>

*clara* 
</dt> <dd>

Especifica los declaradores estándar, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). El declarador de parámetro del declarador de la función, como el nombre del parámetro, es opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El \[ atributo **out** \] indica que un parámetro que actúa como puntero y sus datos asociados en memoria se devolverán desde el procedimiento llamado al procedimiento que realiza la llamada.

El \[ atributo **out** \] debe ser un puntero. Los compiladores de DCE IDL requieren la presencia de un \* declarador de puntero explícito en la declaración del parámetro. Microsoft IDL ofrece una extensión que quita este requisito y permite una matriz o un tipo de puntero definido previamente.

Un atributo relacionado, \[ [**en**](in.md) \] , indica que el parámetro se pasa desde el procedimiento que realiza la llamada al procedimiento llamado. Los \[  \] atributos in y \[ **out** \] especifican la dirección en la que se pasan los parámetros. Un parámetro puede definirse como \[ solo **en**, solo \] \[ **fuera** \] o \[ **en**, **out** \] .

\[  \] Se supone que un parámetro de solo salida está sin definir cuando se llama al procedimiento remoto y el servidor asigna la memoria para el objeto. Dado que el puntero o los parámetros de nivel superior deben apuntar siempre a un almacenamiento válido y, por tanto, no pueden ser **null**, no se \[  \] puede aplicar out a \[ [](unique.md) \] punteros únicos o \[ [**ptr**](ptr.md) de nivel superior \] . Los parámetros que son \[  \] punteros únicos o \[ **ptr** \] deben estar \[ [**en**](in.md) \] \[ los parámetros **out** o in \] .

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[**el primero \_ es**](first-is.md)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**última \_ es**](last-is.md)
</dt> <dt>

[**la longitud \_ es**](length-is.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**Max \_ es**](max-is.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**el tamaño \_ es**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> <dt>

[**Destructor**](struct.md)
</dt> <dt>

[**tipo de conmutador \_**](switch-type.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 