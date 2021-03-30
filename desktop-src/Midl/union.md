---
title: Union (atributo)
description: La palabra clave Union aparece en las funciones relacionadas con las uniones discriminadas.
ms.assetid: 135a6581-e03e-4b90-9fd8-15690820dbd0
keywords:
- atributo de unión (MIDL)
topic_type:
- apiref
api_name:
- union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc683472d67775c4a2900695246d5f9ca920ca32
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104532685"
---
# <a name="union-attribute"></a>Union (atributo)

La palabra clave **Union** aparece en las funciones relacionadas con las uniones discriminadas.

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

*lista de atributos de tipo* 
</dt> <dd>

Especifica cero o más atributos que se aplican al tipo de Unión. Entre los atributos de tipo válidos se incluyen **\[** el [**identificador**](handle.md) **\]** , **\[** [**transmitir \_ como**](transmit-as.md) **\]** ; el atributo de puntero **\[** [**Unique**](unique.md) **\]** , o **\[** [**ptr**](ptr.md) **\]** ; y el identificador de contexto de atributos de uso **\[** [**\_**](context-handle.md) **\]** y **\[** [**omitir**](ignore.md) **\]** . Las uniones encapsuladas también pueden tener el **\[** [](ref.md) **\]** atributo de tipo REF Pointer. Separe varios atributos con comas.

</dd> <dt>

*nombre de struct* 
</dt> <dd>

Especifica una etiqueta opcional que nombra la estructura generada por el compilador de MIDL.

</dd> <dt>

*tipo de conmutador* 
</dt> <dd>

Especifica un tipo [**int**](int.md), [**Char**](char-idl.md), [**enum**](enum.md) o un identificador que se resuelve en uno de estos tipos.

</dd> <dt>

*cambiar nombre* 
</dt> <dd>

Especifica el nombre de la variable de tipo *Switch-Type* que actúa como discriminante de Unión.

</dd> <dt>

*nombre-Unión* 
</dt> <dd>

Especifica un identificador opcional que nombra la Unión en la estructura, generada por el compilador MIDL, que contiene la Unión y el discriminante.

</dd> <dt>

*Lista de casos de estilo C* 
</dt> <dd>

Lista de "**Case** *const-expr* :"

</dd> <dt>

*Limited-Expression-List* 
</dt> <dd>

Especifica una o más expresiones del lenguaje C. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Las expresiones individuales de la lista deben estar separadas por una coma.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican al miembro de Unión. Entre los atributos de campo válidos se incluyen **\[** [**First \_ es**](first-is.md) **\]** , **\[** [**Last \_ es**](last-is.md) **\]** , **\[** [**length \_**](length-is.md)is **\]** , **\[** [**Max \_ is**](max-is.md) **\]** , **\[** [**size \_ es**](size-is.md) **\]** ; los atributos de uso **\[** [**String**](string.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** y **\[** [**\_ Handle context**](context-handle.md), **\]** el atributo de puntero **\[** [**Unique**](unique.md) **\]** o **\[** [**ptr**](ptr.md) **\]** ; y, para los miembros que son uniones no encapsuladas, el **\[** [**\_ tipo de modificador**](switch-type.md)de atributo Union **\]** . Las uniones no encapsuladas también pueden usar el **\[** [](ref.md) **\]** atributo de campo REF Pointer. Separe varios atributos de campo con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un [tipo base](midl-base-types.md), un [**struct**](struct.md), una **Unión**, un tipo de [**enumeración**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*lista de declaradores* 
</dt> <dd>

Uno o varios declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. (Los declaradores de función y las declaraciones de campo de bits no se permiten en las uniones que se transmiten en llamadas a procedimientos remotos. Excepto cuando se usa el modificador de compilador de MIDL [**/OSF**](-osf.md), estos declaradores se permiten en las uniones que no se transmiten.) Separe varios declaradores con comas.

</dd> <dt>

*etiqueta* 
</dt> <dd>

Especifica una etiqueta opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

MIDL admite dos tipos de uniones discriminadas: [uniones encapsuladas](encapsulated-unions.md) y [uniones no encapsuladas](nonencapsulated-unions.md). La Unión encapsulada es compatible con las implementaciones anteriores de RPC (NCA versión 1). La Unión no encapsulada elimina algunas de las restricciones de la Unión encapsulada y proporciona un discriminante más visible que la Unión encapsulada.

La Unión encapsulada se identifica mediante la palabra clave [**Switch**](switch.md) y la ausencia de otras palabras clave relacionadas con uniones.

La Unión no encapsulada, también conocida como Unión, se identifica mediante la presencia del **\[** [**modificador \_ is**](switch-is.md) **\]** y las **\[** palabras clave de [**\_ tipo de conmutador**](switch-type.md) **\]** , que identifican el discriminante y su tipo.

Cuando use **\[** [**in**](in.md), [**out**](out-idl.md) **\]** uniones, tenga en cuenta que el cambio del valor del modificador Union durante la llamada puede hacer que la llamada remota se comporte de forma diferente a una llamada local. En la devolución, el código auxiliar copia el parámetro **\[ in**, **out \]** en la memoria que ya está presente en el cliente. Cuando el procedimiento remoto modifica el valor del modificador Union y, por consiguiente, cambia el tamaño del objeto de datos, el código auxiliar puede sobrescribir la memoria válida con el valor **\[ out \]** . Cuando el modificador Union cambia el objeto de datos de un tipo base a un tipo de puntero, el código auxiliar puede sobrescribir la memoria válida cuando copia el puntero en la ubicación de memoria indicada por el valor **\[ in \]** de un tipo base.

La forma de las uniones debe ser idéntica en todas las plataformas para garantizar la interconectividad.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Uniones encapsuladas](encapsulated-unions.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[Uniones no encapsuladas](nonencapsulated-unions.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**el modificador \_ es**](switch-is.md)
</dt> <dt>

[**tipo de conmutador \_**](switch-type.md)
</dt> </dl>

 

 




