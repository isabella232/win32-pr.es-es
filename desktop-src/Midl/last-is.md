---
title: last_is (atributo)
description: El atributo de campo \last is\ especifica el índice del último elemento de \_ matriz que se va a transmitir. Cuando el índice especificado es cero o negativo, no se transmite ningún elemento de matriz.
ms.assetid: 42a5cb0d-0887-4aa7-b34f-2fbad0f4c8ab
keywords:
- last_is atributo MIDL
topic_type:
- apiref
api_name:
- last_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 453a51109452f3cdacb1a48e67b76ccbc9f2e257
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159519"
---
# <a name="last_is-attribute"></a>el \_ último es el atributo

El atributo field **\[ last \_ especifica \]** el índice del último elemento de matriz que se va a transmitir. Cuando el índice especificado es cero o negativo, no se transmite ningún elemento de matriz.

``` syntax
[last_is( limited-expression-list )]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Especifica una o varias expresiones de lenguaje C. Cada expresión se evalúa como un entero que representa el índice de matriz del último elemento de matriz que se va a transmitir. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Separe varias expresiones con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ último atributo \_ is \]** determina el valor del índice de matriz correspondiente a **\[** [**\_**](length-is.md) **\]** **\[ \_ \]** la longitud es attribute cuando no se especifica length. La relación entre estos índices de matriz es la siguiente: length = last - first + 1.

Si el valor del índice de matriz especificado por first es mayor que el valor especificado por **\[** [**\_**](first-is.md) last **\]** **\[ \_ es \]**, se transmiten cero elementos.

El **\[ último atributo \_ es \]** no se puede usar como atributo de campo al mismo tiempo que **\[** [**la longitud \_ es**](length-is.md) **\]** el atributo o el atributo **\[** [**de**](string.md) **\]** cadena.

El uso de una expresión constante con **\[ el último atributo \_ is \]** es un uso inadecuado del atributo. Es legal, pero ineficaz, y dará lugar a un código de serialización más lento.

Cuando el valor especificado por max es igual o mayor que cero, debe cumplirse la siguiente **\[** [**\_**](max-is.md) relación: 0 <= last es <**\]** = max \_ \_ is.

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

[**en \_ primer lugar es**](first-is.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**length \_ es**](length-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
</dt> </dl>

 

 