---
title: unique (atributo)
description: El atributo \ Unique \ especifica un puntero único.
ms.assetid: 0d668148-e65a-478f-9e47-2528d3caa84c
keywords:
- único atributo MIDL
topic_type:
- apiref
api_name:
- unique
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b839a2abdd546842ef0d33d45a31428af840f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665781"
---
# <a name="unique-attribute"></a>unique (atributo)

El atributo **\[ Unique \]** especifica un puntero único.

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

*lista de atributos de tipo* 
</dt> <dd>

Especifica uno o más atributos que se aplican al tipo. Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** y **\[** [**Ignore**](ignore.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador y lista de declaradores* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea matrices [y Sized-Pointer atributos](array-and-sized-pointer-attributes.md) [**, matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*struct-or-Union-declarator* 
</dt> <dd>

Especifica un [**destructor**](struct.md) o un declarador de [**Unión**](union.md) de MIDL.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican al miembro de estructura, miembro de unión o parámetro de función. Entre los atributos de campo válidos se incluyen **\[** [**First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)es, **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[ \] cadena**, **\[ \] omitir** y **\[ \_ \] identificador de contexto**; el atributo de puntero **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]** y el **\[ \_ tipo \] de modificador** de atributo Union. Separe varios atributos de campo con comas.

</dd> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[ \] Unique** o **\[ ptr \]**; y los atributos de uso **\[ cadena \]**, **\[ omitir \]** y **\[ \_ identificador \] de contexto**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Especifica al menos un declarador de puntero al que se aplica el atributo **\[ único \]** . Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Consta de cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos **\[ de \]** parámetro pueden tomar los atributos direccionales hacia dentro y **\[ hacia \] fuera**; los atributos de campo **\[ primero \_ son \]**, **\[ Last \_ es \]**, **\[ length \_ \]** is, **\[ Max \_ is \]**, **\[ size \_ is \]** y **\[ Switch \_ Type \]**; el atributo de puntero **\[ ref \]**, **Unique** o [**ptr**](ptr.md); y el **\[ \_ identificador \] de contexto** y la **\[ cadena \]** de atributos de uso. El atributo de uso **\[ Ignore \]** no se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los atributos de puntero se pueden aplicar como un atributo de tipo. como atributo de campo que se aplica a un miembro de estructura, miembro de unión o parámetro; o como un atributo de función que se aplica al tipo de valor devuelto de la función. El atributo Pointer también puede aparecer con la **\[** palabra clave [**\_ default del puntero**](pointer-default.md) **\]** .

Un puntero único tiene las siguientes características:

-   Puede tener el valor **null**.
-   Puede cambiar durante una llamada de **null** a un valor **distinto de NULL, de** un valor distinto de **null** a **null** o de un valor distinto de **null** a otro.
-   Puede asignar memoria nueva en el cliente. Cuando el puntero único cambia de **null** a no **null**, los datos devueltos del servidor se escriben en el nuevo almacenamiento.
-   Puede utilizar la memoria existente en el cliente sin asignar memoria nueva. Cuando un puntero único cambia durante una llamada de un valor distinto de **null** a otro, se supone que el puntero apunta a un objeto de datos del mismo tipo. Los datos devueltos del servidor se escriben en el almacenamiento existente especificado por el valor del puntero único antes de la llamada.
-   Puede haber memoria huérfana en el cliente. La memoria a la que hace referencia un puntero único no **nulo** nunca se puede liberar si el puntero único cambia a **null** durante una llamada y el cliente no tiene otro medio para desreferenciar el almacenamiento.
-   No provoca el alias. Al igual que el almacenamiento señalado por un puntero de referencia, no se puede alcanzar el almacenamiento señalado por un puntero único desde cualquier otro nombre de la función.

El código auxiliar llama a las funciones de administración de memoria proporcionadas por el usuario [**MIDL \_ \_ asignar**](/windows/desktop/Rpc/the-midl-user-allocate-function) y [**\_ \_ liberar**](/windows/desktop/Rpc/the-midl-user-free-function) al usuario de MIDL para asignar y desasignar la memoria necesaria para los punteros únicos y sus correspondientes.

Las restricciones siguientes se aplican a los punteros únicos:

-   El atributo **\[ Unique \]** no se puede aplicar a los parámetros de identificador de enlace ( [**Handle \_ t**](handle-t.md)) y de identificador de contexto.
-   El atributo **\[ Unique \]** no se puede aplicar a **\[** [](out-idl.md) **\]** parámetros de puntero de nivel superior solo out (parámetros que solo tienen el atributo Direction de **\[ salida \]** ).
-   De forma predeterminada, los punteros de nivel superior de las listas de parámetros son **\[** [](ref.md) **\]** punteros de referencia. Esto es así incluso si la interfaz especifica **el \_ valor predeterminado del puntero (único)**. Los parámetros de nivel superior de las listas de parámetros deben especificarse con el atributo **\[ Unique \]** como un puntero único.
-   No se pueden usar punteros únicos para describir el tamaño de una matriz o un brazo de Unión porque los punteros únicos pueden tener el valor **null**. Esta restricción evita el error que se produce si se usa un valor **null** como tamaño de la matriz o el tamaño de la Unión-ARM.

## <a name="examples"></a>Ejemplos

``` syntax
pointer_default(unique) 
 
typedef [unique, string] unsigned char * MY_STRING_TYPE; 
 
[unique] char * MyFunction([in, out, unique] long * plNumber);
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

[**identificador \_ t**](handle-t.md)
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

[\_asignación de usuarios de MIDL \_](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[usuario de MIDL \_ \_ gratis](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**puntero \_ predeterminado**](pointer-default.md)
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

[**transmitir \_ como**](transmit-as.md)
</dt> <dt>

[**Unión**](union.md)
</dt> </dl>

 

 