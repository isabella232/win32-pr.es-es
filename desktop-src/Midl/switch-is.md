---
title: switch_is (atributo)
description: El atributo \ switch \_ es \ especifica la expresión o el identificador que actúa como discriminante de Unión que selecciona el miembro de Unión.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is el atributo MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994734"
---
# <a name="switch_is-attribute"></a>el modificador \_ es un atributo

El atributo **\[ Switch \_ es \]** especifica la expresión o el identificador que actúa como discriminante de Unión que selecciona el miembro de Unión.

``` syntax
typedef struct [[ struct-tag ]] 
{
    [ switch_is(limited-expr) [[ , field-attr-list ]] ] union-type-specifier declarator;
    ...
}

[[ [function-attribute-list] ]] type-specifier [[pointer-declarator]] function-name(
    [ switch_is(limited-expr) [[ , param-attr-list ]] ] union-type [[declarator]]
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*struct: etiqueta* 
</dt> <dd>

Especifica una etiqueta opcional para una estructura.

</dd> <dt>

*Limited-expr* 
</dt> <dd>

Especifica una expresión de lenguaje C admitida por MIDL. Se admiten casi todas las expresiones del lenguaje C. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite las invocaciones de función en expresiones y no permite operadores de incremento previo y posterior y de decremento anterior y posterior.

</dd> <dt>

*Field-ATTR-List* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican a un miembro de Unión. Entre los atributos de campo válidos **\[** [**se incluyen First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , length es, **\[** [**\_**](length-is.md) **\]** **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[** [**cadena**](string.md) **\]** , **\[** [**omitir**](ignore.md) **\]** y **\[** [**\_ identificador de contexto**](context-handle.md) **\]** ; el atributo de puntero **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** y para miembros que son uniones, el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** . Separe varios atributos de campo con comas.

</dd> <dt>

*Union-Type-Specifier* 
</dt> <dd>

Especifica el identificador de tipo de [**Unión**](union.md) . Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador y lista de declaradores* 
</dt> <dd>

Especifica un declarador estándar de C, como un identificador, un declarador de puntero y un declarador de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las uniones que se transmiten en llamadas a procedimientos remotos. Estos declaradores se permiten en las uniones que no se transmiten). Separe varios declaradores con comas.

</dd> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son **\[** [**callback**](callback.md) **\]** , **\[** [**local**](local.md) **\]** ; el atributo de puntero **\[ ref \]**, **\[ \] Unique** o **\[ ptr \]**; y los atributos de uso **\[ cadena \]**, **\[ omitir \]** y **\[ \_ identificador \] de contexto**.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una [**Unión**](union.md), un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador de puntero* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*param-ATTR-List* 
</dt> <dd>

Especifica cero o más atributos adecuados para el tipo de parámetro especificado. Los atributos de parámetro pueden tomar los atributos direccionales hacia arriba y **\[ hacia \] fuera**, los atributos **\[ \] de** campo **\[ primero \_ son \]**, **\[ Last \_ es \]**, **\[ length \_ \]** is, **\[ Max \_ is \]**, **\[ size \_ is \]** y **\[ Switch \_ Type \]**; el atributo de puntero **\[ ref \]**, **\[ Unique \]** o **\[ ptr \]**; y el **\[ \_ identificador \] de contexto** y la **\[ cadena \]** de atributos de uso. El atributo de uso **\[ Ignore \]** no se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> <dt>

*tipo de Unión* 
</dt> <dd>

Identifica el especificador de tipo de [**Unión**](union.md) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

El discriminante asociado con el **\[ modificador \_ es \]** el atributo debe definirse en el mismo nivel lógico que la Unión:

-   Cuando la Unión es un parámetro, el discriminante de Unión debe ser otro parámetro.
-   Cuando la Unión es un campo de una estructura, discriminante debe ser otro campo de la misma estructura.

La secuencia de una estructura o una lista de parámetros de función no es significativa. La Unión puede preceder o seguir discriminante.

El atributo **\[ Switch \_ es \]** puede aparecer como atributo de campo o como atributo de parámetro.

## <a name="examples"></a>Ejemplos

``` syntax
typedef [switch_type(short)] union _WILLIE_UNION_TYPE 
{ 
    [case(24)] 
        float fMays; 
    [case(25)] 
        double dMcCovey; 
    [default] 
        ; 
} WILLIE_UNION_TYPE; 
 
typedef struct _WINNER_TYPE 
{ 
    [switch_is(sUniformNumber)] WILLIE_UNION_TYPE w; 
    short sUniformNumber; 
} WINNER_TYPE;
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos base de MIDL](midl-base-types.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[Uniones encapsuladas](encapsulated-unions.md)
</dt> <dt>

[**enumeración**](enum.md)
</dt> <dt>

[**el primero \_ es**](first-is.md)
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

[Uniones no encapsuladas](nonencapsulated-unions.md)
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

 

 




