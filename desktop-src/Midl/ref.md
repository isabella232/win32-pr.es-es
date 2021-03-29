---
title: ref (atributo)
description: El atributo \ Ref \ identifica un puntero de referencia. Se usa simplemente para representar un nivel de direccionamiento indirecto.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- parámetro de referencia MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904535"
---
# <a name="ref-attribute"></a>ref (atributo)

El atributo **\[ ref \]** identifica un puntero de referencia. Se usa simplemente para representar un nivel de direccionamiento indirecto.

``` syntax
pointer_default(ref)

typedef [ ref [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ ref [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ ref [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo. Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; los atributos de puntero **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** . Separe varios atributos con comas.

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

Especifica cero o más atributos de campo que se aplican a la estructura, el miembro de unión o el parámetro de función. Entre los atributos de campo válidos se incluyen **\[** [**First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)es, **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** y el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** . Separe varios atributos de campo con comas.

</dd> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[ \] ref**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** .

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Especifica al menos un declarador de puntero al que se aplica el atributo **\[ ref \]** . Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Consta de cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos de parámetro pueden tomar los atributos direccionales **\[** [](in.md) **\]** hacia dentro y **\[** [**hacia fuera**](out-idl.md) **\]** ; los atributos de campo **\[** [**primero \_ son**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , length is, **\[** [**\_**](length-is.md) **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ is**](size-is.md) **\]** y **\[** [**Switch \_ Type**](switch-type.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el **\[** [**\_ identificador de contexto**](context-handle.md) y la **\]** **\[** [**cadena**](string.md) **\]** de atributos de uso. El atributo de uso **\[** [**Ignore**](ignore.md) **\]** no se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un atributo de puntero se puede aplicar como atributo de tipo, como un atributo de campo que se aplica a un miembro de estructura, miembro de unión o parámetro. o como un atributo de función que se aplica al tipo de valor devuelto de la función. El atributo Pointer también puede aparecer con la **\[** palabra clave [**\_ default del puntero**](pointer-default.md) **\]** .

Un puntero de referencia tiene las siguientes características:

-   Siempre apunta a un almacenamiento válido; nunca tiene el valor **null**. Siempre se puede desreferenciar un puntero de referencia.
-   Nunca cambia durante una llamada. Un puntero de referencia siempre apunta al mismo almacenamiento en el cliente antes y después de la llamada.
-   No asigna memoria nueva en el cliente. Los datos devueltos del servidor se escriben en el almacenamiento existente especificado por el valor del puntero de referencia antes de la llamada.
-   No provoca el alias. No se puede alcanzar el almacenamiento señalado por un puntero de referencia desde cualquier otro nombre de la función.

No se puede usar un puntero de referencia como el tipo de un puntero devuelto por una función.

Si no se especifica ningún atributo para un parámetro de puntero de nivel superior, se trata como un puntero de referencia.

## <a name="examples"></a>Ejemplos

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
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

[**enuncia**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
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

 

 