---
title: atributo union
description: La palabra clave union aparece en funciones relacionadas con uniones discriminadas.
ms.assetid: 135a6581-e03e-4b90-9fd8-15690820dbd0
keywords:
- atributo union MIDL
topic_type:
- apiref
api_name:
- union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc683472d67775c4a2900695246d5f9ca920ca32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159337"
---
# <a name="union-attribute"></a>atributo union

La **palabra clave union** aparece en funciones relacionadas con uniones discriminadas.

``` syntax
/* Encapsulated union*/
typedef [[ [type-attribute-list] ]] union [[ struct-name ]] switch (switch-type switch-name) [[ union-name ]] 
{
  C-style-case-list 
  [[ [ field-attribute-list <> ] ]] type-specifier <> declarator-list <>;

        ...
}

/* Non-encapsulated union*/
typedef [switch_type(switch-type) [[ , type-attr-list ]] ] union [[ tag ]] 
{ 
    [ case ( limited-expr-list) ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  [[ [ default ]
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
  ]]
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*type-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican al tipo de unión. Los atributos de tipo válidos incluyen el identificador , transmitir como ; el atributo de puntero **\[** [](handle.md) **\]** **\[** [**\_**](transmit-as.md) **\]** **\[** [**único**](unique.md) **\]** , **\[** [**o ptr**](ptr.md); **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](ignore.md) **\]** y el identificador de contexto de los atributos de uso y omitir . Las uniones encapsuladas también pueden tener el atributo de tipo de puntero **\[** [**ref.**](ref.md) **\]** Separe varios atributos con comas.

</dd> <dt>

*struct-name* 
</dt> <dd>

Especifica una etiqueta opcional que asigna un nombre a la estructura generada por el compilador midl.

</dd> <dt>

*switch-type* 
</dt> <dd>

Especifica un [**tipo int**](int.md), [**char,**](char-idl.md) [**enum**](enum.md) o un identificador que se resuelve en uno de estos tipos.

</dd> <dt>

*switch-name* 
</dt> <dd>

Especifica el nombre de la variable de tipo *switch-type* que actúa como discriminador de unión.

</dd> <dt>

*union-name* 
</dt> <dd>

Especifica un identificador opcional que asigna un nombre a la unión en la estructura, generada por el compilador MIDL, que contiene la unión y el discriminador.

</dd> <dt>

*C-style-case-list* 
</dt> <dd>

Lista de "**case** *const-expr* :"

</dd> <dt>

*limited-expression-list* 
</dt> <dd>

Especifica una o varias expresiones de lenguaje C. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Las expresiones individuales de la lista deben estar separadas por una coma.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican al miembro de unión. Los atributos de campo válidos incluyen primero es , el último es , la longitud es , max es , size es ; la cadena de atributos de uso , omitir y el identificador de contexto ; el atributo de puntero unique o ptr ; y, para los miembros que no son uniones **\[** [**\_**](first-is.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** **\[** [](ignore.md) **\]** **\[** [**\_**](context-handle.md) **\]** **\[** [](unique.md) **\]** **\[** [](ptr.md) **\]** sincapsuladas, **\[** [**\_**](switch-type.md) **\]** el tipo de modificador de atributo union . Las uniones no superadas también pueden usar el atributo de campo de puntero **\[** [**ref.**](ref.md) **\]** Separe varios atributos de campo con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica un tipo [base,](midl-base-types.md) [**struct**](struct.md), **union,** [**tipo de enumeración**](enum.md) o identificador de tipo. Una especificación de almacenamiento opcional puede *preceder al especificador de tipo*.

</dd> <dt>

*declarator-list* 
</dt> <dd>

Uno o varios declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las uniones que se transmiten en llamadas a procedimiento remoto. Excepto cuando se usa el modificador del compilador MIDL [**/osf**](-osf.md), estos declaradores se permiten en uniones que no se transmiten). Separe varios declaradores con comas.

</dd> <dt>

*etiqueta* 
</dt> <dd>

Especifica una etiqueta opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

MIDL admite dos tipos de uniones discriminadas: [uniones encapsuladas](encapsulated-unions.md) y uniones [no superadas.](nonencapsulated-unions.md) La unión encapsulada es compatible con implementaciones anteriores de RPC (versión 1 de NCA). La unión no encapsulada elimina algunas de las restricciones de la unión encapsulada y proporciona un discriminador más visible que la unión encapsulada.

La unión encapsulada se identifica mediante la palabra clave [**switch**](switch.md) y la ausencia de otras palabras clave relacionadas con la unión.

La unión no superulada, también conocida como unión, se identifica por la presencia del modificador es y las palabras clave de tipo switch, que identifican el discriminador y **\[** [**\_**](switch-is.md) **\]** su **\[** [**\_**](switch-type.md) **\]** tipo.

Cuando use en , out unions, tenga en cuenta que cambiar el valor del modificador de unión durante la llamada puede hacer que la llamada remota se comporte de forma diferente a una **\[** [](in.md) [](out-idl.md) **\]** llamada local. En la devolución, los códigos auxiliares copian **\[ el parámetro en**, **out \]** en la memoria que ya está presente en el cliente. Cuando el procedimiento remoto modifica el valor del modificador de unión y, por consiguiente, cambia el tamaño del objeto de datos, los códigos auxiliares pueden sobrescribir la memoria válida con el **\[ valor out. \]** Cuando el modificador union cambia el objeto de datos de un tipo base a un tipo de puntero, **\[ \]** los códigos auxiliares pueden sobrescribir la memoria válida cuando copian el referenciador de puntero en la ubicación de memoria indicada por en el valor de un tipo base.

La forma de las uniones debe ser idéntica entre plataformas para garantizar la interconectividad.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Uniones encapsuladas](encapsulated-unions.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[Uniones no superadas](nonencapsulated-unions.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**switch \_ es**](switch-is.md)
</dt> <dt>

[**tipo \_ de conmutador**](switch-type.md)
</dt> </dl>

 

 




