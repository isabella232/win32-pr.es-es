---
title: size_is (atributo)
description: Use el atributo \ size \_ es \ para especificar el tamaño de la memoria, en elementos, asignados para punteros de tamaño, punteros de tamaño a punteros de tamaño y matrices de un solo o multidimensionales.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is el atributo MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789861"
---
# <a name="size_is-attribute"></a>el tamaño \_ es Attribute

Use el \[ **atributo \_ size** \] para especificar el tamaño de la memoria, en elementos, asignados para punteros de tamaño, punteros de tamaño a punteros de tamaño y Matrices unidimensionales o únicas.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Limited-Expression-List* 
</dt> <dd>

Especifica una o más expresiones del lenguaje C. Cada expresión se evalúa como un entero no negativo que representa la cantidad de memoria asignada a un puntero de tamaño o una matriz. En el caso de una matriz, especifica una expresión única que representa el tamaño de asignación, en elementos, de la primera dimensión de esa matriz. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Use comas como marcadores de posición para los parámetros implícitos o para separar varias expresiones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si está utilizando el atributo \[ **size \_** \] para asignar memoria para una matriz multidimensional y usa la notación de matriz \[ \] , tenga en cuenta que solo la primera dimensión de una matriz multidimensional se puede determinar dinámicamente en tiempo de ejecución. Las demás dimensiones deben especificarse estáticamente. Para obtener más información sobre el uso del \[ atributo **size \_** \] con varios niveles de punteros para permitir que un servidor devuelva una matriz de datos de tamaño dinámico a un cliente, como se muestra en el Proc7 de ejemplo, vea [varios niveles de punteros](/windows/desktop/Rpc/multiple-levels-of-pointers).

Puede usar cualquier \[ **tamaño \_ es** \] o [**Max \_ es**](max-is.md) (pero no ambos en la misma lista de atributos) para especificar el tamaño de una matriz cuyos límites superiores se determinan en tiempo de ejecución. Tenga en cuenta, sin embargo, que no se \[ **\_** \] puede usar el atributo size en las dimensiones de la matriz que son fijas. El \[ atributo **Max \_ is** \] especifica el índice de matriz válido máximo. Como resultado, la especificación \[ del tamaño \_ es (n) \] equivale a especificar \[ Max \_ es (n-1) \] .

\[ [](in.md) \] \[ No es necesario que un parámetro in o in, [**out**](out-idl.md) \] -array compatible con el atributo de \[ [**cadena**](string.md) \] tenga el \[ atributo **size \_** \] o \[ [**Max \_ is**](max-is.md) \] . En este caso, el tamaño de la asignación se determina a partir del terminador nulo de la cadena de entrada. Todas las demás matrices compatibles con el atributo de \[ cadena \] deben tener el atributo \[ **size \_** \] o \[ **Max \_ is** \] .

Aunque es legal usar el \[ **\_ atributo size** \] con una constante, hacerlo es ineficaz e innecesario. Por ejemplo, use una matriz de tamaño fijo:

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

en lugar de:

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

Puede usar el \[ **tamaño \_** \] y la \[ [**longitud \_ son**](length-is.md) \] atributos juntos. Al hacerlo, el atributo \[ **size \_** \] controla la cantidad de memoria asignada a los datos. El \[ **atributo \_ length** \] especifica el número de elementos que se transmiten. La cantidad de memoria especificada por el \[ **tamaño \_ es** \] y la \[ **longitud \_** de \] los atributos no debe ser la misma. Por ejemplo, el cliente puede pasar un \[ parámetro in, out \] a un servidor y especificar una asignación de memoria grande con \[ **el tamaño \_ es** \] , aunque especifique un número pequeño de elementos de datos que se van a pasar con la \[ **longitud \_** \] . Esto permite que el servidor rellene la matriz con más datos de los recibidos, que puede devolver al cliente.

En general, no es útil especificar \[ **el tamaño \_ es** \] y la \[ [**longitud \_ está**](length-is.md) \] en \[ \] los parámetros in o \[ out \] . En ambos casos, \[ **el tamaño \_ es** \] controlar la asignación de memoria. La aplicación podría usar \[ **el \_ tamaño** \] para asignar más elementos de matriz de los transmitidos (según lo especificado por la \[ **longitud \_ es** \] ). Sin embargo, esto sería ineficaz. También sería ineficaz especificar valores idénticos para \[ **el tamaño \_** \] y la \[ **longitud \_ es** \] . Crearía una sobrecarga adicional durante la serialización de parámetros. Si los valores de \[ **size \_ es** \] y \[ **length \_ es** \] siempre el mismo, omita el atributo \[ **length \_** \] .

## <a name="examples"></a>Ejemplos

``` syntax
HRESULT Proc1(
    [in] short m;
    [in, size_is(m)] short a[]);  // If m = 10, a[10]
HRESULT Proc2(
    [in] short m;
    [in, size_is(m)] short b[][20]);  // If m = 10, b[10][20]
HRESULT Proc3(
    [in] short m;
    [size_is(m)] short * pshort); /* Specifies a pointer
                                  to an m-sized block of shorts */
HRESULT Proc4(
    [in] short m;
    [size_is( , m)] short ** ppshort); /* Specifies a pointer 
                                       to a pointer to an m-sized 
                                       block of shorts */
HRESULT Proc5(
    [in] short m;
    [size_is(m ,)] short ** ppshort); /* Specifies an
                                      m-sized block of pointers 
                                      to shorts */
HRESULT Proc6(
    [in] short m;
    [in] short n;
    [size_is(m,n)] short ** ppshort); /* Specifies a pointer to an 
                                      m-sized block of pointers, each 
                                      of which points to an n-sized 
                                      block of shorts. m associates with
                                      the pointer closeest to the identifer
                                      it decorates. n associates with rest.*/
 HRESULT Proc7(
     [out] long  * pSize,
     [out, size_is( , *pSize)] my_type ** ppMyType); /* Specifies a pointer 
                                              to a sized pointer, 
                                              which points to a block 
                                              of my_types, whose size is
                                              unknown when the stub 
                                              calls the server. */
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**matrices**](arrays-1.md)
</dt> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**el primero \_ es**](first-is.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**de**](in.md)
</dt> <dt>

[**última \_ es**](last-is.md)
</dt> <dt>

[**la longitud \_ es**](length-is.md)
</dt> <dt>

[**Max \_ es**](max-is.md)
</dt> <dt>

[**min \_ es**](min-is.md)
</dt> <dt>

[**enuncia**](out-idl.md)
</dt> <dt>

[**string**](string.md)
</dt> </dl>

 

 