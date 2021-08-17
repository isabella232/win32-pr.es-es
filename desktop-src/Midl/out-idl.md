---
title: out (atributo)
description: El atributo \ out\ identifica los parámetros de puntero que se devuelven desde el procedimiento llamado al procedimiento que realiza la llamada (desde el servidor al cliente).
ms.assetid: f92ef78a-321b-460e-a18a-b63a5e199ad0
keywords:
- atributo out MIDL
topic_type:
- apiref
api_name:
- out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32bdbd18c6412f943a124a62badb9c154fa9aeb64573919970ffc1dc4af17798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066805"
---
# <a name="out-attribute"></a>out (atributo)

El atributo out identifica los parámetros de puntero que se devuelven del procedimiento llamado al procedimiento de llamada \[  \] (del servidor al cliente).

``` syntax
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ out [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero \[ [](callback.md) \] \[ [](local.md) \] \[ [**ref**](ref.md) \] , \[ [**unique**](unique.md) \] o \[ [**ptr**](ptr.md); \] \[ [](string.md) \] \[ [](ignore.md) \] \[ [**\_**](context-handle.md) \] y la cadena de atributos de uso , ignore y el identificador de contexto .

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo base , [**struct**](struct.md), [**union**](union.md)o [**tipo de enumeración**](enum.md) o identificador de tipo. [ \_](midl-base-types.md) Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*pointer-declarator* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del \* designador, modificadores como **, y** el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Especifica cero o más atributos adecuados para un tipo de parámetro especificado. Los atributos de parámetro con el atributo out también pueden sacar el atributo direccional; los atributos de campo primero son , el último es , length es , max es , size es y switch type ; el atributo de puntero \[  \] \[  \] \[ [**\_**](first-is.md) \] \[ [**\_**](last-is.md) \] \[ [**\_**](length-is.md) \] \[ [**\_**](max-is.md) \] \[ [**\_**](size-is.md) \] \[ [**\_**](switch-type.md) \] \[ [**ref**](ref.md) \] , \[ [**unique**](unique.md) \] o \[ [**ptr**](ptr.md); \] \[ [**\_**](context-handle.md) \] \[ [](string.md) \] y el identificador de contexto de los atributos de uso y la cadena . El atributo usage \[ [**ignore no**](ignore.md) \] se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> <dt>

*declarador* 
</dt> <dd>

Especifica los declaradores estándar, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). El declarador de parámetros del declarador de función, como el nombre del parámetro, es opcional.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El atributo out indica que un parámetro que actúa como puntero y sus datos asociados en memoria se van a devolver desde el procedimiento llamado al \[  \] procedimiento que realiza la llamada.

El \[ **atributo out** \] debe ser un puntero. Los compiladores IDL de DCE requieren la presencia de un declarador explícito como \* puntero en la declaración de parámetros. Microsoft IDL ofrece una extensión que elimina este requisito y permite una matriz o un tipo de puntero definido previamente.

Un atributo relacionado, en , indica que el parámetro se pasa del procedimiento que realiza la llamada \[ [](in.md) \] al procedimiento llamado. Los \[ **atributos de** \] entrada \[ **y** salida especifican la dirección \] en la que se pasan los parámetros. Un parámetro se puede definir como \[ **en** \] -only, \[ **out** \] -only o \[ **en**, **out** \] .

Se supone que un parámetro out -only no está definido cuando se llama al procedimiento remoto y el servidor asigna la \[  \] memoria para el objeto. Puesto que el puntero o los parámetros de nivel superior siempre deben apuntar al almacenamiento válido y, por tanto, no pueden ser **NULL,** no se puede aplicar out a punteros únicos o \[  \] \[ [](unique.md) \] \[ [**ptr de**](ptr.md) \] nivel superior. Los parámetros que \[ **son** \] \[ punteros **únicos o ptr** deben estar \] \[ [**en**](in.md) \] o \[ **en** parámetros de **salida.** \]

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT MyFunction([out] short * pcount);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**en \_ primer lugar es**](first-is.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**el \_ último es**](last-is.md)
</dt> <dt>

[**length \_ es**](length-is.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> <dt>

[**Estructura**](struct.md)
</dt> <dt>

[**tipo \_ de conmutador**](switch-type.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 