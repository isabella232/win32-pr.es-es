---
title: ref (atributo)
description: El atributo \ ref\ identifica un puntero de referencia. Se usa simplemente para representar un nivel de direccionamiento indirecto.
ms.assetid: db4ff938-0f38-4f77-bb65-f728ffd609e0
keywords:
- atributo ref MIDL
topic_type:
- apiref
api_name:
- ref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc5762eea78b3ce73ab3db58e9bb567b051675
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159399"
---
# <a name="ref-attribute"></a>ref (atributo)

El **\[ atributo ref \]** identifica un puntero de referencia. Se usa simplemente para representar un nivel de direccionamiento indirecto.

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

*type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo. Los atributos de tipo válidos incluyen el identificador , el tipo de modificador , transmitir como ; los atributos de puntero **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[ ref \]**, **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** y el identificador de contexto de los atributos de uso , la cadena y omitir . Separe varios atributos con comas.

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

Especifica cero o más atributos de campo que se aplican a la estructura, miembro de unión o parámetro de función. Los atributos de campo válidos incluyen primero , el último es , length es , max es , size es ; la cadena de atributos de uso , ignore y el identificador de contexto ; el atributo de puntero **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[ ref \]**, unique **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** **\[** [**\_**](switch-type.md) **\]** o ptr ; y el tipo de modificador de atributo union . Separe varios atributos de campo con comas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[ \] ref**, **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** y la cadena de atributos de uso , ignore y el identificador de contexto .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Especifica al menos un declarador de puntero al que se aplica el atributo **\[ ref. \]** Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del \* designador, modificadores como **, y** el calificador [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Consta de cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos de parámetro pueden tomar los atributos direccionales de entrada y salida; los atributos de campo primero son , el último es , length es , max es , size es y switch type ; el atributo de puntero **\[** [](in.md) **\]** **\[** [](out-idl.md) **\]** **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[ ref \]**, unique o **\[** [](unique.md) **\]** **\[** [**ptr;**](ptr.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** y el identificador de contexto de los atributos de uso y la cadena . El atributo usage **\[** [**ignore no**](ignore.md) **\]** se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un atributo de puntero se puede aplicar como atributo de tipo, como atributo de campo que se aplica a un miembro de estructura, miembro de unión o parámetro; o como un atributo de función que se aplica al tipo de valor devuelto de la función. El atributo de puntero también puede aparecer con la palabra **\[** [**clave default \_ del**](pointer-default.md) **\]** puntero.

Un puntero de referencia tiene las siguientes características:

-   Siempre apunta al almacenamiento válido; nunca tiene el valor **NULL**. Siempre se puede desreferenciar un puntero de referencia.
-   Nunca cambia durante una llamada. Un puntero de referencia siempre apunta al mismo almacenamiento en el cliente antes y después de la llamada.
-   No asigna nueva memoria en el cliente. Los datos devueltos desde el servidor se escriben en el almacenamiento existente especificado por el valor del puntero de referencia antes de la llamada.
-   No provoca alias. Storage a la que apunta un puntero de referencia no se puede acceder desde ningún otro nombre de la función.

Un puntero de referencia no se puede usar como el tipo de un puntero devuelto por una función.

Si no se especifica ningún atributo para un parámetro de puntero de nivel superior, se trata como un puntero de referencia.

## <a name="examples"></a>Ejemplos

``` syntax
[unique] char * GetFirstName( 
    [in, ref] char * pszFullName);
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

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
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

 

 