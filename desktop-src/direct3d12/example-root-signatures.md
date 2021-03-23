---
title: Firmas raíz de ejemplo
description: En la siguiente sección se muestran firmas raíz que varían en complejidad de vacío a completo.
ms.assetid: 493D35C9-2A90-4688-BD7E-74B9EB2B4E72
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d09d355cc1c96d77670c5536400f0b3f93c097
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104010"
---
# <a name="example-root-signatures"></a><span data-ttu-id="7bc4f-103">Firmas raíz de ejemplo</span><span class="sxs-lookup"><span data-stu-id="7bc4f-103">Example Root Signatures</span></span>

<span data-ttu-id="7bc4f-104">En la siguiente sección se muestran firmas raíz que varían en complejidad de vacío a completo.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-104">The following section shows root signatures varying in complexity from empty to completely full.</span></span>

-   [<span data-ttu-id="7bc4f-105">Una firma raíz vacía</span><span class="sxs-lookup"><span data-stu-id="7bc4f-105">An empty root signature</span></span>](#an-empty-root-signature)
-   [<span data-ttu-id="7bc4f-106">Una constante</span><span class="sxs-lookup"><span data-stu-id="7bc4f-106">One constant</span></span>](#one-constant)
-   [<span data-ttu-id="7bc4f-107">Agregar una vista de búfer de constantes raíz</span><span class="sxs-lookup"><span data-stu-id="7bc4f-107">Adding a root Constant Buffer View</span></span>](#adding-a-root-constant-buffer-view)
-   [<span data-ttu-id="7bc4f-108">Enlazar Tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="7bc4f-108">Binding descriptor tables</span></span>](#binding-descriptor-tables)
-   [<span data-ttu-id="7bc4f-109">Una firma raíz más compleja</span><span class="sxs-lookup"><span data-stu-id="7bc4f-109">A more complex root signature</span></span>](#a-more-complex-root-signature)
-   [<span data-ttu-id="7bc4f-110">Vistas de recursos del sombreador de streaming</span><span class="sxs-lookup"><span data-stu-id="7bc4f-110">Streaming Shader Resource Views</span></span>](#streaming-shader-resource-views)
-   [<span data-ttu-id="7bc4f-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bc4f-111">Related topics</span></span>](#related-topics)

## <a name="an-empty-root-signature"></a><span data-ttu-id="7bc4f-112">Una firma raíz vacía</span><span class="sxs-lookup"><span data-stu-id="7bc4f-112">An empty root signature</span></span>

![una firma raíz vacía no tiene enlaces](images/root-tables-0.png)

<span data-ttu-id="7bc4f-114">Una firma raíz vacía no es probable que sea útil, pero se puede usar en un paso de representación trivial con el uso solo del ensamblador de entrada, y los sombreadores de vértices y píxeles mínimos que no tienen acceso a ningún descriptor.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-114">An empty root signature is unlikely to be useful, but could be used in a trivial rendering pass with use of only the input assembler, and minimal vertex and pixel shaders that do not access any descriptors.</span></span> <span data-ttu-id="7bc4f-115">También están disponibles la fase de mezcla, el destino de representación y las fases de estarcido de profundidad, incluso con una firma raíz vacía.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-115">Also the blend stage, render target and depth-stencil stages are available, even with an empty root signature.</span></span>

## <a name="one-constant"></a><span data-ttu-id="7bc4f-116">Una constante</span><span class="sxs-lookup"><span data-stu-id="7bc4f-116">One constant</span></span>

![una constante raíz única](images/root-tables-constant.png)

<span data-ttu-id="7bc4f-118">La ranura de enlace de la API es donde el argumento raíz para este parámetro se enlazará en la hora del registro de la lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-118">The API bind slot is where the root argument for this parameter will be bound at command list record time.</span></span> <span data-ttu-id="7bc4f-119">El número de ranuras de enlace de API es implícito, según el orden de los parámetros en la signatura raíz (el primero es siempre cero).</span><span class="sxs-lookup"><span data-stu-id="7bc4f-119">The number of the API bind slots is implicit, based on the order of the parameters in the root signature (the first is always zero).</span></span> <span data-ttu-id="7bc4f-120">La ranura de enlace HLSL es donde el sombreador verá el parámetro raíz que se muestra.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-120">The HLSL bind slot is where the shader will see the root parameter show up.</span></span> <span data-ttu-id="7bc4f-121">El tipo ("uint" en el ejemplo anterior) no es conocido por el hardware, pero solo es un Comentario de la imagen, el hardware simplemente verá el único valor DWORD como contenido.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-121">The type ("uint" in the above example) is not known to the hardware but is just a comment in the image, the hardware will simply see the single DWORD as the contents.</span></span>

<span data-ttu-id="7bc4f-122">Para enlazar una constante en el momento del registro de la lista de comandos, se utilizaría un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="7bc4f-122">To bind a constant at command-list record time, a command similar to the following would be used:</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstant(0,seed); // 0 is the parameter index, seed is used by the shaders
```

## <a name="adding-a-root-constant-buffer-view"></a><span data-ttu-id="7bc4f-123">Agregar una vista de búfer de constantes raíz</span><span class="sxs-lookup"><span data-stu-id="7bc4f-123">Adding a root Constant Buffer View</span></span>

![agrega una vista de búfer de constantes a la firma raíz.](images/root-tables-cbv.png)

<span data-ttu-id="7bc4f-125">En este ejemplo se muestran dos constantes raíz y una vista de búfer de constantes raíz (CBV) que cuesta dos ranuras DWORD.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-125">This example shows two root constants, and a root Constant Buffer View (CBV) that costs two DWORD slots.</span></span>

<span data-ttu-id="7bc4f-126">Para enlazar una vista de búfer de constantes, use un comando como el siguiente.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-126">To bind a constant buffer view use a command such as the following.</span></span> <span data-ttu-id="7bc4f-127">Tenga en cuenta que el primer parámetro (2) es la ranura que se muestra en la imagen.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-127">Note the first parameter (2) is the slot shown in the image.</span></span> <span data-ttu-id="7bc4f-128">Normalmente, se configurará una matriz de constantes y, a continuación, estará disponible para los sombreadores en B0 como CBV.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-128">Typically an array of constants will be set up and then made available to the shaders at b0 as a CBV.</span></span>

``` syntax
pCmdList->SetGraphicsRootConstantBufferView(2,GPUVAForCurrDynamicConstants);
```

## <a name="binding-descriptor-tables"></a><span data-ttu-id="7bc4f-129">Enlazar Tablas de descriptores</span><span class="sxs-lookup"><span data-stu-id="7bc4f-129">Binding descriptor tables</span></span>

![agrega tablas de descriptores a la firma raíz](images/root-tables-2.png)

<span data-ttu-id="7bc4f-131">En este ejemplo se muestra el uso de dos tablas de descriptores; una que declara una tabla de cinco descriptores que estará disponible en tiempo de ejecución en un \_ montón de \_ descriptor de CBV SRV UAV y otro que declare una tabla de dos descriptores que se mostrarán en tiempo de ejecución en un montón de descriptores de muestra.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-131">This example shows the use of two descriptor tables; one declaring a table of five descriptors that will be available at execution time in a CBV\_SRV\_UAV descriptor heap, and another declaring a table of two descriptors that will show up at execution time in a sampler descriptor heap.</span></span>

<span data-ttu-id="7bc4f-132">Para enlazar las tablas de descriptor al grabar una lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-132">To bind descriptor tables when recording a command list.</span></span>

``` syntax
pCmdList->SetComputeRootDescriptorTable(1, handleToCurrentMaterialDataInHeap);
pCmdList->SetComputeRootDescriptorTable(2, handleToCurrentMaterialDataInSamplerHeap);
```

<span data-ttu-id="7bc4f-133">Otra característica de la firma raíz es la constante raíz FLOAT4 que tiene un tamaño de cuatro DWORD.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-133">Another feature of the root signature is the float4 root constant that is four DWORDS in size.</span></span> <span data-ttu-id="7bc4f-134">El comando siguiente enlaza solo los dos DWORDs centrales de los cuatro.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-134">The following command binds just the middle two DWORDS of the four.</span></span>

``` syntax
pCmdList->SetComputeRoot32BitConstants(0,2,myFloat2Array,1);  // 2 constants starting at offset 1 (middle 2 values in float4)
```

## <a name="a-more-complex-root-signature"></a><span data-ttu-id="7bc4f-135">Una firma raíz más compleja</span><span class="sxs-lookup"><span data-stu-id="7bc4f-135">A more complex root signature</span></span>

![una firma raíz compleja con muchos elementos](images/root-tables-3.png)

<span data-ttu-id="7bc4f-137">En este ejemplo se muestra una firma raíz densa con la mayoría de los tipos de entradas.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-137">This example shows a dense root signature with most types of entries.</span></span> <span data-ttu-id="7bc4f-138">Dos de las tablas de descriptor (en las ranuras 3 y 6) incluyen matrices de tamaño sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-138">Two of the descriptor tables (at slots 3 and 6) include unbounded size arrays.</span></span> <span data-ttu-id="7bc4f-139">La carga aquí está en la aplicación para que solo se toquen los descriptores válidos en un montón.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-139">The burden here is on the application to only touch valid descriptors in a heap.</span></span> <span data-ttu-id="7bc4f-140">Las matrices sin enlazar o de gran tamaño requieren el nivel de hardware 2 y la compatibilidad con enlaces de recursos.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-140">Unbounded, or very large arrays, require hardware tier 2+ of resource binding support.</span></span>

<span data-ttu-id="7bc4f-141">Hay dos muestras estáticas (enlazadas sin necesidad de espacios de firma raíz).</span><span class="sxs-lookup"><span data-stu-id="7bc4f-141">There are two static samplers (bound without requiring root signature slots).</span></span>

<span data-ttu-id="7bc4f-142">En la ranura 9, UAV U4 y UAV U5 se declaran en el mismo desplazamiento de la tabla de descriptores.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-142">At slot 9, UAV u4 and UAV u5 are declared at the same descriptor table offset.</span></span> <span data-ttu-id="7bc4f-143">Este es el uso de un descriptor con alias, un descriptor en la memoria se mostrará como U4 y U5 en los sombreadores de HLSL.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-143">This is use of an aliased descriptor, one descriptor in memory will show up as both u4 and u5 in the HLSL shaders.</span></span> <span data-ttu-id="7bc4f-144">En este caso, el sombreador se debe compilar con la \_ \_ opción de alias D3D10 de los recursos del sombreador \_ \_ y la `/res_may_alias` opción o en FXC.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-144">In this case the shader must be compiled with the D3D10\_SHADER\_RESOURCES\_MAY\_ALIAS option, or the or `/res_may_alias` option in FXC.</span></span> <span data-ttu-id="7bc4f-145">Los descriptores con alias permiten enlazar un descriptor a varios puntos de enlace, sin tener que realizar ningún cambio en los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-145">Aliased descriptors enable one descriptor to be bound to multiple bind points, without having to make any changes to the shaders.</span></span>

## <a name="streaming-shader-resource-views"></a><span data-ttu-id="7bc4f-146">Vistas de recursos del sombreador de streaming</span><span class="sxs-lookup"><span data-stu-id="7bc4f-146">Streaming Shader Resource Views</span></span>

![vistas de recursos del sombreador de streaming en esta firma raíz](images/root-tables-4.png)

<span data-ttu-id="7bc4f-148">Esta firma raíz muestra un escenario en el que todos los SRVs se transmiten dentro y fuera de una matriz grande.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-148">This root signature illustrates a scenario where all SRVs are streamed in and out of one large array.</span></span> <span data-ttu-id="7bc4f-149">En tiempo de ejecución, se puede establecer una tabla de descriptor una vez cuando se establece la firma raíz.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-149">At execution time, a descriptor table can be set once when the root signature is set.</span></span> <span data-ttu-id="7bc4f-150">Después, todas las lecturas de textura se realizan mediante la indexación en la matriz a través de constantes que se introducen a través de los primeros argumentos raíz.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-150">Then all texture reads are done by indexing into the array via constants fed via the first few root arguments.</span></span> <span data-ttu-id="7bc4f-151">Solo se necesita un montón de descriptor y solo se actualiza a medida que las texturas se transmiten dentro o fuera de las ranuras descriptoras libres.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-151">Only a single descriptor heap is needed, and is only updated as textures are streamed in or out of free descriptor slots.</span></span>

<span data-ttu-id="7bc4f-152">Los desplazamientos del descriptor en el montón grande se identifican mediante sombreadores que usan las constantes en las vistas de búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-152">The descriptor offsets in the large heap are identified by shaders using the constants in the Constant Buffer Views.</span></span> <span data-ttu-id="7bc4f-153">Por ejemplo, si un sombreador recibe un identificador de material, puede indizar en la matriz de gran tamaño mediante la constante para tener acceso al descriptor necesario (que hace referencia a la textura necesaria).</span><span class="sxs-lookup"><span data-stu-id="7bc4f-153">For example, if a shader is given a material ID, it can index into the one large array using the constant to access the required descriptor (which references the required texture).</span></span>

<span data-ttu-id="7bc4f-154">Este escenario requiere hardware con enlace de recursos Tier2 +.</span><span class="sxs-lookup"><span data-stu-id="7bc4f-154">This scenario requires hardware with resource binding tier2+.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bc4f-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bc4f-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bc4f-156">Niveles de hardware de enlace de recursos</span><span class="sxs-lookup"><span data-stu-id="7bc4f-156">Resource Binding Hardware Tiers</span></span>](hardware-support.md)
</dt> <dt>

[<span data-ttu-id="7bc4f-157">Enlace de recursos en HLSL</span><span class="sxs-lookup"><span data-stu-id="7bc4f-157">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="7bc4f-158">Firmas raíz</span><span class="sxs-lookup"><span data-stu-id="7bc4f-158">Root Signatures</span></span>](root-signatures.md)
</dt> </dl>

 

 




