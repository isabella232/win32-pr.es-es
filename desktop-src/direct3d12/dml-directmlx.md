---
title: DirectMLX
description: DirectMLX es una biblioteca auxiliar de solo encabezado de C++ para DirectML, diseñada para facilitar la creación de operadores individuales en gráficos.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/05/2020
ms.openlocfilehash: 2ddd6d9063002b76449224ebafdb6dd021b27fa0
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803371"
---
# <a name="directmlx"></a><span data-ttu-id="f08fb-103">DirectMLX</span><span class="sxs-lookup"><span data-stu-id="f08fb-103">DirectMLX</span></span>

<span data-ttu-id="f08fb-104">DirectMLX es una biblioteca auxiliar de solo encabezado de C++ para DirectML, diseñada para facilitar la creación de operadores individuales en gráficos.</span><span class="sxs-lookup"><span data-stu-id="f08fb-104">DirectMLX is a C++ header-only helper library for DirectML, intended to make it easier to compose individual operators into graphs.</span></span>

<span data-ttu-id="f08fb-105">DirectMLX proporciona contenedores cómodos para todos los tipos de operadores de DirectML (DML), así como sobrecargas de operador intuitivas, lo que facilita la creación de instancias de operadores DML y los encadena en gráficos complejos.</span><span class="sxs-lookup"><span data-stu-id="f08fb-105">DirectMLX provides convenient wrappers for all DirectML (DML) operator types, as well as intuitive operator overloads, which makes it simpler to instantiate DML operators, and chain them into complex graphs.</span></span>

## <a name="where-to-find-directmlxh"></a><span data-ttu-id="f08fb-106">Dónde encontrar `DirectMLX.h`</span><span class="sxs-lookup"><span data-stu-id="f08fb-106">Where to find `DirectMLX.h`</span></span>

<span data-ttu-id="f08fb-107">`DirectMLX.h` se distribuye como software de código abierto bajo la licencia MIT.</span><span class="sxs-lookup"><span data-stu-id="f08fb-107">`DirectMLX.h` is distributed as open-source software under the MIT license.</span></span> <span data-ttu-id="f08fb-108">La versión más reciente se puede encontrar en [GitHub de DirectML.](https://github.com/microsoft/DirectML/tree/master/Libraries)</span><span class="sxs-lookup"><span data-stu-id="f08fb-108">The latest version can be found on the [DirectML GitHub](https://github.com/microsoft/DirectML/tree/master/Libraries).</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f08fb-109">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="f08fb-109">Tensor constraints</span></span>

<span data-ttu-id="f08fb-110">DirectMLX requiere directML versión 1.4.0 o posterior (consulte historial [de versiones de DirectML).](dml-version-history.md#version-table)</span><span class="sxs-lookup"><span data-stu-id="f08fb-110">DirectMLX requires DirectML version 1.4.0, or newer (see [DirectML version history](dml-version-history.md#version-table)).</span></span> <span data-ttu-id="f08fb-111">No se admiten versiones anteriores de DirectML.</span><span class="sxs-lookup"><span data-stu-id="f08fb-111">Older versions of DirectML are not supported.</span></span>

<span data-ttu-id="f08fb-112">DirectMLX.h requiere un compilador compatible con C++11, incluido (entre otros):</span><span class="sxs-lookup"><span data-stu-id="f08fb-112">DirectMLX.h requires a C++11-capable compiler, including (but not limited to):</span></span>

* <span data-ttu-id="f08fb-113">Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="f08fb-113">Visual Studio 2017</span></span>
* <span data-ttu-id="f08fb-114">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="f08fb-114">Visual Studio 2019</span></span>
* <span data-ttu-id="f08fb-115">Clang 10</span><span class="sxs-lookup"><span data-stu-id="f08fb-115">Clang 10</span></span>

<span data-ttu-id="f08fb-116">Tenga en cuenta que un compilador de C++17 (o posterior) es la opción que se recomienda.</span><span class="sxs-lookup"><span data-stu-id="f08fb-116">Note that a C++17 (or newer) compiler is the option that we recommend.</span></span> <span data-ttu-id="f08fb-117">La compilación para C++11 es posible, pero requiere el uso de bibliotecas de terceros (como [GSL](https://github.com/microsoft/GSL) y [Abseil)](https://github.com/abseil/abseil-cpp)para reemplazar la funcionalidad de biblioteca estándar que falta.</span><span class="sxs-lookup"><span data-stu-id="f08fb-117">Compiling for C++11 is possible, but it requires the use of third-party libraries (such as [GSL](https://github.com/microsoft/GSL) and [Abseil](https://github.com/abseil/abseil-cpp)) to replace missing standard library functionality.</span></span>

<span data-ttu-id="f08fb-118">Si tiene una configuración que no se puede `DirectMLX.h` compilar, envíe [un problema a nuestro github.](https://github.com/microsoft/DirectML/issues)</span><span class="sxs-lookup"><span data-stu-id="f08fb-118">If you have a configuration that fails to compile `DirectMLX.h`, then please [file an issue on our GitHub](https://github.com/microsoft/DirectML/issues).</span></span>

## <a name="basic-usage"></a><span data-ttu-id="f08fb-119">Uso básico</span><span class="sxs-lookup"><span data-stu-id="f08fb-119">Basic usage</span></span>

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

<span data-ttu-id="f08fb-120">Este es otro ejemplo, que crea un gráfico de DirectML capaz de calcular la [fórmula cuadrática](https://en.wikipedia.org/wiki/Quadratic_formula).</span><span class="sxs-lookup"><span data-stu-id="f08fb-120">Here's another example, which creates a DirectML graph capable of computing the [quadratic formula](https://en.wikipedia.org/wiki/Quadratic_formula).</span></span>

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

## <a name="more-examples"></a><span data-ttu-id="f08fb-121">Más ejemplos</span><span class="sxs-lookup"><span data-stu-id="f08fb-121">More examples</span></span>

<span data-ttu-id="f08fb-122">Puede encontrar ejemplos completos con DirectMLX en el [repositorio de GitHub de DirectML.](https://github.com/microsoft/DirectML/tree/master/Samples)</span><span class="sxs-lookup"><span data-stu-id="f08fb-122">Complete samples using DirectMLX can be found on the [DirectML GitHub repo](https://github.com/microsoft/DirectML/tree/master/Samples).</span></span>

## <a name="compile-time-options"></a><span data-ttu-id="f08fb-123">Opciones en tiempo de compilación</span><span class="sxs-lookup"><span data-stu-id="f08fb-123">Compile-time options</span></span>

<span data-ttu-id="f08fb-124">DirectMLX admite los #define tiempo de compilación para personalizar varias partes del encabezado.</span><span class="sxs-lookup"><span data-stu-id="f08fb-124">DirectMLX supports compile-time #define's to customize various parts of the header.</span></span>

|<span data-ttu-id="f08fb-125">Opción</span><span class="sxs-lookup"><span data-stu-id="f08fb-125">Option</span></span>|<span data-ttu-id="f08fb-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="f08fb-126">Description</span></span>|
|-|-|
|<span data-ttu-id="f08fb-127">**DMLX_NO_EXCEPTIONS**</span><span class="sxs-lookup"><span data-stu-id="f08fb-127">**DMLX_NO_EXCEPTIONS**</span></span>|<span data-ttu-id="f08fb-128">Si #define, hace que los errores den como resultado una llamada a en `std::abort` lugar de producir una excepción.</span><span class="sxs-lookup"><span data-stu-id="f08fb-128">If #define'd, causes errors to result in a call to `std::abort` rather than throwing an exception.</span></span> <span data-ttu-id="f08fb-129">Esto se define de forma predeterminada si las excepciones no están disponibles (por ejemplo, si las excepciones se han deshabilitado en las opciones del compilador).</span><span class="sxs-lookup"><span data-stu-id="f08fb-129">This is defined by default if exceptions are unavailable (for example, if exceptions have been disabled in the compiler options).</span></span>|
|<span data-ttu-id="f08fb-130">**DMLX_USE_WIL**</span><span class="sxs-lookup"><span data-stu-id="f08fb-130">**DMLX_USE_WIL**</span></span>|<span data-ttu-id="f08fb-131">Si #define, las excepciones se inician mediante tipos de excepción [de la biblioteca de implementación de Windows.](https://github.com/microsoft/wil)</span><span class="sxs-lookup"><span data-stu-id="f08fb-131">If #define'd, exceptions are thrown using [Windows Implementation Library](https://github.com/microsoft/wil) exception types.</span></span> <span data-ttu-id="f08fb-132">De lo contrario, se usan tipos de excepción estándar (como `std::runtime_error` ) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f08fb-132">Otherwise, standard exception types (such as `std::runtime_error`) are used instead.</span></span> <span data-ttu-id="f08fb-133">Esta opción no tiene ningún efecto **si DMLX_NO_EXCEPTIONS** está definido.</span><span class="sxs-lookup"><span data-stu-id="f08fb-133">This option has no effect if **DMLX_NO_EXCEPTIONS** is defined.</span></span>|
|<span data-ttu-id="f08fb-134">**DMLX_USE_ABSEIL**</span><span class="sxs-lookup"><span data-stu-id="f08fb-134">**DMLX_USE_ABSEIL**</span></span>|<span data-ttu-id="f08fb-135">Si #define, usa [Abseil](https://github.com/abseil/abseil-cpp) como reemplazos de colocación para los tipos de biblioteca estándar no disponibles en C++11.</span><span class="sxs-lookup"><span data-stu-id="f08fb-135">If #define'd, uses [Abseil](https://github.com/abseil/abseil-cpp) as drop-in replacements for standard library types unavailable in C++11.</span></span> <span data-ttu-id="f08fb-136">Estos tipos incluyen `absl::optional` (en lugar de `std::optional` ), `absl::Span` (en lugar de `std::span` ) y `absl::InlinedVector` .</span><span class="sxs-lookup"><span data-stu-id="f08fb-136">These types include `absl::optional` (in place of `std::optional`), `absl::Span` (in place of `std::span`), and `absl::InlinedVector`.</span></span>|
|<span data-ttu-id="f08fb-137">**DMLX_USE_GSL**</span><span class="sxs-lookup"><span data-stu-id="f08fb-137">**DMLX_USE_GSL**</span></span>|<span data-ttu-id="f08fb-138">Controla si se debe [usar GSL](https://github.com/microsoft/GSL) como reemplazo de `std::span` .</span><span class="sxs-lookup"><span data-stu-id="f08fb-138">Controls whether to use [GSL](https://github.com/microsoft/GSL) as the replacement for `std::span`.</span></span> <span data-ttu-id="f08fb-139">Si #define, los usos de `std::span` se reemplazan por `gsl::span` en compiladores sin `std::span` implementaciones nativas.</span><span class="sxs-lookup"><span data-stu-id="f08fb-139">If #define'd, uses of `std::span` are replaced by `gsl::span` on compilers without native `std::span` implementations.</span></span> <span data-ttu-id="f08fb-140">De lo contrario, se proporciona una implementación de lista desplegable insertda en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f08fb-140">Otherwise, an inline drop-in implementation is provided instead.</span></span> <span data-ttu-id="f08fb-141">Tenga en cuenta que esta opción solo se usa cuando se compila en un compilador anterior a C++20 sin compatibilidad con y cuando no se usa ningún otro reemplazo de biblioteca estándar de colocación `std::span` (como Abseil).</span><span class="sxs-lookup"><span data-stu-id="f08fb-141">Note that this option is only used when compiling on a pre-C++20 compiler without support for `std::span`, and when no other drop-in standard library replacement (like Abseil) is in use.</span></span>|

## <a name="controlling-tensor-layout"></a><span data-ttu-id="f08fb-142">Controlar el diseño del tensor</span><span class="sxs-lookup"><span data-stu-id="f08fb-142">Controlling tensor layout</span></span>

<span data-ttu-id="f08fb-143">Para la mayoría de los operadores, DirectMLX calcula las propiedades de los tensores de salida del operador en su nombre.</span><span class="sxs-lookup"><span data-stu-id="f08fb-143">For most operators, DirectMLX computes the properties of the operator's output tensors on your behalf.</span></span> <span data-ttu-id="f08fb-144">Por ejemplo, al realizar un en ejes con un tensor de entrada de tamaños , DirectMLX calculará automáticamente las propiedades del `dml::Reduce` tensor de salida, incluida la `{ 0, 2, 3 }` `{ 3, 4, 5, 6 }` forma correcta de `{ 1, 4, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="f08fb-144">For example when performing a `dml::Reduce` across axes `{ 0, 2, 3 }` with an input tensor of sizes `{ 3, 4, 5, 6 }`, DirectMLX will automatically compute the properties of the output tensor including the correct shape of `{ 1, 4, 1, 1 }`.</span></span>

<span data-ttu-id="f08fb-145">Sin embargo, las demás propiedades de un tensor de salida incluyen *Strides*, *TotalTensorSizeInBytes* y *GuaranteedBaseOffsetAlignment.*</span><span class="sxs-lookup"><span data-stu-id="f08fb-145">However, the other properties of an output tensor include the *Strides*, *TotalTensorSizeInBytes*, and *GuaranteedBaseOffsetAlignment*.</span></span> <span data-ttu-id="f08fb-146">De forma predeterminada, DirectMLX establece estas propiedades de forma que el tensor no tenga ninguna estructura de striding, ninguna alineación de desplazamiento base garantizada y un tamaño de tensor total en bytes calculado por [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span><span class="sxs-lookup"><span data-stu-id="f08fb-146">By default, DirectMLX sets these properties such that the tensor has no striding, no guaranteed base offset alignment, and a total tensor size in bytes as computed by [DMLCalcBufferTensorSize](./dml-helper-functions.md#dmlcalcbuffertensorsize).</span></span>

<span data-ttu-id="f08fb-147">DirectMLX admite la capacidad de personalizar estas propiedades de tensor de salida, mediante objetos conocidos como *directivas de tensor.*</span><span class="sxs-lookup"><span data-stu-id="f08fb-147">DirectMLX supports the ability to customize these output tensor properties, using objects known as *tensor policies*.</span></span> <span data-ttu-id="f08fb-148">**TensorPolicy** es una devolución de llamada personalizable invocada por DirectMLX y devuelve propiedades de tensor de salida según el tipo de datos, las marcas y los tamaños calculados de un tensor.</span><span class="sxs-lookup"><span data-stu-id="f08fb-148">A **TensorPolicy** is a customizable callback that is invoked by DirectMLX, and returns output tensor properties given a tensor's computed data type, flags, and sizes.</span></span>

<span data-ttu-id="f08fb-149">Las directivas de Tensor se pueden establecer en el **objeto dml::Graph** y se usarán para todos los operadores posteriores de ese gráfico.</span><span class="sxs-lookup"><span data-stu-id="f08fb-149">Tensor policies can be set on the **dml::Graph** object, and will be used for all subsequent operators on that graph.</span></span> <span data-ttu-id="f08fb-150">Las directivas de Tensor también se pueden establecer directamente al construir **un objeto TensorDesc.**</span><span class="sxs-lookup"><span data-stu-id="f08fb-150">Tensor policies can also be set directly when constructing a **TensorDesc**.</span></span>

<span data-ttu-id="f08fb-151">Por lo tanto, el diseño de tensores generado por DirectMLX se puede controlar estableciendo **una propiedad TensorPolicy** que establece los avances adecuados en sus tensores.</span><span class="sxs-lookup"><span data-stu-id="f08fb-151">The layout of tensors produced by DirectMLX can therefore be controlled by setting a **TensorPolicy** that sets the appropriate strides on its tensors.</span></span>

### <a name="example-1"></a><span data-ttu-id="f08fb-152">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="f08fb-152">Example 1</span></span>

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

### <a name="example-2"></a><span data-ttu-id="f08fb-153">Ejemplo 2</span><span class="sxs-lookup"><span data-stu-id="f08fb-153">Example 2</span></span>

<span data-ttu-id="f08fb-154">DirectMLX también proporciona algunas directivas alternativas de tensor integradas.</span><span class="sxs-lookup"><span data-stu-id="f08fb-154">DirectMLX also provides some alternative tensor policies built-in.</span></span> <span data-ttu-id="f08fb-155">La **directiva InterleavedChannel,** por ejemplo, se proporciona por comodidad y se puede usar para generar tensores con avances, de modo que se escriban en orden NHWC.</span><span class="sxs-lookup"><span data-stu-id="f08fb-155">The **InterleavedChannel** policy, for example, is provided as a convenience, and it can be used to produce tensors with strides such that they are written in NHWC order.</span></span>

```cpp
// Set the InterleavedChannel policy on the dml::Graph
dml::Graph graph(/* ... */);
graph.SetTensorPolicy(dml::TensorPolicy::InterleavedChannel());

// When executed, the tensor `result` will be in NHWC layout (rather than the default NCHW)
auto result = dml::Convolution(/* ... */);
```

## <a name="see-also"></a><span data-ttu-id="f08fb-156">Consulta también</span><span class="sxs-lookup"><span data-stu-id="f08fb-156">See also</span></span>

* [<span data-ttu-id="f08fb-157">DirectML GitHub</span><span class="sxs-lookup"><span data-stu-id="f08fb-157">DirectML GitHub</span></span>](https://github.com/microsoft/DirectML/tree/master/Libraries)
* [<span data-ttu-id="f08fb-158">Ejemplo yolov4 de DirectMLX</span><span class="sxs-lookup"><span data-stu-id="f08fb-158">DirectMLX yolov4 sample</span></span>](https://github.com/microsoft/DirectML/tree/master/Samples/yolov4)
* [<span data-ttu-id="f08fb-159">Uso de strides para expresar el relleno y el diseño de memoria</span><span class="sxs-lookup"><span data-stu-id="f08fb-159">Using strides to express padding and memory layout</span></span>](./dml-strides.md)
* [<span data-ttu-id="f08fb-160">DML_GRAPH_DESC estructura</span><span class="sxs-lookup"><span data-stu-id="f08fb-160">DML_GRAPH_DESC structure</span></span>](./directml/ns-directml-dml_graph_desc.md)