---
title: DirectMLX
description: DirectMLX es una biblioteca auxiliar de solo encabezado de C++ para DirectML, diseñada para facilitar la creación de operadores individuales en gráficos.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: ba7eca27a39b690f678bdac1ea0feba1991e8b40
ms.sourcegitcommit: d168355cd7112871f24643b4079c2640b36f4975
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111521222"
---
# <a name="directmlx"></a>DirectMLX

DirectMLX es una biblioteca auxiliar de solo encabezado de C++ para DirectML, diseñada para facilitar la creación de operadores individuales en gráficos.

DirectMLX proporciona contenedores cómodos para todos los tipos de operadores de DirectML (DML), así como sobrecargas de operador intuitivas, lo que facilita la creación de instancias de operadores DML y los encadena en gráficos complejos.

## <a name="where-to-find-directmlxh"></a>Dónde encontrar `DirectMLX.h`

`DirectMLX.h` se distribuye como software de código abierto bajo la licencia MIT. La versión más reciente se puede encontrar en [GitHub de DirectML.](https://github.com/microsoft/DirectML/tree/master/Libraries)

## <a name="tensor-constraints"></a>Restricciones de tensor

DirectMLX requiere directML versión 1.4.0 o posterior (consulte historial [de versiones de DirectML).](dml-version-history.md#version-table) No se admiten versiones anteriores de DirectML.

DirectMLX.h requiere un compilador compatible con C++11, incluido (entre otros):

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Tenga en cuenta que un compilador de C++17 (o posterior) es la opción que se recomienda. La compilación para C++11 es posible, pero requiere el uso de bibliotecas de terceros (como [GSL](https://github.com/microsoft/GSL) y [Abseil)](https://github.com/abseil/abseil-cpp)para reemplazar la funcionalidad de biblioteca estándar que falta.

Si tiene una configuración que no se puede `DirectMLX.h` compilar, envíe [un problema a nuestro github.](https://github.com/microsoft/DirectML/issues)

## <a name="basic-usage"></a>Uso básico

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Graph graph(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

Este es otro ejemplo, que crea un gráfico de DirectML capaz de calcular la [fórmula cuadrática](https://en.wikipedia.org/wiki/Quadratic_formula).

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

std::pair<dml::Expression, dml::Expression>
    QuadraticFormula(dml::Expression a, dml::Expression b, dml::Expression c)
{
    // Quadratic formula: given an equation of the form ax^2 + bx + c = 0, x can be found by:
    //   x = -b +/- sqrt(b^2 - 4ac) / (2a)
    // https://en.wikipedia.org/wiki/Quadratic_formula

    // Note: DirectMLX provides operator overloads for common mathematical expressions. So for 
    // example a*c is equivalent to dml::Multiply(a, c).
    auto x1 = -b + dml::Sqrt(b*b - 4*a*c) / (2*a);
    auto x2 = -b - dml::Sqrt(b*b - 4*a*c) / (2*a);

    return { x1, x2 };
}

/* ... */

dml::Graph graph(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(graph, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(graph, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(graph, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = graph.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a>Más ejemplos

Puede encontrar ejemplos completos con DirectMLX en el [repositorio de GitHub de DirectML.](https://github.com/microsoft/DirectML/tree/master/Samples)

## <a name="compile-time-options"></a>Opciones en tiempo de compilación

DirectMLX admite los #define tiempo de compilación para personalizar varias partes del encabezado.

|Opción|Descripción|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Si #define, hace que los errores den como resultado una llamada a `std::abort` en lugar de producir una excepción. Esto se define de forma predeterminada si las excepciones no están disponibles (por ejemplo, si las excepciones se han deshabilitado en las opciones del compilador).|
|**DMLX_USE_WIL**|Si #define, las excepciones se inician mediante tipos de excepción de la [Biblioteca de implementación de Windows.](https://github.com/microsoft/wil) De lo contrario, se usan tipos de excepción estándar (como `std::runtime_error` ) en su lugar. Esta opción no tiene ningún efecto **si DMLX_NO_EXCEPTIONS** está definido.|
|**DMLX_USE_ABSEIL**|Si #define, usa [Abseil](https://github.com/abseil/abseil-cpp) como reemplazos desplegables para los tipos de biblioteca estándar no disponibles en C++11. Estos tipos incluyen `absl::optional` (en lugar de `std::optional` ), `absl::Span` (en lugar de `std::span` ) y `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Controla si se debe [usar GSL](https://github.com/microsoft/GSL) como reemplazo de `std::span` . Si #define, los usos de `std::span` se reemplazan por en `gsl::span` compiladores sin `std::span` implementaciones nativas. De lo contrario, se proporciona en su lugar una implementación de colocación insertda. Tenga en cuenta que esta opción solo se usa cuando se compila en un compilador anterior a C++20 sin compatibilidad con y cuando no se usa ningún otro reemplazo de biblioteca estándar de `std::span` colocación (como Abseil).|

## <a name="controlling-tensor-layout"></a>Control del diseño del tensor

Para la mayoría de los operadores, DirectMLX calcula las propiedades de los tensores de salida del operador en su nombre. Por ejemplo, al realizar un objeto entre ejes con un tensor de entrada de tamaños , DirectMLX calculará automáticamente las propiedades del `dml::Reduce` `{ 0, 2, 3 }` `{ 3, 4, 5, 6 }` tensor de salida, incluida la forma correcta de `{ 1, 4, 1, 1 }` .

Sin embargo, las demás propiedades de un tensor de salida incluyen *Strides*, *TotalTensorSizeInBytes* y *GuaranteedBaseOffsetAlignment*. De forma predeterminada, DirectMLX establece estas propiedades de modo que el tensor no tenga ninguna striding, ninguna alineación de desplazamiento base garantizada y un tamaño de tensor total en bytes calculado por [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).

DirectMLX admite la capacidad de personalizar estas propiedades de tensor de salida mediante objetos conocidos como *directivas de tensor.* **TensorPolicy** es una devolución de llamada personalizable invocada por DirectMLX y devuelve propiedades de tensor de salida según el tipo de datos, las marcas y los tamaños calculados de un tensor.

Las directivas de Tensor se pueden establecer en el **objeto dml::Graph** y se usarán para todos los operadores posteriores de ese gráfico. Las directivas de Tensor también se pueden establecer directamente al construir **un objeto TensorDesc.**

Por lo tanto, el diseño de los tensores generado por DirectMLX se puede controlar estableciendo **una propiedad TensorPolicy** que establece los avances adecuados en sus tensores.

### <a name="example-1"></a>Ejemplo 1

```cpp
// Define a policy, which is a function that returns a TensorProperties given a data type,
// flags, and sizes.
dml::TensorProperties MyCustomPolicy(
    DML_TENSOR_DATA_TYPE dataType,
    DML_TENSOR_FLAGS flags,
    Span<const uint32_t> sizes)
{
    // Compute your custom strides, total tensor size in bytes, and guaranteed base
    // offset alignment
    dml::TensorProperties props;
    props.strides = /* ... */;
    props.totalTensorSizeInBytes = /* ... */;
    props.guaranteedBaseOffsetAlignment = /* ... */;
    return props;
};

// Set the policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a>Ejemplo 2

DirectMLX también proporciona algunas directivas alternativas de tensor integradas. La **directiva InterleavedChannel,** por ejemplo, se proporciona por comodidad y se puede usar para generar tensores con avances, de modo que se escriban en orden NHWC.

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>Vea también

* [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [Ejemplo yolov4 de DirectMLX](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Uso de strides para expresar el relleno y el diseño de memoria](./dml-strides.md)
* [DML_GRAPH_DESC estructura](/windows/win32/api/directml/ns-directml-dml_graph_desc)