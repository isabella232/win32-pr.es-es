---
title: max_is (atributo)
description: El atributo \ max \_ is\ designa el valor máximo para un índice de matriz válido.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is atributo MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7dfa7e8cdc5b1df752a3a6eb442524157228d354079f262a27a5514860e335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642971"
---
# <a name="max_is-attribute"></a>max \_ is attribute

El **\[ atributo max \_ is \]** designa el valor máximo para un índice de matriz válido.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Especifica una o varias expresiones de lenguaje C. Cada expresión se evalúa como un entero que representa el índice de matriz válido más alto. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Separe varias expresiones con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **\[ atributo max \_ is \]** no se corresponde necesariamente con el número de elementos de la matriz. Para una matriz de tamaño *n* en C, donde el primer elemento de matriz es el elemento número cero, el valor máximo de un índice de matriz válido *es n*–1.

El **\[ atributo max \_ is \]** no se puede usar como atributo de campo al mismo tiempo que **\[** [**el atributo size \_ is.**](size-is.md) **\]**

Aunque es legal usar el atributo **\[ \_ max is \]** con una expresión constante, hacerlo es ineficaz e innecesario. Por ejemplo, use una matriz de tamaño fijo:

``` syntax
/* transmits values of a[0]... a[MAX_SIZE-1] */ 
HRESULT Proc3([in] short Arr[MAX_SIZE]); 
```

en lugar de:

``` syntax
/* legal but marshaling code is much slower */ 
HRESULT Proc3([in max_is(MAX_SIZE-1)] short Arr[] );
```

## <a name="examples"></a>Ejemplos

``` syntax
/* if m = 10, there are 11 transmitted elements (a[0]...a[10])*/ 
HRESULT Proc1( 
    [in] short m, 
    [in, max_is(m)] short a[]);  
 
/* if m = 10, the valid range for b is b[0...10][20] */ 
HRESULT Proc2( 
    [in] short m, 
    [in, max_is(m)] short b[][20];
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**min \_ es**](min-is.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
</dt> </dl>

 

 