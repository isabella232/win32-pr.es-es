---
title: string (atributo)
description: El atributo \ String \ indica que la matriz de caracteres unidimensional, WCHAR \_ t, byte (o equivalente) o el puntero a dicha matriz se debe tratar como una cadena.
ms.assetid: 379cd59e-7540-4188-9b5c-6c25a8928999
keywords:
- atributo de cadena MIDL
topic_type:
- apiref
api_name:
- string
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2bd3c56bcf09d1c47343f903653e9d83113b1d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995205"
---
# <a name="string-attribute"></a>string (atributo)

El atributo de **\[ cadena \]** indica que la matriz de [**caracteres**](char-idl.md)unidimensional, [**WCHAR \_ t**](wchar-t.md), [**byte**](byte.md) (o equivalente) o el puntero a una matriz de este tipo se deben tratar como una cadena. La cadena también puede ser una matriz (o un puntero a una matriz) de construcciones cuyos campos son todo el tipo **byte**.

``` syntax
typedef [ string [[ , type-attribute-list ]] ] type-specifier declarator-list; 

typedef [ struct | union ] 
{
    [ string [[ , field-attribute-list ]] ] type-specifier declarator-list;
    ...
};

[ string [[ , function-attribute-list ]] ] type-specifier ptr-decl function-name(
  [[ [ parameter-attribute-list ] ]] type-specifier [[standard-declarator]]
  , ...);

[[ [ function-attribute-list ] ]] type-specifier [[ptr-decl]] function-name(
    [ string [[ , parameter-attribute-list ]] ] type-specifier [[standard-declarator]]
  , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*lista de atributos de tipo* 
</dt> <dd>

Especifica uno o más atributos que se aplican a un tipo. Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** el [**\_ tipo de conmutador**](switch-type.md) **\]** , **\[** la [**transmisión \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de los atributos de uso **\[** [**\_**](context-handle.md) **\]** , **\[ String \]** y **\[** [**Ignore**](ignore.md) **\]** . Separe varios atributos con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [tipo base](midl-base-types.md), un tipo de [**estructura**](struct.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador estándar* 
</dt> <dd>

Especifica un declarador estándar de C, como un identificador, un declarador de puntero o un declarador de matriz. Para obtener más información, vea matrices [y Sized-Pointer atributos](array-and-sized-pointer-attributes.md) [**, matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*lista de declaradores* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea matrices [y Sized-Pointer atributos](array-and-sized-pointer-attributes.md) [**, matrices**](arrays-1.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican a la estructura, el miembro de unión o el parámetro de función. Los dos atributos de campo válidos son **\[** [**Max \_ is**](max-is.md) **\]** y **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[ \] cadena**, **\[ \] omitir** y **\[ \_ \] identificador de contexto**, el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[ Unique \]** o **\[** [**ptr**](ptr.md) **\]** y el **\[ \_ tipo \] de modificador** de atributo Union. Separe varios atributos de campo con comas.

</dd> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[ \] Unique** o **\[ ptr \]**; y los atributos de uso **\[ cadena \]**, **\[ omitir \]** y **\[ \_ identificador \] de contexto**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Especifica un declarador de puntero opcional al que se aplica el atributo de **\[ cadena \]** . Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Consta de cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos **\[ de \]** parámetro pueden tomar los atributos direccionales **\[ hacia y hacia afuera \]**; los atributos de campo **\[** [**Max \_ es**](max-is.md) **\]** y **\[** [**size \_ es**](size-is.md) **\]** ; el atributo de puntero **\[ \] ref**, **\[ Unique \]** o **\[ ptr \]**; y el **\[ \_ identificador \] de contexto** y la **\[ cadena \]** de atributos de uso. El atributo de uso **\[ Ignore \]** no se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el atributo de **\[ \] cadena** se utiliza con una matriz cuyos límites se determinan en tiempo de ejecución, también debe especificar **\[ \_ \]** un atributo size o **\[ Max \_ is \]** , como en el ejemplo siguiente:

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

El atributo de **\[ cadena \]** no se puede usar con atributos que especifican el intervalo de elementos transmitidos, como **\[ First \_ es \]**, **\[ Last \_ es \]** y **\[ length \_ es \]**.

Cuando se usa en matrices multidimensionales, el atributo de **\[ cadena \]** se aplica a la matriz situada más a la derecha.

Para definir una cadena contada, no use el atributo de **\[ cadena \]** . Use una matriz de caracteres o un puntero basado en caracteres como el siguiente:

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

El atributo de **\[ cadena \]** especifica que el código auxiliar debe utilizar un método proporcionado por el lenguaje para determinar la longitud de las cadenas.

Al declarar cadenas en C, debe asignar espacio para un carácter adicional que marca el final de la cadena.

## <a name="examples"></a>Ejemplos

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**char**](char-idl.md)
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

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**el tamaño \_ es**](size-is.md)
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
</dt> <dt>

[**WCHAR \_ t**](wchar-t.md)
</dt> </dl>

 

 