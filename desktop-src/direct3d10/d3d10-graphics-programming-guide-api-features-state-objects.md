---
description: En Direct3D 10, el estado del dispositivo se agrupa en objetos de estado que reducen considerablemente el costo de los cambios de estado.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Objetos de estado (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335429"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="22625-103">Objetos de estado (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="22625-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="22625-104">En Direct3D 10, el estado del dispositivo se agrupa en objetos de estado que reducen considerablemente el costo de los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="22625-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="22625-105">Hay varios objetos de estado y cada uno de ellos está diseñado para inicializar un conjunto de estado para una fase de canalización determinada.</span><span class="sxs-lookup"><span data-stu-id="22625-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="22625-106">Puede crear hasta 4096 de cada tipo de objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="22625-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="22625-107">Estado de diseño de entrada</span><span class="sxs-lookup"><span data-stu-id="22625-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="22625-108">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="22625-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="22625-109">Estado de galería de símbolos de profundidad</span><span class="sxs-lookup"><span data-stu-id="22625-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="22625-110">Estado de blend</span><span class="sxs-lookup"><span data-stu-id="22625-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="22625-111">Estado del muestreador</span><span class="sxs-lookup"><span data-stu-id="22625-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="22625-112">Consideraciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="22625-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="22625-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22625-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="22625-114">Input-Layout estado</span><span class="sxs-lookup"><span data-stu-id="22625-114">Input-Layout State</span></span>

<span data-ttu-id="22625-115">Este grupo de estado (vea [**D3D10 \_ INPUT \_ ELEMENT \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)determina cómo la fase del [ensamblador](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) de entrada lee los datos de los búferes de entrada y los ensambla para que los use el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="22625-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="22625-116">Esto incluye el estado, como el número de elementos del búfer de entrada y la firma de los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="22625-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="22625-117">La fase de ensamblador de entrada es una nueva fase de la canalización cuyo trabajo es transmitir primitivas de la memoria a la canalización.</span><span class="sxs-lookup"><span data-stu-id="22625-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="22625-118">Para crear un objeto input-layout-state, vea [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="22625-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="22625-119">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="22625-119">Rasterizer State</span></span>

<span data-ttu-id="22625-120">Este grupo de estado (consulte [**D3D10 \_ RASTERIZER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)inicializa la fase [del rasterizador](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="22625-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="22625-121">Este objeto incluye el estado, como los modos de relleno o cull, la habilitación de un rectángulo de recorte para el recorte y la configuración de parámetros multimuestreo.</span><span class="sxs-lookup"><span data-stu-id="22625-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="22625-122">Esta fase rasteriza las primitivas en píxeles, realizando operaciones como el recorte y la asignación de primitivas a la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="22625-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="22625-123">Para crear un objeto de estado de rasterizador, vea [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span><span class="sxs-lookup"><span data-stu-id="22625-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="22625-124">Depth-Stencil estado</span><span class="sxs-lookup"><span data-stu-id="22625-124">Depth-Stencil State</span></span>

<span data-ttu-id="22625-125">Este grupo de estado (vea [**D3D10 \_ DEPTH \_ STENCIL \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)inicializa la parte de la galería de símbolos de profundidad de la fase de fusión [de salida.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)</span><span class="sxs-lookup"><span data-stu-id="22625-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="22625-126">Más concretamente, este objeto inicializa las pruebas de profundidad y galería de símbolos.</span><span class="sxs-lookup"><span data-stu-id="22625-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="22625-127">Para crear un objeto depth-stencil-state, vea [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span><span class="sxs-lookup"><span data-stu-id="22625-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="22625-128">Estado de blend</span><span class="sxs-lookup"><span data-stu-id="22625-128">Blend State</span></span>

<span data-ttu-id="22625-129">Este grupo de estado (vea [**D3D10 \_ BLEND \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)inicializa la parte de mezcla de la fase [de fusión de salida.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)</span><span class="sxs-lookup"><span data-stu-id="22625-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="22625-130">Para crear un objeto blend-state, vea [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span><span class="sxs-lookup"><span data-stu-id="22625-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="22625-131">Estado del muestreador</span><span class="sxs-lookup"><span data-stu-id="22625-131">Sampler State</span></span>

<span data-ttu-id="22625-132">Este grupo de estado (vea [**D3D10 \_ SAMPLER \_ DESC)**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)inicializa un objeto sampler.</span><span class="sxs-lookup"><span data-stu-id="22625-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="22625-133">Las fases del sombreador usan un objeto sampler para filtrar texturas en memoria.</span><span class="sxs-lookup"><span data-stu-id="22625-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



<span data-ttu-id="22625-134">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="22625-134">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="22625-135">En Direct3D 10, el objeto sampler ya no está enlazado a una textura específica, solo describe cómo realizar el filtrado dado cualquier recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="22625-135">In Direct3D 10, the sampler object is no longer bound to a specific texture, it just describes how to do filtering given any attached resource.</span></span>



 

<span data-ttu-id="22625-136">Para crear un objeto sampler-state, vea [**CreateSamplerState.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate)</span><span class="sxs-lookup"><span data-stu-id="22625-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="22625-137">Consideraciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="22625-137">Performance Considerations</span></span>

<span data-ttu-id="22625-138">El diseño de la API para usar objetos de estado crea varias ventajas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="22625-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="22625-139">Esto incluye validar el estado en el momento de la creación del objeto, habilitar el almacenamiento en caché de objetos de estado en hardware y reducir en gran medida la cantidad de estado que se pasa durante una llamada API de configuración de estado (pasando un identificador al objeto de estado en lugar del estado).</span><span class="sxs-lookup"><span data-stu-id="22625-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="22625-140">Para lograr estas mejoras de rendimiento, debe crear los objetos de estado cuando se inicie la aplicación, justo antes del bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="22625-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="22625-141">Los objetos de estado son inmutables, es decir, una vez creados, no se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="22625-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="22625-142">En su lugar, debe destruirlos y volver a crearlos.</span><span class="sxs-lookup"><span data-stu-id="22625-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="22625-143">Para hacer frente a esta restricción, puede crear hasta 4096 de cada tipo de objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="22625-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="22625-144">Por ejemplo, podría crear varios objetos sampler con varias combinaciones de estado de sampler.</span><span class="sxs-lookup"><span data-stu-id="22625-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="22625-145">A continuación, el cambio del estado del muestreador se realiza mediante una llamada a la API Set adecuada que pasa un identificador al objeto (en lugar del estado del muestreador).</span><span class="sxs-lookup"><span data-stu-id="22625-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="22625-146">Esto reduce significativamente la cantidad de sobrecarga durante cada fotograma de representación para cambiar el estado, ya que el número de llamadas y la cantidad de datos se reducen considerablemente.</span><span class="sxs-lookup"><span data-stu-id="22625-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="22625-147">Como alternativa, puede optar por usar el sistema de efectos que administrará automáticamente la creación eficaz y la destrucción de objetos de estado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="22625-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22625-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22625-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22625-149">Características de API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="22625-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
