---
title: switch_is (atributo)
description: El atributo \ switch is\ especifica la expresión o identificador que actúa como discriminador de \_ unión que selecciona el miembro de unión.
ms.assetid: 93552bdf-6a14-47ce-877e-32ed976bb895
keywords:
- switch_is atributo MIDL
topic_type:
- apiref
api_name:
- switch_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52661c4fa1ebce57011f4424901dd1ec18250f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159367"
---
# <a name="switch_is-attribute"></a>switch \_ is attribute

El **\[ atributo switch \_ es \]** especifica la expresión o el identificador que actúa como discriminador de unión que selecciona el miembro de unión.

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

*struct-tag* 
</dt> <dd>

Especifica una etiqueta opcional para una estructura.

</dd> <dt>

*limited-expr* 
</dt> <dd>

Especifica una expresión de lenguaje C compatible con MIDL. Se admiten casi todas las expresiones en lenguaje C. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores previos y posteriores a incrementos y anteriores y posteriores al decremento.

</dd> <dt>

*field-attr-list* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican a un miembro de unión. Los atributos de campo válidos incluyen primero es , el último es , la longitud es , max es , size es ; la cadena de atributos de uso , omitir y el identificador de contexto ; el atributo de puntero ref , unique o ptr ; y para los miembros que son a su vez **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](ref.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** uniones, **\[** [**\_**](switch-type.md) **\]** el tipo de modificador de atributo union . Separe varios atributos de campo con comas.

</dd> <dt>

*union-type-specifier* 
</dt> <dd>

Especifica el identificador [**de tipo**](union.md) de unión. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*declarator y declarator-list* 
</dt> <dd>

Especifica un declarador de C estándar, como un identificador, un declarador de puntero y un declarador de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las uniones que se transmiten en llamadas a procedimiento remoto. Estos declaradores se permiten en uniones que no se transmiten). Separe varios declaradores con comas.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son la devolución de llamada , local; el atributo de puntero **\[** [](callback.md) **\]** **\[** [](local.md) **\]** **\[ \] ref**, **\[ unique \]** o **\[ ptr \]**; **\[ \]** **\[ \]** **\[ \_ \]** y la cadena de atributos de uso , ignore y el identificador de contexto .

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo [base,](midl-base-types.md) [**struct**](struct.md), [**union,**](union.md) [**tipo de enumeración**](enum.md) o identificador de tipo. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*pointer-declarator* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero usado en C; se construye a partir del \* designador, modificadores como **, y** el calificador [**const**](const.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*param-attr-list* 
</dt> <dd>

Especifica cero o más atributos adecuados para el tipo de parámetro especificado. **\[ \_ \]** **\[ \]** **\[ \]** **\[ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \_ \]** **\[ \]** **\[ \]** **\[ Los atributos de parámetro pueden tomar los atributos direccionales en y out , los atributos de campo primero son , el último es , length es , max es , size es y switch type ; el atributo de puntero ref , unique o ptr ; y el identificador de contexto de atributos \]** de uso y la cadena . El atributo usage **\[ ignore no \]** se puede usar como atributo de parámetro. Separe varios atributos con comas.

</dd> <dt>

*union-type* 
</dt> <dd>

Identifica el [**especificador de**](union.md) tipo de unión.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El discriminante asociado al **\[ atributo switch \_ is \]** debe definirse en el mismo nivel lógico que la unión:

-   Cuando la unión es un parámetro, el discriminador de unión debe ser otro parámetro.
-   Cuando la unión es un campo de una estructura, el discriminador debe ser otro campo de la misma estructura.

La secuencia de una estructura o una lista de parámetros de función no es significativa. La unión puede preceder o seguir al discriminador.

El **\[ modificador \_ es \]** el atributo puede aparecer como un atributo de campo o como un atributo de parámetro.

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

[Tipos base midl](midl-base-types.md)
</dt> <dt>

[**devolución de llamada**](callback.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**identificador de \_ contexto**](context-handle.md)
</dt> <dt>

[Uniones encapsuladas](encapsulated-unions.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**en \_ primer lugar es**](first-is.md)
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

[Uniones no superadas](nonencapsulated-unions.md)
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

[**union**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 




