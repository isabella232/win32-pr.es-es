---
title: Convenciones de codificación de Windows
description: Si no está familiarizado con la programación de Windows, puede estar desconcertado cuando vea por primera vez un programa de Windows.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676355"
---
# <a name="windows-coding-conventions"></a>Convenciones de codificación de Windows

Si no está familiarizado con la programación de Windows, puede estar desconcertado cuando vea por primera vez un programa de Windows. El código se rellena con definiciones de tipo extrañas, como **DWORD \_ ptr** y **LPRECT**, y las variables tienen nombres como *HWnd* y *pwsz* (denominado notación húngara). Merece la pena dedicar un momento a aprender algunas de las convenciones de codificación de Windows.

La inmensa mayoría de las API de Windows consta de funciones o interfaces del modelo de objetos componentes (COM). Muy pocas API de Windows se proporcionan como clases de C++. (Una excepción significativa es GDI+, una de las API de gráficos 2D).

## <a name="typedefs"></a>Typedefs

Los encabezados de Windows contienen muchos typedefs. Muchos de ellos se definen en el archivo de encabezado WinDef. h. Estos son algunos de los que encontrará a menudo.

### <a name="integer-types"></a>Tipos enteros



| Tipo de datos     | Tamaño    | Conectado?  |
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



 

Como puede ver, hay una cierta cantidad de redundancia en estas definiciones de nivel. Algunos de estos superpuestos son simplemente debido al historial de las API de Windows. Los tipos enumerados aquí tienen un tamaño fijo y los tamaños son los mismos en las aplicaciones 32 y 64. Por ejemplo, el tipo **DWORD** tiene siempre 32 bits de ancho.

### <a name="boolean-type"></a>Tipo booleano

**Bool** es una definición de tipo para un valor entero que se utiliza en un contexto booleano. El archivo de encabezado WinDef. h también define dos valores para su uso con **bool**.


```C++
#define FALSE    0 
#define TRUE     1
```



A pesar de esta definición de **true**, sin embargo, la mayoría de las funciones que devuelven un tipo **bool** pueden devolver cualquier valor distinto de cero para indicar su veracidad booleana. Por lo tanto, siempre debe escribir lo siguiente:


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



Tenga en cuenta que **bool** es un tipo entero y no es intercambiable con el tipo **bool** de C++.

### <a name="pointer-types"></a>Tipos de puntero

Windows define muchos tipos de datos con el formato *Pointer-to-X*. Normalmente tienen el prefijo *P* o *LP* en el nombre. Por ejemplo, **LPRECT** es un puntero a un [**Rect**](/previous-versions//dd162897(v=vs.85)), donde **Rect** es una estructura que describe un rectángulo. Las siguientes declaraciones de variable son equivalentes.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



Históricamente, *P* significa "Pointer" y *LP* representa el "puntero largo". Los punteros largos (también denominados *punteros Far*) son un Holdover de Windows de 16 bits, cuando eran necesarios para direccionar los intervalos de memoria fuera del segmento actual. El prefijo *LP* se ha conservado para facilitar el traslado del código de 16 bits a Windows de 32 bits. Actualmente no hay ninguna distinción: un puntero es un puntero.

### <a name="pointer-precision-types"></a>Tipos de precisión del puntero

Los siguientes tipos de datos siempre son el tamaño de un puntero, es decir, 32 bits de ancho en aplicaciones de 32 bits y 64 bits de ancho en aplicaciones de 64 bits. El tamaño se determina en tiempo de compilación. Cuando una aplicación de 32 bits se ejecuta en Windows de 64 bits, estos tipos de datos siguen siendo 4 bytes de ancho. (Una aplicación de 64 bits no se puede ejecutar en Windows de 32 bits, por lo que no se produce la situación inversa).

-   **DWORD \_ ptr**
-   **INT \_ ptr**
-   **LONG \_ ptr**
-   **ULONG \_ ptr**
-   **UINT \_ ptr**

Estos tipos se utilizan en situaciones en las que un entero podría convertirse en un puntero. También se usan para definir variables para la aritmética de puntero y para definir contadores de bucle que recorren en iteración el intervalo completo de bytes en los búferes de memoria. En general, aparecen en lugares donde un valor existente de 32 bits se expandió a 64 bits en Windows de 64 bits.

## <a name="hungarian-notation"></a>Notación húngara

La *notación húngara* es la práctica de agregar prefijos a los nombres de variables, para proporcionar información adicional sobre la variable. (El inventoro de la notación, Charles Simonyi, era húngaro, es decir, su nombre).

En su forma original, la notación húngara proporciona información *semántica* sobre una variable, que indica el uso previsto. Por ejemplo, *i* es un índice, *CB* significa un tamaño en bytes ("recuento de bytes") y los números de filas y columnas de *la media de la columna y* *RW* . Estos prefijos están diseñados para evitar el uso accidental de una variable en el contexto equivocado. Por ejemplo, si vio la expresión `rwPosition +  cbTable` , sabrá que se está agregando un número de fila a un tamaño, lo que es casi seguro un error en el código.

Una forma más común de notación húngara usa prefijos para proporcionar información de *tipos* , por ejemplo, *DW* para **DWORD** y *w* para **Word**.

Si busca en la web "notación húngara", encontrará una gran cantidad de opiniones sobre si la notación húngara es buena o mala. Algunos programadores tienen una intensa diferencia en la notación húngara. Otros lo encuentran útiles. Sin embargo, muchos de los ejemplos de código de MSDN usan la notación húngara, pero no es necesario memorizar los prefijos para comprender el código.

## <a name="next"></a>Siguientes

[Trabajar con cadenas](working-with-strings.md)

 

 