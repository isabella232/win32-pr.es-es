---
title: Descriptores de parámetros
description: Como se mencionó anteriormente, \ 8211;Oi y \ 8211;Existen descriptores de parámetros de estilo Oif.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a13b052d49629333bd9cb121b4d1b661722cb3a7a69ad2a17d3e2740a0cd8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927554"
---
# <a name="parameter-descriptors"></a>Descriptores de parámetros

Como se mencionó anteriormente, existen descriptores de parámetros de estilo [**–Oi**](/windows/desktop/Midl/-oi) y **–Oif.**

## <a name="the-oi-parameter-descriptors"></a>Descriptores de parámetros –Oi

Los códigos auxiliares totalmente interpretados requieren información adicional para cada uno de los parámetros de una llamada RPC. Las descripciones de parámetros de un procedimiento siguen inmediatamente después de la descripción del procedimiento.

[**Simple –Oi**](/windows/desktop/Midl/-oi)

**Descriptores de parámetros**

El formato de la descripción de un \[ **parámetro de** tipo simple in \] o return es:

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

-o bien-

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

Donde el \_ tipo simple<1> es el token de FC que indica el tipo simple. Los códigos son los siguientes:

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Otros –Oi**

**Descriptores de parámetros**

El formato de la descripción de todos los demás tipos de parámetros es:

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Donde la dirección del<un campo> para cada una de estas descripciones debe ser uno de los que se muestran \_ en la tabla siguiente.



| Hex | Marca                          | Significado                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4d  | FC \_ IN \_ PARAM                 | Parámetro in.                                            |
| 50  | FC \_ IN \_ OUT \_ PARAM            | Parámetro de entrada y salida.                                        |
| 51  | FC \_ OUT \_ PARAM                | Parámetro Out.                                           |
| 52  | FC \_ RETURN \_ PARAM             | Valor devuelto del procedimiento.                                   |
| 4f  | FC \_ IN \_ PARAM \_ NO \_ FREE \_ INST | En xmit/rep como parámetro para el que no se realiza ninguna liberación. |



 

El tamaño de<1> es el tamaño del parámetro en la pila, expresado como el número de enteros que el parámetro \_ ocupa en la pila.

> [!Note]  
> El [**modo –Oi**](/windows/desktop/Midl/-oi) no se admite en plataformas de 64 bits.

 

El desplazamiento de<campo 2> es el desplazamiento de la tabla de cadenas de formato de tipo, que indica el \_ descriptor de tipo para el argumento .

## <a name="the-oif-parameter-descriptors"></a>Descriptores de parámetros –Oif

Hay dos formatos posibles para una descripción de parámetros, uno para los tipos base y otro para todos los demás tipos.

Tipos base:

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

Otros:

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

En ambos intervalos de<2> indica el desplazamiento en la \_ pila de argumentos virtuales, en bytes. Para los tipos base, el tipo de argumento se da directamente mediante el carácter de formato correspondiente al tipo. Para otros tipos, el desplazamiento de<campo 2> proporciona el desplazamiento en la tabla de cadenas de formato de tipo donde se encuentra el \_ descriptor de tipo para el argumento.

El campo de atributo de parámetro se define de la siguiente manera:

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   El **bit MustSize** solo se establece si se debe ajustar el tamaño del parámetro.
-   El **bit MustFree** se establece si el servidor debe llamar a la rutina Free del \* parámetro.
-   El **bit IsSimpleRef** se establece para un parámetro que es un puntero de referencia a cualquier otro puntero que no sea otro puntero y que no tiene atributos asignados. Para este tipo, el campo de desplazamiento de tipo<> de la descripción del parámetro, excepto un puntero de referencia a un tipo base, proporciona el desplazamiento al tipo del referenciador; el puntero de referencia simplemente se \_ omite.
-   El **bit IsDontCallFreeInst** se establece para ciertas representaciones como parámetros \_ cuyas rutinas de instancia libre no deben llamarse.
-   Los bits **ServerAllocSize** son distintos de cero si el parámetro es out , en , o in,out puntero al puntero o puntero \[  \] \[  \] \[  \] a enum16, **\_** y se inicializarán en la pila del intérprete de servidor, en lugar de usar una llamada a RpcAllocate . Si es distinto de cero, este valor se multiplica por 8 para obtener el número de bytes del parámetro. Tenga en cuenta que esto significa que siempre se asignan al menos 8 bytes para un puntero.
-   El **bit IsBasetype** se establece para los tipos simples que se serializan mediante el bucle del [**intérprete principal –Oif.**](/windows/desktop/Midl/-oi) En concreto, un tipo simple con un atributo de intervalo en él no se marca como un tipo base para forzar la serialización rutinaria del intervalo mediante el envío mediante un token de FC \_ RANGE.
-   El **bit IsByValue** se establece para los tipos compuestos que se envían por valor, pero no se establece para tipos simples, independientemente de si el argumento es un puntero. Los tipos compuestos para los que se establece son estructuras, uniones, transmitir como , representar como , wire [**\_ marshal**](/windows/desktop/Midl/wire-marshal) y SAFEARRAY. [**\_**](/windows/desktop/Midl/transmit-as) [**\_**](/windows/desktop/Midl/represent-as) En general, el bit se introdujo en beneficio del bucle del intérprete principal en el intérprete [**–Oicf,**](/windows/desktop/Midl/-oi) para garantizar que los argumentos no simples (denominados argumentos de tipo compuesto) se desreferencian correctamente. Este bit nunca se usó en versiones anteriores del intérprete.

 

 