---
title: last_is (atributo)
description: El atributo de campo \ Last \_ es \ especifica el índice del último elemento de la matriz que se va a transmitir. Cuando el índice especificado es cero o negativo, no se transmite ningún elemento de la matriz.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is el atributo MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104533160"
---
# <a name="last_is-attribute"></a>el \_ atributo Last es

El atributo de campo **\[ Last \_ \]** especifica el índice del último elemento de la matriz que se va a transmitir. Cuando el índice especificado es cero o negativo, no se transmite ningún elemento de la matriz.

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Limited-Expression-List* 
</dt> <dd>

Especifica una o más expresiones del lenguaje C. Cada expresión se evalúa como un entero que representa el índice de la matriz del último elemento de la matriz que se va a transmitir. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Separe varias expresiones con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ Last \_ es \]** determina el valor del índice de matriz correspondiente a la **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** longitud es Attribute cuando no se especifica length. La relación entre estos índices de matriz es la siguiente: length = Last-First + 1.

Si el valor del índice de matriz especificado por **\[** [**First \_ es**](first-is.md) **\]** mayor que el valor especificado por **\[ Last \_ es \]**, se transmiten cero elementos.

El atributo **\[ Last \_ \] es** no se puede usar como atributo de campo al mismo tiempo que el atributo **\[** [**length \_**](length-is.md) **\]** o el **\[** atributo [**String**](string.md) **\]** .

El uso de una expresión constante con el atributo **\[ Last \_ es \]** un uso inadecuado del atributo. Es legal, pero ineficaz, y dará como resultado un código de serialización más lento.

Cuando el valor especificado por **\[** [**Max \_ es**](max-is.md) **\]** igual o mayor que cero, la relación siguiente debe ser true: 0 <= Last \_ es <= Max \_ es.

## <a name="examples"></a>Ejemplos

``` syntax
proc1(
    [in] short Last,
    [in, last_is(Last)] short asNumbers[MAXSIZE]);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**el primero \_ es**](first-is.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**la longitud \_ es**](length-is.md)
</dt> <dt>

[**Max \_ es**](max-is.md)
</dt> <dt>

[**el tamaño \_ es**](size-is.md)
</dt> </dl>

 

 