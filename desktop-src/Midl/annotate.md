---
title: atributo de anotación
description: El atributo \ Anotate \ permite especificar una cadena de anotación SAL para el método, el parámetro o el campo de estructura especificado.
ms.assetid: D0A35DCD-BD2F-455B-A040-5D63E4572D83
keywords:
- atributo de anotación MIDL
topic_type:
- apiref
api_name:
- annotate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820310c6aca0e5269d6febff5dc7d3208413110c
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795214"
---
# <a name="annotate-attribute"></a>atributo de anotación

El atributo **\[ Anotate \]** permite especificar una cadena de anotación sal para el método, el parámetro o el campo de estructura especificado.

``` syntax
[ annotation(â€œstringâ€0,  [, function-attribute-list] ] function-declarator ;
[ [function-attribute-list] ] type-specifier [pointer-declarator] function-name(
    [ annotation(â€œstringâ€) [ , parameter-attribute-list ] ] type-specifier [declarator]
    , ...);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*string* 
</dt> <dd>

Cadena de anotación SAL especificada.

</dd> <dt>

*lista de atributos de función* 
</dt> <dd>

Especifica cero o más atributos que se aplican a la función. Los atributos de función válidos incluyen la [**\[ devolución \] de llamada**](callback.md); los atributos de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y los atributos de uso [**\[ cadena \]**](string.md), [**\[ omisión \]**](ignore.md)y [**\[ \_ identificador \] de contexto**](context-handle.md). Varios atributos deben estar separados por comas.

</dd> <dt>

*function-declarator* 
</dt> <dd>

Especifica el especificador de tipo, el nombre de función y la lista de parámetros para la función.

</dd> <dt>

*Type-Specifier* 
</dt> <dd>

Especifica un **tipo \_ base**, un [**\[ struct \]**](struct.md), una [**Unión**](union.md)o un tipo de [**\[ enumeración \]**](enum.md) o un identificador de tipo. Una especificación de almacenamiento opcional puede preceder *a Type-Specifier*.

</dd> <dt>

*declarador de puntero* 
</dt> <dd>

Especifica cero o más declaradores de puntero. Un declarador de puntero es el mismo que un declarador de puntero utilizado en C; se construye a partir del \* designador, modificadores como **Far** y el calificador [**\[ const \]**](const.md).

</dd> <dt>

*nombre-de-la-función* 
</dt> <dd>

Especifica el nombre del procedimiento remoto.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Especifica cero o más atributos adecuados para el tipo de parámetro. Los atributos de parámetro con el atributo in también pueden sacar el [**\[ atributo \] direccional; los**](out-idl.md)atributos [**\[ \] de**](in.md) campo [**\[ primero \_ \] son**](first-is.md), [**\[ Last \_ es \]**](last-is.md), [**\[ length \_ \]**](length-is.md)es, [**\[ Max \_ is \]**](max-is.md), [**\[ size \_ is \]**](size-is.md)y [**\[ Switch \_ Type \]**](switch-type.md); los atributos de puntero [**\[ ref \]**](ref.md), [**\[ Unique \]**](unique.md)o [**\[ ptr \]**](ptr.md); y el [**\[ \_ identificador \] de contexto**](context-handle.md) y la [**\[ cadena \]**](string.md)de atributos de uso. El atributo de uso [**\[ Ignore \]**](ignore.md) no se puede usar como atributo de parámetro. Varios atributos deben estar separados por comas.

</dd> <dt>

*clara* 
</dt> <dd>

Especifica los declaradores estándar de C, como identificadores, declaradores de puntero y declaradores de matriz. Para obtener más información, vea [matrices y Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**\[ matrices \]**](../rpc/arrays.md)y [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers). El declarador de parámetro del declarador de la función, como el nombre del parámetro, es opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ Anotate \]** permite reemplazar las anotaciones sal generadas por MIDL o agregarlas en lugares donde MIDL no genera explícitamente una anotación. Si [**/sal**](-sal.md) no se especifica en la línea de comandos, se omite este atributo.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal**](-sal.md)
</dt> <dt>

[**/sal \_ local**](-sal-local.md)
</dt> </dl>

 

 