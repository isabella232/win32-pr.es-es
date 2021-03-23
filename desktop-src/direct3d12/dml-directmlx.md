---
title: DirectMLX
description: DirectMLX es una biblioteca auxiliar de solo encabezado de C++ para DirectML, diseñada para que sea más fácil crear operadores individuales en los gráficos.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 8388edd51b6ad3ca30fe1c65947167cee7dac5e6
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104549199"
---
# <a name="directmlx"></a>DirectMLX

DirectMLX es una biblioteca auxiliar de solo encabezado de C++ para DirectML, diseñada para que sea más fácil crear operadores individuales en los gráficos.

DirectMLX proporciona contenedores útiles para todos los tipos de operador DirectML (DML), así como las sobrecargas de operador intuitivas, lo que simplifica la creación de instancias de operadores DML y su encadenamiento en gráficos complejos.

## <a name="where-to-find-directmlxh"></a>Dónde encontrar `DirectMLX.h`

`DirectMLX.h` se distribuye como software de código abierto bajo la licencia MIT. Puede encontrar la versión más reciente en [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).

## <a name="tensor-constraints"></a>Restricciones de tensores

DirectMLX requiere la versión de DirectML 1.4.0 o posterior (consulte el [historial de versiones de DirectML](dml-version-history.md#version-table)). No se admiten las versiones anteriores de DirectML.

DirectMLX. h requiere un compilador compatible con C + 11, incluido (pero sin limitarse a):

* Visual Studio 2017
* Visual Studio 2019
* Clang 10

Tenga en cuenta que un compilador de C++ 17 (o posterior) es una opción recomendada. Es posible compilar para C++ 11, pero requiere el uso de bibliotecas de terceros (como [GSL](https://github.com/microsoft/GSL) y [abseil](https://github.com/abseil/abseil-cpp)) para reemplazar la funcionalidad de la biblioteca estándar que falta.

Si tiene una configuración que no se puede compilar `DirectMLX.h` , registre [un problema en el GitHub](https://github.com/microsoft/DirectML/issues).

## <a name="basic-usage"></a>Uso básico

```cpp
#include <DirectML.h>
#include <DirectMLX.h>

IDMLDevice* device;

/* ... */

dml::Scope scope(device);

// Input tensor of type FLOAT32 and sizes { 1, 2, 3, 4 }
auto x = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, {1, 2, 3, 4}));

// Create an operator to compute the square root of x
auto y = dml::Sqrt(x);

// Compile a DirectML operator from the graph. When executed, this compiled operator will compute
// the square root of its input.
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { y });

// Now initialize and dispatch the DML operator as usual
```

Este es otro ejemplo, que crea un grafo de DirectML capaz de calcular la [fórmula cuadrática](https://en.wikipedia.org/wiki/Quadratic_formula).

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

dml::Scope scope(device);

dml::TensorDimensions inputSizes = {1, 2, 3, 4};
auto a = dml::InputTensor(scope, 0, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto b = dml::InputTensor(scope, 1, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));
auto c = dml::InputTensor(scope, 2, dml::TensorDesc(DML_TENSOR_DATA_TYPE_FLOAT32, inputSizes));

auto [x1, x2] = QuadraticFormula(a, b, c);

// When executed with input tensors a, b, and c, this compiled operator computes the two outputs
// of the quadratic formula, and returns them as two output tensors x1 and x2
DML_EXECUTION_FLAGS flags = DML_EXECUTION_FLAG_NONE;
ComPtr<IDMLCompiledOperator> op = scope.Compile(flags, { x1, x2 });

// Now initialize and dispatch the DML operator as usual
```

## <a name="more-examples"></a>Más ejemplos

Puede encontrar ejemplos completos mediante DirectMLX en el [repositorio de github de DirectML](https://github.com/microsoft/DirectML/tree/master/Samples).

## <a name="compile-time-options"></a>Opciones de Compile-Time

DirectMLX admite la #define del tiempo de compilación para personalizar varias partes del encabezado.

|Opción|Descripción|
|-|-|
|**DMLX_NO_EXCEPTIONS**|Si #define, hace que los errores provoquen una llamada a en `std::abort` lugar de producir una excepción. Se define de forma predeterminada si las excepciones no están disponibles (por ejemplo, si se han deshabilitado las excepciones en las opciones del compilador).|
|**DMLX_USE_WIL**|Si #define, las excepciones se inician mediante los tipos de excepción de la [biblioteca de implementación de Windows](https://github.com/microsoft/wil) . En caso contrario, se usan los tipos de excepción estándar (como `std::runtime_error` ). Esta opción no tiene ningún efecto si se define **DMLX_NO_EXCEPTIONS** .|
|**DMLX_USE_ABSEIL**|Si #define, utiliza [abseil](https://github.com/abseil/abseil-cpp) como reemplazos para los tipos de biblioteca estándar no disponibles en c++ 11. Estos tipos incluyen `absl::optional` (en lugar de `std::optional` ), `absl::Span` (en lugar de `std::span` ) y `absl::InlinedVector` .|
|**DMLX_USE_GSL**|Controla si se va a utilizar [GSL](https://github.com/microsoft/GSL) como reemplazo de `std::span` . Si #define, los usos de `std::span` se reemplazan por `gsl::span` en los compiladores sin `std::span` implementaciones nativas. En caso contrario, se proporciona una implementación desplegable en línea. Tenga en cuenta que esta opción solo se usa al compilar en un compilador de C + + 20 sin compatibilidad con `std::span` , y cuando no se está usando ninguna otra sustitución de la biblioteca estándar de destino (por ejemplo, abseil).|

## <a name="controlling-tensor-layout"></a>Controlar el diseño de tensores

Para la mayoría de los operadores, DirectMLX calcula las propiedades de los agentes de salida del operador en su nombre. Por ejemplo, al realizar una `dml::Reduce` operación entre ejes `{ 0, 2, 3 }` con una tensores de entrada de tamaños `{ 3, 4, 5, 6 }` , DirectMLX calculará automáticamente las propiedades de la tensores de salida, incluida la forma correcta de `{ 1, 4, 1, 1 }` .

Sin embargo, las otras propiedades de un tensores de salida incluyen los *progresos*, *TotalTensorSizeInBytes* y *GuaranteedBaseOffsetAlignment*. De forma predeterminada, DirectMLX establece estas propiedades de modo que la tensores no tiene un gran volumen, ninguna alineación de desplazamiento base garantizada y un tamaño total de tensores en bytes calculado por [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).

DirectMLX admite la posibilidad de personalizar estas propiedades de tensores de salida, con objetos conocidos como *directivas de tensores*. Un **TensorPolicy** es una devolución de llamada personalizable que se invoca mediante DirectMLX y devuelve las propiedades de salida tensores dado un tipo de datos calculado, marcas y tamaños de tensores.

Las directivas de tensores se pueden establecer en el objeto **DML:: Scope** y se usarán para todos los operadores subsiguientes en ese gráfico. Las directivas de tensores también se pueden establecer directamente al construir un **TensorDesc**.

Por lo tanto, el diseño de los agregadores generados por DirectMLX se puede controlar mediante la configuración de un **TensorPolicy** que establezca los progresos adecuados en sus decenasdores.

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

// Set the policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy(&MyCustomPolicy));
```

### <a name="example-2"></a>Ejemplo 2

DirectMLX también proporciona algunas directivas de tensores alternativas integradas. La directiva **InterleavedChannel** , por ejemplo, se proporciona como una comodidad, y se puede usar para producir decenas de más, con el fin de que se escriban en orden NHWC.

```cpp
// Set the InterleavedChannel policy on the dml::Scope
dml::Scope scope(/* ... */);
scope.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a>Consulte también

* [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [Ejemplo de DirectMLX yolov4](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [Uso de los progresos para expresar el relleno y el diseño de memoria](./dml-strides.md)
* [Estructura de DML_GRAPH_DESC](./directml/ns-directml-dml_graph_desc.md)