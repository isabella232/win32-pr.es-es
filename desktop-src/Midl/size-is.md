---
title: size_is (atributo)
description: Use el atributo \ size is\ para especificar el tamaño de la memoria, en elementos, asignado para punteros de tamaño, punteros de tamaño a punteros de tamaño \_ y matrices multidimensionales o únicas.
ms.assetid: 1f3f3629-f668-460d-86fd-16ef22449973
keywords:
- size_is atributo MIDL
topic_type:
- apiref
api_name:
- size_is
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65a4c3ea93ea9ed55ce4f6f9ce846c81b60fa40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159384"
---
# <a name="size_is-attribute"></a>size \_ es el atributo

Use el atributo size is para especificar el tamaño de la memoria, en elementos, asignado para punteros de tamaño, punteros de tamaño a punteros de tamaño y matrices \[ **\_** \] multidimensionales o únicas.

``` syntax
[ size_is(limited-expression-list) ]
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*limited-expression-list* 
</dt> <dd>

Especifica una o varias expresiones de lenguaje C. Cada expresión se evalúa como un entero no negativo que representa la cantidad de memoria asignada a un puntero de tamaño o una matriz. En el caso de una matriz, especifica una expresión única que representa el tamaño de asignación, en elementos, de la primera dimensión de esa matriz. El compilador MIDL admite expresiones condicionales, expresiones lógicas, expresiones relacionales y expresiones aritméticas. MIDL no permite invocaciones de función en expresiones y no permite operadores de incremento y decremento. Use comas como marcadores de posición para parámetros implícitos o para separar varias expresiones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si usa el atributo size is para asignar memoria para una matriz multidimensional y usa la notación de matriz, tenga en cuenta que solo se puede determinar dinámicamente la primera dimensión de una \[ **\_** \] \[ matriz multidimensional en tiempo de \] ejecución. Las demás dimensiones deben especificarse estáticamente. Para obtener más información sobre el uso del tamaño es el atributo con varios niveles de punteros para permitir que un servidor devuelva una matriz de datos de tamaño dinámico a un cliente, como se muestra en el ejemplo Proc7, vea Varios niveles de \[ **\_** \] [punteros.](/windows/desktop/Rpc/multiple-levels-of-pointers)

Puede usar size es o max es (pero no ambos en la misma lista de atributos) para especificar el tamaño de una matriz cuyos límites superiores se determinan en tiempo \[ **\_** \] de ejecución. [**\_**](max-is.md) Sin embargo, tenga en cuenta que \[ **el atributo size \_ is** \] no se puede usar en dimensiones de matriz fijas. El \[ **atributo max \_ is** \] especifica el índice máximo válido de la matriz. Como resultado, especificar el tamaño es(n) equivale a especificar \[ \_ max \] \[ \_ is(n-1). \]

Un \[ [**parámetro in**](in.md) \] o \[ in, [**out**](out-idl.md) \] conformant-array \[ [](string.md) \] \[ **\_** \] \[ [**\_**](max-is.md) con el \] atributo string no necesita que el tamaño sea o max is attribute. En este caso, el tamaño de la asignación se determina a partir del terminador NULL de la cadena de entrada. Todas las demás matrices compatibles con el atributo \[ string deben tener un tamaño \] \[ **\_ es** \] o max \[ **\_ es** \] attribute.

Aunque es legal usar el tamaño es un atributo con una constante, hacerlo es \[ **\_** \] ineficaz e innecesario. Por ejemplo, use una matriz de tamaño fijo:

``` syntax
HRESULT Proc3([in] short Arr[MAX_SIZE]);
```

en lugar de:

``` syntax
// legal but marshaling code is much slower
HRESULT Proc3([in size_is(MAX_SIZE)] short Arr[] );
```

Puede usar el tamaño \[ **es \_ y** \] length es \[ [**\_ atributos**](length-is.md) \] juntos. Al hacerlo, el \[ **atributo size \_ is** \] controla la cantidad de memoria asignada para los datos. El \[ **atributo length \_ is** \] especifica cuántos elementos se transmiten. La cantidad de memoria especificada por el \[ **tamaño \_ es y** \] la longitud de \[ **\_ los** \] atributos no debe ser la misma. Por ejemplo, el cliente puede pasar un parámetro de entrada y salida a un servidor y especificar una asignación de memoria grande con el tamaño es , aunque especifica un pequeño número de elementos de datos que se pasarán con longitud \[ \] \[ **\_** \] \[ **\_ es** \] . Esto permite que el servidor rellene la matriz con más datos de los que recibió, que luego puede devolver al cliente.

En general, no resulta útil especificar que el tamaño es y la longitud está en los parámetros de entrada \[ **\_** \] o \[ [**\_**](length-is.md) \] \[ \] \[ \] salida. En ambos casos, \[ **el tamaño controla \_ la** \] asignación de memoria. La aplicación podría usar size para asignar más elementos de matriz de los que transmite \[ **\_** \] (como se especifica por \[ **longitud \_ es** \] ). Sin embargo, esto sería ineficaz. También sería ineficaz especificar valores idénticos para \[ **size \_ es** \] y length \[ **\_ es** \] . Crearía una sobrecarga adicional durante la serialización de parámetros. Si los valores de \[ **size son \_ y** \] length \[ **\_ es** \] siempre el mismo, omita \[ **la longitud \_ es** \] attribute.

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

[**Matrices**](arrays-1.md)
</dt> <dt>

[Atributos de campo](/windows/desktop/Rpc/field-attributes)
</dt> <dt>

[**en \_ primer lugar es**](first-is.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**En**](in.md)
</dt> <dt>

[**el \_ último es**](last-is.md)
</dt> <dt>

[**length \_ es**](length-is.md)
</dt> <dt>

[**max \_ is**](max-is.md)
</dt> <dt>

[**min \_ es**](min-is.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Cadena**](string.md)
</dt> </dl>

 

 