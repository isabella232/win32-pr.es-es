---
title: Matrices MIDL
description: Matrices MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- tipos de datos MIDL, matrices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed50ada64ae218d9097a1c188338762c7d20704dd4321d2b888ab5f7a5c7de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869655"
---
# <a name="midl-arrays"></a>Matrices MIDL

Los declaradores de matriz aparecen en el cuerpo de la interfaz del archivo IDL como uno de los siguientes:

-   Parte de una declaración general
-   Miembro de un declarador de estructura o unión
-   Un parámetro para una llamada a procedimiento remoto

Los límites de cada dimensión de la matriz se expresan dentro de un par independiente de corchetes. Una expresión que se evalúa como *n* significa un límite inferior de cero y un límite superior de *n - 1*. Si los corchetes están vacíos o contienen un solo asterisco ( ), el límite inferior es cero y el \* límite superior se determina en tiempo de ejecución.

La matriz también puede contener dos valores separados por puntos suspensivos que representan los límites inferior y superior de la matriz, como en \[ *la parte inferior...* *superior.* \] Rpc de Microsoft requiere un límite inferior de cero. El compilador MIDL no reconoce construcciones que especifican límites inferiores distintos de cero.

Las matrices se pueden asociar con el tamaño de los atributos [**\_**](last-is.md) de campo es [**, \_**](size-is.md)max es , length es , el primero es [**y \_**](first-is.md)el último es especificar el tamaño de la matriz o la parte de la matriz que contiene datos válidos. [**\_**](max-is.md) [**\_**](length-is.md) Estos atributos de campo identifican el parámetro, el campo de estructura o la constante que especifica la dimensión o el índice de la matriz.

La matriz debe asociarse al identificador especificado por el atributo field de la siguiente manera: cuando la matriz es un parámetro, el identificador también debe ser un parámetro para la misma función; cuando la matriz es un campo de estructura, el identificador debe ser otro campo de estructura de esa misma estructura.

Una matriz se denomina "compatible" si el límite superior de cualquier dimensión se determina en tiempo de ejecución. (Solo se pueden determinar los límites superiores en tiempo de ejecución). Para determinar el límite superior, la declaración de matriz debe incluir [**un atributo size \_ is**](size-is.md) o [**max \_ is.**](max-is.md)

Una matriz se denomina "variable" cuando se determinan sus límites en tiempo de compilación, pero el intervalo de elementos transmitidos se determina en tiempo de ejecución. Para determinar el intervalo de elementos transmitidos, la declaración de matriz debe incluir una longitud [**\_ es**](length-is.md), el primero [**\_ es**](first-is.md)o [**el último es \_ el**](last-is.md) atributo .

Una matriz variable compatible (también denominada "open") es una matriz cuyo límite superior y el intervalo de elementos transmitidos se determinan en tiempo de ejecución. Como máximo, una matriz variable compatible o conforme se puede anidar en una estructura de C y debe ser el último elemento de la estructura. Por el contrario, las matrices diferentes no conformes pueden producirse en cualquier parte de una estructura.

## <a name="examples"></a>Ejemplos

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

Para obtener más información, [vea Matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).

## <a name="multidimensional-arrays"></a>Matrices multidimensionales

El usuario puede declarar tipos que son matrices y, a continuación, declarar matrices de objetos de estos tipos. La semántica de *las matrices m*-dimensionales de *los tipos de* matriz n -dimensionales es la misma que la semántica de *las matrices m* + *n*-dimensional.

Por ejemplo, el tipo RECT TYPE se puede definir como una matriz bidimensional y la variable rect se puede definir como una matriz \_ de RECT  \_ TYPE. Esto equivale a la matriz tridimensional *equivalente \_ a rect*:

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

Rpc de Microsoft está orientado a C. Siguiendo las convenciones del lenguaje C, solo se puede determinar la primera dimensión de una matriz multidimensional en tiempo de ejecución. La interoperación con matrices IDL de DCE que admiten otros lenguajes se limita a:

-   Matrices multidimensionales con límites constantes (determinados en tiempo de compilación).
-   Matrices multidimensionales con todos los límites constantes excepto la primera dimensión. El límite superior y el intervalo de elementos transmitidos de la primera dimensión dependen del tiempo de ejecución.
-   Cualquier matriz unidimensional con un límite inferior de cero.

Cuando el **\[** [**atributo de**](string.md) **\]** cadena se usa en matrices multidimensionales, el atributo se aplica a la matriz situada más a la derecha.

## <a name="arrays-of-pointers"></a>Matrices de punteros

Los punteros de referencia deben apuntar a datos válidos. La aplicación cliente debe asignar toda la memoria para una matriz de punteros de referencia de entrada o **\[** [](in.md) **\]** **\[** [](out-idl.md) **\]** **\[ \]** entrada, especialmente cuando la matriz está asociada a en , o **\[** **\] in,out**, **\[** [**length \_ es**](length-is.md) **\]** o last **\[** [**\_ son**](last-is.md) **\]** valores. La aplicación cliente también debe inicializar todos los elementos de la matriz antes de la llamada. Antes de volver al cliente, la aplicación de servidor debe comprobar que todos los elementos de la matriz del intervalo transmitido apuntan al almacenamiento válido.

En el lado servidor, el código auxiliar asigna almacenamiento para todos los elementos de la matriz, independientemente de que la longitud sea o last sea el valor en el momento **\[** [**\_**](length-is.md) de **\]** la **\[** [**\_**](last-is.md) **\]** llamada. Esta característica puede afectar al rendimiento de la aplicación.

No se aplican restricciones en matrices de punteros únicos. Tanto en el cliente como en el servidor, el almacenamiento se asigna para los punteros nulos. Cuando los punteros no son NULL, los datos se colocan en almacenamiento preasignado.

Un declarador de puntero opcional puede preceder al declarador de matriz.

Cuando los punteros de referencia incrustados son parámetros de solo salida, el código del administrador del servidor debe asignar valores válidos a la **\[** [](out-idl.md) **\]** matriz de punteros de referencia. Por ejemplo:

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

Los códigos auxiliares generados asignan la matriz y asignan valores NULL a todos los punteros incrustados en la matriz.

 

 