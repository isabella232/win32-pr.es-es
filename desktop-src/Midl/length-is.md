---
title: length_is (atributo)
description: El atributo \ length \_ es \ especifica el número de elementos de matriz que se van a transmitir. Debe especificar un valor no negativo.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is el atributo MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487683"
---
# <a name="length_is-attribute"></a>la longitud \_ es un atributo

El atributo **\[ length \_ \]** especifica el número de elementos de matriz que se van a transmitir. Debe especificar un valor no negativo.

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Limited-Expression-List* 
</dt> <dd>

Especifica una o más expresiones del lenguaje C. Cada expresión se evalúa como un entero que representa el número de elementos de matriz que se van a transmitir. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Separe varias expresiones con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El atributo **\[ length \_ \]** determina el valor de los índices de matriz correspondientes al **\[** atributo [**\_**](last-is.md) **\]** **\[ \_ \]** Last es cuando no se especifica Last. La relación entre estos índices de matriz es la siguiente: length = Last-First + 1.

El atributo **\[ length \_ \]** no se puede usar al mismo tiempo que el atributo **\[** [**Last \_**](last-is.md) **\]** o el atributo **\[** [**String**](string.md) **\]** .

Para definir una cadena contada con una **\[ longitud \_ \]** o el **\[** atributo [**Last \_ es**](last-is.md) **\]** , utilice una matriz de caracteres o un puntero sin el atributo de **\[** [**cadena**](string.md) **\]** .

El uso de una expresión constante con la **\[ longitud \_ es \]** un atributo que no es apropiado para el atributo. Es legal, pero ineficaz, y dará como resultado un código de serialización más lento.

Puede usar el **\[** [**tamaño \_**](size-is.md) **\]** y la **\[ longitud \_ son \]** atributos juntos. Al hacerlo, el atributo **\[ size \_ \]** controla la cantidad de memoria asignada a los datos. El atributo **\[ length \_ \]** especifica el número de elementos que se transmiten. La cantidad de memoria especificada por el **\[ tamaño \_ es \]** y la **\[ longitud \_ \]** de los atributos no debe ser la misma. Por ejemplo, el cliente puede pasar un parámetro in **, \] out** a un servidor y especificar una asignación **\[ de** memoria grande con **\[ el tamaño \_ es \]**, aunque especifique un **\[ \_ \]** número pequeño de elementos de datos que se van a pasar con la longitud. Esto permite que el servidor rellene la matriz con más datos de los recibidos, que puede devolver al cliente.

En general, no es útil especificar **\[** [**el tamaño \_ es**](size-is.md) **\]** y la **\[ longitud \_ está \]** en **\[** [](in.md) **\]** los parámetros in o **\[** [**out**](out-idl.md) **\]** . En ambos casos, **\[ el \_ tamaño \] es** controlar la asignación de memoria. La aplicación podría usar **\[ el \_ tamaño \]** para asignar más elementos de matriz de los transmitidos (según lo especificado por la **\[ longitud \_ es \]**). Sin embargo, esto sería ineficaz. También sería ineficaz especificar valores idénticos para **\[ el tamaño \_ \]** y la **\[ longitud \_ es \]**. Porque crearía una sobrecarga adicional durante la serialización de parámetros. Cuando los valores de **\[ size \_ es \]** y **\[ length \_ es \]** siempre el mismo, se omite el atributo **\[ length \_ \]** .

## <a name="examples"></a>Ejemplos

``` syntax
/* counted string holding at most "size" characters */ 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
 } COUNTED_STRING_TYPE; 
 
/* counted string holding at most 80 characters */ 
typedef struct 
{ 
    unsigned short length; 
    [length_is(length)] char string[80]; 
} STATIC_COUNTED_STRING_TYPE; 
 
HRESULT Proc1(
    [in] short iLength; 
    [in, length_is(iLength)] short asNumbers[10]);
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**el primero \_ es**](first-is.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**última \_ es**](last-is.md)
</dt> <dt>

[**Max \_ es**](max-is.md)
</dt> <dt>

[**min \_ es**](min-is.md)
</dt> <dt>

[**el tamaño \_ es**](size-is.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 