---
title: ptr (atributo)
description: El atributo \ PTR \ designa un puntero como puntero completo.
ms.assetid: a1233a25-b651-4a01-8abf-a64dc9ee168e
keywords:
- atributo de PTR (MIDL)
topic_type:
- apiref
api_name:
- ptr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2d8b2ee2e3ea4daccd1c4fa37ff1c1f1899dd3c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358862"
---
# <a name="ptr-attribute"></a>ptr (atributo)

El atributo **\[ ptr \]** designa un puntero como puntero completo.

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

*lista de atributos de tipo* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo. Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md)o **\[ ptr \]**; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un tipo [base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md)o un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador estándar* 
</dt> <dd>

Especifica un declarador estándar de C, como un identificador, un declarador de puntero o un declarador de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican al parámetro de la estructura o miembro de la Unión o de la función. Entre los atributos de campo válidos se incluyen **\[** [**First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)es, **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[ \] ptr** y el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** . Separe varios atributos de campo con comas.

</dd> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[ ptr \]**; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Especifica al menos un declarador de puntero al que se aplica el atributo **\[ ptr \]** . Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Consta de cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos [**de**](in.md) parámetro pueden tomar los atributos direccionales [**hacia y hacia afuera**](out-idl.md); los atributos de campo [**primero \_ son**](first-is.md), [**Last \_ es**](last-is.md), [**length \_**](length-is.md)es, [**Max \_ is**](max-is.md), [**size \_ is**](size-is.md)y [**Switch \_ Type**](switch-type.md); el atributo de puntero [**ref**](ref.md), [**Unique**](unique.md)o **\[ ptr \]**; y el identificador de [**contexto \_**](context-handle.md) y la [**cadena**](string.md)de atributos de uso. El atributo de uso [**Ignore**](ignore.md) no se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El puntero completo designado por el atributo **\[ ptr \]** se aproxima a la funcionalidad completa del puntero del lenguaje C. El puntero completo puede tener el valor **null** y puede cambiar durante la llamada de **null** a un valor distinto de **null**. Otros nombres de la aplicación que admiten el alias y los ciclos pueden alcanzar el almacenamiento señalado por punteros completos. Esta funcionalidad requiere más sobrecarga durante una llamada a procedimiento remoto para identificar los datos a los que hace referencia el puntero, determinar si el valor es **null** y detectar si dos punteros apuntan a los mismos datos.

Usar punteros completos para:

-   Valores devueltos remotos.
-   Punteros dobles, cuando no se conoce el tamaño de un parámetro de salida.
-   Punteros **nulos** .

Los punteros completos (y únicos) no se pueden usar para describir el tamaño de una matriz o unión porque estos punteros pueden tener el valor **null**. Esta restricción de MIDL evita un error que puede producirse cuando se utiliza un valor **null** como tamaño.

Se supone que los punteros de referencia y únicos no causan ningún alias de datos. Un grafo dirigido obtenido al iniciarse a partir de un puntero único o de referencia y seguir solo los punteros únicos o de referencia no contiene ninguna reconvergencia ni ciclos.

Para evitar el alias, todos los valores de puntero deben obtenerse a partir de un puntero de entrada de la misma clase de puntero. Si hay más de un puntero que apunta a la misma ubicación de memoria, todos los punteros deben ser punteros completos.

En algunos casos, se pueden mezclar punteros completos y únicos. A un puntero completo se le puede asignar el valor de un puntero único, siempre y cuando la asignación no infrinja las restricciones sobre el cambio del valor de un puntero único. Sin embargo, cuando se asigna un puntero único al valor de un puntero completo, puede producirse un alias.

La combinación de punteros completos y únicos puede producir el alias, tal como se muestra en el ejemplo siguiente:

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

Aunque "t->left" y "t->Right" apuntan a ubicaciones de memoria únicas, "t->Left->pdata" y "t->correcto->pdata" tienen alias. Por esta razón, los algoritmos de compatibilidad con alias deben seguir todos los punteros (incluidos los punteros únicos y de referencia) que puedan llegar a un puntero completo.

## <a name="examples"></a>Ejemplos

``` syntax
pointer_default(ptr) 
 
typedef [ptr, string] unsigned char * MY_STRING_TYPE; 
 
[ptr] char * MyFunction([in, out, unique] long * plNumber);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Atributos array y Sized-Pointer](array-and-sized-pointer-attributes.md)
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

[**asa**](handle.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**omitir**](ignore.md)
</dt> <dt>

[**última \_ es**](last-is.md)
</dt> <dt>

[**la longitud \_ es**](length-is.md)
</dt> <dt>

[**localizar**](local.md)
</dt> <dt>

[**Max \_ es**](max-is.md)
</dt> <dt>

[**puntero \_ predeterminado**](pointer-default.md)
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

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**Unión**](union.md)
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 