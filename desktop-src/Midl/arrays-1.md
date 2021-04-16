---
title: arrays (atributo)
description: Las matrices son colecciones homogéneas de datos a los que tiene acceso un número de índice o elemento.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- matrices (atributo) MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685630"
---
# <a name="arrays-attribute"></a>arrays (atributo)

Las matrices son colecciones homogéneas de datos a los que tiene acceso un número de índice o elemento.

``` syntax
typedef [ [type-attr-list] ] type-specifier [pointer-decl] array-declarator;

typedef [ [type-attr-list] ] struct [ tag ] 
{
    [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
    ...
};

typedef [ [type-attr-list] ] union [ tag ] 
{
    [ case (limited-expression [ , ... ] ) ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  [ [ default ]
  [ [ field-attribute-list ] ] type-specifier [pointer-decl] array-declarator;
  ]
};

[[ [function-attribute-list] ]] type-specifier [[pointer-decl]] function-name(
        [[ [param-attr-list] ]] type-specifier [[pointer-decl]] array-declarator
        , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Type-ATTR-List* 
</dt> <dd>

Especifica cero o más atributos que se aplican al tipo. Entre los atributos de tipo válidos se incluyen el [**\[ \] identificador**](handle.md), el [**\[ \_ \] tipo de conmutador**](switch-type.md), la [**\[ transmisión \_ como \]**](transmit-as.md); el atributo de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y el [**\[ \_ identificador \] de contexto**](context-handle.md)de los atributos de uso, [**\[ String \]**](string.md)y [**\[ Ignore \]**](ignore.md). Separe varios atributos con comas.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica el identificador de tipo, tipo base, [**estructura**](struct.md), [**Unión**](union.md)o tipo de [**enumeración**](enum.md) . La especificación de tipo puede incluir una especificación de almacenamiento opcional.

</dd> <dt>

*puntero-decl* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero utilizado en C, construido a partir del **\*** designador, modificadores como **Far** y el calificador [**const**](const.md).

</dd> <dt>

*array-declarator* 
</dt> <dd>

Especifica el nombre de la matriz, seguido de una de las construcciones siguientes para cada dimensión de la matriz: "**\[ \]**", " **\[\*\]** ", "**\[ ***Const1*** \]**" o "**\[ ***Lower...*** Upper \]**", donde *inferior* y *superior* son valores constantes que representan los límites inferior y superior. La constante *inferior* debe evaluarse como cero.

</dd> <dt>

*etiqueta* 
</dt> <dd>

Especifica una etiqueta opcional para la estructura o Unión.

</dd> <dt>

*lista de atributos de campo* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican a la estructura, el miembro de unión o el parámetro de función. Entre los atributos de campo válidos se incluyen [**\[ First \_ \] es**](first-is.md), [**\[ Last \_ \] es**](last-is.md), [**\[ length \_ \]**](length-is.md)is, [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ es \]**](size-is.md); la [**\[ cadena \]**](string.md)de atributos de uso y [**\[ Ignore \]**](ignore.md); los atributos de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)y [**\[ ptr \]**](ptr.md); y el [**\[ \_ tipo \] de modificador**](switch-type.md)de atributo Union. Separe varios atributos de campo con comas. Tenga en cuenta que los atributos enumerados anteriormente, **\[ First \_ \] is**, **\[ Last \_ is \]** y [**\[ Ignore \]**](ignore.md) no son válidos para uniones.

</dd> <dt>

*Limited-Expression* 
</dt> <dd>

Especifica una expresión del lenguaje C. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.

</dd> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son [**\[ callback \]**](callback.md), [**\[ \] local**](local.md); el atributo de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y la [**\[ cadena \]**](string.md)de atributos de uso, y el [**\[ \_ identificador \] de contexto**](context-handle.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*param-ATTR-List* 
</dt> <dd>

Especifica los atributos direccionales y uno o varios atributos de campo opcionales que se aplican al parámetro de la matriz. Entre los atributos de campo válidos [**\[ se incluyen Max \_ \] is**](max-is.md), [**\[ size \_ is \]**](size-is.md), [**\[ length \_ is \]**](length-is.md), [**\[ First \_ is \]**](first-is.md)y [**\[ Last \_ is \]**](last-is.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las matrices de MIDL usan un estilo similar a, pero no exactamente igual que C y C++. Para obtener más información, vea [matrices de MIDL](midl-arrays.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

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
</dt> <dt>

[**espeficarse**](unique.md)
</dt> </dl>

 

 




