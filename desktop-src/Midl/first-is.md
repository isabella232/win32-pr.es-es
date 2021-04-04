---
title: first_is (atributo)
description: El atributo \ First \_ es \ especifica el índice del primer elemento de la matriz que se va a transmitir.
ms.assetid: 1de7821c-19e7-4b2c-98fc-2fae3563831c
keywords:
- first_is el atributo MIDL
topic_type:
- apiref
api_name:
- first_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d8d1be33299354e77ef92d885bb3b092cccfb6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904603"
---
# <a name="first_is-attribute"></a>el \_ atributo First es

El \[ **primero \_ es** el \] atributo que especifica el índice del primer elemento de la matriz que se va a transmitir.

``` syntax
first_is(limited-expression-list)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Limited-Expression-List* 
</dt> <dd>

Especifica una o más expresiones del lenguaje C. Cada expresión se evalúa como un entero que representa el índice de la matriz del primer elemento de la matriz que se va a transmitir. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Separe varias expresiones con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si el **\[ primer \_ \]** atributo no está presente, o si el índice especificado es un número negativo, el elemento de matriz cero es el primer elemento transmitido.

El **\[ primero \_ es \]** el atributo que también puede ayudar a determinar los valores de los índices de matriz correspondientes al **\[** atributo [**Last \_ es**](last-is.md) **\]** o **\[** [**length \_ es**](length-is.md) **\]** cuando no se especifican estos atributos. La relación entre estos índices de matriz es:

``` syntax
length = last - first + 1
```

La relación siguiente también debe contener:

``` syntax
0 <= first_is <= max_is
```

La siguiente relación debe contener cuando **\[** [**Max \_ es**](max-is.md) **\] <= 0:**

``` syntax
first_is == 0
```

El **\[ \_ primer \]** atributo no se puede usar al mismo tiempo que el atributo de **\[** [**cadena**](string.md) **\]** .

El uso de una expresión constante con el **\[ primer \_ \]** atributo es un uso inadecuado del atributo. Es legal, pero ineficaz, y dará como resultado un código de serialización más lento.

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT Proc1(
    [in] short First,
    [first_is(First)] Arr[10]);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[atributos de campo \_](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**última \_ es**](last-is.md)
</dt> <dt>

[**la longitud \_ es**](length-is.md)
</dt> <dt>

[**Max \_ es**](max-is.md)
</dt> <dt>

[**min \_ es**](min-is.md)
</dt> <dt>

[**el tamaño \_ es**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 