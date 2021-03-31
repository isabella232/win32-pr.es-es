---
title: Matrices de MIDL
description: Matrices de MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- tipos de datos MIDL, matrices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077697"
---
# <a name="midl-arrays"></a>Matrices de MIDL

Los declaradores de matriz aparecen en el cuerpo de la interfaz del archivo IDL como uno de los siguientes:

-   Parte de una declaración general
-   Miembro de un declarador de estructura o Unión
-   Un parámetro para una llamada a procedimiento remoto

Los límites de cada dimensión de la matriz se expresan dentro de un par independiente de corchetes. Una expresión que se evalúa como *n* significa un límite inferior de cero y un límite superior de *n-1*. Si los corchetes están vacíos o contienen un solo asterisco ( \* ), el límite inferior es cero y el límite superior se determina en tiempo de ejecución.

La matriz también puede contener dos valores separados por puntos suspensivos que representan los límites inferior y superior de la matriz, como en la \[ *parte inferior*... *Upper* \] . Microsoft RPC requiere un límite inferior de cero. El compilador MIDL no reconoce las construcciones que especifican límites inferiores distintos de cero.

Las matrices se pueden asociar con el tamaño de los atributos de campo [**\_ es**](size-is.md), [**Max \_ es**](max-is.md), [**length \_**](length-is.md)es, [**First \_ is**](first-is.md)y [**Last \_ es**](last-is.md) para especificar el tamaño de la matriz o la parte de la matriz que contiene datos válidos. Estos atributos de campo identifican el parámetro, el campo de estructura o la constante que especifica la dimensión o el índice de la matriz.

La matriz debe estar asociada con el identificador especificado por el atributo de campo de la siguiente manera: cuando la matriz es un parámetro, el identificador también debe ser un parámetro de la misma función. Cuando la matriz es un campo de estructura, el identificador debe ser otro campo de estructura de la misma estructura.

Una matriz se denomina "compatible" si el límite superior de cualquier dimensión se determina en tiempo de ejecución. (Solo se pueden determinar en tiempo de ejecución los límites superiores). Para determinar el límite superior, la declaración de la matriz debe [**incluir \_ el atributo size**](size-is.md) o [**Max \_ is**](max-is.md) .

Una matriz se denomina "varying" cuando sus límites se determinan en tiempo de compilación, pero el intervalo de elementos transmitidos se determina en tiempo de ejecución. Para determinar el intervalo de elementos transmitidos, la declaración de la matriz debe incluir una [**longitud \_**](length-is.md), el [**primero \_ es**](first-is.md)o el atributo [**Last \_**](last-is.md) .

Una matriz variable compatible (también denominada "abrir") es una matriz cuyo límite superior y el intervalo de elementos transmitidos se determinan en tiempo de ejecución. Como máximo, se puede anidar una matriz variable compatible o compatible en una estructura de C y debe ser el último elemento de la estructura. En cambio, las matrices variables no conformes pueden aparecer en cualquier parte de una estructura.

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

Para obtener más información, vea [matrices y punteros](/windows/desktop/Rpc/arrays-and-pointers).

## <a name="multidimensional-arrays"></a>Matrices multidimensionales

El usuario puede declarar tipos que son matrices y, a continuación, declarar matrices de objetos de estos tipos. La *semántica de las* Matrices unidimensionales de tipos de matriz de *n* dimensiones es la misma que la semántica de las  + matrices de *n* dimensiones de m.

Por ejemplo, el tipo RECT Type \_ se puede definir como una matriz bidimensional y la variable *Rect* se puede definir como una matriz de tipo Rect \_ . Esto es equivalente a la matriz tridimensional *equivalente \_ Rect*:

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

Microsoft RPC está orientado a C. Según las convenciones del lenguaje C, solo la primera dimensión de una matriz multidimensional se puede determinar en tiempo de ejecución. La interoperación con matrices de DCE IDL que admiten otros idiomas se limita a:

-   Matrices multidimensionales con límites constantes (determinadas en tiempo de compilación).
-   Matrices multidimensionales con todos los límites constantes excepto la primera dimensión. El límite superior y el intervalo de elementos transmitidos de la primera dimensión dependen del tiempo de ejecución.
-   Cualquier matriz unidimensional con un límite inferior de cero.

Cuando el **\[** [](string.md) **\]** atributo de cadena se usa en matrices multidimensionales, el atributo se aplica a la matriz situada más a la derecha.

## <a name="arrays-of-pointers"></a>Matrices de punteros

Los punteros de referencia deben apuntar a datos válidos. La aplicación cliente debe asignar toda la memoria para una **\[** [](in.md) **\]** matriz de punteros de referencia en, o **\[** **en,**[**fuera**](out-idl.md) **\]** de, en especial cuando la matriz está asociada a los valores **\[ en \]**, o **\[** **en, fuera \]** de la **\[** [**longitud \_**](length-is.md)o en el **\]** **\[** [**último \_**](last-is.md) **\]** valor. La aplicación cliente también debe inicializar todos los elementos de la matriz antes de la llamada. Antes de volver al cliente, la aplicación de servidor debe comprobar que todos los elementos de matriz del punto de intervalo transmitido sean de almacenamiento válido.

En el lado del servidor, el código auxiliar asigna almacenamiento a todos los elementos de la matriz, independientemente de que la **\[** [**longitud \_ sea**](length-is.md) **\]** o la **\[** [**última \_ sea**](last-is.md) **\]** el valor en el momento de la llamada. Esta característica puede afectar al rendimiento de la aplicación.

No se aplican restricciones a las matrices de punteros únicos. En el cliente y en el servidor, el almacenamiento se asigna para punteros nulos. Cuando los punteros no son NULL, los datos se colocan en el almacenamiento preasignado.

Un declarador de puntero opcional puede preceder al declarador de matriz.

Cuando los punteros de referencia incrustados son **\[** [](out-idl.md) **\]** de solo salida, el código del administrador del servidor debe asignar valores válidos a la matriz de punteros de referencia. Por ejemplo:

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

El código auxiliar generado asigna la matriz y asigna valores NULL a todos los punteros incrustados en la matriz.

 

 