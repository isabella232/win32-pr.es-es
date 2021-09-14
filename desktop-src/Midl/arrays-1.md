---
title: atributo arrays
description: Las matrices son colecciones homogéneos de datos a las que accede un índice o un número de elemento.
ms.assetid: 375fb795-8f18-45b7-898c-99f1273746d8
keywords:
- atributo de matrices MIDL
topic_type:
- apiref
api_name:
- arrays
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e189eb1784a4ff24b799c7a4d4482d0f56b20e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159681"
---
# <a name="arrays-attribute"></a>atributo arrays

Las matrices son colecciones homogéneos de datos a las que accede un índice o un número de elemento.

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

*type-attr-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican al tipo. Los atributos [**de tipo \[ \]**](handle.md)válidos incluyen el identificador [**\[ \]**](unique.md) [**\[ \]**](ref.md) [**\[ \]**](ignore.md) [**\[ \]**](string.md) [**\[ \_ \]**](switch-type.md), el tipo de modificador , [**\[ transmitir \_ \]**](transmit-as.md)como ; el atributo de puntero ref , unique o [**\[ ptr \]**](ptr.md); [**\[ \_ \]**](context-handle.md)y el identificador de contexto de los atributos de uso , la cadena y omitir . Separe varios atributos con comas.

</dd> <dt>

*type-specifier* 
</dt> <dd>

Especifica el identificador de tipo, el tipo base, [**la estructura**](struct.md), [**la unión**](union.md)o el tipo [**de enumeración.**](enum.md) La especificación de tipo puede incluir una especificación de almacenamiento opcional.

</dd> <dt>

*pointer-decl* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que el declarador de puntero usado en C, construido a partir del **\* *designador _ ,*** modificadores como _ far y el calificador [**const**](const.md).

</dd> <dt>

*array-declarator* 
</dt> <dd>

Especifica el nombre de la matriz, seguido de una de las **\[ \]** construcciones siguientes para cada dimensión de la matriz: " ", " **\[\*\]** ", " **\[** _const1_ *_\]_* " o " **\[** _lower... upper_ *_\]_* " donde lower *y* *upper son* valores constantes que representan los límites inferior y superior. La constante *inferior debe* evaluarse como cero.

</dd> <dt>

*etiqueta* 
</dt> <dd>

Especifica una etiqueta opcional para la estructura o unión.

</dd> <dt>

*field-attribute-list* 
</dt> <dd>

Especifica cero o más atributos de campo que se aplican a la estructura, miembro de unión o parámetro de función. [**\[ \]**](ref.md) [**\[ \]**](unique.md) [**\[ \_ \]**](switch-type.md) [**\[ \_ \]**](max-is.md) [**\[ \]**](ignore.md) [**\[ \_ \]**](length-is.md) [**Los atributos de campo válidos incluyen primero , el último es \[ \_ , length es , max es , size es ; la cadena de atributos de uso y ignore ; los atributos de puntero ref , unique y ptr ; y el tipo de modificador de atributo union . \]**](first-is.md) [**\[ \]**](string.md) [**\[ \_ \]**](size-is.md) [**\[ \_ \]**](last-is.md) [**\[ \]**](ptr.md) Separe varios atributos de campo con comas. Tenga en cuenta que de los atributos enumerados anteriormente, **\[ el primero \_ \] es**, **\[ el último \_ es \]** y [**\[ ignore \]**](ignore.md) no son válidos para las uniones.

</dd> <dt>

*limited-expression* 
</dt> <dd>

Especifica una expresión de lenguaje C. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento.

</dd> <dt>

*function-attribute-list* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos son [**\[ \] la devolución**](callback.md)de llamada , [**\[ local; \]**](local.md)el atributo de puntero [**\[ ref \]**](ref.md), [**\[ unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y la cadena de atributos [**\[ \]**](string.md)de uso y el identificador de [**\[ \_ contexto \]**](context-handle.md).

</dd> <dt>

*function-name* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*param-attr-list* 
</dt> <dd>

Especifica los atributos direccionales y uno o varios atributos de campo opcionales que se aplican al parámetro de matriz. Los atributos de campo válidos [**\[ incluyen max \_ es \]**](max-is.md), [**\[ el tamaño \_ es \]**](size-is.md), [**\[ length \_ es \]**](length-is.md), [**\[ el primero \_ es \]**](first-is.md)y [**\[ el último \_ es \]**](last-is.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las matrices de MIDL usan un estilo similar, pero no exactamente igual que C y C++. Para obtener más información, vea [MidL Arrays](midl-arrays.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

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

[**union**](union.md)
</dt> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 




