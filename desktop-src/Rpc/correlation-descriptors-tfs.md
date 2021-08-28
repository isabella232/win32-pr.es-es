---
title: Descriptores de correlación
description: Un descriptor de correlación es una cadena de formato que describe una expresión basada en un argumento relacionado con otro argumento.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbbeb682a7c558cd8c45050d27ea9bf64c39016a056a88566aef7048f3c0d610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022365"
---
# <a name="correlation-descriptors"></a>Descriptores de correlación

Un descriptor de correlación es una cadena de formato que describe una expresión basada en un argumento relacionado con otro argumento. Se necesita un descriptor de correlación para controlar la semántica relacionada con atributos como \[ **size \_ is()** \] , length \[ **\_ is()** \] , switch \[ **\_ is()** \] e \[ **iid \_ is()** \] . Los descriptores de correlación se usan con matrices, punteros de tamaño, uniones y punteros de interfaz. El valor de expresión final puede ser un tamaño, una longitud, un discriminador de unión o un puntero a un IID, respectivamente. En términos de cadenas de formato, los descriptores de correlación se usan con matrices, uniones y punteros de interfaz. Un puntero de tamaño se describe en cadenas de formato como un puntero a una matriz.

Hay dos rutinas que realizan cálculos de expresiones básicos: MidpComputeConformance se usa para tamaños, modificadores e IID, mientras que PlatpComputeVariance se usa para las \* longitudes. También hay una sola rutina para realizar una validación del valor de correlación para la funcionalidad de denegación de ataque.

Los descriptores de correlación se han diseñado para admitir solo expresiones muy limitadas. En situaciones complicadas, el compilador genera una rutina de evaluación de expresiones a la que llamará el motor cuando sea necesario.

Un descriptor de correlación tiene el formato siguiente:

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

El tipo de correlación del descriptor de correlación<1> consta de dos nibbles: los 4 bits superiores describen dónde se puede encontrar la expresión y los 4 bits inferiores describen el tipo del valor de \_ expresión.

La nibble superior puede tener uno de estos cinco valores:

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>\_CONFORMIDAD NORMAL DE FC \_
</dt> <dd>

Un caso normal de conformidad, como el descrito en un campo de una estructura.

</dd> <dt>

<span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>CONFORMIDAD \_ CON EL PUNTERO \_ FC
</dt> <dd>

Para los punteros con atributos **(size \_ is()**, **length \_ is()**) que son campos de una estructura. Esto afecta a la forma en que se establece el puntero de memoria base.

</dd> <dt>

<span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>CONFORMIDAD \_ DE NIVEL SUPERIOR \_ \_ DE FC
</dt> <dd>

Para la conformidad de nivel superior descrita por otro parámetro.

</dd> <dt>

<span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>CONFORMIDAD \_ \_ \_ MULTID DE NIVEL \_ SUPERIOR DE FC
</dt> <dd>

Para la conformidad de nivel superior de una matriz multidimensional descrita por otro parámetro.

> [!Note]  
> Las matrices de tamaño multidimensional y los punteros desencadenan un modificador a [**–Oicf**](/windows/desktop/Midl/-oi).

 

</dd> <dt>

<span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>CONFORMIDAD \_ DE CONSTANTE DE \_ FC
</dt> <dd>

Para un valor constante. El compilador precalcula el valor de una expresión constante proporcionada por el usuario. Cuando este es el caso, los 3 bytes posteriores de la descripción de conformidad contienen los 3 bytes inferiores de un largo que describe el tamaño de conformidad. No se requiere ningún cálculo adicional.

</dd> </dl>

El valor nibble inferior proporciona el tipo del valor que se debe extraer de la memoria:

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> No se admiten expresiones de 64 bits. FC \_ HYPER solo se usa para **iid \_ is()** en plataformas de 64 bits para extraer el valor del puntero para IID. \*
>
> El compilador establece el tipo nibble en cero para los siguientes casos: expresión constante mencionada anteriormente y cuando es necesario llamar a la rutina de expresión de evaluación, por ejemplo, cuando se usan FC CONSTANT CONFORMANCE y \_ \_ FC \_ CALLBACK.

 

El tamaño es op<1> campo permite aplicar una de las siguientes operaciones a \_ \_ la variable de conformidad:

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

La constante FC DEREFERENCE se usa para que la correlación sea un valor máximo, como \_ para size **\[ \_ is( \* pL). \]** Los operadores aritméticos solo usan la constante indicada. La constante FC CALLBACK indica que es necesario llamar a una rutina de evaluación \_ de expresiones.

El desplazamiento<2> es normalmente un desplazamiento de memoria relativa a la variable de argumento de expresión. También puede ser un índice rutinario de evaluación de expresiones. Como se mencionó anteriormente en este documento, para las expresiones constantes forma parte del valor de expresión final real.

La interpretación del campo offset<2> como desplazamiento de memoria depende de la complejidad de la expresión, la ubicación de la variable de expresión y, en el caso de una matriz, si la matriz es realmente un puntero con atributos.

Si la matriz es un puntero con atributos y la variable de conformidad es un campo de una estructura, el campo de desplazamiento contiene el desplazamiento desde el principio de la estructura hasta el campo que describe la conformidad. Si la matriz no es un puntero con atributos y la variable de conformidad es un campo de una estructura, el campo de desplazamiento contiene el desplazamiento desde el final de la parte no conforme de la estructura hasta el campo que describe la conformidad. Normalmente, la matriz conforme está al final de la estructura.

Para la conformidad de nivel superior, el campo de desplazamiento contiene el desplazamiento desde la ubicación del primer parámetro del código auxiliar en la pila hasta el parámetro que describe la conformidad. Esto no se usa en **el modo –OS.** Hay otras excepciones a la interpretación del campo de desplazamiento; Estas excepciones se describen en la descripción de esos tipos.

Cuando offset<2> se usa con FC CALLBACK, contiene un índice en la tabla rutinaria de evaluación de expresiones generada \_ por el compilador. El mensaje de código auxiliar se pasa a la rutina de evaluación, que calcula el valor de conformidad y lo asigna al campo MaxCount del mensaje de código auxiliar.

Las marcas sólidas<campo 2> se han agregado para \_ Windows 2000 para admitir [**/robust,**](/windows/desktop/Midl/-robust)como la característica de denegación de ataques. Las marcas siguientes se definen en el primer byte:

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

La marca Early indica una correlación temprana frente a tardía. Una correlación temprana es cuando el argumento de expresión precede al argumento descrito, por ejemplo, un argumento de tamaño es anterior a un argumento de puntero de tamaño. Una correlación tardía es cuando el argumento de expresión viene después del argumento relacionado. El motor realiza la validación de los valores de correlación temprana inmediatamente; los valores de correlación en tiempo de ejecución se almacenan para la comprobación una vez que se realiza la desmarque.

La marca Split indica una división asincrónica entre \[ los argumentos de \] entrada \[ y \] salida. Por ejemplo, un argumento de tamaño puede estar en mientras que el puntero de tamaño \[ \] puede ser out \[ \] . En el contexto asincrónico de DCOM, estos argumentos se pueden encontrar en pilas diferentes, por lo que el motor debe tener esto en cuenta.

La marca IsIidIs indica una correlación **de iid \_ is().** La rutina ComposiciónComputeConformance está complicada para obtener un puntero a IID como un valor de expresión, pero la rutina de validación no puede comparar dichos valores (serían punteros) y, por tanto, la marca indica que es necesario comparar los IID reales.

### <a name="variance-description-and-other-array-attributes"></a>Descripción de varianza y otros atributos de matriz

El formato del campo de descripción de varianza es idéntico al campo de descripción de conformidad. La diferencia es que un campo de mensaje de código auxiliar diferente se usa en el motor TEMPORARI como una variable temporal. En el caso de la descripción de varianza, es la longitud que se evalúa y el campo correspondiente se denomina ActualLength.

Con la varianza, el desplazamiento inicial suele ser cero y el motor se optimiza en consecuencia. Si el **primer \_ atributo is()** se aplica a una matriz de variación compatible, se fuerza una devolución de llamada a una rutina de evaluación de expresiones.

 

 