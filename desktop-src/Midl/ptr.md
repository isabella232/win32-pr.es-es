---
title: ptr (atributo)
description: El atributo \ ptr\ designa un puntero como puntero completo.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- MidL del atributo ptr
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159406"
---
# <a name="ptr-attribute"></a>ptr (atributo)

El **\[ atributo \] ptr** designa un puntero como puntero completo.

``` syntax
pointer_default(ptr)

typedef [ ptr [ , type-attribute-list ] ] type-specifier declarator-list; 

typedef [ struct | union ]
{
    [ ptr [ , field-attribute-list ] ] type-specifier declarator-list;
    ...
}

[ ptr [ , function-attribute-list ] ] type-specifier ptr-decl function-name(
    [ [ parameter-attribute-list ] ] type-specifier [standard-declarator]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ptr [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo. Los atributos de tipo válidos incluyen el identificador , el tipo de modificador , transmitir como ; el atributo de puntero **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md)o **\[ ptr \]**; **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** y el identificador de contexto de los atributos de uso , la cadena y omitir . Separe varios atributos con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo [base](midl-base-types.md), [**struct**](struct.md), [**unión**](union.md)o tipo [**de enumeración**](enum.md) o identificador de tipo. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*standard-declarator* 
</dt> <dd>

Especifica un declarador de C estándar, como un identificador, un declarador de puntero o un declarador de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md), and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican al parámetro de función o miembro de estructura o unión. Los atributos de campo válidos incluyen primero , el último es , length es , max es , size es ; la cadena de atributos de uso , ignore y el identificador de contexto ; el atributo de puntero ref , unique o **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[ ptr \]**; **\[** [**\_**](switch-type.md) **\]** y el tipo de modificador de atributo union . Separe varios atributos de campo con comas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[ ptr \]**; **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** y la cadena de atributos de uso , ignore y el identificador de contexto .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Especifica al menos un declarador de puntero al que se aplica el atributo **\[ ptr. \]** Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del \* designador, modificadores como **, y** el calificador [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Consta de cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos de parámetro pueden tomar los atributos [**direccionales dentro**](in.md) y [**fuera**](out-idl.md)de ; los atributos de campo primero son [**, \_**](first-is.md)el último es [**, \_**](last-is.md)length es [**\_ ,**](length-is.md) [**\_**](context-handle.md) max es , size es y [**switch \_ type**](switch-type.md); el atributo de puntero [**ref**](ref.md), [**unique**](unique.md)o **\[ \] ptr**; y el identificador de contexto de los atributos de uso y la [**cadena**](string.md). [**\_**](max-is.md) [**\_**](size-is.md) El atributo usage [**ignore no**](ignore.md) se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El puntero completo designado por el **\[ atributo ptr \]** se aproxima a la funcionalidad completa del puntero en lenguaje C. El puntero completo puede tener el valor **NULL** y puede cambiar durante la llamada de **NULL** a **non-NULL.** Storage punteros completos a los que apuntan otros nombres de la aplicación que admiten alias y ciclos. Esta funcionalidad requiere más sobrecarga durante una llamada a procedimiento remoto para identificar los datos a los que hace referencia el puntero, determinar si el valor es **NULL** y detectar si dos punteros apuntan a los mismos datos.

Use punteros completos para:

-   Valores devueltos remotos.
-   Punteros dobles, cuando no se conoce el tamaño de un parámetro de salida.
-   **Punteros NULL.**

No se pueden usar punteros completos (y únicos) para describir el tamaño de una matriz o unión porque estos punteros pueden tener el valor **NULL**. Esta restricción de MIDL evita un error que puede producirse cuando se usa un valor **NULL** como tamaño.

Se supone que los punteros únicos y de referencia no provocan ningún alias de los datos. Un gráfico dirigido obtenido a partir de un puntero único o de referencia y siguiendo solo punteros únicos o de referencia no contiene ninguna reconvergencia ni ciclos.

Para evitar el alias, todos los valores de puntero deben obtenerse de un puntero de entrada de la misma clase de puntero. Si más de un puntero apunta a la misma ubicación de memoria, todos estos punteros deben ser punteros completos.

En algunos casos, se pueden mezclar punteros completos y únicos. Se puede asignar a un puntero completo el valor de un puntero único, siempre y cuando la asignación no infrinja las restricciones para cambiar el valor de un puntero único. Sin embargo, al asignar a un puntero único el valor de un puntero completo, puede provocar alias.

La combinación de punteros completos y únicos puede provocar alias, como se muestra en el ejemplo siguiente:

``` syntax
typedef struct 
{ 
    [ptr] short * pdata;          // full pointer  
} GRAPH_NODE_TYPE; 
 
typedef struct 
{ 
    [unique] graph_node * left;   // unique pointer  
    [unique] graph_node * right;  // unique pointer 
} TREE_NODE_TYPE; 
 
// application code: 
short a = 5; 
TREE_NODE_TYPE * t; 
GRAPH_NODE_TYPE g, h; 
 
g.pdata = h.pdata = &a; 
t->left = &g; 
t->right = &h; 
// t->left->pdata == t->right->pdata == &a
```

Aunque "t->left" y "t->right" apuntan a ubicaciones de memoria únicas, "t->left->pdata" y "t->right->pdata" tienen alias. Por esta razón, los algoritmos de compatibilidad con alias deben seguir todos los punteros (incluidos los punteros únicos y de referencia) que pueden llegar finalmente a un puntero completo.

## <a name="examples"></a>Ejemplos

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos de matriz Sized-Pointer matriz](array-and-sized-pointer-attributes.md)
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

[**en primer \_ lugar es**](first-is.md)
</dt> <dt>

[**handle**](handle.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorar**](ignore.md)
</dt> <dt>

[**el \_ último es**](last-is.md)
</dt> <dt>

[**length \_ es**](length-is.md)
</dt> <dt>

[**Local**](local.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**valor \_ predeterminado del puntero**](pointer-default.md)
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

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**union**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 