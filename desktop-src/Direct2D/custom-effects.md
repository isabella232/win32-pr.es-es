---
title: Efectos personalizados
description: Muestra cómo escribir sus propios efectos personalizados mediante HLSL estándar.
ms.assetid: 5D22CA84-6465-4882-863D-81A632ACDD9C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca6b15fe81ff4ccbd6cebbcee8c0d1955967056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149600"
---
# <a name="custom-effects"></a><span data-ttu-id="ecffa-103">Efectos personalizados</span><span class="sxs-lookup"><span data-stu-id="ecffa-103">Custom effects</span></span>

<span data-ttu-id="ecffa-104">[Direct2D](./direct2d-portal.md) se suministra con una biblioteca de efectos que realizan una serie de operaciones de imagen comunes.</span><span class="sxs-lookup"><span data-stu-id="ecffa-104">[Direct2D](./direct2d-portal.md) ships with a library of effects that perform a variety of common image operations.</span></span> <span data-ttu-id="ecffa-105">Vea el tema sobre [efectos integrados](built-in-effects.md) para obtener una lista completa de los efectos.</span><span class="sxs-lookup"><span data-stu-id="ecffa-105">See the [built-in effects](built-in-effects.md) topic for the complete list of effects.</span></span> <span data-ttu-id="ecffa-106">En el caso de las funciones que no se pueden lograr con los efectos integrados, Direct2D le permite escribir sus propios efectos personalizados mediante [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)estándar.</span><span class="sxs-lookup"><span data-stu-id="ecffa-106">For functionality that cannot be achieved with the built-in effects, Direct2D allows you to write your own custom effects using standard [HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl).</span></span> <span data-ttu-id="ecffa-107">Puede usar estos efectos personalizados junto con los efectos integrados que se envían con Direct2D.</span><span class="sxs-lookup"><span data-stu-id="ecffa-107">You can use these custom effects alongside the built-in effects that ship with Direct2D.</span></span>

<span data-ttu-id="ecffa-108">Para ver ejemplos de un efecto completo de píxeles, vértices y sombreador de cálculo, consulte el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="ecffa-108">To see examples of a complete pixel, vertex, and compute shader effect, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="ecffa-109">En este tema, le mostraremos los pasos y los conceptos que necesita para diseñar y crear un efecto personalizado con todas las características.</span><span class="sxs-lookup"><span data-stu-id="ecffa-109">In this topic, we show you the steps and concepts you need to design and create a fully-featured custom effect.</span></span>

## <a name="introduction-what-is-inside-an-effect"></a><span data-ttu-id="ecffa-110">Introducción: ¿Qué hay dentro de un efecto?</span><span class="sxs-lookup"><span data-stu-id="ecffa-110">Introduction: What is inside an effect?</span></span>

![diagrama de efecto de sombra paralela.](images/custom-effects1.png)

<span data-ttu-id="ecffa-112">Conceptualmente, un efecto de [Direct2D](./direct2d-portal.md) realiza una tarea de creación de imágenes, como cambiar el brillo, dessaturar una imagen o como se mostró anteriormente, creando una sombra paralela.</span><span class="sxs-lookup"><span data-stu-id="ecffa-112">Conceptually, a [Direct2D](./direct2d-portal.md) effect performs an imaging task, like changing brightness, de-saturating an image, or as shown above, creating a drop shadow.</span></span> <span data-ttu-id="ecffa-113">En la aplicación, son sencillas.</span><span class="sxs-lookup"><span data-stu-id="ecffa-113">To the app, they are simple.</span></span> <span data-ttu-id="ecffa-114">Pueden aceptar cero o más imágenes de entrada, exponer varias propiedades que controlan su funcionamiento y generar una sola imagen de salida.</span><span class="sxs-lookup"><span data-stu-id="ecffa-114">They can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="ecffa-115">Hay cuatro partes diferentes de un efecto personalizado que el autor de un efecto es responsable de:</span><span class="sxs-lookup"><span data-stu-id="ecffa-115">There are four different parts of a custom effect that an effect author is responsible for:</span></span>

1.  <span data-ttu-id="ecffa-116">Interfaz de efecto: la interfaz de efecto define conceptualmente cómo interactúa una aplicación con un efecto personalizado (como cuántas entradas acepta el efecto y qué propiedades están disponibles).</span><span class="sxs-lookup"><span data-stu-id="ecffa-116">Effect Interface: The effect interface conceptually defines how an app interacts with a custom effect (like how many inputs the effect accepts and what properties are available).</span></span> <span data-ttu-id="ecffa-117">La interfaz de efecto administra un gráfico de transformación, que contiene las operaciones de creación de imágenes reales.</span><span class="sxs-lookup"><span data-stu-id="ecffa-117">The effect interface manages a transform graph, which contains the actual imaging operations.</span></span>
2.  <span data-ttu-id="ecffa-118">Transformar gráfico: cada efecto crea un gráfico de transformación interno formado por transformaciones individuales.</span><span class="sxs-lookup"><span data-stu-id="ecffa-118">Transform graph: Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="ecffa-119">Cada transformación representa una operación de una sola imagen.</span><span class="sxs-lookup"><span data-stu-id="ecffa-119">Each transform represents a single image operation.</span></span> <span data-ttu-id="ecffa-120">El efecto es responsable de vincular estas transformaciones en un gráfico para realizar el efecto de imagen previsto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-120">The effect is responsible for linking these transforms together into a graph to perform the intended imaging effect.</span></span> <span data-ttu-id="ecffa-121">Un efecto puede Agregar, quitar, modificar y reordenar las transformaciones en respuesta a los cambios en las propiedades externas del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-121">An effect can add, remove, modify, and reorder transforms in response to changes to the effect's external properties.</span></span>
3.  <span data-ttu-id="ecffa-122">Transform: una transformación representa una operación de una sola imagen.</span><span class="sxs-lookup"><span data-stu-id="ecffa-122">Transform: A transform represents a single image operation.</span></span> <span data-ttu-id="ecffa-123">Su finalidad principal es hospedar los sombreadores que se ejecutan para cada píxel de salida.</span><span class="sxs-lookup"><span data-stu-id="ecffa-123">Its main purpose is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="ecffa-124">Para ello, es responsable de calcular el nuevo tamaño de la imagen de salida basándose en la lógica de sus sombreadores.</span><span class="sxs-lookup"><span data-stu-id="ecffa-124">To that end, it is responsible for calculating the new size of its output image based on logic in its shaders.</span></span> <span data-ttu-id="ecffa-125">También debe calcular qué área de la imagen de entrada deben leer los sombreadores para representar la región de salida solicitada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-125">It also must calculate which area of its input image the shaders need to read from to render the requested output region.</span></span>
4.  <span data-ttu-id="ecffa-126">Sombreador: se ejecuta un sombreador en la entrada de la transformación en la GPU (o CPU si se especifica la representación de software cuando la aplicación crea el dispositivo Direct3D).</span><span class="sxs-lookup"><span data-stu-id="ecffa-126">Shader: A shader is executed against the transform's input on the GPU (or CPU if software rendering is specified when the app creates the Direct3D device).</span></span> <span data-ttu-id="ecffa-127">Los sombreadores de efectos se escriben en el lenguaje de sombreado de alto nivel ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) y se compilan en código de bytes durante la compilación del efecto, que después se carga por el efecto durante el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ecffa-127">Effect shaders are written in High Level Shading Language ([HLSL](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl)) and are compiled into byte code during the effect's compilation, which is then loaded by the effect during run-time.</span></span> <span data-ttu-id="ecffa-128">En este documento de referencia se describe cómo escribir HLSL compatible con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ecffa-128">This reference document describes how to write [Direct2D](./direct2d-portal.md)-compliant HLSL.</span></span> <span data-ttu-id="ecffa-129">La documentación de Direct3D contiene información general básica de HLSL.</span><span class="sxs-lookup"><span data-stu-id="ecffa-129">The Direct3D documentation contains a basic HLSL overview.</span></span>

## <a name="creating-an-effect-interface"></a><span data-ttu-id="ecffa-130">Crear una interfaz de efecto</span><span class="sxs-lookup"><span data-stu-id="ecffa-130">Creating an effect interface</span></span>

<span data-ttu-id="ecffa-131">La interfaz de efecto define cómo interactúa una aplicación con el efecto personalizado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-131">The effect interface defines how an app interacts with the custom effect.</span></span> <span data-ttu-id="ecffa-132">Para crear una interfaz de efecto, una clase debe implementar ID2D1EffectImpl, definir metadatos que describan el efecto (como su nombre, recuento de entradas y propiedades) y crear métodos que registren el efecto personalizado para su uso con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ecffa-132">To create an effect interface, a class must implement ID2D1EffectImpl, define metadata that describes the effect (such as its name, input count and properties), and create methods that register the custom effect for use with [Direct2D](./direct2d-portal.md).</span></span>

<span data-ttu-id="ecffa-133">Una vez que se han implementado todos los componentes de una interfaz de efecto, el encabezado de la clase se parecerá a este:</span><span class="sxs-lookup"><span data-stu-id="ecffa-133">Once all of the components for an effect interface have been implemented, the class' header will appear like this:</span></span>


```C++
#include <d2d1_1.h>
#include <d2d1effectauthor.h>  
#include <d2d1effecthelpers.h>

// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);

class SampleEffect : public ID2D1EffectImpl
{
public:
    // 2.1 Declare ID2D1EffectImpl implementation methods.
    IFACEMETHODIMP Initialize(
        _In_ ID2D1EffectContext* pContextInternal,
        _In_ ID2D1TransformGraph* pTransformGraph
        );

    IFACEMETHODIMP PrepareForRender(D2D1_CHANGE_TYPE changeType);
    IFACEMETHODIMP SetGraph(_In_ ID2D1TransformGraph* pGraph);

    // 2.2 Declare effect registration methods.
    static HRESULT Register(_In_ ID2D1Factory1* pFactory);
    static HRESULT CreateEffect(_Outptr_ IUnknown** ppEffectImpl);

    // 2.3 Declare IUnknown implementation methods.
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(_In_ REFIID riid, _Outptr_ void** ppOutput);

private:
    // Constructor should be private since it should never be called externally.
    SampleEffect();

    LONG m_refCount; // Internal ref count used by AddRef() and Release() methods.
};
```



### <a name="implement-id2d1effectimpl"></a><span data-ttu-id="ecffa-134">Implementación de ID2D1EffectImpl</span><span class="sxs-lookup"><span data-stu-id="ecffa-134">Implement ID2D1EffectImpl</span></span>

<span data-ttu-id="ecffa-135">La interfaz [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) contiene tres métodos que debe implementar:</span><span class="sxs-lookup"><span data-stu-id="ecffa-135">The [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) interface contains three methods that you must implement:</span></span>

### <a name="initializeid2d1effectcontext-pcontextinternal-id2d1transformgraph-ptransformgraph"></a><span data-ttu-id="ecffa-136">Initialize (ID2D1EffectContext \* pContextInternal, ID2D1TransformGraph \* pTransformGraph)</span><span class="sxs-lookup"><span data-stu-id="ecffa-136">Initialize(ID2D1EffectContext \*pContextInternal, ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="ecffa-137">[Direct2D](./direct2d-portal.md) llama al método [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) una vez que la aplicación ha llamado al método [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-137">[Direct2D](./direct2d-portal.md) calls the [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method after the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method has been called by the app.</span></span> <span data-ttu-id="ecffa-138">Puede utilizar este método para realizar la inicialización interna o cualquier otra operación necesaria para el efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-138">You can use this method to perform internal initialization or any other operations needed for the effect.</span></span> <span data-ttu-id="ecffa-139">Además, puede utilizarlo para crear el gráfico de transformación inicial del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-139">Additionally, you can use it to create the effect's initial transform graph.</span></span>

### <a name="setgraphid2d1transformgraph-ptransformgraph"></a><span data-ttu-id="ecffa-140">SetGraph (ID2D1TransformGraph \* pTransformGraph)</span><span class="sxs-lookup"><span data-stu-id="ecffa-140">SetGraph(ID2D1TransformGraph \*pTransformGraph)</span></span>

<span data-ttu-id="ecffa-141">[Direct2D](./direct2d-portal.md) llama al método [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) cuando se cambia el número de entradas del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-141">[Direct2D](./direct2d-portal.md) calls the [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) method when the number of inputs to the effect is changed.</span></span> <span data-ttu-id="ecffa-142">Aunque la mayoría de los efectos tienen un número constante de entradas, otras como el [efecto compuesto](composite.md) admiten un número variable de entradas.</span><span class="sxs-lookup"><span data-stu-id="ecffa-142">While most effects have a constant number of inputs, others like the [Composite effect](composite.md) support a variable number of inputs.</span></span> <span data-ttu-id="ecffa-143">Este método permite que estos efectos actualicen su gráfico de transformación en respuesta a un recuento de entrada cambiante.</span><span class="sxs-lookup"><span data-stu-id="ecffa-143">This method allows these effects to update their transform graph in response to a changing input count.</span></span> <span data-ttu-id="ecffa-144">Si un efecto no admite un recuento de entrada variable, este método simplemente puede devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="ecffa-144">If an effect does not support a variable input count, this method can simply return E\_NOTIMPL.</span></span>

### <a name="prepareforrender-d2d1_change_type-changetype"></a><span data-ttu-id="ecffa-145">PrepareForRender (tipo de cambio de D2D1 \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="ecffa-145">PrepareForRender (D2D1\_CHANGE\_TYPE changeType)</span></span>

<span data-ttu-id="ecffa-146">El método [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) proporciona una oportunidad para que los efectos realicen operaciones en respuesta a cambios externos.</span><span class="sxs-lookup"><span data-stu-id="ecffa-146">The [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method provides an opportunity for effects to perform any operations in response to external changes.</span></span> <span data-ttu-id="ecffa-147">[Direct2D](./direct2d-portal.md) llama a este método justo antes de representar un efecto si al menos uno de ellos es true:</span><span class="sxs-lookup"><span data-stu-id="ecffa-147">[Direct2D](./direct2d-portal.md) calls this method just before it renders an effect if at least one of these is true:</span></span>

-   <span data-ttu-id="ecffa-148">El efecto se ha inicializado anteriormente, pero aún no se ha dibujado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-148">The effect has been previously initialized but not yet drawn.</span></span>
-   <span data-ttu-id="ecffa-149">Una propiedad de efecto ha cambiado desde la última llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="ecffa-149">An effect property has changed since the last draw call.</span></span>
-   <span data-ttu-id="ecffa-150">El estado del contexto de [Direct2D](./direct2d-portal.md) que realiza la llamada (como dpi) ha cambiado desde la última llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="ecffa-150">The state of the calling [Direct2D](./direct2d-portal.md) context (like DPI) has changed since the last draw call.</span></span>

### <a name="implement-the-effect-registration-and-callback-methods"></a><span data-ttu-id="ecffa-151">Implementar los métodos de registro y devolución de llamada de efecto</span><span class="sxs-lookup"><span data-stu-id="ecffa-151">Implement the effect registration and callback methods</span></span>

<span data-ttu-id="ecffa-152">Las aplicaciones deben registrar efectos con [Direct2D](./direct2d-portal.md) antes de crear una instancia de ellos.</span><span class="sxs-lookup"><span data-stu-id="ecffa-152">Apps must register effects with [Direct2D](./direct2d-portal.md) before instantiating them.</span></span> <span data-ttu-id="ecffa-153">Este registro está en el ámbito de una instancia de un generador de Direct2D y debe repetirse cada vez que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-153">This registration is scoped to an instance of a Direct2D factory, and must be repeated each time the app is run.</span></span> <span data-ttu-id="ecffa-154">Para habilitar este registro, un efecto personalizado define un GUID único, un método público que registra el efecto y un método de devolución de llamada privado que devuelve una instancia del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-154">To enable this registration, a custom effect defines a unique GUID, a public method that registers the effect, and a private callback method that returns an instance of the effect.</span></span>

### <a name="define-a-guid"></a><span data-ttu-id="ecffa-155">Definir un GUID</span><span class="sxs-lookup"><span data-stu-id="ecffa-155">Define a GUID</span></span>

<span data-ttu-id="ecffa-156">Debe definir un GUID que identifique de forma única el efecto de registro con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ecffa-156">You must define a GUID that uniquely identifies the effect for registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="ecffa-157">La aplicación usa el mismo para identificar el efecto cuando llama a [**ID2D1DeviceContext:: CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span><span class="sxs-lookup"><span data-stu-id="ecffa-157">The app uses the same to identify the effect when it calls [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect).</span></span>

<span data-ttu-id="ecffa-158">Este código muestra cómo definir dicho GUID para un efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-158">This code demonstrates defining such a GUID for an effect.</span></span> <span data-ttu-id="ecffa-159">Debe crear su propio GUID único mediante una herramienta de generación de GUID como guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="ecffa-159">You must create its own unique GUID using a GUID generation tool such as guidgen.exe.</span></span>


```C++
// Example GUID used to uniquely identify the effect. It is passed to Direct2D during
// effect registration, and used by the developer to identify the effect for any
// ID2D1DeviceContext::CreateEffect calls in the app. The app should create
// a unique name for the effect, as well as a unique GUID using a generation tool.
DEFINE_GUID(CLSID_SampleEffect, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="define-a-public-registration-method"></a><span data-ttu-id="ecffa-160">Definir un método de registro público</span><span class="sxs-lookup"><span data-stu-id="ecffa-160">Define a public registration method</span></span>

<span data-ttu-id="ecffa-161">A continuación, defina un método público para que la aplicación llame a para registrar el efecto con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ecffa-161">Next, define a public method for the app to call to register the effect with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="ecffa-162">Dado que el registro de efectos es específico de una instancia de un generador de Direct2D, el método acepta una interfaz [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) como parámetro.</span><span class="sxs-lookup"><span data-stu-id="ecffa-162">Because effect registration is specific to an instance of a Direct2D factory, the method accepts an [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface as a parameter.</span></span> <span data-ttu-id="ecffa-163">Para registrar el efecto, el método llama entonces a la API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) en el parámetro **ID2D1Factory1** .</span><span class="sxs-lookup"><span data-stu-id="ecffa-163">To register the effect, the method then calls the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API on the **ID2D1Factory1** parameter.</span></span>

<span data-ttu-id="ecffa-164">Esta API acepta una cadena XML que describe los metadatos, las entradas y las propiedades del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-164">This API accepts an XML string that describes the metadata, inputs, and properties of the effect.</span></span> <span data-ttu-id="ecffa-165">Los metadatos de un efecto solo tienen fines informativos y la aplicación puede consultarlos a través de la interfaz [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-165">The metadata for an effect is for informational purposes only, and can be queried by the app through the [**ID2D1Properties**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1properties) interface.</span></span> <span data-ttu-id="ecffa-166">Los datos de entrada y de propiedad, por otro lado, se usan en [Direct2D](./direct2d-portal.md) y representan la funcionalidad del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-166">The input and property data, on the other hand, is used by [Direct2D](./direct2d-portal.md) and represents the effect's functionality.</span></span>

<span data-ttu-id="ecffa-167">Aquí se muestra una cadena XML para un efecto de muestra mínimo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-167">An XML string for a minimal sample effect is shown here.</span></span> <span data-ttu-id="ecffa-168">La adición de propiedades personalizadas al XML se trata en la sección agregar propiedades personalizadas a un efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-168">Adding custom properties to the XML is covered in the Adding custom properties to an effect section.</span></span>


```XML
#define XML(X) TEXT(#X) // This macro creates a single string from multiple lines of text.

PCWSTR pszXml =
    XML(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description' type='string' value='This is a demo effect.'/>
            <Inputs>
                <Input name='SourceOne'/>
                <!-- <Input name='SourceTwo'/> -->
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
        </Effect>
        );
```



### <a name="define-an-effect-factory-callback-method"></a><span data-ttu-id="ecffa-169">Definir un método de devolución de llamada del generador de efectos</span><span class="sxs-lookup"><span data-stu-id="ecffa-169">Define an effect factory callback method</span></span>

<span data-ttu-id="ecffa-170">El efecto también debe proporcionar un método de devolución de llamada privado que devuelva una instancia del efecto a través de un único \* \* parámetro IUnknown.</span><span class="sxs-lookup"><span data-stu-id="ecffa-170">The effect must also provide a private callback method that returns an instance of the effect through a single IUnknown\*\* parameter.</span></span> <span data-ttu-id="ecffa-171">Se proporciona un puntero a este método a [Direct2D](./direct2d-portal.md) cuando el efecto se registra a través de la API [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) a través del parámetro de [**\_ \_ generador de efectos PD2D1**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) \\ .</span><span class="sxs-lookup"><span data-stu-id="ecffa-171">A pointer to this method is provided to [Direct2D](./direct2d-portal.md) when the effect is registered via the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) API through the [**PD2D1\_EFFECT\_FACTORY**](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory)\\ parameter.</span></span>


```C++
HRESULT __stdcall SampleEffect::CreateEffect(_Outptr_ IUnknown** ppEffectImpl)
{
    // This code assumes that the effect class initializes its reference count to 1.
    *ppEffectImpl = static_cast<ID2D1EffectImpl*>(new SampleEffect());

    if (*ppEffectImpl == nullptr)
    {
        return E_OUTOFMEMORY;
    }

    return S_OK;
}
```



### <a name="implement-the-iunknown-interface"></a><span data-ttu-id="ecffa-172">Implementar la interfaz IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecffa-172">Implement the IUnknown interface</span></span>

<span data-ttu-id="ecffa-173">Por último, el efecto debe implementar la interfaz IUnknown para la compatibilidad con COM.</span><span class="sxs-lookup"><span data-stu-id="ecffa-173">Finally, the effect must implement the IUnknown interface for compatibility with COM.</span></span>

## <a name="creating-the-effects-transform-graph"></a><span data-ttu-id="ecffa-174">Crear el gráfico de transformación del efecto</span><span class="sxs-lookup"><span data-stu-id="ecffa-174">Creating the effect's transform graph</span></span>

<span data-ttu-id="ecffa-175">Un efecto puede usar varias transformaciones diferentes (operaciones de imagen individuales) para crear el efecto de imagen deseado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-175">An effect can use several different transforms (individual image operations) to create its desired imaging effect.</span></span> <span data-ttu-id="ecffa-176">Para controlar el orden en el que estas transformaciones se aplican a la imagen de entrada, el efecto las organiza en un gráfico de transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-176">To control the order in which these transforms are applied to the input image, the effect arranges them into a transform graph.</span></span> <span data-ttu-id="ecffa-177">Un gráfico de transformación puede hacer uso de los efectos y las transformaciones incluidos en [Direct2D](./direct2d-portal.md) , así como las transformaciones personalizadas creadas por el autor del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-177">A transform graph can make use of the effects and transforms included in [Direct2D](./direct2d-portal.md) as well as custom transforms created by the effect author.</span></span>

### <a name="using-transforms-included-with-direct2d"></a><span data-ttu-id="ecffa-178">Usar transformaciones incluidas con Direct2D</span><span class="sxs-lookup"><span data-stu-id="ecffa-178">Using transforms included with Direct2D</span></span>

<span data-ttu-id="ecffa-179">Estas son las transformaciones que se usan con más frecuencia y que se proporcionan con [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ecffa-179">These are the most commonly used transforms provided with [Direct2D](./direct2d-portal.md).</span></span>

-   <span data-ttu-id="ecffa-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): esta transformación combina un número arbitrario de entradas en función de una descripción de Blend, vea el tema de [**\_ \_ Descripción de D2D1 Blend**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) y el [ejemplo de modos de efecto compuesto de Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) para obtener ejemplos de fusión.</span><span class="sxs-lookup"><span data-stu-id="ecffa-180">[**ID2D1BlendTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1blendtransform): This transform blends an arbitrary number of inputs together based on a blend description, see the [**D2D1\_BLEND\_DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) topic and the [Direct2D composite effect modes sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample) for blending examples.</span></span> <span data-ttu-id="ecffa-181">Esta transformación es devuelta por el método [**ID2D1EffectContext:: CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-181">This transform is returned by the [**ID2D1EffectContext::CreateBlendTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createblendtransform) method.</span></span>
-   <span data-ttu-id="ecffa-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): esta transformación expande el tamaño de salida de una imagen según el [**\_ \_ modo de extensión D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) especificado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-182">[**ID2D1BorderTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1bordertransform): This transform expands an image's output size according to the [**D2D1\_EXTEND\_MODE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) specified.</span></span> <span data-ttu-id="ecffa-183">Esta transformación es devuelta por el método [**ID2D1EffectContext:: CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-183">This transform is returned by the [**ID2D1EffectContext::CreateBorderTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createbordertransform) method.</span></span>
-   <span data-ttu-id="ecffa-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): esta transformación desplaza (traduce) su entrada en cualquier número entero de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ecffa-184">[**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform): This transform offsets (translates) its input by any whole number of pixels.</span></span> <span data-ttu-id="ecffa-185">Esta transformación es devuelta por el método [**ID2D1EffectContext:: CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-185">This transform is returned by the [**ID2D1EffectContext::CreateOffsetTransform**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createoffsettransform) method.</span></span>
-   <span data-ttu-id="ecffa-186">Cualquier efecto existente se puede tratar como una transformación con el fin de transformar la creación del gráfico mediante el método [**ID2D1EffectContext:: CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-186">Any existing effect can be treated as a transform for the purposes of transform graph creation by using the [**ID2D1EffectContext::CreateTransformNodeFromEffect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createtransformnodefromeffect) method.</span></span>

### <a name="creating-a-single-node-transform-graph"></a><span data-ttu-id="ecffa-187">Crear un gráfico de transformación de un solo nodo</span><span class="sxs-lookup"><span data-stu-id="ecffa-187">Creating a single-node transform graph</span></span>

<span data-ttu-id="ecffa-188">Una vez que se crea una transformación, la entrada del efecto debe estar conectada a la entrada de la transformación y la salida de la transformación debe estar conectada a la salida del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-188">Once you create a transform, the effect's input needs to be connected to the transform's input, and the transform's output needs to be connected to the effect's output.</span></span> <span data-ttu-id="ecffa-189">Cuando un efecto solo contiene una única transformación, puede usar el método [**ID2D1TransformGraph:: SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) para lograrlo fácilmente.</span><span class="sxs-lookup"><span data-stu-id="ecffa-189">When an effect only contains a single transform, you can use the [**ID2D1TransformGraph::SetSingleTransformNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setsingletransformnode) method to easily accomplish this.</span></span>

<span data-ttu-id="ecffa-190">Puede crear o modificar una transformación en los métodos [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) o [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) del efecto mediante el parámetro ID2D1TransformGraph proporcionado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-190">You can create or modify a transform in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) or [**SetGraph**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-setgraph) methods using the provided ID2D1TransformGraph parameter.</span></span> <span data-ttu-id="ecffa-191">Si un efecto tiene que realizar cambios en el gráfico de transformación en otro método en el que este parámetro no está disponible, el efecto puede guardar el parámetro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) como una variable miembro de la clase y acceder a él en otro lugar, como [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) o un método de devolución de llamada de propiedad personalizada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-191">If an effect needs to make changes to the transform graph in another method where this parameter is not available, the effect can save the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter as a member variable of the class and access it elsewhere, such as [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) or a custom property callback method.</span></span>

<span data-ttu-id="ecffa-192">Aquí se muestra un método de [**inicialización**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-192">A sample [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method is shown here.</span></span> <span data-ttu-id="ecffa-193">Este método crea un gráfico de transformación de un solo nodo que desplaza la imagen en 100 píxeles en cada eje.</span><span class="sxs-lookup"><span data-stu-id="ecffa-193">This method creates a single-node transform graph that offsets the image by one hundred pixels in each axis.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext,
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{
    HRESULT hr = pEffectContext->CreateOffsetTransform(
        D2D1::Point2L(100,100),  // Offsets the input by 100px in each axis.
        &m_pOffsetTransform
        );

    if (SUCCEEDED(hr))
    {
        // Connects the effect's input to the transform's input, and connects
        // the transform's output to the effect's output.
        hr = pTransformGraph->SetSingleTransformNode(m_pOffsetTransform);
    }

    return hr;
}
```



### <a name="creating-a-multi-node-transform-graph"></a><span data-ttu-id="ecffa-194">Crear un gráfico de transformación de varios nodos</span><span class="sxs-lookup"><span data-stu-id="ecffa-194">Creating a multi-node transform graph</span></span>

<span data-ttu-id="ecffa-195">Agregar varias transformaciones al gráfico de transformación de un efecto permite que los efectos realicen internamente varias operaciones de imagen que se presentan a una aplicación como un solo efecto unificado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-195">Adding multiple transforms to an effect's transform graph allows effects to internally perform multiple image operations that are presented to an app as a single unified effect.</span></span>

<span data-ttu-id="ecffa-196">Como se indicó anteriormente, el gráfico de transformación del efecto se puede editar en cualquier método de efecto mediante el parámetro [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) recibido en el método [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-196">As noted above, the effect's transform graph may be edited in any effect method using the [**ID2D1TransformGraph**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transformgraph) parameter received in the effect's [**Initialize**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-initialize) method.</span></span> <span data-ttu-id="ecffa-197">Las siguientes API de esa interfaz se pueden usar para crear o modificar un gráfico de transformación de un efecto:</span><span class="sxs-lookup"><span data-stu-id="ecffa-197">The following APIs on that interface can be used to create or modify an effect's transform graph:</span></span>

### <a name="addnodeid2d1transformnode-pnode"></a><span data-ttu-id="ecffa-198">AddNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="ecffa-198">AddNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="ecffa-199">El método [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) , en efecto, ' registra ' la transformación con el efecto y se debe llamar antes de que se pueda usar la transformación con cualquiera de los demás métodos del gráfico de transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-199">The [**AddNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-addnode) method, in effect, 'registers' the transform with the effect, and must be called before the transform can be used with any of the other transform graph methods.</span></span>

### <a name="connecttoeffectinputuint32-toeffectinputindex-id2d1transformnode-pnode-uint32-tonodeinputindex"></a><span data-ttu-id="ecffa-200">ConnectToEffectInput (UINT32 toEffectInputIndex, ID2D1TransformNode \* pNode, UINT32 toNodeInputIndex)</span><span class="sxs-lookup"><span data-stu-id="ecffa-200">ConnectToEffectInput(UINT32 toEffectInputIndex, ID2D1TransformNode \*pNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="ecffa-201">El método [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) conecta la entrada de imagen del efecto a la entrada de una transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-201">The [**ConnectToEffectInput**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connecttoeffectinput) method connects the effect's image input to a transform's input.</span></span> <span data-ttu-id="ecffa-202">La misma entrada de efecto puede estar conectada a varias transformaciones.</span><span class="sxs-lookup"><span data-stu-id="ecffa-202">The same effect input can be connected to multiple transforms.</span></span>

### <a name="connectnodeid2d1transformnode-pfromnode-id2d1transformnode-ptonode-uint32-tonodeinputindex"></a><span data-ttu-id="ecffa-203">ConnectNode (ID2D1TransformNode \* pFromNode, ID2D1TransformNode \* PTONODE, UINT32 toNodeInputIndex)</span><span class="sxs-lookup"><span data-stu-id="ecffa-203">ConnectNode(ID2D1TransformNode \*pFromNode, ID2D1TransformNode \*pToNode, UINT32 toNodeInputIndex)</span></span>

<span data-ttu-id="ecffa-204">El método [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) conecta la salida de una transformación a otra entrada de la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-204">The [**ConnectNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-connectnode) method connects a transform's output to another transform's input.</span></span> <span data-ttu-id="ecffa-205">Una salida de transformación se puede conectar a varias transformaciones.</span><span class="sxs-lookup"><span data-stu-id="ecffa-205">A transform output can be connected to multiple transforms.</span></span>

### <a name="setoutputnodeid2d1transformnode-pnode"></a><span data-ttu-id="ecffa-206">SetOutputNode (ID2D1TransformNode \* pNode)</span><span class="sxs-lookup"><span data-stu-id="ecffa-206">SetOutputNode(ID2D1TransformNode \*pNode)</span></span>

<span data-ttu-id="ecffa-207">El método [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) conecta la salida de una transformación a la salida del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-207">The [**SetOutputNode**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transformgraph-setoutputnode) method connects a transform's output to the effect's output.</span></span> <span data-ttu-id="ecffa-208">Dado que un efecto solo tiene una salida, solo se puede designar una única transformación como el "nodo de salida".</span><span class="sxs-lookup"><span data-stu-id="ecffa-208">Because an effect only has one output, only a single transform can be designated as the 'output node'.</span></span>

<span data-ttu-id="ecffa-209">Este código usa dos transformaciones independientes para crear un efecto unificado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-209">This code uses two separate transforms to create a unified effect.</span></span> <span data-ttu-id="ecffa-210">En este caso, el efecto es una sombra paralela traducida.</span><span class="sxs-lookup"><span data-stu-id="ecffa-210">In this case, the effect is a translated drop shadow.</span></span>


```C++
IFACEMETHODIMP SampleEffect::Initialize(
    _In_ ID2D1EffectContext* pEffectContext, 
    _In_ ID2D1TransformGraph* pTransformGraph
    )
{   
    // Create the shadow effect.
    HRESULT hr = pEffectContext->CreateEffect(CLSID_D2D1Shadow, &m_pShadowEffect);

    // Create the shadow transform from the shadow effect.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateTransformNodeFromEffect(m_pShadowEffect, &m_pShadowTransform);
    }

    // Create the offset transform.
    if (SUCCEEDED(hr))
    {
        hr = pEffectContext->CreateOffsetTransform(
            D2D1::Point2L(0,0),
            &m_pOffsetTransform
            );
    }

    // Register both transforms with the effect graph.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pShadowTransform);
    }

    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->AddNode(m_pOffsetTransform);
    }

    // Connect the custom effect's input to the shadow transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectToEffectInput(
            0,                  // Input index of the effect.
            m_pShadowTransform, // The receiving transform.
            0                   // Input index of the receiving transform.
            );
    }

    // Connect the shadow transform's output to the offset transform's input.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->ConnectNode(
            m_pShadowTransform, // 'From' node.
            m_pOffsetTransform, // 'To' node.
            0                   // Input index of the 'to' node. There is only one output for the 'From' node.
            );
    }

    // Connect the offset transform's output to the custom effect's output.
    if (SUCCEEDED(hr))
    {
        hr = pTransformGraph->SetOutputNode(
            m_pOffsetTransform
            );
    }

    return hr;
}
```



## <a name="adding-custom-properties-to-an-effect"></a><span data-ttu-id="ecffa-211">Agregar propiedades personalizadas a un efecto</span><span class="sxs-lookup"><span data-stu-id="ecffa-211">Adding custom properties to an effect</span></span>

<span data-ttu-id="ecffa-212">Los efectos pueden definir propiedades personalizadas que permiten a una aplicación cambiar el comportamiento del efecto durante el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="ecffa-212">Effects can define custom properties that allow an app to change the effect's behavior during runtime.</span></span> <span data-ttu-id="ecffa-213">Hay tres pasos para definir una propiedad para un efecto personalizado:</span><span class="sxs-lookup"><span data-stu-id="ecffa-213">There are three steps to define a property for a custom effect:</span></span>

### <a name="add-the-property-metadata-to-the-effects-registration-data"></a><span data-ttu-id="ecffa-214">Agregar los metadatos de la propiedad a los datos de registro del efecto</span><span class="sxs-lookup"><span data-stu-id="ecffa-214">Add the property metadata to the effect's registration data</span></span>

### <a name="add-property-to-registration-xml"></a><span data-ttu-id="ecffa-215">Agregar propiedad a XML de registro</span><span class="sxs-lookup"><span data-stu-id="ecffa-215">Add property to registration XML</span></span>

<span data-ttu-id="ecffa-216">Debe definir las propiedades de un efecto personalizado durante el registro inicial del efecto en [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ecffa-216">You must define a custom effect's properties during the effect's initial registration with [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="ecffa-217">En primer lugar, debe actualizar el XML de registro del efecto en su método de registro público con la nueva propiedad:</span><span class="sxs-lookup"><span data-stu-id="ecffa-217">First, you must update the effect's registration XML in its public registration method with the new property:</span></span>


```C++
PCWSTR pszXml =
    TEXT(
        <?xml version='1.0'?>
        <Effect>
            <!-- System Properties -->
            <Property name='DisplayName' type='string' value='SampleEffect'/>
            <Property name='Author' type='string' value='Contoso'/>
            <Property name='Category' type='string' value='Sample'/>
            <Property name='Description'
                type='string'
                value='Translates an image by a user-specifiable amount.'/>
            <Inputs>
                <Input name='Source'/>
                <!-- Additional inputs go here. -->
            </Inputs>
            <!-- Custom Properties go here. -->
            <Property name='Offset' type='vector2'>
                <Property name='DisplayName' type='string' value='Image Offset'/>
                <!— Optional sub-properties -->
                <Property name='Min' type='vector2' value='(-1000.0, -1000.0)' />
                <Property name='Max' type='vector2' value='(1000.0, 1000.0)' />
                <Property name='Default' type='vector2' value='(0.0, 0.0)' />
            </Property>
        </Effect>
        );
```



<span data-ttu-id="ecffa-218">Cuando se define una propiedad de efecto en XML, se necesita un nombre, un tipo y un nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ecffa-218">When you define an effect property in XML, it needs a name, a type, and a display name.</span></span> <span data-ttu-id="ecffa-219">El nombre para mostrar de una propiedad, así como los valores de categoría, autor y descripción del efecto general, pueden y deben localizarse.</span><span class="sxs-lookup"><span data-stu-id="ecffa-219">A property's display name, as well as the overall effect's category, author, and description values can and should be localized.</span></span>

<span data-ttu-id="ecffa-220">Para cada propiedad, un efecto puede especificar opcionalmente valores predeterminados, mínimos y máximos.</span><span class="sxs-lookup"><span data-stu-id="ecffa-220">For each property, an effect can optionally specify default, min, and max values.</span></span> <span data-ttu-id="ecffa-221">Estos valores son solo para uso informativo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-221">These values are for informational use only.</span></span> <span data-ttu-id="ecffa-222">No se aplican en [Direct2D](./direct2d-portal.md).</span><span class="sxs-lookup"><span data-stu-id="ecffa-222">They are not enforced by [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="ecffa-223">Depende de usted implementar la lógica predeterminada/Min/Max especificada en la clase Effect.</span><span class="sxs-lookup"><span data-stu-id="ecffa-223">It is up to you to implement any specified default/min/max logic in the effect class yourself.</span></span>

<span data-ttu-id="ecffa-224">El valor de tipo que aparece en el XML de la propiedad debe coincidir con el tipo de datos correspondiente utilizado por los métodos de captador y establecedor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="ecffa-224">The type value listed in the XML for the property must match the corresponding data type used by the property's getter and setter methods.</span></span> <span data-ttu-id="ecffa-225">En esta tabla se muestran los valores XML correspondientes para cada tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="ecffa-225">Corresponding XML values for each data type are shown in this table:</span></span>



| <span data-ttu-id="ecffa-226">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="ecffa-226">Data type</span></span>                                                                                                                              | <span data-ttu-id="ecffa-227">Valor XML correspondiente</span><span class="sxs-lookup"><span data-stu-id="ecffa-227">Corresponding XML value</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="ecffa-228">PWSTR</span><span class="sxs-lookup"><span data-stu-id="ecffa-228">PWSTR</span></span>                                                                                                                                  | <span data-ttu-id="ecffa-229">string</span><span class="sxs-lookup"><span data-stu-id="ecffa-229">string</span></span>                  |
| <span data-ttu-id="ecffa-230">BOOL</span><span class="sxs-lookup"><span data-stu-id="ecffa-230">BOOL</span></span>                                                                                                                                   | <span data-ttu-id="ecffa-231">bool</span><span class="sxs-lookup"><span data-stu-id="ecffa-231">bool</span></span>                    |
| <span data-ttu-id="ecffa-232">UINT</span><span class="sxs-lookup"><span data-stu-id="ecffa-232">UINT</span></span>                                                                                                                                   | <span data-ttu-id="ecffa-233">uint32</span><span class="sxs-lookup"><span data-stu-id="ecffa-233">uint32</span></span>                  |
| <span data-ttu-id="ecffa-234">INT</span><span class="sxs-lookup"><span data-stu-id="ecffa-234">INT</span></span>                                                                                                                                    | <span data-ttu-id="ecffa-235">int32</span><span class="sxs-lookup"><span data-stu-id="ecffa-235">int32</span></span>                   |
| <span data-ttu-id="ecffa-236">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ecffa-236">FLOAT</span></span>                                                                                                                                  | <span data-ttu-id="ecffa-237">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ecffa-237">float</span></span>                   |
| [<span data-ttu-id="ecffa-238">**\_Vector D2D \_ 2F**</span><span class="sxs-lookup"><span data-stu-id="ecffa-238">**D2D\_VECTOR\_2F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f)                                                                                               | <span data-ttu-id="ecffa-239">vector2</span><span class="sxs-lookup"><span data-stu-id="ecffa-239">vector2</span></span>                 |
| [<span data-ttu-id="ecffa-240">**\_Vector D2D \_ 3F**</span><span class="sxs-lookup"><span data-stu-id="ecffa-240">**D2D\_VECTOR\_3F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f)                                                                                               | <span data-ttu-id="ecffa-241">Vector3</span><span class="sxs-lookup"><span data-stu-id="ecffa-241">vector3</span></span>                 |
| [<span data-ttu-id="ecffa-242">**D2D \_ Vector \_ 4F**</span><span class="sxs-lookup"><span data-stu-id="ecffa-242">**D2D\_VECTOR\_4F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f)                                                                                               | <span data-ttu-id="ecffa-243">Vector4</span><span class="sxs-lookup"><span data-stu-id="ecffa-243">vector4</span></span>                 |
| <span data-ttu-id="ecffa-244">[**D2D \_ Matrix \_ 3x2 \_ F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span><span class="sxs-lookup"><span data-stu-id="ecffa-244">[**D2D\_MATRIX\_3X2\_F**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-strokecontainspoint(d2d1_point_2f_float_id2d1strokestyle_constd2d1_matrix_3x2_f__bool))</span></span> | <span data-ttu-id="ecffa-245">matrix3x2</span><span class="sxs-lookup"><span data-stu-id="ecffa-245">matrix3x2</span></span>               |
| [<span data-ttu-id="ecffa-246">**D2D \_ Matrix \_ 4X3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="ecffa-246">**D2D\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)                                                                                        | <span data-ttu-id="ecffa-247">matrix4x3</span><span class="sxs-lookup"><span data-stu-id="ecffa-247">matrix4x3</span></span>               |
| [<span data-ttu-id="ecffa-248">**\_Matriz D2D \_ 4x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="ecffa-248">**D2D\_MATRIX\_4X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f)                                                                                        | <span data-ttu-id="ecffa-249">matrix4x4</span><span class="sxs-lookup"><span data-stu-id="ecffa-249">matrix4x4</span></span>               |
| [<span data-ttu-id="ecffa-250">**D2D \_ Matrix \_ 5x4 \_ F**</span><span class="sxs-lookup"><span data-stu-id="ecffa-250">**D2D\_MATRIX\_5X4\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f)                                                                                        | <span data-ttu-id="ecffa-251">matrix5x4</span><span class="sxs-lookup"><span data-stu-id="ecffa-251">matrix5x4</span></span>               |
| <span data-ttu-id="ecffa-252">BYTES\[\]</span><span class="sxs-lookup"><span data-stu-id="ecffa-252">BYTE\[\]</span></span>                                                                                                                               | <span data-ttu-id="ecffa-253">blob</span><span class="sxs-lookup"><span data-stu-id="ecffa-253">blob</span></span>                    |
| <span data-ttu-id="ecffa-254">IUnknown\*</span><span class="sxs-lookup"><span data-stu-id="ecffa-254">IUnknown\*</span></span>                                                                                                                             | <span data-ttu-id="ecffa-255">IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecffa-255">iunknown</span></span>                |
| <span data-ttu-id="ecffa-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span><span class="sxs-lookup"><span data-stu-id="ecffa-256">[**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)\*</span></span>                                                                                       | <span data-ttu-id="ecffa-257">colorcontext</span><span class="sxs-lookup"><span data-stu-id="ecffa-257">colorcontext</span></span>            |
| <span data-ttu-id="ecffa-258">CLSID</span><span class="sxs-lookup"><span data-stu-id="ecffa-258">CLSID</span></span>                                                                                                                                  | <span data-ttu-id="ecffa-259">clsid</span><span class="sxs-lookup"><span data-stu-id="ecffa-259">clsid</span></span>                   |
| <span data-ttu-id="ecffa-260">Enumeración [**( \_ \_ modo de interpolación D2D1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span><span class="sxs-lookup"><span data-stu-id="ecffa-260">Enumeration ([**D2D1\_INTERPOLATION\_MODE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_interpolation_mode), etc.)</span></span>                                                | <span data-ttu-id="ecffa-261">enum</span><span class="sxs-lookup"><span data-stu-id="ecffa-261">enum</span></span>                    |



 

### <a name="map-the-new-property-to-getter-and-setter-methods"></a><span data-ttu-id="ecffa-262">Asignar la nueva propiedad a métodos getter y Setter</span><span class="sxs-lookup"><span data-stu-id="ecffa-262">Map the new property to getter and setter methods</span></span>

<span data-ttu-id="ecffa-263">A continuación, el efecto debe asignar esta nueva propiedad a los métodos getter y Setter.</span><span class="sxs-lookup"><span data-stu-id="ecffa-263">Next, the effect must map this new property to getter and setter methods.</span></span> <span data-ttu-id="ecffa-264">Esto se hace a través de la matriz de [**\_ \_ enlace de la propiedad D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) que se pasa al método [**ID2D1Factory1:: RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-264">This is done through the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array that is passed into the [**ID2D1Factory1::RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method.</span></span>

<span data-ttu-id="ecffa-265">La matriz de [**\_ \_ enlace de la propiedad D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) tiene el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="ecffa-265">The [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array looks like this:</span></span>


```C++
const D2D1_PROPERTY_BINDING bindings[] =
{
    D2D1_VALUE_TYPE_BINDING(
        L"Offset",      // The name of property. Must match name attribute in XML.
        &SetOffset,     // The setter method that is called on "SetValue".
        &GetOffset      // The getter method that is called on "GetValue".
        )
};
```



<span data-ttu-id="ecffa-266">Una vez que cree la matriz XML y los enlaces, pásela al método [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) :</span><span class="sxs-lookup"><span data-stu-id="ecffa-266">Once you create the XML and bindings array, pass them into the [**RegisterEffectFromString**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring) method:</span></span>


```C++
pFactory->RegisterEffectFromString(
    CLSID_SampleEffect,  // GUID defined in class header file.
    pszXml,              // Previously-defined XML that describes effect.
    bindings,            // The previously-defined property bindings array.
    ARRAYSIZE(bindings), // Number of entries in the property bindings array.    
    CreateEffect         // Static method that returns an instance of the effect's class.
    );
```



<span data-ttu-id="ecffa-267">La \_ macro de enlace de tipo de valor D2D1 \_ \_ requiere que la clase de efecto herede de [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) antes que cualquier otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="ecffa-267">The D2D1\_VALUE\_TYPE\_BINDING macro requires the effect class to inherit from [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl) before any other interface.</span></span>

<span data-ttu-id="ecffa-268">Las propiedades personalizadas de un efecto se indizan en el orden en el que se declaran en el XML y, una vez creada, la aplicación puede acceder a ella mediante los métodos [**ID2D1Properties:: SetValue**](id2d1properties-setvalue-overload.md) y [**ID2D1Properties:: GetValue**](id2d1properties-getvalue-overload.md) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-268">Custom properties for an effect are indexed in the order they are declared in the XML, and once created can be accessed by the app using the [**ID2D1Properties::SetValue**](id2d1properties-setvalue-overload.md) and [**ID2D1Properties::GetValue**](id2d1properties-getvalue-overload.md) methods.</span></span> <span data-ttu-id="ecffa-269">Para mayor comodidad, puede crear una enumeración pública que muestre cada propiedad en el archivo de encabezado del efecto:</span><span class="sxs-lookup"><span data-stu-id="ecffa-269">For convenience, you can create a public enumeration that lists each property in the effect's header file:</span></span>


```C++
typedef enum SAMPLEEFFECT_PROP
{
    SAMPLEFFECT_PROP_OFFSET = 0
};
```



### <a name="create-the-getter-and-setter-methods-for-the-property"></a><span data-ttu-id="ecffa-270">Crear los métodos de captador y establecedor para la propiedad</span><span class="sxs-lookup"><span data-stu-id="ecffa-270">Create the getter and setter methods for the property</span></span>

<span data-ttu-id="ecffa-271">El siguiente paso consiste en crear los métodos de captador y establecedor para la nueva propiedad.</span><span class="sxs-lookup"><span data-stu-id="ecffa-271">The next step is to create the getter and setter methods for the new property.</span></span> <span data-ttu-id="ecffa-272">Los nombres de los métodos deben coincidir con los especificados en la matriz de [**\_ \_ enlace de la propiedad D2D1**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-272">The names of the methods must match the ones specified in the [**D2D1\_PROPERTY\_BINDING**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) array.</span></span> <span data-ttu-id="ecffa-273">Además, el tipo de propiedad especificado en el XML del efecto debe coincidir con el tipo del parámetro del método setter y el valor devuelto del método del captador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-273">In addition, the property type specified in the effect's XML must match the type of the setter method's parameter and the getter method's return value.</span></span>


```C++
HRESULT SampleEffect::SetOffset(D2D_VECTOR_2F offset)
{
    // Method must manually clamp to values defined in XML.
    offset.x = min(offset.x, 1000.0f); 
    offset.x = max(offset.x, -1000.0f); 

    offset.y = min(offset.y, 1000.0f); 
    offset.y = max(offset.y, -1000.0f); 

    m_offset = offset;

    return S_OK;
}

D2D_VECTOR_2F SampleEffect::GetOffset() const
{
    return m_offset;
}
```



### <a name="update-effects-transforms-in-response-to-property-change"></a><span data-ttu-id="ecffa-274">Transformaciones del efecto de actualización en respuesta al cambio de propiedad</span><span class="sxs-lookup"><span data-stu-id="ecffa-274">Update effect's transforms in response to property change</span></span>

<span data-ttu-id="ecffa-275">Para actualizar realmente la salida de la imagen de un efecto en respuesta a un cambio de propiedad, el efecto debe cambiar sus transformaciones subyacentes.</span><span class="sxs-lookup"><span data-stu-id="ecffa-275">To actually update an effect's image output in response to a property change, the effect needs to change its underlying transforms.</span></span> <span data-ttu-id="ecffa-276">Esto se hace normalmente en el método [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) del efecto, al que [Direct2D](./direct2d-portal.md) llama automáticamente cuando se ha cambiado una de las propiedades de un efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-276">This is typically done in the effect's [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender) method which [Direct2D](./direct2d-portal.md) automatically calls when one of an effect's properties has been changed.</span></span> <span data-ttu-id="ecffa-277">Sin embargo, las transformaciones se pueden actualizar en cualquiera de los métodos del efecto: como inicializar o los métodos de establecedor de propiedad del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-277">However, transforms can be updated in any of the effect's methods: such as Initialize or the effect's property setter methods.</span></span>

<span data-ttu-id="ecffa-278">Por ejemplo, si un efecto contenía un [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) y desea modificar su valor de desplazamiento en respuesta a la propiedad de desplazamiento del efecto que se está cambiando, agregaría el código siguiente en [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span><span class="sxs-lookup"><span data-stu-id="ecffa-278">For example, if an effect contained an [**ID2D1OffsetTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1offsettransform) and wanted to modify its offset value in response to the effect's Offset property being changed, it would add the following code in [**PrepareForRender**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectimpl-prepareforrender):</span></span>


```C++
IFACEMETHODIMP SampleEffect::PrepareForRender(D2D1_CHANGE_TYPE changeType)
{
    // All effect properties are DPI independent (specified in DIPs). In this offset
    // example, the offset value provided must be scaled from DIPs to pixels to ensure
    // a consistent appearance at different DPIs (excluding minor scaling artifacts).
    // A context's DPI can be retrieved using the ID2D1EffectContext::GetDPI API.
    
    D2D1_POINT_2L pixelOffset;
    pixelOffset.x = static_cast<LONG>(m_offset.x * (m_dpiX / 96.0f));
    pixelOffset.y = static_cast<LONG>(m_offset.y * (m_dpiY / 96.0f));
    
    // Update the effect's offset transform with the new offset value.
    m_pOffsetTransform->SetOffset(pixelOffset);

    return S_OK;
}
```



## <a name="creating-a-custom-transform"></a><span data-ttu-id="ecffa-279">Crear una transformación personalizada</span><span class="sxs-lookup"><span data-stu-id="ecffa-279">Creating a custom transform</span></span>

<span data-ttu-id="ecffa-280">Para implementar las operaciones de imagen más allá de lo que se proporciona en [Direct2D](./direct2d-portal.md), debe implementar transformaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ecffa-280">To implement image operations beyond what is provided in [Direct2D](./direct2d-portal.md), you must implement custom transforms.</span></span> <span data-ttu-id="ecffa-281">Las transformaciones personalizadas pueden cambiar arbitrariamente una imagen de entrada mediante el uso de sombreadores HLSL personalizados.</span><span class="sxs-lookup"><span data-stu-id="ecffa-281">Custom transforms can arbitrarily change an input image through the use of custom HLSL shaders.</span></span>

<span data-ttu-id="ecffa-282">Las transformaciones implementan una de dos interfaces diferentes en función de los tipos de sombreadores que usan.</span><span class="sxs-lookup"><span data-stu-id="ecffa-282">Transforms implement one of two different interfaces depending on the types of shaders they use.</span></span> <span data-ttu-id="ecffa-283">Las transformaciones que utilizan sombreadores de píxeles o de vértices deben implementar [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), mientras que las transformaciones mediante sombreadores de cálculo deben implementar [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span><span class="sxs-lookup"><span data-stu-id="ecffa-283">Transforms using pixel and/or vertex shaders must implement [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform), while transforms using compute shaders must implement [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform).</span></span> <span data-ttu-id="ecffa-284">Estas interfaces heredan de [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="ecffa-284">These interfaces both inherit from [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span> <span data-ttu-id="ecffa-285">Esta sección se centra en la implementación de la funcionalidad que es común a ambos.</span><span class="sxs-lookup"><span data-stu-id="ecffa-285">This section focuses on implementing the functionality that is common to both.</span></span>

<span data-ttu-id="ecffa-286">La interfaz [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) tiene cuatro métodos para implementar:</span><span class="sxs-lookup"><span data-stu-id="ecffa-286">The [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface has four methods to implement:</span></span>

### <a name="getinputcount"></a><span data-ttu-id="ecffa-287">GetInputCount</span><span class="sxs-lookup"><span data-stu-id="ecffa-287">GetInputCount</span></span>

<span data-ttu-id="ecffa-288">Este método devuelve un entero que representa el recuento de entradas de la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-288">This method returns an integer representing the input count for the transform.</span></span>


```C++
IFACEMETHODIMP_(UINT32) GetInputCount() const
{
    return 1;
}
```



### <a name="mapinputrectstooutputrect"></a><span data-ttu-id="ecffa-289">MapInputRectsToOutputRect</span><span class="sxs-lookup"><span data-stu-id="ecffa-289">MapInputRectsToOutputRect</span></span>

<span data-ttu-id="ecffa-290">[Direct2D](./direct2d-portal.md) llama al método [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) cada vez que se representa la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-290">[Direct2D](./direct2d-portal.md) calls the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) method each time the transform is rendered.</span></span> <span data-ttu-id="ecffa-291">Direct2D pasa un rectángulo que representa los límites de cada una de las entradas a la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-291">Direct2D passes a rectangle representing the bounds of each of the inputs to the transform.</span></span> <span data-ttu-id="ecffa-292">La transformación es responsable de calcular los límites de la imagen de salida.</span><span class="sxs-lookup"><span data-stu-id="ecffa-292">The transform is then responsible for calculating the bounds of the output image.</span></span> <span data-ttu-id="ecffa-293">El tamaño de los rectángulos de todos los métodos de esta interfaz ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) se define en píxeles, no en los DIP.</span><span class="sxs-lookup"><span data-stu-id="ecffa-293">The size of the rectangles for all the methods on this interface ([**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform)) are defined in pixels, not DIPs.</span></span>

<span data-ttu-id="ecffa-294">Este método también es responsable de calcular la región de la salida que es opaca en función de la lógica de su sombreador y las regiones opacas de cada entrada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-294">This method is also responsible for calculating the region of the output that is opaque based on the logic of its shader and the opaque regions of each input.</span></span> <span data-ttu-id="ecffa-295">Una región opaca de una imagen se define como donde el canal alfa es ' 1 ' para la totalidad del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-295">An opaque region of an image is defined as that where the alpha channel is '1' for the entirety of the rectangle.</span></span> <span data-ttu-id="ecffa-296">Si no está claro si la salida de una transformación es opaca, el rectángulo opaco de salida debe establecerse en (0, 0, 0,0) como un valor seguro.</span><span class="sxs-lookup"><span data-stu-id="ecffa-296">If it is unclear whether a transform's output is opaque, the output opaque rectangle should be set to (0, 0, 0, 0) as a safe value.</span></span> <span data-ttu-id="ecffa-297">[Direct2D](./direct2d-portal.md) usa esta información para realizar optimizaciones de representación con contenido opaco garantizado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-297">[Direct2D](./direct2d-portal.md) uses this info to perform rendering optimizations with 'guaranteed opaque' content.</span></span> <span data-ttu-id="ecffa-298">Si este valor no es preciso, se puede producir una representación incorrecta.</span><span class="sxs-lookup"><span data-stu-id="ecffa-298">If this value is inaccurate, it can result in incorrect rendering.</span></span>

<span data-ttu-id="ecffa-299">Puede modificar el comportamiento de representación de la transformación (tal y como se define en las secciones 6 a 8) durante este método.</span><span class="sxs-lookup"><span data-stu-id="ecffa-299">The you can modify the transform's rendering behavior (as defined in sections 6 through 8) during this method.</span></span> <span data-ttu-id="ecffa-300">Sin embargo, no puede modificar otras transformaciones en el gráfico de transformación o aquí el diseño del gráfico.</span><span class="sxs-lookup"><span data-stu-id="ecffa-300">However, the you can't modify other transforms in the transform graph, or the graph layout itself here.</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInputRectsToOutputRect(
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
    _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
    UINT32 inputRectCount,
    _Out_ D2D1_RECT_L* pOutputRect,
    _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
    )
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The output of the transform will be the same size as the input.
    *pOutputRect = pInputRects[0];
    // Indicate that the image's opacity has not changed.
    *pOutputOpaqueSubRect = pInputOpaqueSubRects[0];
    // The size of the input image can be saved here for subsequent operations.
    m_inputRect = pInputRects[0];

    return S_OK;
}
```



<span data-ttu-id="ecffa-301">Para obtener un ejemplo más complejo, considere cómo se representaría una operación de desenfoque simple:</span><span class="sxs-lookup"><span data-stu-id="ecffa-301">For a more complex example, consider how a simple blur operation would be represented:</span></span>

<span data-ttu-id="ecffa-302">Si una operación de desenfoque utiliza un radio de 5 píxeles, el tamaño del rectángulo de salida debe expandirse en 5 píxeles, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-302">If a blur operation uses a 5 pixel radius, the size of the output rectangle must expand by 5 pixels, as shown below.</span></span> <span data-ttu-id="ecffa-303">Al modificar las coordenadas del rectángulo, una transformación debe asegurarse de que su lógica no cause ningún desbordamiento en las coordenadas del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-303">When modifying rectangle coordinates, a transform must ensure that its logic does not cause any over/underflows in the rectangle coordinates.</span></span>


```C++
// Expand output image by 5 pixels.

// Do not expand empty input rectangles.
if (pInputRects[0].right  > pInputRects[0].left &&
    pInputRects[0].bottom > pInputRects[0].top
    )
{
    pOutputRect->left   = ((pInputRects[0].left   - 5) < pInputRects[0].left  ) ? (pInputRects[0].left   - 5) : LONG_MIN;
    pOutputRect->top    = ((pInputRects[0].top    - 5) < pInputRects[0].top   ) ? (pInputRects[0].top    - 5) : LONG_MIN;
    pOutputRect->right  = ((pInputRects[0].right  + 5) > pInputRects[0].right ) ? (pInputRects[0].right  + 5) : LONG_MAX;
    pOutputRect->bottom = ((pInputRects[0].bottom + 5) > pInputRects[0].bottom) ? (pInputRects[0].bottom + 5) : LONG_MAX;
}
```



<span data-ttu-id="ecffa-304">Dado que la imagen está borrosa, una región de la imagen que era opaca ahora puede ser parcialmente transparente.</span><span class="sxs-lookup"><span data-stu-id="ecffa-304">Because the image is blurred, a region of the image which was opaque may now be partially transparent.</span></span> <span data-ttu-id="ecffa-305">Esto se debe a que el área fuera de la imagen tiene como valor predeterminado negro transparente y esta transparencia se combinará en la imagen alrededor de los bordes.</span><span class="sxs-lookup"><span data-stu-id="ecffa-305">This is because the area outside the image defaults to transparent black and this transparency will be blended into the image around the edges.</span></span> <span data-ttu-id="ecffa-306">La transformación debe reflejar esto en sus cálculos de rectángulo opaco de salida:</span><span class="sxs-lookup"><span data-stu-id="ecffa-306">The transform must reflect this in its output opaque rectangle calculations:</span></span>


```C++
// Shrink opaque region by 5 pixels.
pOutputOpaqueSubRect->left   = pInputOpaqueSubRects[0].left   + 5;
pOutputOpaqueSubRect->top    = pInputOpaqueSubRects[0].top    + 5;
pOutputOpaqueSubRect->right  = pInputOpaqueSubRects[0].right  - 5;
pOutputOpaqueSubRect->bottom = pInputOpaqueSubRects[0].bottom - 5;
```



<span data-ttu-id="ecffa-307">Estos cálculos se visualizan aquí:</span><span class="sxs-lookup"><span data-stu-id="ecffa-307">These calculations are visualized here:</span></span>

![Ilustración de cálculo de rectángulo.](images/custom-effects2.png)

<span data-ttu-id="ecffa-309">Para obtener más información sobre este método, consulte la página de referencia de [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-309">For more info about this method, see the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) reference page.</span></span>

### <a name="mapoutputrecttoinputrects"></a><span data-ttu-id="ecffa-310">MapOutputRectToInputRects</span><span class="sxs-lookup"><span data-stu-id="ecffa-310">MapOutputRectToInputRects</span></span>

<span data-ttu-id="ecffa-311">[Direct2D](./direct2d-portal.md) llama al método [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) después de [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="ecffa-311">[Direct2D](./direct2d-portal.md) calls the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) method after [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="ecffa-312">La transformación debe calcular qué parte de la imagen debe leerse para representar correctamente la región de salida solicitada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-312">The transform must calculate what portion of the image it needs to read from in order to correctly render the requested output region.</span></span>

<span data-ttu-id="ecffa-313">Como antes, si un efecto asigna estrictamente los píxeles 1-1, puede pasar el rectángulo de salida a través del rectángulo de entrada:</span><span class="sxs-lookup"><span data-stu-id="ecffa-313">As before, if an effect strictly maps pixels 1-1, it can pass the output rectangle through to the input rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapOutputRectToInputRects(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
    UINT32 inputRectCount
    ) const
{
    // This transform is designed to only accept one input.
    if (inputRectCount != 1)
    {
        return E_INVALIDARG;
    }

    // The input needed for the transform is the same as the visible output.
    pInputRects[0] = *pOutputRect;
    return S_OK;
}
```



<span data-ttu-id="ecffa-314">Del mismo modo, si una transformación reduce o expande una imagen (como el ejemplo de desenfoque aquí), los píxeles suelen utilizar píxeles circundantes para calcular su valor.</span><span class="sxs-lookup"><span data-stu-id="ecffa-314">Likewise, if a transform shrinks or expands an image (like the blur example here), pixels often use surrounding pixels to calculate their value.</span></span> <span data-ttu-id="ecffa-315">Con un desenfoque, se calcula el promedio de un píxel con sus píxeles circundantes, incluso si están fuera de los límites de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-315">With a blur, a pixel is averaged with its surrounding pixels, even if they are outside of the bounds of the input image.</span></span> <span data-ttu-id="ecffa-316">Este comportamiento se refleja en el cálculo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-316">This behavior is reflected in the calculation.</span></span> <span data-ttu-id="ecffa-317">Como antes, la transformación comprueba los desbordamientos al expandir las coordenadas de un rectángulo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-317">As before, the transform checks for overflows when expanding a rectangle's coordinates.</span></span>


```C++
// Expand the input rectangle to reflect that more pixels need to 
// be read from than are necessarily rendered in the effect's output.
pInputRects[0].left   = ((pOutputRect->left   - 5) < pOutputRect->left  ) ? (pOutputRect->left   - 5) : LONG_MIN;
pInputRects[0].top    = ((pOutputRect->top    - 5) < pOutputRect->top   ) ? (pOutputRect->top    - 5) : LONG_MIN;
pInputRects[0].right  = ((pOutputRect->right  + 5) > pOutputRect->right ) ? (pOutputRect->right  + 5) : LONG_MAX;
pInputRects[0].bottom = ((pOutputRect->bottom + 5) > pOutputRect->bottom) ? (pOutputRect->bottom + 5) : LONG_MAX;
```



<span data-ttu-id="ecffa-318">En esta ilustración se visualiza el cálculo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-318">This figure visualizes the calculation.</span></span> <span data-ttu-id="ecffa-319">[Direct2D](./direct2d-portal.md) muestrea automáticamente los píxeles negros transparentes en los que no existe la imagen de entrada, lo que permite mezclar gradualmente el desenfoque con el contenido existente en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ecffa-319">[Direct2D](./direct2d-portal.md) automatically samples transparent black pixels where the input image doesn't exist, allowing the blur to be blended gradually with the existing content on the screen.</span></span>

![Ilustración de un efecto muestreo de píxeles negros transparentes fuera de un rectángulo.](images/custom-effects3.png)

<span data-ttu-id="ecffa-321">Si la asignación no es trivial, este método debe establecer el rectángulo de entrada en el área máxima para garantizar resultados correctos.</span><span class="sxs-lookup"><span data-stu-id="ecffa-321">If the mapping is non-trivial, then this method should set the input rectangle to the maximum area to guarantee correct results.</span></span> <span data-ttu-id="ecffa-322">Para ello, establezca los bordes izquierdo y superior en INT \_ min y los bordes inferior y derecho en int \_ máx.</span><span class="sxs-lookup"><span data-stu-id="ecffa-322">To do this, set the left and top edges to INT\_MIN, and the right and bottom edges to INT\_MAX.</span></span>

<span data-ttu-id="ecffa-323">Para obtener más información sobre este método, vea el tema [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-323">For more info about this method, see the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) topic.</span></span>

### <a name="mapinvalidrect"></a><span data-ttu-id="ecffa-324">MapInvalidRect</span><span class="sxs-lookup"><span data-stu-id="ecffa-324">MapInvalidRect</span></span>

<span data-ttu-id="ecffa-325">[Direct2D](./direct2d-portal.md) también llama al método [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-325">[Direct2D](./direct2d-portal.md) also calls the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) method.</span></span> <span data-ttu-id="ecffa-326">Sin embargo, a diferencia de los métodos [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) y [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) Direct2D no se garantiza que lo llame en un momento determinado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-326">However, unlike the [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect) and [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) methods Direct2D is not guaranteed to call it at any particular time.</span></span> <span data-ttu-id="ecffa-327">Este método decide conceptualmente qué parte de la salida de una transformación se debe volver a representar en respuesta a una parte o a todo su cambio de entrada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-327">This method conceptually decides what part of a transform's output needs to be re-rendered in response to part or all of its input changing.</span></span> <span data-ttu-id="ecffa-328">Hay tres escenarios diferentes para los que se calcula el rectángulo no válido de una transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-328">There are three different scenarios for which to calculate a transform's invalid rect.</span></span>

### <a name="transforms-with-one-to-one-pixel-mapping"></a><span data-ttu-id="ecffa-329">Transformaciones con asignación de píxeles de uno a uno</span><span class="sxs-lookup"><span data-stu-id="ecffa-329">Transforms with one-to-one pixel mapping</span></span>

<span data-ttu-id="ecffa-330">En el caso de las transformaciones que asignan píxeles 1-1, simplemente pase el rectángulo de entrada no válido a través del rectángulo de salida no válido:</span><span class="sxs-lookup"><span data-stu-id="ecffa-330">For transforms that map pixels 1-1, simply pass the invalid input rectangle through to the invalid output rectangle:</span></span>


```C++
IFACEMETHODIMP SampleTransform::MapInvalidRect(
    UINT32 inputIndex,
    D2D1_RECT_L invalidInputRect,
    _Out_ D2D1_RECT_L* pInvalidOutputRect
    ) const
{
    // This transform is designed to only accept one input.
    if (inputIndex != 0)
    {
        return E_INVALIDARG;
    }

    // If part of the transform's input is invalid, mark the corresponding
    // output region as invalid. 
    *pInvalidOutputRect = invalidInputRect;

    return S_OK;
}
```



### <a name="transforms-with-many-to-many-pixel-mapping"></a><span data-ttu-id="ecffa-331">Transformaciones con asignación de píxeles de varios a varios</span><span class="sxs-lookup"><span data-stu-id="ecffa-331">Transforms with many-to-many pixel mapping</span></span>

<span data-ttu-id="ecffa-332">Cuando los píxeles de salida de una transformación dependen de su área circundante, el rectángulo de entrada no válido debe expandirse de forma correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ecffa-332">When a transform's output pixels are dependent on their surrounding area, the invalid input rectangle must correspondingly be expanded.</span></span> <span data-ttu-id="ecffa-333">Esto es para reflejar que los píxeles que rodean el rectángulo de entrada no válido también se verán afectados y dejarán de ser válidos.</span><span class="sxs-lookup"><span data-stu-id="ecffa-333">This is to reflect that pixels surrounding the invalid input rectangle will also be affected and become invalid.</span></span> <span data-ttu-id="ecffa-334">Por ejemplo, un desenfoque de cinco píxeles usa el siguiente cálculo:</span><span class="sxs-lookup"><span data-stu-id="ecffa-334">For example, a five pixel blur uses the following calculation:</span></span>


```C++
// Expand the input invalid rectangle by five pixels in each direction. This
// reflects that a change in part of the given input image will cause a change
// in an expanded part of the output image (five pixels in each direction).
pInvalidOutputRect->left   = ((invalidInputRect.left   - 5) < invalidInputRect.left  ) ? (invalidInputRect.left   - 5) : LONG_MIN;
pInvalidOutputRect->top    = ((invalidInputRect.top    - 5) < invalidInputRect.top   ) ? (invalidInputRect.top    - 5) : LONG_MIN;
pInvalidOutputRect->right  = ((invalidInputRect.right  + 5) > invalidInputRect.right ) ? (invalidInputRect.right  + 5) : LONG_MAX;
pInvalidOutputRect->bottom = ((invalidInputRect.bottom + 5) > invalidInputRect.bottom) ? (invalidInputRect.bottom + 5) : LONG_MAX;
```



### <a name="transforms-with-complex-pixel-mapping"></a><span data-ttu-id="ecffa-335">Transformaciones con asignación de píxeles complejos</span><span class="sxs-lookup"><span data-stu-id="ecffa-335">Transforms with complex pixel mapping</span></span>

<span data-ttu-id="ecffa-336">En el caso de las transformaciones en las que los píxeles de entrada y salida no tienen una asignación simple, todo el resultado se puede marcar como no válido.</span><span class="sxs-lookup"><span data-stu-id="ecffa-336">For transforms where input and output pixels do not have a simple mapping, the entire output can be marked as invalid.</span></span> <span data-ttu-id="ecffa-337">Por ejemplo, si una transformación simplemente genera el color medio de la entrada, la salida completa de la transformación cambia si se cambia incluso una pequeña parte de la entrada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-337">For example, if a transform simply outputs the average color of the input, the entire output of the transform changes if even a small part of the input is changed.</span></span> <span data-ttu-id="ecffa-338">En este caso, el rectángulo de salida no válido debe establecerse en un rectángulo lógicamente infinito (se muestra a continuación).</span><span class="sxs-lookup"><span data-stu-id="ecffa-338">In this case, the invalid output rectangle should be set to a logically infinite rectangle (shown below).</span></span> <span data-ttu-id="ecffa-339">[Direct2D](./direct2d-portal.md) lo fija automáticamente en los límites de la salida.</span><span class="sxs-lookup"><span data-stu-id="ecffa-339">[Direct2D](./direct2d-portal.md) automatically clamps this to the bounds of the output.</span></span>


```C++
// If any change in the input image affects the entire output, the
// transform should set pInvalidOutputRect to a logically infinite rect.
*pInvalidOutputRect = D2D1::RectL(LONG_MIN, LONG_MIN, LONG_MAX, LONG_MAX);
```



<span data-ttu-id="ecffa-340">Para obtener más información sobre este método, vea el tema [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-340">For more info about this method, see the [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) topic.</span></span>

<span data-ttu-id="ecffa-341">Una vez implementados estos métodos, el encabezado de la transformación contendrá lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ecffa-341">Once these methods have been implemented, your transform's header will contain the following:</span></span>


```C++
class SampleTransform : public ID2D1Transform 
{
public:
    SampleTransform();

    // ID2D1TransformNode Methods:
    IFACEMETHODIMP_(UINT32) GetInputCount() const;
    
    // ID2D1Transform Methods:
    IFACEMETHODIMP MapInputRectsToOutputRect(
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputRects,
        _In_reads_(inputRectCount) const D2D1_RECT_L* pInputOpaqueSubRects,
        UINT32 inputRectCount,
        _Out_ D2D1_RECT_L* pOutputRect,
        _Out_ D2D1_RECT_L* pOutputOpaqueSubRect
        );    

    IFACEMETHODIMP MapOutputRectToInputRects(
        _In_ const D2D1_RECT_L* pOutputRect,
        _Out_writes_(inputRectCount) D2D1_RECT_L* pInputRects,
        UINT32 inputRectCount
        ) const;

    IFACEMETHODIMP MapInvalidRect(
        UINT32 inputIndex,
        D2D1_RECT_L invalidInputRect,
        _Out_ D2D1_RECT_L* pInvalidOutputRect 
        ) const;

    // IUnknown Methods:
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
    IFACEMETHODIMP QueryInterface(REFIID riid, _Outptr_ void** ppOutput);

private:
    LONG m_cRef; // Internal ref count used by AddRef() and Release() methods.
    D2D1_RECT_L m_inputRect; // Stores the size of the input image.
};
```



## <a name="adding-a-pixel-shader-to-a-custom-transform"></a><span data-ttu-id="ecffa-342">Agregar un sombreador de píxeles a una transformación personalizada</span><span class="sxs-lookup"><span data-stu-id="ecffa-342">Adding a pixel shader to a custom transform</span></span>

<span data-ttu-id="ecffa-343">Una vez creada una transformación, debe proporcionar un sombreador que manipule los píxeles de la imagen.</span><span class="sxs-lookup"><span data-stu-id="ecffa-343">Once a transform has been created, it needs to provide a shader that will manipulate the image pixels.</span></span> <span data-ttu-id="ecffa-344">En esta sección se describen los pasos para usar un sombreador de píxeles con una transformación personalizada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-344">This section covers the steps to using a pixel shader with a custom transform.</span></span>

### <a name="implementing-id2d1drawtransform"></a><span data-ttu-id="ecffa-345">Implementación de ID2D1DrawTransform</span><span class="sxs-lookup"><span data-stu-id="ecffa-345">Implementing ID2D1DrawTransform</span></span>

<span data-ttu-id="ecffa-346">Para usar un sombreador de píxeles, la transformación debe implementar la interfaz [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , que hereda de la interfaz [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) descrita en la sección 5.</span><span class="sxs-lookup"><span data-stu-id="ecffa-346">To use a pixel shader, the transform must implement the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, which inherits from the [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform) interface described in section 5.</span></span> <span data-ttu-id="ecffa-347">Esta interfaz contiene un nuevo método para implementar:</span><span class="sxs-lookup"><span data-stu-id="ecffa-347">This interface contains one new method to implement:</span></span>

### <a name="setdrawinfoid2d1drawinfo-pdrawinfo"></a><span data-ttu-id="ecffa-348">SetDrawInfo (ID2D1DrawInfo \* pDrawInfo)</span><span class="sxs-lookup"><span data-stu-id="ecffa-348">SetDrawInfo(ID2D1DrawInfo \*pDrawInfo)</span></span>

<span data-ttu-id="ecffa-349">[Direct2D](./direct2d-portal.md) llama al método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) cuando la transformación se agrega por primera vez al gráfico de transformación de un efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-349">[Direct2D](./direct2d-portal.md) calls the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="ecffa-350">Este método proporciona un parámetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) que controla cómo se representa la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-350">This method provides an [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="ecffa-351">Vea el tema **ID2D1DrawInfo** para obtener los métodos disponibles aquí.</span><span class="sxs-lookup"><span data-stu-id="ecffa-351">See the **ID2D1DrawInfo** topic for the methods available here.</span></span>

<span data-ttu-id="ecffa-352">Si la transformación decide almacenar este parámetro como una variable de miembro de clase, se puede tener acceso al objeto *drawInfo* y cambiarlo desde otros métodos, como establecedores de propiedad o [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="ecffa-352">If the transform chooses to store this parameter as a class member variable, the *drawInfo* object can be accessed and changed from other methods such as property setters or [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span> <span data-ttu-id="ecffa-353">En particular, no se puede llamar a desde los métodos [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) o [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) en [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span><span class="sxs-lookup"><span data-stu-id="ecffa-353">Notably, it cannot be called from the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) or [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods on [**ID2D1Transform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1transform).</span></span>

### <a name="creating-a-guid-for-the-pixel-shader"></a><span data-ttu-id="ecffa-354">Crear un GUID para el sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ecffa-354">Creating a GUID for the pixel shader</span></span>

<span data-ttu-id="ecffa-355">A continuación, la transformación debe definir un GUID único para el propio sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ecffa-355">Next, the transform must define a unique GUID for the pixel shader itself.</span></span> <span data-ttu-id="ecffa-356">Se usa cuando [Direct2D](./direct2d-portal.md) carga el sombreador en la memoria, así como cuando la transformación elige qué sombreador de píxeles se va a usar para la ejecución.</span><span class="sxs-lookup"><span data-stu-id="ecffa-356">This is used when [Direct2D](./direct2d-portal.md) loads the shader into memory, as well as when the transform chooses which pixel shader to use for execution.</span></span> <span data-ttu-id="ecffa-357">Se pueden usar herramientas como guidgen.exe, que se incluye con Visual Studio, para generar un GUID aleatorio.</span><span class="sxs-lookup"><span data-stu-id="ecffa-357">Tools such as guidgen.exe, which is included with Visual Studio, can be used to generate a random GUID.</span></span>


```C++
// Example GUID used to uniquely identify HLSL shader. Passed to Direct2D during
// shader load, and used by the transform to identify the shader for the
// ID2D1DrawInfo::SetPixelShader method. The effect author should create a
// unique name for the shader as well as a unique GUID using
// a GUID generation tool.
DEFINE_GUID(GUID_SamplePixelShader, 0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



### <a name="loading-the-pixel-shader-with-direct2d"></a><span data-ttu-id="ecffa-358">Cargar el sombreador de píxeles con Direct2D</span><span class="sxs-lookup"><span data-stu-id="ecffa-358">Loading the pixel shader with Direct2D</span></span>

<span data-ttu-id="ecffa-359">Un sombreador de píxeles debe cargarse en memoria antes de que lo pueda usar la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-359">A pixel shader must be loaded into memory before it can be used by the transform.</span></span>

<span data-ttu-id="ecffa-360">Para cargar el sombreador de píxeles en la memoria, la transformación debe leer el código de byte del sombreador compilado de. Archivo CSO generado por Visual Studio (consulte la documentación de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obtener más detalles) en una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="ecffa-360">To load the pixel shader into memory, the transform should read the compiled shader byte code from the .CSO file generated by Visual Studio (see [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details) into a byte array.</span></span> <span data-ttu-id="ecffa-361">Esta técnica se muestra en detalle en el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="ecffa-361">This technique is demonstrated in detail in the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="ecffa-362">Una vez que los datos del sombreador se han cargado en una matriz de bytes, llame al método [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) en el objeto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-362">Once the shader data has been loaded into a byte array, call the [**LoadPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader) method on the effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object.</span></span> <span data-ttu-id="ecffa-363">[Direct2D](./direct2d-portal.md) omite las llamadas a **LoadPixelShader** cuando ya se ha cargado un sombreador con el mismo GUID.</span><span class="sxs-lookup"><span data-stu-id="ecffa-363">[Direct2D](./direct2d-portal.md) ignores calls to **LoadPixelShader** when a shader with the same GUID has already been loaded.</span></span>

<span data-ttu-id="ecffa-364">Una vez que se ha cargado un sombreador de píxeles en la memoria, la transformación debe seleccionarlo para su ejecución pasando su GUID al método [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) en el parámetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) proporcionado durante el método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-364">After a pixel shader has been loaded into memory, the transform needs to select it for execution by passing its GUID to the [**SetPixelShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided during the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="ecffa-365">El sombreador de píxeles debe estar ya cargado en la memoria antes de que se seleccione para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="ecffa-365">The pixel shader must be already loaded into memory before being selected for execution.</span></span>

### <a name="changing-shader-operation-with-constant-buffers"></a><span data-ttu-id="ecffa-366">Cambiar el funcionamiento del sombreador con búferes de constantes</span><span class="sxs-lookup"><span data-stu-id="ecffa-366">Changing shader operation with constant buffers</span></span>

<span data-ttu-id="ecffa-367">Para cambiar el modo en que se ejecuta un sombreador, una transformación puede pasar un búfer de constantes al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ecffa-367">To change how a shader executes, a transform may pass a constant buffer to the pixel shader.</span></span> <span data-ttu-id="ecffa-368">Para ello, una transformación define un struct que contiene las variables deseadas en el encabezado de clase:</span><span class="sxs-lookup"><span data-stu-id="ecffa-368">To do so, a transform defines a struct that contains the desired variables in the class header:</span></span>


```C++
// This struct defines the constant buffer of the pixel shader.
struct
{
    float valueOne;
    float valueTwo;
} m_constantBuffer;
```



<span data-ttu-id="ecffa-369">A continuación, la transformación llama al método [**ID2D1DrawInfo:: SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) en el parámetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) proporcionado en el método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) para pasar este búfer al sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-369">The transform then calls the [**ID2D1DrawInfo::SetPixelShaderConstantBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setpixelshaderconstantbuffer) method on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter provided in the [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method to pass this buffer to the shader.</span></span>

<span data-ttu-id="ecffa-370">[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) también debe definir un struct correspondiente que represente el búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="ecffa-370">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) also needs to define a corresponding struct that represents the constant buffer.</span></span> <span data-ttu-id="ecffa-371">Las variables contenidas en el struct del sombreador deben coincidir con las de la estructura de la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-371">The variables contained in the shader's struct must match those in the transform's struct.</span></span>


```C++
cbuffer constants : register(b0)
{
    float valueOne : packoffset(c0.x);
    float valueTwo : packoffset(c0.y);
};
```



<span data-ttu-id="ecffa-372">Una vez definido el búfer, los valores contenidos en se pueden leer desde cualquier parte del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ecffa-372">Once the buffer has been defined, the values contained within can be read from anywhere within the pixel shader.</span></span>

### <a name="writing-a-pixel-shader-for-direct2d"></a><span data-ttu-id="ecffa-373">Escribir un sombreador de píxeles para Direct2D</span><span class="sxs-lookup"><span data-stu-id="ecffa-373">Writing a pixel shader for Direct2D</span></span>

<span data-ttu-id="ecffa-374">Las transformaciones de [Direct2D](./direct2d-portal.md) usan sombreadores creados mediante [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)estándar.</span><span class="sxs-lookup"><span data-stu-id="ecffa-374">[Direct2D](./direct2d-portal.md) transforms use shaders authored using standard [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="ecffa-375">Sin embargo, hay algunos conceptos clave para escribir un sombreador de píxeles que se ejecuta desde el contexto de una transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-375">However, there are a few key concepts to writing a pixel shader that executes from the context of a transform.</span></span> <span data-ttu-id="ecffa-376">Para obtener un ejemplo completo de un sombreador de píxeles totalmente funcional, vea el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="ecffa-376">For a completed example of a fully functionally pixel shader, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

<span data-ttu-id="ecffa-377">[Direct2D](./direct2d-portal.md) asigna automáticamente las entradas de una transformación a los objetos [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) y [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) en HLSL.</span><span class="sxs-lookup"><span data-stu-id="ecffa-377">[Direct2D](./direct2d-portal.md) automatically maps a transform's inputs to [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) and [**SamplerState**](/windows/desktop/api/d3d11/nn-d3d11-id3d11samplerstate) objects in the HLSL.</span></span> <span data-ttu-id="ecffa-378">El primer **Texture2D** se encuentra en el registro T0 y el primer **SamplerState** se encuentra en el registro S0.</span><span class="sxs-lookup"><span data-stu-id="ecffa-378">The first **Texture2D** is located at register t0, and the first **SamplerState** is located at register s0.</span></span> <span data-ttu-id="ecffa-379">Cada entrada adicional se encuentra en los siguientes registros correspondientes (T1 y S1, por ejemplo).</span><span class="sxs-lookup"><span data-stu-id="ecffa-379">Each additional input is located at the next corresponding registers (t1 and s1 for example).</span></span> <span data-ttu-id="ecffa-380">Los datos de píxeles de una entrada determinada se pueden muestrear llamando a sample en el objeto **Texture2D** y pasando el objeto **SamplerState** correspondiente y las coordenadas textura.</span><span class="sxs-lookup"><span data-stu-id="ecffa-380">Pixel data for a particular input can be sampled by calling Sample on the **Texture2D** object and passing in the corresponding **SamplerState** object and the texel coordinates.</span></span>

<span data-ttu-id="ecffa-381">Un sombreador de píxeles personalizado se ejecuta una vez para cada píxel que se representa.</span><span class="sxs-lookup"><span data-stu-id="ecffa-381">A custom pixel shader is run once for each pixel that is rendered.</span></span> <span data-ttu-id="ecffa-382">Cada vez que se ejecuta el sombreador, [Direct2D](./direct2d-portal.md) proporciona automáticamente tres parámetros que identifican su posición de ejecución actual:</span><span class="sxs-lookup"><span data-stu-id="ecffa-382">Each time the shader is run, [Direct2D](./direct2d-portal.md) automatically provides three parameters that identify its current execution position:</span></span>

-   <span data-ttu-id="ecffa-383">Salida de espacio de escena: este parámetro representa la posición de ejecución actual en términos de la superficie de destino general.</span><span class="sxs-lookup"><span data-stu-id="ecffa-383">Scene-space output: This parameter represents the current execution position in terms of the overall target surface.</span></span> <span data-ttu-id="ecffa-384">Se define en píxeles y sus valores Min/Max se corresponden con los límites del rectángulo devuelto por [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span><span class="sxs-lookup"><span data-stu-id="ecffa-384">It is defined in pixels and its min/max values correspond to the bounds of the rectangle returned by [**MapInputRectsToOutputRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinputrectstooutputrect).</span></span>
-   <span data-ttu-id="ecffa-385">Salida de espacio de recorte: este parámetro lo usa Direct3D y no debe usarse en el sombreador de píxeles de una transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-385">Clip-space output: This parameter is used by Direct3D, and is must not be used in a transform's pixel shader.</span></span>
-   <span data-ttu-id="ecffa-386">Entrada de espacio textura: este parámetro representa la posición de ejecución actual en una textura de entrada determinada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-386">Texel-space input: This parameter represents the current execution position in a particular input texture.</span></span> <span data-ttu-id="ecffa-387">Un sombreador no debe tomar ninguna dependencia sobre cómo se calcula este valor.</span><span class="sxs-lookup"><span data-stu-id="ecffa-387">A shader should not take any dependencies on how this value is calculated.</span></span> <span data-ttu-id="ecffa-388">Solo debe usarlo para muestrear la entrada del sombreador de píxeles, tal como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="ecffa-388">It should only use it to sample the pixel shader's input, as shown in the code below:</span></span>


```C++
Texture2D InputTexture : register(t0);
SamplerState InputSampler : register(s0);

float4 main(
    float4 clipSpaceOutput  : SV_POSITION,
    float4 sceneSpaceOutput : SCENE_POSITION,
    float4 texelSpaceInput0 : TEXCOORD0
    ) : SV_Target
{
    // Samples pixel from ten pixels above current position.

    float2 sampleLocation =
        texelSpaceInput0.xy    // Sample position for the current output pixel.
        + float2(0,-10)        // An offset from which to sample the input, specified in pixels.
        * texelSpaceInput0.zw; // Multiplier that converts pixel offset to sample position offset.

    float4 color = InputTexture.Sample(
        InputSampler,          // Sampler and Texture must match for a given input.
        sampleLocation
        );

    return color;
}
```



## <a name="adding-a-vertex-shader-to-a-custom-transform"></a><span data-ttu-id="ecffa-389">Agregar un sombreador de vértices a una transformación personalizada</span><span class="sxs-lookup"><span data-stu-id="ecffa-389">Adding a vertex shader to a custom transform</span></span>

<span data-ttu-id="ecffa-390">Puede usar sombreadores de vértices para realizar diferentes escenarios de creación de imágenes que los sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ecffa-390">You can use vertex shaders to accomplish different imaging scenarios than pixel shaders.</span></span> <span data-ttu-id="ecffa-391">En concreto, los sombreadores de vértices pueden realizar efectos de imagen basados en geometría transformando los vértices que componen una imagen.</span><span class="sxs-lookup"><span data-stu-id="ecffa-391">In particular, vertex shaders can perform geometry-based image effects by transforming vertices that comprise an image.</span></span> <span data-ttu-id="ecffa-392">Los sombreadores de vértices se pueden usar de forma independiente o junto con los sombreadores de píxeles especificados por la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-392">Vertex shaders can be used independently of or in conjunction with transform-specified pixel shaders.</span></span> <span data-ttu-id="ecffa-393">Si no se especifica un sombreador de vértices, [Direct2D](./direct2d-portal.md) sustituye en un sombreador de vértices predeterminado para usarlo con el sombreador de píxeles personalizado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-393">If a vertex shader is not specified, [Direct2D](./direct2d-portal.md) substitutes in a default vertex shader for use with the custom pixel shader.</span></span>

<span data-ttu-id="ecffa-394">El proceso para agregar un sombreador de vértices a una transformación personalizada es similar al de un sombreador de píxeles: la transformación implementa la interfaz [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) , crea un GUID y (opcionalmente) pasa búferes de constantes al sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-394">The process for adding a vertex shader to a custom transform is similar to that of a pixel shader – the transform implements the [**ID2D1DrawTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform) interface, creates a GUID, and (optionally) passes constant buffers to the shader.</span></span> <span data-ttu-id="ecffa-395">Sin embargo, hay algunos pasos adicionales clave que son exclusivos de los sombreadores de vértices:</span><span class="sxs-lookup"><span data-stu-id="ecffa-395">However, there are a few key additional steps that are unique to vertex shaders:</span></span>

### <a name="creating-a-vertex-buffer"></a><span data-ttu-id="ecffa-396">Crear un búfer de vértices</span><span class="sxs-lookup"><span data-stu-id="ecffa-396">Creating a vertex buffer</span></span>

<span data-ttu-id="ecffa-397">Un sombreador de vértices por definición se ejecuta en los vértices que se le pasan, no en píxeles individuales.</span><span class="sxs-lookup"><span data-stu-id="ecffa-397">A vertex shader by definition executes on vertices passed to it, not individual pixels.</span></span> <span data-ttu-id="ecffa-398">Para especificar los vértices para los que se va a ejecutar el sombreador, una transformación crea un búfer de vértice para pasar al sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-398">To specify the vertices for the shader to execute on, a transform creates a vertex buffer to pass to the shader.</span></span> <span data-ttu-id="ecffa-399">El diseño de los búferes de vértices está fuera del ámbito de este documento.</span><span class="sxs-lookup"><span data-stu-id="ecffa-399">The layout of vertex buffers is beyond the scope of this document.</span></span> <span data-ttu-id="ecffa-400">Vea la [referencia de Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obtener más información o el ejemplo de [SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obtener una implementación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-400">Please see the [Direct3D reference](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) for details, or the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="ecffa-401">Después de crear un búfer de vértices en la memoria, la transformación usa el método [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) en el objeto [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) del efecto contenedor para pasar esos datos a la GPU.</span><span class="sxs-lookup"><span data-stu-id="ecffa-401">After creating a vertex buffer in memory, the transform uses the [**CreateVertexBuffer**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer) method on the containing effect's [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) object to pass that data to the GPU.</span></span> <span data-ttu-id="ecffa-402">De nuevo, vea el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obtener una implementación de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-402">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a sample implementation.</span></span>

<span data-ttu-id="ecffa-403">Si no se especifica ningún búfer de vértices mediante la transformación, [Direct2D](./direct2d-portal.md) pasa un búfer de vértices predeterminado que representa la ubicación de la imagen rectangular.</span><span class="sxs-lookup"><span data-stu-id="ecffa-403">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) passes a default vertex buffer representing the rectangular image location.</span></span>

### <a name="changing-setdrawinfo-to-utilize-a-vertex-shader"></a><span data-ttu-id="ecffa-404">Cambiar SetDrawInfo para que use un sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ecffa-404">Changing SetDrawInfo to utilize a vertex shader</span></span>

<span data-ttu-id="ecffa-405">Al igual que con los sombreadores de píxeles, la transformación debe cargarse y seleccionar un sombreador de vértices para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="ecffa-405">Like with pixel shaders, the transform must load and select a vertex shader for execution.</span></span> <span data-ttu-id="ecffa-406">Para cargar el sombreador de vértices, llama al método [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) en el método [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) recibido en el método Initialize del efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-406">To load the vertex shader, it calls the [**LoadVertexShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader) method on the [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext) method received in the effect's Initialize method.</span></span> <span data-ttu-id="ecffa-407">Para seleccionar el sombreador de vértices para la ejecución, llama a [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) en el parámetro [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) recibido en el método [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) de la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-407">To select the vertex shader for execution, it calls [**SetVertexProcessing**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawinfo-setvertexprocessing) on the [**ID2D1DrawInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo) parameter received in the transform's [**SetDrawInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1drawtransform-setdrawinfo) method.</span></span> <span data-ttu-id="ecffa-408">Este método acepta un GUID para un sombreador de vértices cargado previamente y, opcionalmente, un búfer de vértice creado previamente para que se ejecute el sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-408">This method accepts a GUID for a previously-loaded vertex shader as well as (optionally) a previously-created vertex buffer for the shader to execute on.</span></span>

### <a name="implementing-a-direct2d-vertex-shader"></a><span data-ttu-id="ecffa-409">Implementar un sombreador de vértices de Direct2D</span><span class="sxs-lookup"><span data-stu-id="ecffa-409">Implementing a Direct2D vertex shader</span></span>

<span data-ttu-id="ecffa-410">Una transformación de dibujo puede contener un sombreador de píxeles y un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="ecffa-410">A draw transform can contain both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="ecffa-411">Si una transformación define un sombreador de píxeles y un sombreador de vértices, la salida del sombreador de vértices se proporciona directamente al sombreador de píxeles: la aplicación puede personalizar la firma devuelta del sombreador de vértices/los parámetros del sombreador de píxeles siempre que sean coherentes.</span><span class="sxs-lookup"><span data-stu-id="ecffa-411">If a transform defines both a pixel shader and a vertex shader, then the output from the vertex shader is given directly to the pixel shader: the app can customize the return signature of the vertex shader / the parameters of the pixel shader as long as they are consistent.</span></span>

<span data-ttu-id="ecffa-412">Por otro lado, si una transformación solo contiene un sombreador de vértices y se basa en el sombreador de píxeles de paso predeterminado de [Direct2D](./direct2d-portal.md), debe devolver la siguiente salida predeterminada:</span><span class="sxs-lookup"><span data-stu-id="ecffa-412">On the other hand, if a transform only contains a vertex shader, and relies on [Direct2D](./direct2d-portal.md)'s default pass-through pixel shader, it must return the following default output:</span></span>


```C++
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="ecffa-413">Un sombreador de vértices almacena el resultado de sus transformaciones de vértices en la variable de salida de espacio de la escena del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-413">A vertex shader stores the result of its vertex transformations in the shader's Scene-space output variable.</span></span> <span data-ttu-id="ecffa-414">Para calcular la salida del espacio de clips y las variables de entrada de espacio textura, [Direct2D](./direct2d-portal.md) proporciona automáticamente matrices de conversión en un búfer de constantes:</span><span class="sxs-lookup"><span data-stu-id="ecffa-414">To compute the Clip-space output and the Texel-space input variables, [Direct2D](./direct2d-portal.md) automatically provides conversion matrices in a constant buffer:</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};
```



<span data-ttu-id="ecffa-415">Se puede encontrar código de sombreador de vértices de ejemplo a continuación que usa las matrices de conversión para calcular el clip correcto y los espacios de textura esperados por [Direct2D](./direct2d-portal.md):</span><span class="sxs-lookup"><span data-stu-id="ecffa-415">Sample vertex shader code can be found below that uses the conversion matrices to calculate the correct clip and texel spaces expected by [Direct2D](./direct2d-portal.md):</span></span>


```C++
// Constant buffer b0 is used to store the transformation matrices from scene space
// to clip space. Depending on the number of inputs to the vertex shader, there
// may be more or fewer "sceneToInput" matrices.
cbuffer Direct2DTransforms : register(b0)
{
    float2x1 sceneToOutputX;
    float2x1 sceneToOutputY;
    float2x1 sceneToInput0X;
    float2x1 sceneToInput0Y;
};

// Default output structure. This can be customized if transform also contains pixel shader.
struct VSOut
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};

// The parameter(s) passed to the vertex shader are defined by the vertex buffer's layout
// as specified by the transform. If no vertex buffer is specified, Direct2D passes two
// triangles representing the rectangular image with the following layout:
//
//    float4 outputScenePosition : OUTPUT_SCENE_POSITION;
//
//    The x and y coordinates of the outputScenePosition variable represent the image's
//    position on the screen. The z and w coordinates are used for perspective and
//    depth-buffering.

VSOut GeometryVS(float4 outputScenePosition : OUTPUT_SCENE_POSITION) 
{
    VSOut output;

    // Compute Scene-space output (vertex simply passed-through here). 
    output.sceneSpaceOutput.x = outputScenePosition.x;
    output.sceneSpaceOutput.y = outputScenePosition.y;
    output.sceneSpaceOutput.z = outputScenePosition.z;
    output.sceneSpaceOutput.w = outputScenePosition.w;

    // Generate standard Clip-space output coordinates.
    output.clipSpaceOutput.x = (output.sceneSpaceOutput.x * sceneToOutputX[0]) +
        output.sceneSpaceOutput.w * sceneToOutputX[1];

    output.clipSpaceOutput.y = (output.sceneSpaceOutput.y * sceneToOutputY[0]) + 
        output.sceneSpaceOutput.w * sceneToOutputY[1];

    output.clipSpaceOutput.z = output.sceneSpaceOutput.z;
    output.clipSpaceOutput.w = output.sceneSpaceOutput.w;

    // Generate standard Texel-space input coordinates.
    output.texelSpaceInput0.x = (outputScenePosition.x * sceneToInput0X[0]) + sceneToInput0X[1];
    output.texelSpaceInput0.y = (outputScenePosition.y * sceneToInput0Y[0]) + sceneToInput0Y[1];
    output.texelSpaceInput0.z = sceneToInput0X[0];
    output.texelSpaceInput0.w = sceneToInput0Y[0];

    return output;  
}
```



<span data-ttu-id="ecffa-416">El código anterior se puede usar como punto de partida para un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="ecffa-416">The above code can be used as a starting point for a vertex shader.</span></span> <span data-ttu-id="ecffa-417">Simplemente pasa por la imagen de entrada sin realizar ninguna transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-417">It merely passes through the input image without performing any transforms.</span></span> <span data-ttu-id="ecffa-418">De nuevo, vea el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para una transformación basada en sombreador de vértices totalmente implementada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-418">Again, see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for a fully-implemented vertex shader-based transform.</span></span>

<span data-ttu-id="ecffa-419">Si la transformación no especifica ningún búfer de vértice, [Direct2D](./direct2d-portal.md) sustituye en un búfer de vértices predeterminado que representa la ubicación de la imagen rectangular.</span><span class="sxs-lookup"><span data-stu-id="ecffa-419">If no vertex buffer is specified by the transform, [Direct2D](./direct2d-portal.md) substitutes in a default vertex buffer representing the rectangular image location.</span></span> <span data-ttu-id="ecffa-420">Los parámetros para el sombreador de vértices se cambian a los de la salida del sombreador predeterminado:</span><span class="sxs-lookup"><span data-stu-id="ecffa-420">The parameters to the vertex shader are changed to those of the default shader output:</span></span>


```C++
struct VSIn
{
    float4 clipSpaceOutput  : SV_POSITION; 
    float4 sceneSpaceOutput : SCENE_POSITION;
    float4 texelSpaceInput0 : TEXCOORD0;  
};
```



<span data-ttu-id="ecffa-421">El sombreador de vértices no puede modificar sus parámetros *sceneSpaceOutput* y *clipSpaceOutput* .</span><span class="sxs-lookup"><span data-stu-id="ecffa-421">The vertex shader may not modify its *sceneSpaceOutput* and *clipSpaceOutput* parameters.</span></span> <span data-ttu-id="ecffa-422">Debe devolverlos sin cambios.</span><span class="sxs-lookup"><span data-stu-id="ecffa-422">It must return them unchanged.</span></span> <span data-ttu-id="ecffa-423">Sin embargo, puede modificar los parámetros *texelSpaceInput* de cada imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-423">It may however modify the *texelSpaceInput* parameter(s) for each input image.</span></span> <span data-ttu-id="ecffa-424">Si la transformación también contiene un sombreador de píxeles personalizado, el sombreador de vértices sigue pudiendo pasar parámetros personalizados adicionales directamente al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ecffa-424">If the transform also contains a custom pixel shader, the vertex shader is still able to pass additional custom parameters directly to the pixel shader.</span></span> <span data-ttu-id="ecffa-425">Además, ya no se proporciona el búfer personalizado de las matrices de conversión *sceneSpace* (b0).</span><span class="sxs-lookup"><span data-stu-id="ecffa-425">Additionally, the *sceneSpace* conversion matrices custom buffer (b0) is no longer provided.</span></span>

## <a name="adding-a-compute-shader-to-a-custom-transform"></a><span data-ttu-id="ecffa-426">Agregar un sombreador de cálculo a una transformación personalizada</span><span class="sxs-lookup"><span data-stu-id="ecffa-426">Adding a compute shader to a custom transform</span></span>

<span data-ttu-id="ecffa-427">Por último, las transformaciones personalizadas pueden emplear sombreadores de cálculo para determinados escenarios de destino.</span><span class="sxs-lookup"><span data-stu-id="ecffa-427">Finally, custom transforms may utilize compute shaders for certain targeted scenarios.</span></span> <span data-ttu-id="ecffa-428">Los sombreadores de cálculo se pueden usar para implementar efectos de imagen complejos que requieren acceso arbitrario a los búferes de imagen de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="ecffa-428">Compute shaders can be used to implement complex image effects that require arbitrary access to input and output image buffers.</span></span> <span data-ttu-id="ecffa-429">Por ejemplo, un algoritmo de histograma básico no se puede implementar con un sombreador de píxeles debido a las limitaciones en el acceso a la memoria.</span><span class="sxs-lookup"><span data-stu-id="ecffa-429">For example, a basic histogram algorithm cannot be implemented with a pixel shader due to limitations on memory access.</span></span>

<span data-ttu-id="ecffa-430">Dado que los sombreadores de cálculo tienen más requisitos de nivel de características de hardware que los sombreadores de píxeles, se deben usar sombreadores de píxeles cuando sea posible para implementar un efecto determinado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-430">Because compute shaders have higher hardware feature level requirements than pixel shaders, pixel shaders should be used when possible to implement a given effect.</span></span> <span data-ttu-id="ecffa-431">En concreto, los sombreadores de cálculo solo se ejecutan en la mayoría de las tarjetas de nivel de DirectX 10 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ecffa-431">Specifically, compute shaders only run on most DirectX 10 level cards and higher.</span></span> <span data-ttu-id="ecffa-432">Si una transformación decide usar un sombreador de cálculo, debe comprobar la compatibilidad de hardware adecuada durante la creación de instancias además de implementar la interfaz [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-432">If a transform chooses to use a compute shader, it must check for the appropriate hardware support during instantiation in addition to implementing the [**ID2D1ComputeTransform**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform) interface.</span></span>

### <a name="checking-for-compute-shader-support"></a><span data-ttu-id="ecffa-433">Comprobando la compatibilidad del sombreador de cálculo</span><span class="sxs-lookup"><span data-stu-id="ecffa-433">Checking for Compute Shader support</span></span>

<span data-ttu-id="ecffa-434">Si un efecto usa un sombreador de cálculo, debe comprobar la compatibilidad del sombreador de cálculo durante su creación mediante el método [**ID2D1EffectContext:: CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-434">If an effect uses a compute shader, it must check for compute shader support during its creation using the [**ID2D1EffectContext::CheckFeatureSupport**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-checkfeaturesupport) method.</span></span> <span data-ttu-id="ecffa-435">Si la GPU no admite los sombreadores de cálculo, el efecto debe devolver [**D2DERR \_ insuficientes \_ \_ funcionalidades del dispositivo**](direct2d-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ecffa-435">If the GPU does not support compute shaders, the effect must return [**D2DERR\_INSUFFICIENT\_DEVICE\_CAPABILITIES**](direct2d-error-codes.md).</span></span>

<span data-ttu-id="ecffa-436">Hay dos tipos diferentes de sombreadores de cálculo que una transformación puede usar: Shader Model 4 (DirectX 10) y Shader Model 5 (DirectX 11).</span><span class="sxs-lookup"><span data-stu-id="ecffa-436">There are two different types of compute shaders that a transform can use: Shader Model 4 (DirectX 10) and Shader Model 5 (DirectX 11).</span></span> <span data-ttu-id="ecffa-437">Hay ciertas limitaciones en los sombreadores modelo 4 de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-437">There are certain limitations to Shader Model 4 shaders.</span></span> <span data-ttu-id="ecffa-438">Consulte la documentación de [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="ecffa-438">See the [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) documentation for details.</span></span> <span data-ttu-id="ecffa-439">Las transformaciones pueden contener ambos tipos de sombreadores y pueden revertir al modelo de sombreador 4 cuando sea necesario: vea el [ejemplo de SDK de D2DCustomEffects](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) para obtener una implementación de este.</span><span class="sxs-lookup"><span data-stu-id="ecffa-439">Transforms can contain both types of shaders, and can fall back to Shader Model 4 when required: see the [D2DCustomEffects SDK sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects) for an implementation of this.</span></span>

### <a name="implement-id2d1computetransform"></a><span data-ttu-id="ecffa-440">Implementación de ID2D1ComputeTransform</span><span class="sxs-lookup"><span data-stu-id="ecffa-440">Implement ID2D1ComputeTransform</span></span>

<span data-ttu-id="ecffa-441">Esta interfaz contiene dos nuevos métodos que se deben implementar además de los de [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="ecffa-441">This interface contains two new methods to implement in addition to the ones in [**ID2D1Transform**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)):</span></span>

### <a name="setcomputeinfoid2d1computeinfo-pcomputeinfo"></a><span data-ttu-id="ecffa-442">SetComputeInfo (ID2D1ComputeInfo \* pComputeInfo)</span><span class="sxs-lookup"><span data-stu-id="ecffa-442">SetComputeInfo(ID2D1ComputeInfo \*pComputeInfo)</span></span>

<span data-ttu-id="ecffa-443">Al igual que con los sombreadores de píxeles y vértices, [Direct2D](./direct2d-portal.md) llama al método [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) cuando la transformación se agrega por primera vez al gráfico de transformación de un efecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-443">Like with pixel and vertex shaders, [Direct2D](./direct2d-portal.md) calls the [**SetComputeInfo**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-setcomputeinfo) method when the transform is first added to an effect's transform graph.</span></span> <span data-ttu-id="ecffa-444">Este método proporciona un parámetro [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) que controla cómo se representa la transformación.</span><span class="sxs-lookup"><span data-stu-id="ecffa-444">This method provides an [**ID2D1ComputeInfo**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computeinfo) parameter that controls how the transform is rendered.</span></span> <span data-ttu-id="ecffa-445">Esto incluye elegir el sombreador de cálculo que se va a ejecutar a través del método [**ID2D1ComputeInfo:: SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-445">This includes choosing the compute shader to execute through the [**ID2D1ComputeInfo::SetComputeShader**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computeinfo-setcomputeshaderconstantbuffer) method.</span></span> <span data-ttu-id="ecffa-446">Si la transformación decide almacenar este parámetro como una variable de miembro de clase, se puede tener acceso al mismo y cambiarlo desde cualquier método de transformación o efecto con la excepción de los métodos [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) y [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) .</span><span class="sxs-lookup"><span data-stu-id="ecffa-446">If the transform chooses to store this parameter as a class member variable, it can be accessed and changed from any transform or effect method with the exception of the [**MapOutputRectToInputRects**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapoutputrecttoinputrects) and [**MapInvalidRect**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1transform-mapinvalidrect) methods.</span></span> <span data-ttu-id="ecffa-447">Vea el tema **ID2D1ComputeInfo** para ver otros métodos disponibles aquí.</span><span class="sxs-lookup"><span data-stu-id="ecffa-447">See the **ID2D1ComputeInfo** topic for other methods available here.</span></span>

### <a name="calculatethreadgroupsid2d1computeinfo-poutputrect-uint32-pdimensionx-uint32-pdimensiony-uint32-pdimensionz"></a><span data-ttu-id="ecffa-448">CalculateThreadgroups (ID2D1ComputeInfo \* pOutputRect, UInt32 \* PDIMENSIONX, UInt32 \* pDimensionY, UInt32 \* pDimensionZ)</span><span class="sxs-lookup"><span data-stu-id="ecffa-448">CalculateThreadgroups(ID2D1ComputeInfo \*pOutputRect, UINT32 \*pDimensionX, UINT32 \*pDimensionY, UINT32 \*pDimensionZ)</span></span>

<span data-ttu-id="ecffa-449">Mientras que los sombreadores de píxeles se ejecutan por píxel y los sombreadores de vértices se ejecutan por vértices, los sombreadores de cálculo se ejecutan por cada 'threadgroup.</span><span class="sxs-lookup"><span data-stu-id="ecffa-449">Whereas pixel shaders are executed on a per-pixel basis and vertex shaders are executed on a per-vertex basis, compute shaders are executed on a per-'threadgroup' basis.</span></span> <span data-ttu-id="ecffa-450">Un elemento threadgroup representa un número de subprocesos que se ejecutan simultáneamente en la GPU.</span><span class="sxs-lookup"><span data-stu-id="ecffa-450">A threadgroup represents a number of threads that execute concurrently on the GPU.</span></span> <span data-ttu-id="ecffa-451">El código HLSL del sombreador de cálculo decide cuántos subprocesos se deben ejecutar por elemento threadgroup.</span><span class="sxs-lookup"><span data-stu-id="ecffa-451">The compute shader HLSL code decides how many threads should be executed per threadgroup.</span></span> <span data-ttu-id="ecffa-452">El efecto escala el número de threadgroups de forma que el sombreador ejecute el número deseado de veces, en función de la lógica del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-452">The effect scales the number of threadgroups so that the shader executes the desired number of times, depending on the shader's logic.</span></span>

<span data-ttu-id="ecffa-453">El método [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) permite a la transformación informar a [Direct2D](./direct2d-portal.md) el número de grupos de subprocesos necesarios, en función del tamaño de la imagen y el conocimiento de la transformación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-453">The [**CalculateThreadgroups**](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1computetransform-calculatethreadgroups) method allows the transform to inform [Direct2D](./direct2d-portal.md) how many thread groups are required, based on the size of the image and the transform's own knowledge of the shader.</span></span>

<span data-ttu-id="ecffa-454">El número de veces que se ejecuta el sombreador de cálculo es un producto de los recuentos de elemento threadgroup especificados aquí y la anotación ' numthreads ' en el [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-454">The number of times the compute shader is executed is a product of the threadgroup counts specified here and the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span> <span data-ttu-id="ecffa-455">Por ejemplo, si la transformación establece las dimensiones elemento threadgroup en (2, 2, 1), el sombreador especifica (3, 3, 1) subprocesos por elemento threadgroup y, a continuación, se ejecutarán 4 threadgroups, cada uno con 9 subprocesos en ellos, para un total de 36 instancias de subproceso.</span><span class="sxs-lookup"><span data-stu-id="ecffa-455">For example, if the transform sets the threadgroup dimensions to be (2,2,1) the shader specifies (3,3,1) threads per threadgroup, then 4 threadgroups will be executed, each with 9 threads in them, for a total of 36 thread instances.</span></span>

<span data-ttu-id="ecffa-456">Un escenario común es procesar un píxel de salida por cada instancia del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="ecffa-456">A common scenario is to process one output pixel for each instance of the compute shader.</span></span> <span data-ttu-id="ecffa-457">Para calcular el número de grupos de subprocesos para este escenario, la transformación divide el ancho y el alto de la imagen por las dimensiones x e y respectivas de la anotación ' numthreads ' en el [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl)del sombreador de proceso.</span><span class="sxs-lookup"><span data-stu-id="ecffa-457">To calculate the number of thread groups for this scenario, the transform divides the width and height of the image by the respective x and y dimensions of the 'numthreads' annotation in the compute shader [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl).</span></span>

<span data-ttu-id="ecffa-458">Lo importante es que, si se realiza esta división, el número de grupos de subprocesos solicitados siempre se debe redondear al entero más cercano; de lo contrario, los píxeles de ' resto ' no se ejecutarán en.</span><span class="sxs-lookup"><span data-stu-id="ecffa-458">Importantly, if this division is performed, then the number of thread groups requested must always be rounded up to the nearest integer, otherwise the 'remainder' pixels will not be executed upon.</span></span> <span data-ttu-id="ecffa-459">Si un sombreador (por ejemplo) calcula un solo píxel con cada subproceso, el código del método tendría el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="ecffa-459">If a shader (for example) computes a single pixel with each thread, the method's code would appear as follows.</span></span>


```C++
IFACEMETHODIMP SampleTransform::CalculateThreadgroups(
    _In_ const D2D1_RECT_L* pOutputRect,
    _Out_ UINT32* pDimensionX,
    _Out_ UINT32* pDimensionY,
    _Out_ UINT32* pDimensionZ
    )
{    
    // The input image's dimensions are divided by the corresponding number of threads in each
    // threadgroup. This is specified in the HLSL, and in this example is 24 for both the x and y
    // dimensions. Dividing the image dimensions by these values calculates the number of
    // thread groups that need to be executed.

    *pDimensionX = static_cast<UINT32>(
         ceil((m_inputRect.right - m_inputRect.left) / 24.0f);

    *pDimensionY = static_cast<UINT32>(
         ceil((m_inputRect.bottom - m_inputRect.top) / 24.0f);

    // The z dimension is set to '1' in this example because the shader will
    // only be executed once for each pixel in the two-dimensional input image.
    // This value can be increased to perform additional executions for a given
    // input position.
    *pDimensionZ = 1;

    return S_OK;
}
```



<span data-ttu-id="ecffa-460">[HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) usa el siguiente código para especificar el número de subprocesos de cada grupo de subprocesos:</span><span class="sxs-lookup"><span data-stu-id="ecffa-460">The [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) uses the following code to specify the number of threads in each thread group:</span></span>


```hlsl
// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup. 
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(24, 24, 1)]
void main(
...
```



<span data-ttu-id="ecffa-461">Durante la ejecución, el elemento threadgroup actual y el índice del subproceso actual se pasan como parámetros al método de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ecffa-461">During execution, the current threadgroup and current thread index are passed as parameters to the shader method:</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768. For Shader Model 5, z <= 64 and x*y*z <= 1024.
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in ID2D1ComputeTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
...
```



### <a name="reading-image-data"></a><span data-ttu-id="ecffa-462">Leer datos de imagen</span><span class="sxs-lookup"><span data-stu-id="ecffa-462">Reading image data</span></span>

<span data-ttu-id="ecffa-463">Los sombreadores de cálculo tienen acceso a la imagen de entrada de la transformación como una sola textura bidimensional:</span><span class="sxs-lookup"><span data-stu-id="ecffa-463">Compute shaders access the transform's input image as a single two-dimensional texture:</span></span>


```hlsl
Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);
```



<span data-ttu-id="ecffa-464">Sin embargo, al igual que los sombreadores de píxeles, no se garantiza que los datos de la imagen empiecen en (0,0) en la textura.</span><span class="sxs-lookup"><span data-stu-id="ecffa-464">However, like pixel shaders, the image's data is not guaranteed to begin at (0, 0) on the texture.</span></span> <span data-ttu-id="ecffa-465">En su lugar, [Direct2D](./direct2d-portal.md) proporciona constantes del sistema que permiten a los sombreadores compensar cualquier desplazamiento:</span><span class="sxs-lookup"><span data-stu-id="ecffa-465">Instead, [Direct2D](./direct2d-portal.md) provides system constants that allow shaders to compensate for any offset:</span></span>


```hlsl
// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the input rectangle to the shader in terms of pixels.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}
```



<span data-ttu-id="ecffa-466">Una vez definidos el método auxiliar y el búfer de constantes anteriores, el sombreador puede realizar un muestreo de los datos de imagen mediante lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ecffa-466">Once the above constant buffer and helper method have been defined, the shader can sample image data using the following:</span></span>


```hlsl
float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by input image offset.
            ),
        0
        );
```



### <a name="writing-image-data"></a><span data-ttu-id="ecffa-467">Escribir datos de imagen</span><span class="sxs-lookup"><span data-stu-id="ecffa-467">Writing image data</span></span>

<span data-ttu-id="ecffa-468">[Direct2D](./direct2d-portal.md) espera que un sombreador defina un búfer de salida para la imagen resultante que se va a colocar.</span><span class="sxs-lookup"><span data-stu-id="ecffa-468">[Direct2D](./direct2d-portal.md) expects a shader to define an output buffer for the resulting image to be placed.</span></span> <span data-ttu-id="ecffa-469">En el modelo de sombreador 4 (DirectX 10), este debe ser un búfer unidimensional debido a las restricciones de características:</span><span class="sxs-lookup"><span data-stu-id="ecffa-469">In Shader Model 4 (DirectX 10), this must be a single-dimensional buffer due to feature constraints:</span></span>


```hlsl
// Shader Model 4 does not support RWTexture2D, must use 1D buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);
```



<span data-ttu-id="ecffa-470">La textura de salida se indexa primero a fila para permitir que se almacene toda la imagen.</span><span class="sxs-lookup"><span data-stu-id="ecffa-470">The output texture is indexed row-first to allow the entire image to be stored.</span></span>


```hlsl
uint imageWidth = resultRect[2] - resultRect[0];
uint imageHeight = resultRect[3] - resultRect[1];
OutputTexture[yIndex * imageWidth + xIndex] = color;
```



<span data-ttu-id="ecffa-471">Por otro lado, los sombreadores modelo de sombreador 5 (DirectX 11) pueden usar texturas de salida bidimensionales:</span><span class="sxs-lookup"><span data-stu-id="ecffa-471">On the other hand, Shader Model 5 (DirectX 11) shaders can use two-dimensional output textures:</span></span>


```hlsl
RWTexture2D<float4> OutputTexture : register(t1);
```



<span data-ttu-id="ecffa-472">Con los sombreadores modelo de sombreador 5, [Direct2D](./direct2d-portal.md) proporciona un parámetro ' outputOffset ' adicional en el búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="ecffa-472">With Shader Model 5 shaders, [Direct2D](./direct2d-portal.md) provides an additional 'outputOffset' parameter in the constant buffer.</span></span> <span data-ttu-id="ecffa-473">La salida del sombreador debe offsettedse en esta cantidad:</span><span class="sxs-lookup"><span data-stu-id="ecffa-473">The shader's output should be offsetted by this amount:</span></span>


```hlsl
OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="ecffa-474">A continuación se muestra un sombreador de cálculo del modelo de sombreador de paso 5 completado.</span><span class="sxs-lookup"><span data-stu-id="ecffa-474">A completed pass-through Shader Model 5 compute shader is shown below.</span></span> <span data-ttu-id="ecffa-475">En ella, cada uno de los subprocesos del sombreador de cálculo Lee y escribe un solo píxel de la imagen de entrada.</span><span class="sxs-lookup"><span data-stu-id="ecffa-475">In it, each of the compute shader threads reads and writes a single pixel of the input image.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

RWTexture2D<float4> OutputTexture : register(t1);

// These are default constants passed by D2D.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    int2 outputOffset;
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 5, z <= 64 and x*y*z <= 1024
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y,
    // groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups.
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    uint imageWidth = resultRect.z - resultRect.x;
    uint imageHeight = resultRect.w - resultRect.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is
    // executed in chunks sized by the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups.
    // For this reason each shader should ensure the current dispatchThreadId is within the bounds of the input
    // image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[uint2(xIndex, yIndex) + outputOffset.xy] = color;
```



<span data-ttu-id="ecffa-476">En el código siguiente se muestra la versión equivalente del modelo de sombreador 4 del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ecffa-476">The code below shows the equivalent Shader Model 4 version of the shader.</span></span> <span data-ttu-id="ecffa-477">Observe que el sombreador ahora se representa en un búfer de salida de una sola dimensión.</span><span class="sxs-lookup"><span data-stu-id="ecffa-477">Notice that the shader now renders into a single-dimensional output buffer.</span></span>


```hlsl
#define NUMTHREADS_X 24
#define NUMTHREADS_Y 24

Texture2D<float4> InputTexture : register(t0);
SamplerState InputSampler : register(s0);

// Shader Model 4 does not support RWTexture2D, must use one-dimensional buffer instead.
RWStructuredBuffer<float4> OutputTexture : register(t1);

// These are default constants passed by D2D. See PixelShader and VertexShader
// projects for how to pass custom values into a shader.
cbuffer systemConstants : register(b0)
{
    int4 resultRect; // Represents the region of the output image.
    float2 sceneToInput0X;
    float2 sceneToInput0Y;
};

// The image does not necessarily begin at (0,0) on InputTexture. The shader needs
// to use the coefficients provided by Direct2D to map the requested image data to
// where it resides on the texture.
float2 ConvertInput0SceneToTexelSpace(float2 inputScenePosition)
{
    float2 ret;
    ret.x = inputScenePosition.x * sceneToInput0X[0] + sceneToInput0X[1];
    ret.y = inputScenePosition.y * sceneToInput0Y[0] + sceneToInput0Y[1];
    
    return ret;
}

// numthreads(x, y, z)
// This specifies the number of threads in each dispatched threadgroup.
// For Shader Model 4, z == 1 and x*y*z <= 768
[numthreads(NUMTHREADS_X, NUMTHREADS_Y, 1)]
void main(
    // dispatchThreadId - Uniquely identifies a given execution of the shader, most commonly used parameter.
    // Definition: (groupId.x * NUM_THREADS_X + groupThreadId.x, groupId.y * NUMTHREADS_Y + groupThreadId.y, groupId.z * NUMTHREADS_Z + groupThreadId.z)
    uint3 dispatchThreadId  : SV_DispatchThreadID,

    // groupThreadId - Identifies an individual thread within a thread group.
    // Range: (0 to NUMTHREADS_X - 1, 0 to NUMTHREADS_Y - 1, 0 to NUMTHREADS_Z - 1)
    uint3 groupThreadId     : SV_GroupThreadID,

    // groupId - Identifies which thread group the individual thread is being executed in.
    // Range defined in DFTVerticalTransform::CalculateThreadgroups
    uint3 groupId           : SV_GroupID, 

    // One dimensional indentifier of a compute shader thread within a thread group.
    // Range: (0 to NUMTHREADS_X * NUMTHREADS_Y * NUMTHREADS_Z - 1)
    uint  groupIndex        : SV_GroupIndex
    )
{
    uint imageWidth = resultRect[2] - resultRect[0];
    uint imageHeight = resultRect[3] - resultRect[1];

    uint xIndex = dispatchThreadId.x;
    uint yIndex = dispatchThreadId.y;

    // It is likely that the compute shader will execute beyond the bounds of the input image, since the shader is executed in chunks sized by
    // the threadgroup size defined in ID2D1ComputeTransform::CalculateThreadgroups. For this reason each shader should ensure the current
    // dispatchThreadId is within the bounds of the input image before proceeding.
    if (xIndex >= imageWidth || yIndex >= imageHeight)
    {
        return;
    }

    float4 color = InputTexture.SampleLevel(
        InputSampler, 
        ConvertInput0SceneToTexelSpace(
            float2(xIndex + .5, yIndex + .5) + // Add 0.5 to each coordinate to hit the center of the pixel.
            resultRect.xy // Offset sampling location by image offset.
            ),
        0
        );

    OutputTexture[yIndex * imageWidth + xIndex] = color;
}
```



## <a name="related-topics"></a><span data-ttu-id="ecffa-478">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ecffa-478">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecffa-479">Ejemplo de SDK de D2DCustomEffects</span><span class="sxs-lookup"><span data-stu-id="ecffa-479">D2DCustomEffects SDK sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)
</dt> </dl>

 

 