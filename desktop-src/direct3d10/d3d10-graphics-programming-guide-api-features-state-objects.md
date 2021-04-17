---
description: En Direct3D 10, el estado del dispositivo se agrupa en objetos de estado, lo que reduce en gran medida el costo de los cambios de estado.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Objetos de estado (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a06e8603361a83049440774cfd2e12b4148b183
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705259"
---
# <a name="state-objects-direct3d-10"></a><span data-ttu-id="61523-103">Objetos de estado (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="61523-103">State Objects (Direct3D 10)</span></span>

<span data-ttu-id="61523-104">En Direct3D 10, el estado del dispositivo se agrupa en objetos de estado, lo que reduce en gran medida el costo de los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="61523-104">In Direct3D 10, device state is grouped into state objects which greatly reduce the cost of state changes.</span></span> <span data-ttu-id="61523-105">Hay varios objetos de estado y cada uno está diseñado para inicializar un conjunto de estado para una fase de canalización determinada.</span><span class="sxs-lookup"><span data-stu-id="61523-105">There are several state objects, and each one is designed to initialize a set of state for a particular pipeline stage.</span></span> <span data-ttu-id="61523-106">Puede crear hasta 4096 de cada tipo de objeto de estado.</span><span class="sxs-lookup"><span data-stu-id="61523-106">You can create up to 4096 of each type of state object.</span></span>

-   [<span data-ttu-id="61523-107">Estado de diseño de entrada</span><span class="sxs-lookup"><span data-stu-id="61523-107">Input-Layout State</span></span>](#input-layout-state)
-   [<span data-ttu-id="61523-108">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="61523-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="61523-109">Profundidad: estado de estarcido</span><span class="sxs-lookup"><span data-stu-id="61523-109">Depth-Stencil State</span></span>](#depth-stencil-state)
-   [<span data-ttu-id="61523-110">Estado de Blend</span><span class="sxs-lookup"><span data-stu-id="61523-110">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="61523-111">Estado de muestra</span><span class="sxs-lookup"><span data-stu-id="61523-111">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="61523-112">Consideraciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="61523-112">Performance Considerations</span></span>](#performance-considerations)
-   [<span data-ttu-id="61523-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61523-113">Related topics</span></span>](#related-topics)

## <a name="input-layout-state"></a><span data-ttu-id="61523-114">Estado de Input-Layout</span><span class="sxs-lookup"><span data-stu-id="61523-114">Input-Layout State</span></span>

<span data-ttu-id="61523-115">Este grupo de estado (vea [**la \_ \_ \_ Descripción del elemento de entrada D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) determina cómo la fase del [ensamblador de entrada](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) Lee los datos fuera de los búferes de entrada y los ensambla para que los use el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="61523-115">This group of state (see [**D3D10\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) dictates how the [input-assembler stage](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) reads data out of the input buffers and assembles it for use by the vertex shader.</span></span> <span data-ttu-id="61523-116">Esto incluye el estado como el número de elementos en el búfer de entrada y la firma de los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="61523-116">This includes state such as the number of elements in the input buffer and the signature of the input data.</span></span> <span data-ttu-id="61523-117">La fase de ensamblador de entrada es una nueva fase de la canalización cuyo trabajo es transmitir los primitivos de la memoria a la canalización.</span><span class="sxs-lookup"><span data-stu-id="61523-117">The input-assembler stage is a new stage in the pipeline whose job is to stream primitives from memory into the pipeline.</span></span>

<span data-ttu-id="61523-118">Para crear un objeto de estado de diseño de entrada, vea [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="61523-118">To create a input-layout-state object, see [**CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

## <a name="rasterizer-state"></a><span data-ttu-id="61523-119">Estado del rasterizador</span><span class="sxs-lookup"><span data-stu-id="61523-119">Rasterizer State</span></span>

<span data-ttu-id="61523-120">Este grupo de estado (consulte [**D3D10 \_ rasterizador \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) inicializa la [fase de rasterizador](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span><span class="sxs-lookup"><span data-stu-id="61523-120">This group of state (see [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) initializes the [rasterizer stage](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md).</span></span> <span data-ttu-id="61523-121">Este objeto incluye el estado, como los modos de relleno o de selección, habilitando un rectángulo de recorte en tijera y estableciendo parámetros de ejemplo múltiples.</span><span class="sxs-lookup"><span data-stu-id="61523-121">This object includes state such as fill or cull modes, enabling a scissor rectangle for clipping, and setting multisample parameters.</span></span> <span data-ttu-id="61523-122">Esta fase rasteriza los primitivos en píxeles y realiza operaciones como el recorte y la asignación de primitivos a la ventanilla.</span><span class="sxs-lookup"><span data-stu-id="61523-122">This stage rasterizes primitives into pixels, performing operations like clipping and mapping primitives to the viewport.</span></span>

<span data-ttu-id="61523-123">Para crear un objeto de estado de rasterizador, vea [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span><span class="sxs-lookup"><span data-stu-id="61523-123">To create a rasterizer-state object, see [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).</span></span>

## <a name="depth-stencil-state"></a><span data-ttu-id="61523-124">Estado de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="61523-124">Depth-Stencil State</span></span>

<span data-ttu-id="61523-125">Este grupo de estado (consulte [**D3D10 \_ Depth \_ estarcido \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) inicializa la parte de la galería de símbolos de profundidad de la [fase de combinación de resultados](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="61523-125">This group of state (see [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) initializes the depth-stencil portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="61523-126">Más concretamente, este objeto inicializa las pruebas de profundidad y de estarcido.</span><span class="sxs-lookup"><span data-stu-id="61523-126">More specifically, this object initializes depth and stencil testing.</span></span>

<span data-ttu-id="61523-127">Para crear un objeto de estado de galería de símbolos de profundidad, vea [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span><span class="sxs-lookup"><span data-stu-id="61523-127">To create a depth-stencil-state object, see [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).</span></span>

## <a name="blend-state"></a><span data-ttu-id="61523-128">Estado de Blend</span><span class="sxs-lookup"><span data-stu-id="61523-128">Blend State</span></span>

<span data-ttu-id="61523-129">Este grupo de estado (vea [**D3D10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) inicializa la parte de mezcla de la [fase de combinación de salida](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="61523-129">This group of state (see [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) initializes the blending portion of the [output-merger stage](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md).</span></span>

<span data-ttu-id="61523-130">Para crear un objeto de estado de Blend, vea [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span><span class="sxs-lookup"><span data-stu-id="61523-130">To create a blend-state object, see [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).</span></span>

## <a name="sampler-state"></a><span data-ttu-id="61523-131">Estado de muestra</span><span class="sxs-lookup"><span data-stu-id="61523-131">Sampler State</span></span>

<span data-ttu-id="61523-132">Este grupo de estado (vea [**D3D10 \_ muestra \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) inicializa un objeto de muestra.</span><span class="sxs-lookup"><span data-stu-id="61523-132">This group of state (see [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) initializes a sampler object.</span></span> <span data-ttu-id="61523-133">Las fases del sombreador usan un objeto de muestra para filtrar las texturas en memoria.</span><span class="sxs-lookup"><span data-stu-id="61523-133">A sampler object is used by the shader stages to filter textures in memory.</span></span>



|                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61523-134">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="61523-134">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="61523-135">En Direct3D 10, el objeto de muestra ya no está enlazado a una textura específica; simplemente describe cómo realizar el filtrado dado cualquier recurso asociado.</span><span class="sxs-lookup"><span data-stu-id="61523-135">In Direct3D 10, the sampler object is no longer bound to a specific texture - it just describes how to do filtering given any attached resource.</span></span> |



 

<span data-ttu-id="61523-136">Para crear un objeto de estado de muestra, vea [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span><span class="sxs-lookup"><span data-stu-id="61523-136">To create a sampler-state object, see [**CreateSamplerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).</span></span>

## <a name="performance-considerations"></a><span data-ttu-id="61523-137">Consideraciones de rendimiento</span><span class="sxs-lookup"><span data-stu-id="61523-137">Performance Considerations</span></span>

<span data-ttu-id="61523-138">El diseño de la API para usar objetos de estado crea varias ventajas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="61523-138">Designing the API to use state objects creates several performance advantages.</span></span> <span data-ttu-id="61523-139">Incluyen la validación del estado en el momento de la creación del objeto, la habilitación del almacenamiento en caché de objetos de estado en hardware y la reducción en gran medida de la cantidad de estado que se pasa durante una llamada de API de configuración de estado (pasando un identificador al objeto de estado en lugar del estado).</span><span class="sxs-lookup"><span data-stu-id="61523-139">These include validating state at object creation time, enabling caching of state objects in hardware, and greatly reducing the amount of state that is passed during a state-setting API call (by passing a handle to the state object instead of the state).</span></span>

<span data-ttu-id="61523-140">Para lograr estas mejoras de rendimiento, debe crear los objetos de estado cuando la aplicación se inicia, bien antes del bucle de representación.</span><span class="sxs-lookup"><span data-stu-id="61523-140">To achieve these performance improvements, you should create your state objects when your application starts up, well before your render loop.</span></span> <span data-ttu-id="61523-141">Los objetos de estado son inmutables, es decir, una vez que se crean, no se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="61523-141">State objects are immutable, that is, once they are created, you cannot change them.</span></span> <span data-ttu-id="61523-142">En su lugar, debe destruirlos y volver a crearlos.</span><span class="sxs-lookup"><span data-stu-id="61523-142">Instead you must destroy and recreate them.</span></span> <span data-ttu-id="61523-143">Para hacer frente a esta restricción, puede crear hasta 4096 de cada tipo de objetos de estado.</span><span class="sxs-lookup"><span data-stu-id="61523-143">To cope with this restriction, you can create up to 4096 of each type of state objects.</span></span> <span data-ttu-id="61523-144">Por ejemplo, podría crear varios objetos de muestra con varias combinaciones de estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="61523-144">For example, you could create several sampler objects with various sampler-state combinations.</span></span> <span data-ttu-id="61523-145">El cambio del estado de la muestra se realiza mediante una llamada a la API de conjunto adecuada que pasa un identificador al objeto (en contraposición al estado de muestra).</span><span class="sxs-lookup"><span data-stu-id="61523-145">Changing the sampler state is then accomplished by calling the appropriate Set API which passes a handle to the object (as opposed to the sampler state).</span></span> <span data-ttu-id="61523-146">Esto reduce considerablemente la cantidad de sobrecarga durante cada fotograma de representación para cambiar el estado, ya que el número de llamadas y la cantidad de datos se reducen considerablemente.</span><span class="sxs-lookup"><span data-stu-id="61523-146">This significantly reduces the amount of overhead during each render frame for changing state since the number of calls and the amount of data are greatly reduced.</span></span>

<span data-ttu-id="61523-147">Como alternativa, puede optar por usar el sistema de efectos, que administrará automáticamente la creación y destrucción eficientes de los objetos de estado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="61523-147">Alternatively, you can choose to use the effect system which will automatically manage efficient creation and destruction of state objects for your application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61523-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="61523-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61523-149">Características de la API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="61523-149">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
