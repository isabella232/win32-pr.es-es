---
title: unique (atributo)
description: El atributo \ unique\ especifica un puntero único.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- MIDL de atributo único
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c176c9a246329b6193c97ca5ce356c2b433cb421b77b374e103778df1b79dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822035"
---
# <a name="unique-attribute"></a>unique (atributo)

El **\[ atributo \]** unique especifica un puntero único.

``` syntax
pointer_default(unique)

typedef [ unique [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef struct-or-union-declarator 
{
    [ unique [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...}

[ unique [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
    [[ [ parameter-attribute-list ] ]] type-specifier [[declarator]]
    , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ unique [[ , parameter-attribute-list ]] ] type-specifier [[declarator]]
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican al tipo. Los atributos de tipo válidos incluyen el identificador , el tipo de modificador , transmitir como ; el atributo de puntero **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[ unique \]** o **\[** [**ptr**](ptr.md); **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** y el identificador de contexto de los atributos de uso , la cadena y omitir . Separe varios atributos con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo [base](midl-base-types.md), [**struct**](struct.md), [**union**](union.md), [**enum**](enum.md) type o type identifier. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*declarator y declarator-list* 
</dt> <dd>

Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*struct-or-union-declarator* 
</dt> <dd>

Especifica un declarador de [](union.md) [**unión o estructura**](struct.md) MIDL.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican al miembro de estructura, miembro de unión o parámetro de función. Los atributos de campo válidos incluyen primero , el último es , length es , max es , size es **\[** [**\_**](first-is.md); **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[ \_ \]** **\[ \]** **\[ \_ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \]** la cadena de atributos de uso , ignore y el identificador de contexto ; el atributo de puntero ref , unique o ptr ; y el tipo de modificador de atributo union . Separe varios atributos de campo con comas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[ \] ref**, **\[ unique \]** o **\[ ptr \]**; **\[ \]** **\[ \]** **\[ \_ \]** y la cadena de atributos de uso , ignore y el identificador de contexto .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Especifica al menos un declarador de puntero al que **\[ se aplica el \]** atributo único. Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del \* designador, modificadores como **, y** el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Consta de cero o más atributos adecuados para el tipo de parámetro especificado. **\[ \_ \]** **\[ \]**  **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \] Los** atributos de parámetro pueden tomar los atributos direccionales de entrada y salida; los atributos de campo primero son , el último es , length es , max es , size es y switch type ; el atributo de puntero ref , unique o [**ptr;**](ptr.md)y el identificador de contexto de los atributos de uso y la cadena . **\[ \]** **\[ \]** El atributo usage **\[ ignore no \]** se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los atributos de puntero se pueden aplicar como atributo de tipo; como atributo de campo que se aplica a un miembro de estructura, miembro de unión o parámetro; o como un atributo de función que se aplica al tipo de valor devuelto de la función. El atributo de puntero también puede aparecer con la palabra **\[** [**clave default \_ del**](pointer-default.md) **\]** puntero.

Un puntero único tiene las siguientes características:

-   Puede tener el valor **NULL**.
-   Puede cambiar durante una llamada de **NULL** a **non-NULL**, de non- NULL a **NULL** o de un valor distinto de **NULL** a otro.
-   Puede asignar nueva memoria en el cliente. Cuando el puntero único cambia de **NULL** a no **NULL,** los datos devueltos desde el servidor se escriben en un nuevo almacenamiento.
-   Puede usar la memoria existente en el cliente sin asignar memoria nueva. Cuando un puntero único cambia durante una llamada de un valor distinto de **NULL** a otro, se supone que el puntero apunta a un objeto de datos del mismo tipo. Los datos devueltos desde el servidor se escriben en el almacenamiento existente especificado por el valor del puntero único antes de la llamada.
-   Puede tener memoria huérfana en el cliente. La memoria a la que hace referencia un puntero único distinto de **NULL** nunca se puede liberar si el puntero único cambia a **NULL** durante una llamada y el cliente no tiene otro medio de desreferenciar el almacenamiento.
-   No provoca alias. Al igual que el almacenamiento al que apunta un puntero de referencia, no se puede acceder al almacenamiento al que apunta un puntero único desde ningún otro nombre de la función.

Los códigos auxiliares llaman a las funciones de administración de memoria proporcionadas por el usuario [**midl \_ user \_ allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function) y [**midl \_ user \_ free**](/windows/desktop/Rpc/the-midl-user-free-function) para asignar y desasignar la memoria necesaria para punteros únicos y sus referenciadores.

Las restricciones siguientes se aplican a los punteros únicos:

-   El **\[ atributo único \]** no se puede aplicar a parámetros de identificador de enlace [**\_ (identificador t)**](handle-t.md)y parámetros de identificador de contexto.
-   El **\[ \] atributo** único no se puede aplicar a los parámetros de puntero de nivel superior (parámetros que **\[** [](out-idl.md) **\]** solo tienen el **\[ atributo direccional \]** out).
-   De forma predeterminada, los punteros de nivel superior de las listas de parámetros son **\[** [**punteros ref.**](ref.md) **\]** Esto es cierto incluso si la interfaz especifica **el puntero \_ default(unique)**. Los parámetros de nivel superior de las listas de parámetros deben especificarse con el **\[ atributo único \]** para que sea un puntero único.
-   Los punteros únicos no se pueden usar para describir el tamaño de una matriz o un arm de unión porque los punteros únicos pueden tener el valor **NULL**. Esta restricción evita el error que se produce si se usa un valor **NULL** como tamaño de matriz o tamaño union-arm.

## <a name="examples"></a>Ejemplos

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
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

[**handle \_ t**](handle-t.md)
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

[midl \_ user \_ allocate](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[midl \_ user \_ free](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**valor \_ predeterminado del puntero**](pointer-default.md)
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

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**Unión**](union.md)
</dt> </dl>

 

 