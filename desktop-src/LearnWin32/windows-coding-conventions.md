---
title: Windows Convenciones de codificación
description: Si no está Windows programación, puede ser desconcertante la primera vez que vea un Windows programa.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78c24f38f9f2f410c044637ca3aa59d4baa39e9b671b3485c5b85899b69c2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387400"
---
# <a name="windows-coding-conventions"></a>Windows Convenciones de codificación

Si no está Windows programación, puede ser desconcertante la primera vez que vea un Windows programa. El código se rellena con definiciones de tipos extraños, como **DWORD \_ PTR** y **LPRECT,** y las variables tienen nombres como *hWnd* y *pwsz* (denominada notación húngaro). Merece la pena aprovechar un momento para conocer algunas de las convenciones Windows codificación.

La gran mayoría de Windows API están formadas por funciones o interfaces de Modelo de objetos componentes (COM). Muy pocos Windows API se proporcionan como clases de C++. (Una excepción importante es GDI+, una de las API de gráficos 2D).

## <a name="typedefs"></a>Typedefs

Los Windows encabezados contienen una gran cantidad de definiciones de tipo. Muchos de ellos se definen en el archivo de encabezado WinDef.h. Estos son algunos de los que encontrará con frecuencia.

### <a name="integer-types"></a>Tipos enteros



| Tipo de datos     | Size    | ¿Firmado?  |
|---------------|---------|----------|
| **BYTE**      | 8 bits  | Sin signo |
| **DWORD**     | 32 bits | Sin signo |
| **INT32**     | 32 bits | Firmado   |
| **INT64**     | 64 bits | Firmado   |
| **LONG**      | 32 bits | Firmado   |
| **LONGLONG**  | 64 bits | Firmado   |
| **UINT32**    | 32 bits | Sin signo |
| **UINT64**    | 64 bits | Sin signo |
| **ULONG**     | 32 bits | Sin signo |
| **ULONGLONG** | 64 bits | Sin signo |
| **WORD**      | 16 bits | Sin signo |



 

Como puede ver, hay una cierta cantidad de redundancia en estas definiciones de tipo. Parte de esta superposición se debe simplemente al historial de Windows API. Los tipos enumerados aquí tienen un tamaño fijo y los tamaños son los mismos en aplicaciones de 32 y 64 bits. Por ejemplo, el **tipo DWORD** siempre tiene 32 bits de ancho.

### <a name="boolean-type"></a>Tipo booleano

**BOOL** es una definición de tipo para un valor entero que se usa en un contexto booleano. El archivo de encabezado WinDef.h también define dos valores para su uso con **BOOL.**


```C++
#define FALSE    0 
#define TRUE     1
```



Sin embargo, a pesar de esta definición de **TRUE,** la mayoría de las funciones que devuelven un tipo **BOOL** pueden devolver cualquier valor distinto de cero para indicar la verdad booleana. Por lo tanto, siempre debe escribir esto:


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



y no esto:


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



Tenga en cuenta **que BOOL** es un tipo entero y no es intercambiable con el tipo **bool de** C++.

### <a name="pointer-types"></a>Tipos de puntero

Windows define muchos tipos de datos con el formato *puntero a X.* Normalmente tienen el prefijo *P-* o *LP- en* el nombre. Por ejemplo, **LPRECT** es un puntero a [**un RECT**](/previous-versions//dd162897(v=vs.85)), donde **RECT** es una estructura que describe un rectángulo. Las siguientes declaraciones de variable son equivalentes.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



Históricamente, *P* significa "puntero" y *LP* significa "puntero largo". Los punteros largos (también *denominados punteros lejanos)* son una retención de Windows de 16 bits, cuando eran necesarios para abordar intervalos de memoria fuera del segmento actual. El *prefijo LP* se conserva para que sea más fácil porte código de 16 bits a código de 32 Windows. Hoy en día no hay ninguna distinción: un puntero es un puntero.

### <a name="pointer-precision-types"></a>Tipos de precisión de puntero

Los siguientes tipos de datos siempre tienen el tamaño de un puntero, es decir, 32 bits de ancho en aplicaciones de 32 bits y 64 bits de ancho en aplicaciones de 64 bits. El tamaño se determina en tiempo de compilación. Cuando una aplicación de 32 bits se ejecuta en archivos de 64 Windows, estos tipos de datos siguen teniendo 4 bytes de ancho. (Una aplicación de 64 bits no se puede ejecutar en aplicaciones de 32 Windows, por lo que no se produce la situación inversa).

-   **DWORD \_ PTR**
-   **INT \_ PTR**
-   **LONG \_ PTR**
-   **ULONG \_ PTR**
-   **UINT \_ PTR**

Estos tipos se usan en situaciones en las que un entero se puede convertir en un puntero. También se usan para definir variables para la aritmética de punteros y para definir contadores de bucle que recorren en iteración el intervalo completo de bytes en búferes de memoria. Por lo general, aparecen en lugares en los que un valor de 32 bits existente se expandió a 64 bits en conjuntos de 64 Windows.

## <a name="hungarian-notation"></a>Notation húngaro

*La notación húngaro* es la práctica de agregar prefijos a los nombres de variables para proporcionar información adicional sobre la variable. (El inventor de la notación, Charles Simonyi, era húngaro, de ahí su nombre).

En su forma original, la notación húngaro proporciona información *semántica* sobre una variable, que le informa del uso previsto. Por ejemplo, *significa un* índice, *cb* significa un tamaño en bytes ("recuento de bytes") y rw *y* *col* mean row y column numbers. Estos prefijos están diseñados para evitar el uso accidental de una variable en el contexto incorrecto. Por ejemplo, si ve la expresión , sabrá que se está agregando un número de fila a un tamaño, lo que es casi seguro un `rwPosition +  cbTable` error en el código.

Una forma más común de la notación húngaro usa prefijos para proporcionar información de tipo, por ejemplo, *dw* para **DWORD** y *w* para **WORD**. 

Si busca en la Web la "notación húngaro", encontrará muchas opiniones sobre si la notación húngaro es buena o mala. Algunos programadores tienen un gran rechazo a la notación húngaro. A otros les resulta útil. Independientemente de ello, muchos de los ejemplos de código de MSDN usan la notación húngaro, pero no es necesario que memorice los prefijos para comprender el código.

## <a name="next"></a>Siguientes

[Trabajar con cadenas](working-with-strings.md)

 

 