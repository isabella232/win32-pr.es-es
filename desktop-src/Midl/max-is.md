---
title: max_is (atributo)
description: El atributo \ Max \_ es \ designa el valor máximo de un índice de matriz válido.
ms.assetid: 8d09f610-cae6-45f6-815c-5ba916d8a5e7
keywords:
- max_is el atributo MIDL
topic_type:
- apiref
api_name:
- max_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f2e2040acbc0e8f65c02f4f4ec7c3ad329959b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358866"
---
# <a name="max_is-attribute"></a>\_atributo Max is

El atributo **\[ Max \_ is \]** designa el valor máximo de un índice de matriz válido.

``` syntax
[max_is(limited-expression-list )]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Limited-Expression-List* 
</dt> <dd>

Especifica una o más expresiones del lenguaje C. Cada expresión se evalúa como un entero que representa el índice de matriz válido más alto. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Separe varias expresiones con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ Max \_ is no se \]** corresponde necesariamente con el número de elementos de la matriz. En el caso de una matriz de tamaño *n* en C, donde el primer elemento de la matriz es el número de elemento cero, el valor máximo de un índice de matriz válido es *n*– 1.

El atributo **\[ Max \_ is \]** no se puede usar como atributo de campo al mismo tiempo que el **\[** [**atributo \_ size**](size-is.md) **\]** .

Aunque es legal usar el atributo **\[ Max \_ is \]** con una expresión constante, hacerlo es ineficaz e innecesario. Por ejemplo, use una matriz de tamaño fijo:

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

[**el tamaño \_ es**](size-is.md)
</dt> </dl>

 

 