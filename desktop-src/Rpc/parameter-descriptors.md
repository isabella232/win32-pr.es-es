---
title: Descriptores de parámetros
description: Como se mencionó anteriormente, los descriptores de parámetros de estilo 8211, OI y \ 8211; existen.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793209"
---
# <a name="parameter-descriptors"></a>Descriptores de parámetros

Como se mencionó anteriormente, los descriptores de parámetros de estilo [**-OI**](/windows/desktop/Midl/-oi) y **-** transformated Style existen.

## <a name="the-oi-parameter-descriptors"></a>Descriptores de parámetros – OI

Los códigos auxiliares totalmente interpretados requieren información adicional para cada uno de los parámetros de una llamada RPC. Las descripciones de los parámetros de un procedimiento siguen inmediatamente después de la descripción del procedimiento.

[**Simple: OI**](/windows/desktop/Midl/-oi)

**Descriptores de parámetros**

El formato de la descripción de un \[  \] parámetro de tipo simple in o Return es:

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

**Otro: OI**

**Descriptores de parámetros**

El formato de la descripción de todos los demás tipos de parámetro es:

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Donde la dirección del parámetro \_<1> campo para cada una de estas descripciones debe ser uno de los que se muestran en la tabla siguiente.



| Hex | Marca                          | Significado                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4d  | FC \_ en \_ param                 | Parámetro in.                                            |
| 50  | \_parámetro FC in \_ out \_            | Parámetro in/out.                                        |
| 51  | \_parámetro de salida FC \_                | Parámetro Out.                                           |
| 52  | \_parámetro de devolución de FC \_             | Valor devuelto de un procedimiento.                                   |
| 4F  | FC \_ en \_ parámetro \_ no \_ disponible \_ inst. | En transmisión/REP como un parámetro para el que no se realiza ninguna liberación. |



 

El \_ tamaño de la pila<1> es el tamaño del parámetro en la pila, expresado como el número de enteros que el parámetro ocupa en la pila.

> [!Note]  
> El modo [**– OI**](/windows/desktop/Midl/-oi) no se admite en las plataformas de 64 bits.

 

El \_ desplazamiento de tipo<2> campo es el desplazamiento en la tabla de cadenas de formato de tipo, que indica el descriptor de tipos para el argumento.

## <a name="the-oif-parameter-descriptors"></a>Descriptores de parámetros – interfaces

Hay dos formatos posibles para una descripción de parámetro, uno para los tipos base, otro para todos los demás tipos.

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

En \_ el desplazamiento de la pila<2> indica el desplazamiento en la pila de argumentos virtuales, en bytes. En el caso de los tipos base, el tipo de argumento lo proporciona directamente el carácter de formato correspondiente al tipo. Para otros tipos, el \_ campo desplazamiento de tipo<2> proporciona el desplazamiento en la tabla de cadenas de formato de tipo donde se encuentra el descriptor de tipos para el argumento.

El campo atributo de parámetro se define de la siguiente manera:

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

-   El bit **MustSize** solo se establece si se debe ajustar el tamaño del parámetro.
-   El bit **MustFree** se establece si el servidor debe llamar a la rutina NdrFree del parámetro \* .
-   El bit **IsSimpleRef** se establece para un parámetro que es un puntero de referencia a cualquier otro puntero y que no tiene atributos de asignación. Para este tipo, el desplazamiento de tipo de la descripción del parámetro \_<> campo, excepto un puntero de referencia a un tipo base, proporciona el desplazamiento al tipo del campo de referencia; el puntero de referencia simplemente se omite.
-   El bit **IsDontCallFreeInst** se establece para ciertos representan \_ como parámetros cuyas rutinas de instancia gratuitas no deben llamarse.
-   Los bits **ServerAllocSize** son distintos de cero si el parámetro está \[ **fuera** \] , \[ **en** \] , o \[ **en,** un puntero \] a puntero o puntero a enum16, y se inicializará en la pila del intérprete del servidor, en lugar de usar una llamada a **I \_ RpcAllocate**. Si es distinto de cero, este valor se multiplica por 8 para obtener el número de bytes para el parámetro. Tenga en cuenta que esto significa que siempre se asignan al menos 8 bytes para un puntero.
-   El bit **IsBasetype** se establece para los tipos simples que se van a serializar mediante el bucle del intérprete principal [**– saliente**](/windows/desktop/Midl/-oi) . En concreto, un tipo simple con un atributo de intervalo en él no se marca como un tipo base para forzar el cálculo de referencias de rutina de intervalo mediante el envío mediante un \_ token de intervalo FC.
-   El bit **IsByValue** se establece para los tipos compuestos que se envían por valor, pero no se establece para los tipos simples, independientemente de si el argumento es un puntero. Los tipos compuestos para los que se establece son estructuras, uniones, [**transmitir \_ como**](/windows/desktop/Midl/transmit-as), [**representar \_ como**](/windows/desktop/Midl/represent-as), [**\_ serialización de cable**](/windows/desktop/Midl/wire-marshal) y SafeArray. En general, el bit se incorporó a la ventaja del bucle del intérprete principal en el intérprete [**– Oicf**](/windows/desktop/Midl/-oi) , para asegurarse de que los argumentos no simples (conocidos como argumentos de tipo compuesto) se desreferencian correctamente. Este bit nunca se usaba en versiones anteriores del intérprete.

 

 