---
title: Descriptores de correlación
description: Un descriptor de correlación es una cadena de formato que describe una expresión basada en un argumento relacionado con otro argumento.
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904791"
---
# <a name="correlation-descriptors"></a>Descriptores de correlación

Un descriptor de correlación es una cadena de formato que describe una expresión basada en un argumento relacionado con otro argumento. Un descriptor de correlación es necesario para administrar la semántica relacionada con atributos como \[ **el tamaño \_ es ()** \] , la \[ **longitud \_ es ()** \] , el \[ **modificador \_ es ()** \] y \[ **IID \_ es ()** \] . Los descriptores de correlación se utilizan con matrices, punteros de tamaño, uniones y punteros de interfaz. El valor de la expresión final puede ser un tamaño, una longitud, un discriminante de unión o un puntero a un IID, respectivamente. En cuanto a las cadenas de formato, los descriptores de correlación se utilizan con matrices, uniones y punteros de interfaz. Un puntero de tamaño se describe en cadenas de formato como un puntero a una matriz.

Hay dos rutinas que realizan cálculos de expresiones básicas: NdrpComputeConformance se usa para tamaños, modificadores y IID, \* mientras que NdrpComputeVariance se usa para longitudes. También hay una rutina única para realizar una validación del valor de correlación para la funcionalidad de denegación de ataque.

Los descriptores de correlación se han diseñado para admitir solo expresiones muy limitadas. En situaciones complicadas, el compilador genera una rutina de evaluación de expresión a la que llamará el motor cuando sea necesario.

Un descriptor de correlación tiene el siguiente formato:

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

El tipo de correlación del descriptor \_ de correlación<1> consta de dos recortes: los 4 bits superiores describen dónde se puede encontrar la expresión y los 4 bits inferiores describen el tipo del valor de la expresión.

El recorte superior puede tener uno de estos cinco valores:

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>COMPATIBILIDAD con FC \_ normal \_
</dt> <dd>

Un caso normal de conformidad, como el que se describe en un campo de una estructura.

</dd> <dt>

<span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>CONFORMIDAD con el \_ puntero FC \_
</dt> <dd>

En el caso de los punteros con atributos (**el tamaño \_ es ()**, la **longitud \_ es ()**), que son campos en una estructura. Esto afecta a la manera en que se establece el puntero de memoria base.

</dd> <dt>

<span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>\_conformidad de \_ nivel \_ superior de FC
</dt> <dd>

Para el cumplimiento de nivel superior descrito por otro parámetro.

</dd> <dt>

<span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>\_conformidad con \_ \_ múltiples niveles \_ de FC superior
</dt> <dd>

Para la conformidad de nivel superior de una matriz multidimensional descrita por otro parámetro.

> [!Note]  
> Las matrices y punteros de tamaño multidimensional desencadenan un cambio a [**– Oicf**](/windows/desktop/Midl/-oi).

 

</dd> <dt>

<span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>CONFORMIDAD de FC \_ Constant \_
</dt> <dd>

Para un valor constante. El compilador calcula el valor de una expresión constante proporcionada por el usuario. En este caso, los 3 bytes siguientes en la descripción del cumplimiento contienen los 3 bytes inferiores de un largo que describe el tamaño del cumplimiento. No es necesario realizar ningún cálculo adicional.

</dd> </dl>

El recorte inferior proporciona el tipo de valor que debe extraerse de la memoria:

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> no se admiten las expresiones de 64 bits. FC \_ Hyper solo se usa para **IID \_ es ()** en plataformas de 64 bits para extraer el valor de puntero para IID \* .
>
> El compilador establece el tipo Nibble en cero para los siguientes casos: expresión constante mencionada anteriormente y cuando es necesario llamar a la rutina de expresión de evaluación, por ejemplo, cuando \_ se utiliza el cumplimiento de la constante FC \_ y la devolución de llamada de FC \_ .

 

El tamaño \_ es \_ OP<1> campo permite aplicar una de las siguientes operaciones a la variable de conformidad:

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

La \_ constante de DESreferencia de FC se usa para que la correlación sea un puntero, como para **\[ el tamaño \_ es ( \* PL) \]**. Los operadores aritméticos solo usan la constante indicada. La constante de devolución de llamada de FC \_ indica que es necesario llamar a una rutina de evaluación de expresión.

El campo offset<2> es normalmente un desplazamiento de memoria relativa a la variable de argumento Expression. También puede ser una evaluación de expresión: índice de rutina. Como se mencionó anteriormente en este documento, para las expresiones constantes forma parte del valor de la expresión final real.

La interpretación del campo offset<2> como desplazamiento de memoria depende de la complejidad de la expresión, la ubicación de la variable Expression y, en el caso de una matriz, si la matriz es realmente un puntero con atributo.

Si la matriz es un puntero con atributos y la variable de conformidad es un campo de una estructura, el campo de desplazamiento contiene el desplazamiento desde el principio de la estructura hasta el campo conformidad-Descripción. Si la matriz no es un puntero con atributos y la variable de conformidad es un campo de una estructura, el campo de desplazamiento contiene el desplazamiento desde el final de la parte no conforme de la estructura hasta el campo conformidad-Descripción. Normalmente, la matriz compatible está al final de la estructura.

En el caso del cumplimiento de nivel superior, el campo de desplazamiento contiene el desplazamiento desde la ubicación del primer parámetro del código auxiliar en la pila hasta el parámetro que describe la conformidad. No se utiliza en modo **– os** . Hay otras excepciones a la interpretación del campo de desplazamiento. dichas excepciones se describen en la descripción de esos tipos.

Cuando se usa offset<2> con \_ la devolución de llamada FC, contiene un índice en la tabla de rutina de evaluación de expresiones generada por el compilador. El mensaje de código auxiliar se pasa a la rutina de evaluación, que luego calcula el valor de conformidad y lo asigna al campo MaxCount del mensaje de código auxiliar.

Se \_ han agregado las marcas sólidas<2> campo para Windows 2000 para admitir [**/Robust**](/windows/desktop/Midl/-robust), como la característica de denegación de ataques. Las marcas siguientes se definen en el primer byte:

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

La marca temprana indica la correlación temprana y tardía. Una correlación temprana es cuando el argumento de expresión precede al argumento descrito; por ejemplo, un argumento de tamaño está delante de un argumento de puntero de tamaño. Una correlación tardía es cuando el argumento de expresión aparece después del argumento relacionado. El motor realiza la validación de los valores de la correlación temprana de inmediato, mientras que los valores de la correlación tardía se almacenan para la comprobación después de que se haya anulado la serialización.

La marca de división indica una división asincrónica entre los \[ \] argumentos in y \[ out \] . Por ejemplo, un argumento de tamaño puede estar \[ en, \] mientras que el puntero de tamaño puede estar \[ fuera \] . En el contexto asincrónico DCOM, estos argumentos se producen en pilas diferentes, por lo que el motor debe ser consciente de ello.

La marca IsIidIs indica que una correlación **\_ es ()** . La rutina NdrComputeConformance se engaña para obtener un puntero a IID como un valor de expresión, pero la rutina de validación no puede comparar estos valores (son punteros) y, por tanto, la marca indica que se deben comparar los IID reales.

### <a name="variance-description-and-other-array-attributes"></a>Descripción de la varianza y otros atributos de la matriz

El formato del campo de descripción de la varianza es idéntico al campo Descripción del cumplimiento. La diferencia es que el motor NDR usa un campo de mensaje de código auxiliar diferente como una variable temporal. En el caso de la descripción de la varianza, es la longitud que se evalúa y el campo correspondiente se denomina ActualLength.

Con varianza, el desplazamiento inicial suele ser cero y el motor se optimiza en consecuencia. Si el **primer atributo \_ es ()** se aplica a una matriz variable conforme, se fuerza una devolución de llamada a una rutina de evaluación de expresión.

 

 