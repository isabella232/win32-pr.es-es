---
title: Uso de los progresos para expresar el relleno y el diseño de memoria
description: Los DirectML se describen mediante propiedades conocidas como los *tamaños* y los *progresos* de la tensores.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b944b1a2600febe27f209bffcc0e355c6a9fc7db
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104549112"
---
# <a name="using-strides-to-express-padding-and-memory-layout"></a>Uso de los progresos para expresar el relleno y el diseño de memoria

Los DirectML &mdash; de los que están respaldados por los búferes de Direct3D 12 &mdash; se describen mediante propiedades conocidas como los *tamaños* y los *progresos* de la tensores. Los *tamaños* de tensores describen las dimensiones lógicas de tensores. Por ejemplo, un tensores 2D podría tener un alto de 2 y un ancho de 3. Lógicamente, el tensores tiene 6 elementos distintos, aunque los tamaños no especifican cómo se almacenan dichos elementos en la memoria. Los *progresos* del tensores describen el diseño de memoria física de los elementos de tensores.

## <a name="two-dimensional-2d-arrays"></a>Matrices bidimensionales (2D)

Considere un tensores 2D que tenga un alto de 2 y un ancho de 3; los datos constan de caracteres de texto. En C/C++, esto podría expresarse mediante una matriz multidimensional.

```cpp
constexpr int rows = 2;
constexpr int columns = 3;
char tensor[rows][columns];
tensor[0][0] = 'A';
tensor[0][1] = 'B';
tensor[0][2] = 'C';
tensor[1][0] = 'D';
tensor[1][1] = 'E';
tensor[1][2] = 'F';
```

A continuación se muestra la vista lógica del tensores anterior.

```console
A B C
D E F
```

En C/C++, una matriz multidimensional se almacena en orden de fila principal. En otras palabras, los elementos consecutivos a lo largo de la dimensión de ancho se almacenan de forma contigua en el espacio de memoria lineal.

Offset:|0|1|2|3|4|5
-|-|-|-|-|-|-
Valor:|A|B|C|D|E|F

El *paso* de una dimensión es el número de elementos que se van a omitir para tener acceso al siguiente elemento de esa dimensión. Progresa el diseño de tensores en memoria. Con un orden de fila principal, el paso de la dimensión de ancho es siempre 1, ya que los elementos adyacentes a lo largo de la dimensión se almacenan de forma contigua. El paso de la dimensión de alto depende del tamaño de la dimensión de ancho; en el ejemplo anterior, la distancia entre los elementos consecutivos a lo largo de la dimensión de alto (por ejemplo, a a D) es igual al ancho de tensores (que es 3 en este ejemplo).

Para ilustrar un diseño diferente, considere el orden de la columna principal. En otras palabras, los elementos consecutivos a lo largo de la dimensión de alto se almacenan de forma contigua en el espacio de memoria lineal. En este caso, el ajuste de alto es siempre 1 y el intervalo de ancho es 2 (el tamaño de la dimensión de alto).

Offset:|0|1|2|3|4|5
-|-|-|-|-|-|-
Valor:|A|D|B|E|C|F

## <a name="higher-dimensions"></a>Dimensiones superiores

Cuando llega a más de dos dimensiones, no es difícil hacer referencia a un diseño como fila principal o columna principal. Por lo tanto, en el resto de este tema se usan términos y etiquetas como estos.

- 2D: &mdash; el alto de "HW" es la dimensión de orden superior (fila principal).
- 2D: el ancho "qu" &mdash; es la dimensión de orden superior (columna principal).
- 3D: la profundidad "DHW" &mdash; es la dimensión de orden superior, seguida de alto y ancho.
- 3D: el ancho "WHD" &mdash; es la dimensión de orden superior, seguido de alto y luego profundidad.
- 4D: "NCHW" &mdash; el número de imágenes (tamaño de lote), después el número de canales, el alto y el ancho.

En general, el paso *empaquetado* de una dimensión es igual al producto de los tamaños de las dimensiones de orden inferior. Por ejemplo, con un diseño "DHW", el intervalo D es igual a H * W; el intervalo H es igual a W; y el intervalo W es igual a 1. Se dice que los progresos están *empaquetados* cuando el tamaño físico total del tensores es igual al tamaño lógico total del tensores; en otras palabras, no hay espacio adicional ni elementos superpuestos.

Vamos a ampliar el ejemplo de 2D a tres dimensiones, de modo que tengamos un tensores con profundidad 2, alto 2 y ancho 3 (para un total de 12 elementos lógicos).

```console
A B C
D E F

G H I
J K L
```

Con un diseño "DHW", este tensores se almacena como se indica a continuación.

Offset:|0|1|2|3|4|5|6|7|8|9|10|11|
-|-|-|-|-|-|-|-|-|-|-|-|-|
Valor:|A|B|C|D|E|F|G|H|I|J|K|L|

- D-STRIDE = alto (2) * ancho (3) = 6 (por ejemplo, la distancia entre ' A ' y ' G ').
- H-STRIDE = ancho (3) = 3 (por ejemplo, la distancia entre ' A ' y ' d ').
- W-STRIDE = 1 (por ejemplo, la distancia entre ' A ' y ' B ').

El producto escalar de los índices/coordenadas de un elemento y los progresos proporciona el desplazamiento a ese elemento en el búfer. Por ejemplo, el desplazamiento del elemento H (d = 1, H = 0, w = 1) es 7.

{1, 0, 1} ⋅ {6, 3, 1} = 1 * 6 + 0 * 3 + 1 * 1 = 7

## <a name="packed-tensors"></a>Decenas empaquetados

En los ejemplos anteriores se ilustran los ampliadores *empaquetados* . Se dice que un tensores está *empaquetado* cuando el tamaño lógico de tensores (en elementos) es igual al tamaño físico del búfer (en elementos) y cada elemento tiene una dirección o desplazamiento único. Por ejemplo, un 2x2x3 tensores se empaqueta si el búfer tiene 12 elementos de longitud y ningún par de elementos comparte el mismo desplazamiento en el búfer. Los diez empaquetados son el caso más común; pero los progresos permiten diseños de memoria más complejos.

## <a name="broadcasting-with-strides"></a>Difusión con grandes progresos

Si el tamaño de búfer de un tensores (en elementos) es menor que el del producto de sus dimensiones lógicas, entonces debe haber una superposición de elementos. El caso habitual de esto se conoce como *difusión*; donde los elementos de una dimensión son un duplicado de otra dimensión. Por ejemplo, volvamos a revisar el ejemplo de 2D. Supongamos que queremos un tensores lógico de 2x3, pero la segunda fila es idéntica a la primera fila. Este es el aspecto.

```console
A B C
A B C
```

Esto podría almacenarse como un tensores de HW/Row principal empaquetado. Pero un almacenamiento más compacto solo incluiría 3 elementos (A, B y C) y usaría un valor de Height-STRIDE 0 en lugar de 3. En este caso, el tamaño físico de la tensores es 3 elementos, pero el tamaño lógico es de 6 elementos.

En general, si el paso de una dimensión es 0, todos los elementos de las dimensiones de orden inferior se repiten a lo largo de la dimensión difundida; por ejemplo, si tensores es NCHW y el intervalo C es 0, cada canal tiene los mismos valores en H y W.

## <a name="padding-with-strides"></a>Relleno con grandes progresos

Se dice que un tensores está *rellenado* si su tamaño físico es mayor que el tamaño mínimo necesario para ajustarse a sus elementos. Cuando no hay elementos de difusión ni superpuestos, el tamaño mínimo de tensores (en elementos) es simplemente el producto de sus dimensiones. Puede usar la función auxiliar `DMLCalcBufferTensorSize` (consulte [funciones auxiliares de DirectML](dml-helper-functions.md) para obtener una lista de esa función) para calcular el tamaño de búfer *mínimo* para los diez DirectML.

Supongamos que un búfer contiene los siguientes valores (los elementos ' x ' indican valores de relleno).

0|1|2|3|4|5|6|7|8|9|
-|-|-|-|-|-|-|-|-|-|
A|B|C|x|x|D|E|F|x|x

El tensores rellenado se puede describir mediante un alto-STRIDE 5 en lugar de 3. En lugar de recorrer 3 elementos para llegar a la siguiente fila, el paso es 5 elementos (3 elementos *reales* más 2 elementos de relleno). El relleno es habitual en los gráficos del equipo, por ejemplo, para asegurarse de que una imagen tiene una alineación de potencia de dos.

```console
A B C
D E F
```

## <a name="directml-buffer-tensor-descriptions"></a>Descripciones de tensores de búfer de DirectML

DirectML puede trabajar con diversos diseños de tensores físicos, ya que la estructura de [ **DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) tiene `Sizes` miembros y `Strides` . Algunas implementaciones de operador pueden ser más eficaces con un diseño específico, por lo que no es raro cambiar cómo se almacenan los datos de tensores para mejorar el rendimiento.

La mayoría de los operadores de DirectML requieren decenas o 5D, y el orden de los valores de los tamaños y los progresos es fijo. Al corregir el orden de los tamaños y los valores de STRIDE en una descripción de tensores, es posible que DirectML deduzca distintos diseños físicos.

**4D**
- [**DML_BUFFER_TENSOR_DESC:: Sizes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = {N-size, C-size, H-size, W-size}
- [**DML_BUFFER_TENSOR_DESC:: progresos**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) = {N-STRIDE, C-STRIDE, H-STRIDE, W-STRIDE}

**1]5D**
- **DML_BUFFER_TENSOR_DESC:: Sizes** = {N-size, C-size, D-size, H-size, W-size}
- **DML_BUFFER_TENSOR_DESC::** saaltos = {N-STRIDE, C-STRIDE, D-STRIDE, H-STRIDE, W-STRIDE}

Si un operador DirectML requiere 4D o un tensores, pero los datos reales tienen un rango más pequeño (por ejemplo, 2D), las dimensiones iniciales se deben rellenar con 1. Por ejemplo, un tensores "HW" se establece mediante **DML_BUFFER_TENSOR_DESC:: Sizes** = {1, 1, H, W}.

Si los datos de tensores se almacenan en NCHW/NCDHW, no es necesario establecer **DML_BUFFER_TENSOR_DESC:: progresa**, a menos que quiera difundir o rellenar. Puede establecer el campo progresa en `nullptr` . Sin embargo, si los datos de tensores se almacenan en otro diseño, como NHWC, deberá progresar para expresar la transformación de NCHW a ese diseño.

Para ver un ejemplo sencillo, considere la descripción de un tensores 2D con el alto 3 y el ancho 5.

**NCHW empaquetado (avances implícitos)**
- **DML_BUFFER_TENSOR_DESC:: Sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: progresos** = `nullptr`

**NCHW empaquetado (los progresos explícitos)**
- N-STRIDE = C-size * H-size * W-size = 1 * 3 * 5 = 15
- C-STRIDE = H-size * W-size = 3 * 5 = 15
- H-STRIDE = W-size = 5
- W-STRIDE = 1
- **DML_BUFFER_TENSOR_DESC:: Sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: progresos** = {15, 15, 5, 1}

**NHWC empaquetado**
- N-STRIDE = H-size * W-Size * C-size = 3 * 5 * 1 = 15
- H-STRIDE = W-Size * C-size = 5 * 1 = 5
- W-STRIDE = C-size = 1
- C-STRIDE = 1
- **DML_BUFFER_TENSOR_DESC:: Sizes** = {1, 1, 3, 5}
- **DML_BUFFER_TENSOR_DESC:: progresos** = {15, 1, 5, 1}

## <a name="see-also"></a>Consulte también

* [Funciones auxiliares de DirectML](dml-helper-functions.md)
* [Estructura de DML_BUFFER_TENSOR_DESC](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)
