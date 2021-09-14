---
title: string (atributo)
description: El atributo \ string\ indica que la matriz unidimensional char, wchar t, byte (o equivalente) o el puntero a dicha matriz deben tratarse \_ como una cadena.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159376"
---
# <a name="string-attribute"></a>string (atributo)

El **\[ \] atributo string** indica que la matriz [**unidimensional char**](char-idl.md), [**wchar \_ t**](wchar-t.md), [**byte**](byte.md) (o equivalente) o el puntero a dicha matriz deben tratarse como una cadena. La cadena también puede ser una matriz (o un puntero a una matriz) de construcciones cuyos campos son todos del tipo **byte**.

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

*type-attribute-list* 
</dt> <dd>

Especifica uno o varios atributos que se aplican a un tipo. Los atributos de tipo válidos incluyen el identificador , el tipo de modificador , transmitir como ; el atributo de puntero **\[** [](handle.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[** [**ref**](ref.md) **\]** , **\[** [**unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md); **\]** **\[** [**\_**](context-handle.md) **\]** **\[ \]** **\[** [](ignore.md) **\]** y el identificador de contexto de los atributos de uso , la cadena y omitir . Separe varios atributos con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo [base,](midl-base-types.md) [**un tipo de estructura**](struct.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*standard-declarator* 
</dt> <dd>

Especifica un declarador de C estándar, como un identificador, un declarador de puntero o un declarador de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).

</dd> <dt>

*declarator-list* 
</dt> <dd>

Especifica declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers). La *lista de declaradores* consta de uno o varios declaradores separados por comas. El identificador de nombre de parámetro en el declarador de función es opcional.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican a la estructura, al miembro de unión o al parámetro de función. Los dos atributos de campo válidos son max is y size es **\[** [**\_**](max-is.md) ; **\]** **\[** [**\_**](size-is.md) **\]** **\[ \_ \]** **\[ \]** **\[ \]** **\[** [](ref.md) **\]** **\[ \]** **\[** [](ptr.md) **\]** **\[ \_ \]** la cadena de atributos de uso , omitir y el identificador de contexto , el atributo de puntero ref , unique o ptr y el tipo de modificador de atributo union . Separe varios atributos de campo con comas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[ \] ref**, **\[ unique \]** o **\[ ptr \]**; **\[ \]** **\[ \]** **\[ \_ \]** y la cadena de atributos de uso , ignore y el identificador de contexto .

</dd> <dt>

*ptr-decl* 
</dt> <dd>

Especifica un declarador de puntero opcional al que **se \[ \]** aplica el atributo de cadena. Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del \* designador, modificadores como **, y** el calificador [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*parameter-attribute-list* 
</dt> <dd>

Consta de cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos de **\[ \]** **\[ \]** parámetro pueden tomar los atributos direccionales dentro y fuera; los atributos de campo max es y size es ; el atributo de puntero **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[ \] ref**, **\[ unique \]** o **\[ \] ptr**; **\[ \_ \]** **\[ \]** y el identificador de contexto de atributos de uso y la cadena . El atributo usage **\[ ignore no \]** se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el **\[ atributo de \]** cadena se usa con una matriz cuyos límites se determinan en tiempo de ejecución, también debe especificar un atributo size **\[ \_ is \]** o max **\[ \_ is, \]** como en el ejemplo siguiente:

``` syntax
/* a string that can hold up to MAX_STRING_LENGTH characters */
typedef [string, max_is(MAX_STRING_LENGTH)] char line[];
```

El **\[ \] atributo** de cadena no se puede usar con atributos que especifican el intervalo de elementos transmitidos, como first **\[ \_ es \]**, last **\[ \_ es \]** y length **\[ \_ es \]**.

Cuando se usa en matrices multidimensionales, el **\[ atributo de cadena \]** se aplica a la matriz situada más a la derecha.

Para definir una cadena con recuento, no use el **\[ atributo de \]** cadena. Use una matriz de caracteres o un puntero basado en caracteres como el siguiente:

``` syntax
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string;
```

El **\[ atributo \]** string especifica que el código auxiliar debe usar un método proporcionado por el lenguaje para determinar la longitud de las cadenas.

Al declarar cadenas en C, debe asignar espacio para un carácter adicional que marca el final de la cadena.

## <a name="examples"></a>Ejemplos

``` syntax
/* a string type that can hold up to 80 characters */ 
typedef [string] char line[81]; 
 
HRESULT Proc1([in, string] char * pszName);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Matrices**](arrays-1.md)
</dt> <dt>

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**Char**](char-idl.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**en \_ primer lugar es**](first-is.md)
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

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
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
</dt> <dt>

[**wchar \_ t**](wchar-t.md)
</dt> </dl>

 

 