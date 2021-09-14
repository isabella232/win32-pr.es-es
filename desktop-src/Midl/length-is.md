---
title: length_is (atributo)
description: El atributo \ length is\ especifica el número de elementos de \_ matriz que se transmitirán. Debe especificar un valor no negativo.
ms.assetid: 060dbd4a-3078-4050-abfe-c1b633c06861
keywords:
- length_is atributo MIDL
topic_type:
- apiref
api_name:
- length_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac217bae01c6896c7dadd36bb18f15e425a0427
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159513"
---
# <a name="length_is-attribute"></a>length \_ es un atributo

El **\[ atributo length \_ is \]** especifica el número de elementos de matriz que se transmitirán. Debe especificar un valor no negativo.

``` syntax
[length_is( limited-expression-list )]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Especifica una o varias expresiones de lenguaje C. Cada expresión se evalúa como un entero que representa el número de elementos de matriz que se transmitirán. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Separe varias expresiones con comas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\[ longitud \_ \] es** atributo determina el valor de los índices de matriz correspondientes al último atributo **\[** [**\_ is**](last-is.md) **\]** cuando no se especifica **\[ last. \_ \]** La relación entre estos índices de matriz es la siguiente: length = last - first + 1.

La **\[ longitud \_ es \]** atributo no se puede usar al mismo tiempo que el **\[** [**último atributo \_ es**](last-is.md) **\]** o el atributo **\[** [**de**](string.md) **\]** cadena.

Para definir una cadena con recuento con **\[ \_ \]** una longitud es o el último es el atributo , use una matriz de caracteres o un puntero sin el atributo **\[** [**\_**](last-is.md) **\]** **\[** [**de**](string.md) **\]** cadena.

El uso de una expresión constante **\[ con la longitud \_ es \]** un atributo es un uso inadecuado del atributo. Es legal, pero ineficaz, y dará lugar a un código de serialización más lento.

Puede usar el tamaño **\[** [**es y \_ length**](size-is.md) **\]** es **\[ \_ atributos \]** juntos. Al hacerlo, el **\[ tamaño es \_ un \]** atributo que controla la cantidad de memoria asignada para los datos. El **\[ atributo length \_ is \]** especifica cuántos elementos se transmiten. La cantidad de memoria especificada por el **\[ tamaño \_ es \]** y **\[ la longitud de \_ los \]** atributos no debe ser la misma. Por ejemplo, el cliente puede pasar un parámetro **\[ de** entrada **\] y** salida a **\[ \_ \]** un servidor y especificar una asignación de memoria grande con el tamaño es , aunque especifique un número pequeño de elementos de datos que se pasarán con longitud **\[ \_ es \]**. Esto permite que el servidor rellene la matriz con más datos de los que recibió, que luego puede devolver al cliente.

En general, no resulta útil especificar que el tamaño es y **\[** [**\_**](size-is.md) **\]** la **\[ \_ \] longitud** está en **\[** [**los parámetros de**](in.md) entrada **\]** **\[** [**o**](out-idl.md) **\]** salida. En ambos casos, **\[ el tamaño \_ controla \]** la asignación de memoria. La aplicación podría usar **\[ size para \_ asignar \]** más elementos de matriz de los que transmite (como se especifica en **\[ length \_ es \]**). Sin embargo, esto sería ineficaz. También sería ineficaz especificar valores idénticos para **\[ size \_ es \]** y **\[ length \_ es \]**. Dado que crearía una sobrecarga adicional durante la serialización de parámetros. Cuando los valores de **\[ size es \_ y \]** **\[ length \_ es \]** siempre el mismo, omita **\[ la longitud \_ es \]** attribute.

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

[**en primer \_ lugar es**](first-is.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**el \_ último es**](last-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**min \_ es**](min-is.md)
</dt> <dt>

[**el \_ tamaño es**](size-is.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> </dl>

 

 