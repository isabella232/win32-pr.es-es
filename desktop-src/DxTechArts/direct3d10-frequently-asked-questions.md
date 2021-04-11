---
title: Preguntas más frecuentes sobre Direct3D 10
description: Este artículo contiene algunas de las preguntas más frecuentes sobre Direct3D 10 desde el punto de vista de un desarrollador que está migrando una aplicación existente de Direct3D 9 (D3D9) a Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149402"
---
# <a name="direct3d-10-frequently-asked-questions"></a><span data-ttu-id="0e824-103">Preguntas más frecuentes sobre Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="0e824-103">Direct3D 10 Frequently Asked Questions</span></span>

<span data-ttu-id="0e824-104">Este artículo contiene algunas de las preguntas más frecuentes sobre Direct3D 10 desde el punto de vista de un desarrollador que está migrando una aplicación existente de Direct3D 9 (D3D9) a Direct3D 10 (D3D10).</span><span class="sxs-lookup"><span data-stu-id="0e824-104">This article contains some of the frequently asked questions surrounding Direct3D 10 from the point of view of a developer who is porting an existing application from Direct3D 9 (D3D9) to Direct3D 10 (D3D10).</span></span>

-   [<span data-ttu-id="0e824-105">Búferes de constantes</span><span class="sxs-lookup"><span data-stu-id="0e824-105">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="0e824-106">State</span><span class="sxs-lookup"><span data-stu-id="0e824-106">State</span></span>](#state)
-   [<span data-ttu-id="0e824-107">Formatos</span><span class="sxs-lookup"><span data-stu-id="0e824-107">Formats</span></span>](#formats)
-   [<span data-ttu-id="0e824-108">Vinculación del sombreador</span><span class="sxs-lookup"><span data-stu-id="0e824-108">Shader Linkage</span></span>](#shader-linkage)
-   [<span data-ttu-id="0e824-109">Llamadas a Draw</span><span class="sxs-lookup"><span data-stu-id="0e824-109">Draw Calls</span></span>](#draw-calls)
-   [<span data-ttu-id="0e824-110">Recursos</span><span class="sxs-lookup"><span data-stu-id="0e824-110">Resources</span></span>](#resources)
-   [<span data-ttu-id="0e824-111">Profundidad como textura</span><span class="sxs-lookup"><span data-stu-id="0e824-111">Depth as Texture</span></span>](#depth-as-texture)
-   [<span data-ttu-id="0e824-112">MSAA</span><span class="sxs-lookup"><span data-stu-id="0e824-112">MSAA</span></span>](#msaa)
-   [<span data-ttu-id="0e824-113">Bloqueos</span><span class="sxs-lookup"><span data-stu-id="0e824-113">Crashes</span></span>](#crashes)
-   [<span data-ttu-id="0e824-114">Representación de predicado</span><span class="sxs-lookup"><span data-stu-id="0e824-114">Predicated Rendering</span></span>](#predicated-rendering)
-   [<span data-ttu-id="0e824-115">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="0e824-115">Geometry Shader</span></span>](#geometry-shader)
-   [<span data-ttu-id="0e824-116">HLSL</span><span class="sxs-lookup"><span data-stu-id="0e824-116">HLSL</span></span>](#hlsl)

## <a name="constant-buffers"></a><span data-ttu-id="0e824-117">Búferes de constantes</span><span class="sxs-lookup"><span data-stu-id="0e824-117">Constant Buffers</span></span>

<dl> <dt>

<span data-ttu-id="0e824-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>¿Cuál es la mejor manera de actualizar búferes de constantes?</span><span class="sxs-lookup"><span data-stu-id="0e824-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>What is the best way to update constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="0e824-119">UpdateSubresource y MAP with discard deben ser aproximadamente la misma velocidad.</span><span class="sxs-lookup"><span data-stu-id="0e824-119">UpdateSubresource and Map with Discard should be about the same speed.</span></span> <span data-ttu-id="0e824-120">Elija entre ellos en función de cuál copie la cantidad mínima de memoria.</span><span class="sxs-lookup"><span data-stu-id="0e824-120">Choose between them depending on which one copies the least amount of memory.</span></span> <span data-ttu-id="0e824-121">Si ya tiene los datos almacenados en memoria en un bloque contiguo, use UpdateSubresource.</span><span class="sxs-lookup"><span data-stu-id="0e824-121">If you already have your data stored in memory in one contiguous block, use UpdateSubresource.</span></span> <span data-ttu-id="0e824-122">Si necesita acumular datos de otros lugares, use Map con discard.</span><span class="sxs-lookup"><span data-stu-id="0e824-122">If you need to accumulate data from other places, use Map with Discard.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>¿Cuál es la peor manera de organizar los búferes de constantes?</span><span class="sxs-lookup"><span data-stu-id="0e824-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>What is the worst way to organize constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="0e824-124">El peor rendimiento se realiza colocando todas las constantes de un sombreador determinado en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-124">The worst performance is realized by putting all constants for a particular shader into one constant buffer.</span></span> <span data-ttu-id="0e824-125">Aunque esta suele ser la manera más fácil de migrar de D3D9 a D3D10, puede perjudicar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0e824-125">While this often is the easiest way to port from D3D9 to D3D10, it can cripple performance.</span></span> <span data-ttu-id="0e824-126">Por ejemplo, considere un escenario que usa el siguiente búfer de constantes:</span><span class="sxs-lookup"><span data-stu-id="0e824-126">For example, consider a scenario that uses the following constant buffer:</span></span>

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

<span data-ttu-id="0e824-127">El búfer es de 6560 bytes.</span><span class="sxs-lookup"><span data-stu-id="0e824-127">The buffer is 6560 bytes.</span></span> <span data-ttu-id="0e824-128">Supongamos que hay una aplicación con 1000 objetos que se van a representar, 100 de las cuales son mallas con forma de máscaras y 900 son mallas estáticas.</span><span class="sxs-lookup"><span data-stu-id="0e824-128">Assume there is an application with 1000 objects to be rendered, 100 of which are skinned meshes, and 900 of which are static meshes.</span></span> <span data-ttu-id="0e824-129">Además, supongamos que esta aplicación está usando la asignación de instantáneas con una fuente de luz.</span><span class="sxs-lookup"><span data-stu-id="0e824-129">Also, assume that this application is using shadow mapping with one light source.</span></span> <span data-ttu-id="0e824-130">Esto significa que hay dos pasos, uno para el mapa de profundidad representado a partir de la luz y otro para el paso de representación hacia delante.</span><span class="sxs-lookup"><span data-stu-id="0e824-130">This means there are two passes, one for the depth map rendered from the light, and one for the forward rendering pass.</span></span> <span data-ttu-id="0e824-131">Esto da como resultado 2000 llamadas a Draw.</span><span class="sxs-lookup"><span data-stu-id="0e824-131">This results in 2000 draw calls.</span></span> <span data-ttu-id="0e824-132">Aunque no es necesario que cada llamada a Draw actualice cada parte del búfer de constantes, todo el búfer de constantes se actualiza y se envía a la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="0e824-132">Although each draw call does not NEED to update every part of the constant buffer, the entire constant buffer still is updated and sent to the card.</span></span> <span data-ttu-id="0e824-133">Esto da como resultado la actualización de 13 MB de datos cada fotograma (2000 llamadas a Draw en el plazo de 6560 KB).</span><span class="sxs-lookup"><span data-stu-id="0e824-133">This results in the update of 13 MB of data every frame (2000 draw calls times 6560 KB).</span></span>

</dd> <dt>

<span data-ttu-id="0e824-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>¿Cuál es la mejor manera de organizar mis búferes de constantes?</span><span class="sxs-lookup"><span data-stu-id="0e824-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>What is the best way to organize my constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="0e824-135">La mejor manera es organizar los búferes de constantes según la frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="0e824-135">The best way is to organize constant buffers by frequency of update.</span></span> <span data-ttu-id="0e824-136">Las constantes que se actualizan en frecuencias similares deben estar en el mismo búfer.</span><span class="sxs-lookup"><span data-stu-id="0e824-136">Constants that are updated at similar frequencies should be in the same buffer.</span></span> <span data-ttu-id="0e824-137">Por ejemplo, considere el escenario que se presenta en "¿Cuál es la peor manera de organizar los búferes de constantes?", pero con un diseño mejor constante:</span><span class="sxs-lookup"><span data-stu-id="0e824-137">For example, consider the scenario presented under, "What is the worst way to organize constant buffers?," but with a better constant layout:</span></span>

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

<span data-ttu-id="0e824-138">Los búferes de constantes se dividen por su frecuencia de actualización, pero solo es la mitad de la solución.</span><span class="sxs-lookup"><span data-stu-id="0e824-138">Constant buffers are split by their update frequency, but this only is half of the solution.</span></span> <span data-ttu-id="0e824-139">La aplicación necesita actualizar los búferes de constantes correctamente para sacar el máximo partido de la división.</span><span class="sxs-lookup"><span data-stu-id="0e824-139">The application needs to update the constant buffers correctly in order to take full advantage of the split.</span></span> <span data-ttu-id="0e824-140">Se asumirá la misma escena anterior: 900 mallas estáticas, las mallas de nivel 100, un paso de luz y un pase hacia delante.</span><span class="sxs-lookup"><span data-stu-id="0e824-140">We will assume the same scene as above: 900 static meshes, 100 skinned meshes, one light pass, and one forward pass.</span></span> <span data-ttu-id="0e824-141">También se supone que se almacenarán algunos búferes de constantes por objeto.</span><span class="sxs-lookup"><span data-stu-id="0e824-141">We also will assume that some constant buffers per-object will be stored.</span></span> <span data-ttu-id="0e824-142">Esto significa que cada objeto contendrá un VSPerSkinnedCB o un VSPerStaticCB, en función de si está o no o no o no.</span><span class="sxs-lookup"><span data-stu-id="0e824-142">This means that each object will contain either a VSPerSkinnedCB or a VSPerStaticCB, depending on whether or not it is skinned or static.</span></span> <span data-ttu-id="0e824-143">Hacemos esto para evitar la duplicación de la cantidad de matrices enviadas a través de la canalización.</span><span class="sxs-lookup"><span data-stu-id="0e824-143">We do this in order to avoid doubling the amount of matrices sent through the pipeline.</span></span>

<span data-ttu-id="0e824-144">Dividimos el marco en tres fases.</span><span class="sxs-lookup"><span data-stu-id="0e824-144">We split the frame into three phases.</span></span> <span data-ttu-id="0e824-145">La primera fase es el principio del marco y no implica ninguna representación, solo actualizaciones constantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-145">The first phase is the beginning of the frame and involves no rendering, just constant updates.</span></span>

<dl> <dt>

<span data-ttu-id="0e824-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Inicio del marco**</span><span class="sxs-lookup"><span data-stu-id="0e824-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Begin Frame**</span></span>
</dt> <dd>

-   <span data-ttu-id="0e824-147">Actualizar VSGlobalPerFrameCB para tiempo de aplicación (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="0e824-147">Update VSGlobalPerFrameCB for application time (4 bytes)</span></span>
-   <span data-ttu-id="0e824-148">Update 100 VSPerSkinnedCB para los objetos de la piel 100 (640000 bytes)</span><span class="sxs-lookup"><span data-stu-id="0e824-148">Update 100 VSPerSkinnedCB for the 100 skinned objects (640000 bytes)</span></span>
-   <span data-ttu-id="0e824-149">Actualizar VSPerStaticCB para los objetos estáticos 900 (57600 bytes)</span><span class="sxs-lookup"><span data-stu-id="0e824-149">Update VSPerStaticCB for 900 static objects (57600 bytes)</span></span>

<span data-ttu-id="0e824-150">A continuación se encuentra el paso de asignación de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="0e824-150">Next is the shadow map pass.</span></span> <span data-ttu-id="0e824-151">Tenga en cuenta que el único búfer de constantes que se actualiza realmente es VSPerPassCB.</span><span class="sxs-lookup"><span data-stu-id="0e824-151">Notice that the only constant buffer that actually updates is VSPerPassCB.</span></span> <span data-ttu-id="0e824-152">El resto de búferes de constantes se actualizaron durante el paso de inicio del marco.</span><span class="sxs-lookup"><span data-stu-id="0e824-152">All other constant buffers were updated during the begin frame pass.</span></span> <span data-ttu-id="0e824-153">Aunque todavía necesitamos enlazar estos búferes de constantes, la cantidad de información que se pasa a la tarjeta de vídeo es mínima, ya que los búferes ya se han actualizado.</span><span class="sxs-lookup"><span data-stu-id="0e824-153">While we still need to bind these constant buffers, the amount of information passed to the video card is minimal, because the buffers already have been updated.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Paso de sombra**</span><span class="sxs-lookup"><span data-stu-id="0e824-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Shadow Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="0e824-155">Actualizar VSPerPassCB (72 bytes)</span><span class="sxs-lookup"><span data-stu-id="0e824-155">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="0e824-156">Dibujo de mallas de la piel 100 (100 enlaces, sin actualizaciones)</span><span class="sxs-lookup"><span data-stu-id="0e824-156">Draw 100 skinned meshes (100 binds, no updates)</span></span>
-   <span data-ttu-id="0e824-157">Dibujo de mallas estáticas de 900 (100 enlaces, sin actualizaciones)</span><span class="sxs-lookup"><span data-stu-id="0e824-157">Draw 900 static meshes (100 binds, no updates)</span></span>

<span data-ttu-id="0e824-158">Del mismo modo, el paso de representación hacia delante solo necesita actualizar los datos por material, porque no se almacenó por malla.</span><span class="sxs-lookup"><span data-stu-id="0e824-158">Similarly, the forward rendering pass only needs to update per-material data, because it was not stored per-mesh.</span></span> <span data-ttu-id="0e824-159">Si damos por hecho que hay 500 materiales en uso en la escena:</span><span class="sxs-lookup"><span data-stu-id="0e824-159">If we assume that there are 500 materials in use in the scene:</span></span>

</dd> <dt>

<span data-ttu-id="0e824-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Paso adelante**</span><span class="sxs-lookup"><span data-stu-id="0e824-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="0e824-161">Actualizar VSPerPassCB (72 bytes)</span><span class="sxs-lookup"><span data-stu-id="0e824-161">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="0e824-162">Update 500 VSPerMaterialCBs (10000 bytes)</span><span class="sxs-lookup"><span data-stu-id="0e824-162">Update 500 VSPerMaterialCBs (10000 bytes)</span></span>

<span data-ttu-id="0e824-163">Esto da como resultado un total de solo 707 KB.</span><span class="sxs-lookup"><span data-stu-id="0e824-163">This results in a total of just 707 KB.</span></span> <span data-ttu-id="0e824-164">Aunque se trata de un escenario muy inventado, muestra la cantidad de sobrecarga de actualización constante que se puede reducir mediante la ordenación de constantes por frecuencia de actualización.</span><span class="sxs-lookup"><span data-stu-id="0e824-164">Although this is a very contrived scenario, it illustrates just how much constant update overhead can be reduced by sorting constants by frequency of update.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0e824-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>¿Qué ocurre si no tengo espacio suficiente para almacenar búferes de constantes individuales para mis mallas, material, etc.?</span><span class="sxs-lookup"><span data-stu-id="0e824-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>What if I do not have enough space to store individual constant buffers for my meshes, material, and so on?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-166">Siempre puede usar un sistema en capas de búferes de constantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-166">You always can use a tiered system of constant buffers.</span></span> <span data-ttu-id="0e824-167">Cree búferes de constantes de tamaño variable (16 bytes, 32 bytes, 64 bytes, etc.) hasta el tamaño de búfer constante más grande necesario.</span><span class="sxs-lookup"><span data-stu-id="0e824-167">Create variable-sized constant buffers (16 bytes, 32 bytes, 64 bytes, and so on) up to the largest constant buffer size needed.</span></span> <span data-ttu-id="0e824-168">Cuando sea el momento de enlazar un búfer de constantes a un sombreador, seleccione el búfer de constantes más pequeño que puede contener los datos que necesita el sombreador.</span><span class="sxs-lookup"><span data-stu-id="0e824-168">When it is time to bind a constant buffer to a shader, select the smallest constant buffer that can hold the data needed by the shader.</span></span> <span data-ttu-id="0e824-169">Aunque este enfoque es ligeramente menos eficaz, es un buen paso intermedio.</span><span class="sxs-lookup"><span data-stu-id="0e824-169">Although this approach is slightly less efficient, it is a good intermediate step.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Estoy compartiendo búferes de constantes entre diferentes sombreadores.</span><span class="sxs-lookup"><span data-stu-id="0e824-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>I am sharing constant buffers between different shaders.</span></span> <span data-ttu-id="0e824-171">Un sombreador puede utilizar todas las constantes, pero otra puede utilizar algunas de las constantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-171">One shader may use all of the constants, but another may use some of the constants.</span></span> <span data-ttu-id="0e824-172">¿Cuál es la mejor manera de actualizarlos?</span><span class="sxs-lookup"><span data-stu-id="0e824-172">What is the best way to update these?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-173">Un enfoque consiste en dividir el búfer de constantes aún más.</span><span class="sxs-lookup"><span data-stu-id="0e824-173">One approach is to split the constant buffer even further.</span></span> <span data-ttu-id="0e824-174">Sin embargo, llega un momento en el que se enlazan demasiados búferes de constantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-174">However, there comes a point at which too many constant buffers are bound.</span></span> <span data-ttu-id="0e824-175">En este caso, mueva las constantes que es probable que estén sin usar en varios sombreadores hasta el final del búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-175">In this case, move the constants that are likely to be unused by several shaders to the end of the constant buffer.</span></span> <span data-ttu-id="0e824-176">Al obtener los datos de variables del sombreador, use la \_ marca D3D10 SVF \_ Used de la \_ variable de sombreador D3D10 \_ \_ para determinar si se utiliza la variable.</span><span class="sxs-lookup"><span data-stu-id="0e824-176">When getting the variable data from the shader, use the D3D10\_SVF\_USED flag from the D3D10\_SHADER\_VARIABLE\_DESC to determine if the variable is used.</span></span> <span data-ttu-id="0e824-177">Al colocar variables no usadas al final del búfer de constantes, puede enlazar un búfer más pequeño al sombreador que no utiliza estas variables, con lo que se ahorra el costo de actualización.</span><span class="sxs-lookup"><span data-stu-id="0e824-177">By placing unused variables at the end of the constant buffer, you can bind a smaller buffer to the shader that does not use these variables, thus saving the update cost.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>¿Cuánto se puede mejorar la velocidad de fotogramas si solo se cargan los huesos de mi carácter una vez por fotograma en lugar de una vez por paso/dibujo?</span><span class="sxs-lookup"><span data-stu-id="0e824-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>How much can I improve my frame rate if I only upload my character's bones once per frame instead of once per pass/draw?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-179">Puede mejorar la velocidad de fotogramas entre el 8 y el 50 por ciento, en función de la cantidad de datos redundantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-179">You can improve frame rate between 8 percent and 50 percent depending on the amount of redundant data.</span></span> <span data-ttu-id="0e824-180">En el peor de los casos, no se reducirá el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0e824-180">In the worst case, performance will not be reduced.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>¿Cuántos búferes de constantes debo haber enlazado a la vez?</span><span class="sxs-lookup"><span data-stu-id="0e824-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>How many constant buffers should I have bound at once?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-182">Enlace el número mínimo de búferes de constantes que se tarda en obtener todos los datos en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="0e824-182">Bind the minimum number of constant buffers it takes to get all of your data into the shader.</span></span> <span data-ttu-id="0e824-183">En un escenario realista, cinco es el número recomendado de búferes de constantes que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="0e824-183">In a realistic scenario, five is the recommended number of constant buffers to use.</span></span> <span data-ttu-id="0e824-184">El uso compartido de búferes de constantes entre los sombreadores (enlace de la misma CB a VS y PS) también puede mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0e824-184">Sharing constant buffers between shaders (binding the same CB to the VS and PS) also can improve performance.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>¿Hay algún costo por enlazar búferes de constantes sin usarlos?</span><span class="sxs-lookup"><span data-stu-id="0e824-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Is there a cost for binding constant buffers without using them?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-186">Sí, si realmente no va a usar el búfer, no llame a VSSetConsantBuffer o PSSetConstantBuffer.</span><span class="sxs-lookup"><span data-stu-id="0e824-186">Yes, if you are not actually going to use the buffer, then do not call VSSetConsantBuffer or PSSetConstantBuffer.</span></span> <span data-ttu-id="0e824-187">Esta sobrecarga adicional de API puede agregarse en el transcurso de varias llamadas a Draw.</span><span class="sxs-lookup"><span data-stu-id="0e824-187">This extra API overhead can add up over the course of multiple draw calls.</span></span>

</dd> </dl>

## <a name="state"></a><span data-ttu-id="0e824-188">Estado</span><span class="sxs-lookup"><span data-stu-id="0e824-188">State</span></span>

<dl> <dt>

<span data-ttu-id="0e824-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>¿Cuál es la mejor manera de administrar el estado en D3D10?</span><span class="sxs-lookup"><span data-stu-id="0e824-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>What is the best way to manage state in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-190">La mejor solución es conocer todos los Estados por adelantado y crear los objetos de estado por adelantado.</span><span class="sxs-lookup"><span data-stu-id="0e824-190">The best solution is to know all of your state up front and to create the state objects up front.</span></span> <span data-ttu-id="0e824-191">Esto significa que, en el momento de la representación, el enlace de estado es la única operación que debe producirse.</span><span class="sxs-lookup"><span data-stu-id="0e824-191">This means that at render time, state binding is the only operation that needs to happen.</span></span> <span data-ttu-id="0e824-192">D3D10 también filtra los duplicados.</span><span class="sxs-lookup"><span data-stu-id="0e824-192">D3D10 also filter outs duplicates.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Mi juego se cargó dinámicamente o tiene contenido generado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0e824-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>My game has dynamically loaded or has user-generated content.</span></span> <span data-ttu-id="0e824-194">No puedo cargar todos los objetos de estado por adelantado.</span><span class="sxs-lookup"><span data-stu-id="0e824-194">I cannot load all of my state objects up front.</span></span> <span data-ttu-id="0e824-195">¿Cuál debo hacer?</span><span class="sxs-lookup"><span data-stu-id="0e824-195">What should I do?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-196">Hay dos soluciones aquí.</span><span class="sxs-lookup"><span data-stu-id="0e824-196">There are two solutions here.</span></span> <span data-ttu-id="0e824-197">La primera es crear simplemente objetos de estado sobre la marcha y dejar que D3D10 filtre los duplicados.</span><span class="sxs-lookup"><span data-stu-id="0e824-197">The first is to just create state objects on the fly and to let D3D10 filter out duplicates.</span></span> <span data-ttu-id="0e824-198">Sin embargo, esto no se recomienda en escenarios con muchos cambios de objetos de estado por fotograma.</span><span class="sxs-lookup"><span data-stu-id="0e824-198">This, however, is not recommended for scenarios with many state object changes per frame.</span></span> <span data-ttu-id="0e824-199">Una mejor solución consiste en aplicar un algoritmo hash a los objetos de estado y crear un objeto de estado solo si no se encuentra uno que se ajuste a los requisitos en la tabla hash.</span><span class="sxs-lookup"><span data-stu-id="0e824-199">A better solution is to hash the state objects yourself and to create a state object only if one that fits the requirements is not found in the hash table.</span></span> <span data-ttu-id="0e824-200">La razón por la que se usa una tabla hash personalizada es que una aplicación puede seleccionar un hash rápido según el escenario de uso específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e824-200">The reasoning behind using a custom hash table is that an application can select a fast hash based upon the usage scenario particular to that application.</span></span> <span data-ttu-id="0e824-201">Por ejemplo, si una aplicación solo cambia rendertargetwritemask en BlendState y mantiene todos los demás valores iguales, la aplicación puede generar un hash a partir de rendertargetwritemask en lugar de la estructura completa.</span><span class="sxs-lookup"><span data-stu-id="0e824-201">For example, if an application only changes the rendertargetwritemask in the BlendState and keeps all other values the same, the application can generate a hash from the rendertargetwritemask instead of the entire structure.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>El estado de AlphaTest ha desaparecido.</span><span class="sxs-lookup"><span data-stu-id="0e824-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest state is gone.</span></span> <span data-ttu-id="0e824-203">¿Dónde estaba?</span><span class="sxs-lookup"><span data-stu-id="0e824-203">Where did it go?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-204">AlphaTest Now debe ser rendimiento en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="0e824-204">AlphaTest now should be performance in the shader.</span></span> <span data-ttu-id="0e824-205">Vea el ejemplo FixedFuncEMU.</span><span class="sxs-lookup"><span data-stu-id="0e824-205">See the FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>¿Qué ha ocurrido con los planos de clips del usuario?</span><span class="sxs-lookup"><span data-stu-id="0e824-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>What happened to user clip planes?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-207">Los planos de clips del usuario se han pasado al sombreador.</span><span class="sxs-lookup"><span data-stu-id="0e824-207">User clip planes have moved into the shader.</span></span> <span data-ttu-id="0e824-208">Hay dos formas de controlar esto.</span><span class="sxs-lookup"><span data-stu-id="0e824-208">There are two ways to handle this.</span></span> <span data-ttu-id="0e824-209">El primero es la salida \_ de la VP ClipDistance del sombreador de vértices o del sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="0e824-209">The first is to output SV\_ClipDistance from the vertex shader or the geometry shader.</span></span> <span data-ttu-id="0e824-210">La otra opción es usar discard en el sombreador de píxeles en función de algún valor pasado por el sombreador de vértices o el sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="0e824-210">The other option is to use discard in the pixel shader based upon some value passed down by the vertex shader or the geometry shader.</span></span> <span data-ttu-id="0e824-211">Experimente con ambos para ver cuál es más rápido para su escenario concreto.</span><span class="sxs-lookup"><span data-stu-id="0e824-211">Experiment with both to see which is faster for your particular scenario.</span></span> <span data-ttu-id="0e824-212">El uso de VP \_ ClipDistance podría hacer que el hardware utilizara una rutina de recorte basada en geometría que puede provocar que las llamadas de dibujo enlazadas a geometría se ejecuten más lentamente.</span><span class="sxs-lookup"><span data-stu-id="0e824-212">Using SV\_ClipDistance could cause the hardware to use a geometry-based clipping routine that may cause geometry bound draw calls to run slower.</span></span> <span data-ttu-id="0e824-213">Del mismo modo, el uso de discard desplaza el trabajo al sombreador de píxeles, lo que puede provocar que las llamadas a Draw enlazadas a píxeles se ejecuten más lentamente.</span><span class="sxs-lookup"><span data-stu-id="0e824-213">Likewise, using discard shifts the work to the pixel shader, which may cause pixel-bound draw calls to run slower.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Los borrados no respetan ninguna configuración de estado, como la configuración de rectángulos de tijeras en mi estado de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="0e824-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Clears do not respect any state settings, such as my scissor rect settings in my Rasterizer State.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-215">Los borrados se han separado del estado de la canalización.</span><span class="sxs-lookup"><span data-stu-id="0e824-215">Clears have been separated from the pipeline state.</span></span> <span data-ttu-id="0e824-216">Para obtener el comportamiento del estilo de D3D9, eMule borra el dibujo de un cuádruple de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="0e824-216">In order to get D3D9-style behavior, emulate clears by drawing a full-screen quad.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Estableció mis Estados de nuevo en predeterminado para probar y diagnosticar un error de representación.</span><span class="sxs-lookup"><span data-stu-id="0e824-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>I set my states back to default to try and diagnose a rendering error.</span></span> <span data-ttu-id="0e824-218">Ahora la pantalla aparece en negro, aunque sé que estoy dibujando objetos en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="0e824-218">Now my screen just shows black, although I know I am drawing objects onto the screen.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-219">Al volver a establecer el estado en valores predeterminados (NULL), asegúrese de que SampleMask en la llamada a OMSetBlendState nunca sea cero.</span><span class="sxs-lookup"><span data-stu-id="0e824-219">When setting state back to default values (NULL), ensure that the SampleMask in the call to OMSetBlendState is never zero.</span></span> <span data-ttu-id="0e824-220">Si SampleMask se establece en cero, todos los ejemplos serán lógicamente y con cero.</span><span class="sxs-lookup"><span data-stu-id="0e824-220">If SampleMask is set to zero, then all samples will logically AND with zero.</span></span> <span data-ttu-id="0e824-221">En este escenario, ningún ejemplo pasará la prueba de Blend.</span><span class="sxs-lookup"><span data-stu-id="0e824-221">In this scenario, no samples will pass the blend test.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>¿Dónde se D3DSAMP el \_ Estado de SRGBTEXTURE?</span><span class="sxs-lookup"><span data-stu-id="0e824-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Where did the D3DSAMP\_SRGBTEXTURE state go?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-223">SRGB se quitó como parte del estado de la muestra y ahora está vinculado al formato de textura.</span><span class="sxs-lookup"><span data-stu-id="0e824-223">SRGB was removed as part of the sampler state and now is tied to the texture format.</span></span> <span data-ttu-id="0e824-224">Enlazar una textura SRGB dará como resultado el mismo muestreo que obtendría si se especificara D3DSAMP \_ SRGBTEXTURE en Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0e824-224">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> </dl>

## <a name="formats"></a><span data-ttu-id="0e824-225">Formatos</span><span class="sxs-lookup"><span data-stu-id="0e824-225">Formats</span></span>

<dl> <dt>

<span data-ttu-id="0e824-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>¿Qué formato de D3D9 corresponde al formato D3D10?</span><span class="sxs-lookup"><span data-stu-id="0e824-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Which D3D9 format corresponds to which D3D10 format?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-227">Para obtener información, consulte [consideraciones de Direct3D 9 a Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span><span class="sxs-lookup"><span data-stu-id="0e824-227">For info, see [Direct3D 9 to Direct3D 10 Considerations](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span></span>

</dd> <dt>

<span data-ttu-id="0e824-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>¿Qué ha ocurrido con los formatos de textura de A8R8G8B8?</span><span class="sxs-lookup"><span data-stu-id="0e824-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>What happened to A8R8G8B8 texture formats?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-229">Están en desuso en D3D10.</span><span class="sxs-lookup"><span data-stu-id="0e824-229">They have been deprecated in D3D10.</span></span> <span data-ttu-id="0e824-230">Puede volver a crear las texturas como R8G8B8A8, o puede swizzle en la carga o puede swizzle en el sombreador.</span><span class="sxs-lookup"><span data-stu-id="0e824-230">You can re-source your textures as R8G8B8A8, or you can swizzle on load, or you can swizzle in the shader.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>¿Cómo usar texturas de paleta?</span><span class="sxs-lookup"><span data-stu-id="0e824-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>How do I use palettized textures?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-232">Coloque la paleta de colores en una textura o en un búfer de constantes y enlácelo a la canalización.</span><span class="sxs-lookup"><span data-stu-id="0e824-232">Place your color palette in a texture or a constant buffer and bind it to the pipeline.</span></span> <span data-ttu-id="0e824-233">En el sombreador de píxeles, realice una búsqueda indirecta mediante el índice en la textura de paleta.</span><span class="sxs-lookup"><span data-stu-id="0e824-233">In the pixel shader do an indirect lookup using the index in your palettized texture.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>¿Cuáles son estos nuevos formatos SRGB?</span><span class="sxs-lookup"><span data-stu-id="0e824-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>What are these new SRGB formats?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-235">SRGB se quitó como parte del estado de la muestra y ahora está vinculado al formato de textura.</span><span class="sxs-lookup"><span data-stu-id="0e824-235">SRGB was removed as part of the sampler state and is now tied to the texture format.</span></span> <span data-ttu-id="0e824-236">Enlazar una textura SRGB dará como resultado el mismo muestreo que obtendría si se especificara D3DSAMP \_ SRGBTEXTURE en Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="0e824-236">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>¿Dónde están los ventiladores de triángulo?</span><span class="sxs-lookup"><span data-stu-id="0e824-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Where did triangle fans go?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-238">Los ventiladores de triángulo han quedado en desuso en D3D10.</span><span class="sxs-lookup"><span data-stu-id="0e824-238">Triangle fans have been deprecated in D3D10.</span></span> <span data-ttu-id="0e824-239">Los ventiladores de triángulo deberán convertirse en la canalización de contenido o en la carga.</span><span class="sxs-lookup"><span data-stu-id="0e824-239">Triangle fans will need to be converted either in the content pipeline or on load.</span></span>

</dd> </dl>

## <a name="shader-linkage"></a><span data-ttu-id="0e824-240">Vinculación del sombreador</span><span class="sxs-lookup"><span data-stu-id="0e824-240">Shader Linkage</span></span>

<dl> <dt>

<span data-ttu-id="0e824-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Mis sombreadores de Direct3D 9 se compilan correctamente en el modelo de sombreador 4,0, pero cuando se enlazan a la canalización, obtengo errores de vinculación que se muestran en la salida de depuración con el tiempo de ejecución de depuración.</span><span class="sxs-lookup"><span data-stu-id="0e824-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>My Direct3D 9 shaders compile fine to Shader Model 4.0, but when I bind them to the pipeline, I get linkage errors showing up in the debug output with the debug runtime.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-242">La vinculación del sombreador es mucho más estricta en D3D10.</span><span class="sxs-lookup"><span data-stu-id="0e824-242">Shader linkage is much stricter in D3D10.</span></span> <span data-ttu-id="0e824-243">Los elementos de una fase posterior se deben leer en el orden en que se generan en la fase anterior.</span><span class="sxs-lookup"><span data-stu-id="0e824-243">Elements in a subsequent stage must be read in the order they are output from the previous stage.</span></span> <span data-ttu-id="0e824-244">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0e824-244">For example:</span></span>

<span data-ttu-id="0e824-245">Un sombreador de vértices produce:</span><span class="sxs-lookup"><span data-stu-id="0e824-245">A vertex shader outputs:</span></span>

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="0e824-246">Un sombreador de píxeles lee:</span><span class="sxs-lookup"><span data-stu-id="0e824-246">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="0e824-247">Aunque la posición no es necesaria en el sombreador de píxeles, se producirá un error de vinculación, ya que la posición se genera desde el sombreador de vértices, pero no es leída por el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0e824-247">Although the position is not needed in the pixel shader, this will cause a linkage error, because position is being output from the vertex shader, but not read by the pixel shader.</span></span> <span data-ttu-id="0e824-248">La versión más correcta tendría el siguiente aspecto:</span><span class="sxs-lookup"><span data-stu-id="0e824-248">The more correct version would look like this:</span></span>

<span data-ttu-id="0e824-249">Un sombreador de vértices produce:</span><span class="sxs-lookup"><span data-stu-id="0e824-249">A vertex shader outputs:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

<span data-ttu-id="0e824-250">Un sombreador de píxeles lee:</span><span class="sxs-lookup"><span data-stu-id="0e824-250">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="0e824-251">En este caso, el sombreador de vértices está generando la misma información, pero ahora el sombreador de píxeles está leyendo elementos en la salida del pedido.</span><span class="sxs-lookup"><span data-stu-id="0e824-251">In this case, the vertex shader is outputting the same information, but now the pixel shader is reading things in the order output.</span></span> <span data-ttu-id="0e824-252">Dado que el sombreador de píxeles no lee nada después de Tex, no es necesario preocuparse de que VS esté generando más información de la que la PS está leyendo.</span><span class="sxs-lookup"><span data-stu-id="0e824-252">Because the pixel shader is not reading anything after Tex, we do not have to worry that the VS is outputting more information than the PS is reading.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Necesito una firma de sombreador para crear un diseño de entrada, pero cargaré mis mallas y creo diseños antes de crear los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="0e824-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>I need a shader signature in order to create an Input Layout, but I load my meshes and create layouts before creating shaders.</span></span> <span data-ttu-id="0e824-254">¿Qué puedo hacer?</span><span class="sxs-lookup"><span data-stu-id="0e824-254">What do I do?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-255">Una solución consiste en cambiar el orden y cargar los sombreadores antes de cargar las mallas.</span><span class="sxs-lookup"><span data-stu-id="0e824-255">One solution is to switch the order and load shaders before loading meshes.</span></span> <span data-ttu-id="0e824-256">Sin embargo, esto es mucho más fácil decir que listo.</span><span class="sxs-lookup"><span data-stu-id="0e824-256">However, this is much easier said than done.</span></span> <span data-ttu-id="0e824-257">Siempre puede crear los diseños de entrada a petición cuando lo necesite la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e824-257">You always can create the Input Layouts on demand when needed by the application.</span></span> <span data-ttu-id="0e824-258">Tendrá que mantener una versión de la firma del sombreador en torno a.</span><span class="sxs-lookup"><span data-stu-id="0e824-258">You will have to keep a version of the shader signature around.</span></span> <span data-ttu-id="0e824-259">Debe crear un hash basado en el sombreador y el diseño del búfer, y solo puede crear el diseño de entrada si ya no existe uno que coincida.</span><span class="sxs-lookup"><span data-stu-id="0e824-259">You should create a hash based off of the shader and buffer layout, and only create the Input Layout if one that matches does not exist already.</span></span>

</dd> </dl>

## <a name="draw-calls"></a><span data-ttu-id="0e824-260">Llamadas a Draw</span><span class="sxs-lookup"><span data-stu-id="0e824-260">Draw Calls</span></span>

<dl> <dt>

<span data-ttu-id="0e824-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>¿Cuál es el límite de llamadas a Draw para que D3D10 llegue a 60 Hz?</span><span class="sxs-lookup"><span data-stu-id="0e824-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>What is my limit on draw calls for D3D10 to reach 60 Hz?</span></span> <span data-ttu-id="0e824-262">¿30 Hz?</span><span class="sxs-lookup"><span data-stu-id="0e824-262">30 Hz?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-263">Direct3D 9 tenía una limitación en cuanto al número de llamadas a Draw debido al costo de CPU por llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="0e824-263">Direct3D 9 had a limitation on the number of draw calls because of the CPU cost per draw call.</span></span> <span data-ttu-id="0e824-264">En Direct3D 10, se ha reducido el costo de cada llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="0e824-264">On Direct3D 10, the cost of each draw call has been reduced.</span></span> <span data-ttu-id="0e824-265">Sin embargo, ya no existe una correlación definitiva entre las llamadas a Draw y las velocidades de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0e824-265">However, there is no longer a definite correlation between draw calls and frame rates.</span></span> <span data-ttu-id="0e824-266">Dado que las llamadas a Draw a menudo requieren muchas llamadas de soporte (actualizaciones de búfer de constantes, enlaces de texturas, configuración de estado, etc.), el impacto de la velocidad de fotogramas de la API ahora es más dependiente del uso general de la API en lugar de simplemente dibujar recuentos de llamadas.</span><span class="sxs-lookup"><span data-stu-id="0e824-266">Because draw calls often require many support calls ( constant buffer updates, texture bindings, state setting, and so on) the frame rate impact of the API is now more dependent on the overall API usage as opposed to simply draw call counts.</span></span>

</dd> </dl>

## <a name="resources"></a><span data-ttu-id="0e824-267">Recursos</span><span class="sxs-lookup"><span data-stu-id="0e824-267">Resources</span></span>

<dl> <dt>

<span data-ttu-id="0e824-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>¿Qué tipo de uso de recursos debo usar para las operaciones?</span><span class="sxs-lookup"><span data-stu-id="0e824-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>What resource usage type should I use for what operations?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-269">Use la siguiente hoja de referencia rápida:</span><span class="sxs-lookup"><span data-stu-id="0e824-269">Use the following cheat-sheet:</span></span>

-   <span data-ttu-id="0e824-270">La CPU actualiza el recurso más de una vez por fotograma: D3D10 \_ Usage \_ Dynamic</span><span class="sxs-lookup"><span data-stu-id="0e824-270">The CPU updates the resource more than once per frame: D3D10\_USAGE\_DYNAMIC</span></span>
-   <span data-ttu-id="0e824-271">La CPU actualiza el recurso menos de una vez por fotograma: D3D10 \_ uso \_ predeterminado</span><span class="sxs-lookup"><span data-stu-id="0e824-271">The CPU updates the resource less than once per frame: D3D10\_USAGE\_DEFAULT</span></span>
-   <span data-ttu-id="0e824-272">La CPU no actualiza el recurso: D3D10 \_ Usage \_ inmutable</span><span class="sxs-lookup"><span data-stu-id="0e824-272">The CPU does not update the resource: D3D10\_USAGE\_IMMUTABLE</span></span>
-   <span data-ttu-id="0e824-273">La CPU debe leer el recurso: \_ almacenamiento provisional del uso de D3D10 \_</span><span class="sxs-lookup"><span data-stu-id="0e824-273">The CPU needs to read the resource: D3D10\_USAGE\_STAGING</span></span>

<span data-ttu-id="0e824-274">Dado que los búferes de constantes siempre están diseñados para actualizarse con frecuencia, no se ajustan a la "hoja de referencia".</span><span class="sxs-lookup"><span data-stu-id="0e824-274">Because constant buffers are always meant to be update frequently, they do not conform to the "cheat-sheet."</span></span> <span data-ttu-id="0e824-275">Para saber qué tipos de recursos se deben usar para los búferes de constantes, consulte la sección de [búferes de constantes](#constant-buffers) .</span><span class="sxs-lookup"><span data-stu-id="0e824-275">For which resource types to use for constant buffers, see the [Constant Buffers](#constant-buffers) section.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>¿Qué ha ocurrido con DrawPrimitiveUP y DrawIndexedPrimitiveUP?</span><span class="sxs-lookup"><span data-stu-id="0e824-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>What happened to DrawPrimitiveUP and DrawIndexedPrimitiveUP?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-277">Están en D3D10.</span><span class="sxs-lookup"><span data-stu-id="0e824-277">They are gone in D3D10.</span></span> <span data-ttu-id="0e824-278">En el caso de la geometría dinámica, use un búfer dinámico de uso grande de D3D10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0e824-278">For dynamic geometry use a large D3D10\_USAGE\_DYNAMIC buffer.</span></span> <span data-ttu-id="0e824-279">Al principio del marco, asígnelo con D3D10 \_ map \_ Write \_ discard.</span><span class="sxs-lookup"><span data-stu-id="0e824-279">At the beginning of the frame, map it with D3D10\_MAP\_WRITE\_DISCARD.</span></span> <span data-ttu-id="0e824-280">Para cada llamada subsiguiente a Draw, se avanza el puntero de escritura más allá de la posición de los vértices dibujados previamente y se asigna el búfer con D3D10 \_ map \_ WRITE \_ no \_ overwrite.</span><span class="sxs-lookup"><span data-stu-id="0e824-280">For each subsequent draw call advance the write pointer past the position of the previously drawn vertices and map the buffer with D3D10\_MAP\_WRITE\_NO\_OVERWRITE.</span></span> <span data-ttu-id="0e824-281">Si está cerca del final del búfer antes del final del marco, ajuste el puntero de escritura alrededor del principio y asigne el \_ \_ descartado de escritura de asignación de D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="0e824-281">If you near the end of the buffer before the end of the frame, wrap the write pointer around to the beginning and map with D3D10\_MAP\_WRITE\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>¿Puedo escribir índices de 16 bits y índices de 32 bits en el mismo búfer de geometría dinámico?</span><span class="sxs-lookup"><span data-stu-id="0e824-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Can I write 16-bit indices and 32-bit indices into the same dynamic geometry buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-283">Sí, pero esto puede suponer una reducción del rendimiento en cierto hardware.</span><span class="sxs-lookup"><span data-stu-id="0e824-283">Yes, you can, but this can incur a performance penalty on certain hardware.</span></span> <span data-ttu-id="0e824-284">Es más seguro crear búferes independientes para datos dinámicos de índice de 16 bits y datos de índice de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0e824-284">It is a safer to create separate buffers for dynamic 16-bit index data and 32-bit index data.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Cómo leer los datos de la GPU a la CPU?</span><span class="sxs-lookup"><span data-stu-id="0e824-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>How do I read data back from the GPU to the CPU?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-286">Debe utilizar un recurso de almacenamiento provisional.</span><span class="sxs-lookup"><span data-stu-id="0e824-286">You must use a staging resource.</span></span> <span data-ttu-id="0e824-287">Copie los datos del recurso de GPU en el recurso de almacenamiento provisional mediante CopyResource.</span><span class="sxs-lookup"><span data-stu-id="0e824-287">Copy the data from the GPU resource to the staging resource using CopyResource.</span></span> <span data-ttu-id="0e824-288">Asigne el recurso de almacenamiento provisional para leer los datos.</span><span class="sxs-lookup"><span data-stu-id="0e824-288">Map the staging resource to read the data.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Mi aplicación depende de la funcionalidad de StretchRect.</span><span class="sxs-lookup"><span data-stu-id="0e824-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>My application was dependent on StretchRect functionality.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-290">Dado que se trata básicamente de un contenedor para la funcionalidad básica de Direct3D, se quitó de la API.</span><span class="sxs-lookup"><span data-stu-id="0e824-290">Because this was essentially a wrapper for basic Direct3D functionality, it was removed from the API.</span></span> <span data-ttu-id="0e824-291">Parte de la funcionalidad de StretchRect se ha pasado a D3DX10LoadTextureFromTexture.</span><span class="sxs-lookup"><span data-stu-id="0e824-291">Some of the StretchRect functionality was moved into D3DX10LoadTextureFromTexture.</span></span> <span data-ttu-id="0e824-292">En el caso de las conversiones de formato y la copia de texturas, D3DX10LoadTextureFromTexture puede realizar el trabajo.</span><span class="sxs-lookup"><span data-stu-id="0e824-292">For format conversions and copying textures, D3DX10LoadTextureFromTexture may do the job.</span></span> <span data-ttu-id="0e824-293">Sin embargo, las operaciones como la conversión de un tamaño a otro probablemente requerirán una operación de representación en la textura en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e824-293">However, operations such as converting from one size to another likely will require a render to texture operation in the application.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>No hay desplazamientos ni tamaños en las llamadas de mapa para los recursos.</span><span class="sxs-lookup"><span data-stu-id="0e824-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>There are no offsets or sizes on Map calls for resources.</span></span> <span data-ttu-id="0e824-295">Se trataban de llamadas de bloqueo en Direct3D 9; ¿por qué han cambiado?</span><span class="sxs-lookup"><span data-stu-id="0e824-295">These were there on Lock calls on Direct3D 9; why did they change?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-296">Los desplazamientos y los tamaños de las llamadas de bloqueo en Direct3D 9 eran básicamente el desorden de la API y el controlador los omitió a menudo.</span><span class="sxs-lookup"><span data-stu-id="0e824-296">The offsets and sizes on Lock calls on Direct3D 9 were basically API clutter and often ignored by the driver.</span></span> <span data-ttu-id="0e824-297">Los desplazamientos deben calcularse en su lugar por la aplicación a partir del puntero devuelto en la llamada de asignación.</span><span class="sxs-lookup"><span data-stu-id="0e824-297">Offsets should be calculated instead by the application from the pointer returned in the Map call.</span></span>

</dd> </dl>

## <a name="depth-as-texture"></a><span data-ttu-id="0e824-298">Profundidad como textura</span><span class="sxs-lookup"><span data-stu-id="0e824-298">Depth as Texture</span></span>

<dl> <dt>

<span data-ttu-id="0e824-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>¿Cuál es más rápido?</span><span class="sxs-lookup"><span data-stu-id="0e824-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Which is faster?</span></span> <span data-ttu-id="0e824-300">¿Usar la profundidad como textura o escribir profundidad en alfa y leer eso?</span><span class="sxs-lookup"><span data-stu-id="0e824-300">Using depth as a texture or writing depth to alpha and reading that?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-301">Esto es específico de la aplicación y del hardware.</span><span class="sxs-lookup"><span data-stu-id="0e824-301">This is application and hardware specific.</span></span> <span data-ttu-id="0e824-302">Use el que guarde el mayor ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="0e824-302">Use whichever one saves the most bandwidth.</span></span> <span data-ttu-id="0e824-303">Si ya usa varios destinos de representación y tiene un canal adicional, la profundidad de escritura del sombreador puede ser una solución mejor.</span><span class="sxs-lookup"><span data-stu-id="0e824-303">If you already are using multiple render targets and have an extra channel, then writing depth from the shader may be a better solution.</span></span> <span data-ttu-id="0e824-304">Además, escribir profundidad en alfa u otro destino de representación permite escribir valores de profundidad lineal que pueden acelerar los cálculos que necesitan tener acceso al búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0e824-304">Also, writing depth to alpha or another render target allows you to write linear depth values that may speed up calculations that need to access the depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>¿Se puede enlazar una textura como entrada y enlazada como textura de la galería de símbolos de profundidad siempre que se deshabiliten las escrituras de profundidad?</span><span class="sxs-lookup"><span data-stu-id="0e824-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Can I have a texture bound as an input AND bound as a depth-stencil texture as long as I disable depth writes?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-306">No está en D3D10.</span><span class="sxs-lookup"><span data-stu-id="0e824-306">Not in D3D10.</span></span>

</dd> </dl>

## <a name="msaa"></a><span data-ttu-id="0e824-307">MSAA</span><span class="sxs-lookup"><span data-stu-id="0e824-307">MSAA</span></span>

<dl> <dt>

<span data-ttu-id="0e824-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>¿Puedo resolver una textura de la galería de símbolos de profundidad de MSAA?</span><span class="sxs-lookup"><span data-stu-id="0e824-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Can I resolve an MSAA depth-stencil texture?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-309">No está en D3D10.</span><span class="sxs-lookup"><span data-stu-id="0e824-309">Not in D3D10.</span></span> <span data-ttu-id="0e824-310">Sin embargo, puede muestrear ejemplos individuales de la textura de MSAA.</span><span class="sxs-lookup"><span data-stu-id="0e824-310">However, you can sample individual samples from the MSAA texture.</span></span> <span data-ttu-id="0e824-311">Consulte la sección [HLSL](#hlsl) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="0e824-311">See the [HLSL](#hlsl) section for details.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>¿Por qué mi aplicación se bloquea en cuanto habilito MSAA?</span><span class="sxs-lookup"><span data-stu-id="0e824-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Why does my application crash as soon as I enable MSAA?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-313">Asegúrese de que está habilitando un recuento de muestras de MSAA y un número de calidad que el controlador enumera realmente.</span><span class="sxs-lookup"><span data-stu-id="0e824-313">Ensure you are enabling an MSAA sample count and quality number that actually are enumerated by the driver.</span></span>

</dd> </dl>

## <a name="crashes"></a><span data-ttu-id="0e824-314">Bloqueos</span><span class="sxs-lookup"><span data-stu-id="0e824-314">Crashes</span></span>

<dl> <dt>

<span data-ttu-id="0e824-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Mi aplicación se bloquea en D3D10 o en el controlador y no sé por qué.</span><span class="sxs-lookup"><span data-stu-id="0e824-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>My application crashes in D3D10 or in the driver and I do not know why.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-316">El primer paso es habilitar el tiempo de ejecución de depuración (D3D10 crear el marcador de [**\_ \_ \_ depuración de dispositivo**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) pasado a [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="0e824-316">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="0e824-317">Esto expondrá los errores más comunes como salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="0e824-317">This will expose the most common errors as debug output.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX se bloquea al intentar usar la aplicación con él.</span><span class="sxs-lookup"><span data-stu-id="0e824-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX crashes when I try to use my application with it.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-319">El primer paso es habilitar el tiempo de ejecución de depuración (D3D10 crear el marcador de [**\_ \_ \_ depuración de dispositivo**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) pasado a [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="0e824-319">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="0e824-320">PIX tiene una probabilidad mucho mayor de bloqueo si la salida de depuración no está limpia.</span><span class="sxs-lookup"><span data-stu-id="0e824-320">PIX has a much higher probability of crashing if the debug output is not clean.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Mi juego se queda sin espacio de direcciones virtuales en la vista de 32 bits en D3D10.</span><span class="sxs-lookup"><span data-stu-id="0e824-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>My game runs out of virtual address space on 32-bit Vista under D3D10.</span></span> <span data-ttu-id="0e824-322">No tiene problemas en D3D9.</span><span class="sxs-lookup"><span data-stu-id="0e824-322">It does not have problems on D3D9.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-323">Hubo algunos problemas con D3D10 y el espacio de direcciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="0e824-323">There were some issues with D3D10 and virtual address space.</span></span> <span data-ttu-id="0e824-324">Esto se ha corregido en [KB940105](https://support.microsoft.com/kb/940105).</span><span class="sxs-lookup"><span data-stu-id="0e824-324">This has been fixed in [KB940105](https://support.microsoft.com/kb/940105).</span></span> <span data-ttu-id="0e824-325">Si esto no soluciona el problema, asegúrese de que no está creando más recursos que se pueden asignar (bloqueado) en D3D10 de los que estaba creando en D3D9.</span><span class="sxs-lookup"><span data-stu-id="0e824-325">If that does not fix your problem, ensure you are not creating more resources that can be mapped (locked) in D3D10 than you were creating in D3D9.</span></span> <span data-ttu-id="0e824-326">Piense también en trasladar a 64 bits, ya que esto se hará más frecuente en el futuro.</span><span class="sxs-lookup"><span data-stu-id="0e824-326">Also think about porting to 64-bit since this will become more prevalent in the future.</span></span>

</dd> </dl>

## <a name="predicated-rendering"></a><span data-ttu-id="0e824-327">Representación de predicado</span><span class="sxs-lookup"><span data-stu-id="0e824-327">Predicated Rendering</span></span>

<dl> <dt>

<span data-ttu-id="0e824-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>He usado la representación predicada (basada en los resultados de la consulta de oclusión).</span><span class="sxs-lookup"><span data-stu-id="0e824-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>I used Predicated rendering (based on occlusion query results).</span></span> <span data-ttu-id="0e824-329">¿Por qué la aplicación sigue siendo la misma velocidad?</span><span class="sxs-lookup"><span data-stu-id="0e824-329">Why is my app still the same speed?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-330">En primer lugar, asegúrese de que la representación que desea omitir es realmente el cuello de botella de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e824-330">First, ensure that the rendering you would like to skip is actually the application bottleneck.</span></span> <span data-ttu-id="0e824-331">Si no es el cuello de botella, omitir la representación no ayudará a la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0e824-331">If it is not the bottleneck, then skipping the rendering will not help frame rate.</span></span>

<span data-ttu-id="0e824-332">En segundo lugar, asegúrese de que ha transcurrido el tiempo suficiente entre el problema de la consulta y la representación que desea predicar.</span><span class="sxs-lookup"><span data-stu-id="0e824-332">Second, make sure that enough time has passed between the issue of the query and rendering that you wish to predicate.</span></span> <span data-ttu-id="0e824-333">Si la consulta no ha finalizado en el momento en que la llamada de representación alcanza la GPU, se producirá la representación de todos modos.</span><span class="sxs-lookup"><span data-stu-id="0e824-333">If the query has not finished by the time the render call hits the GPU, the rendering will occur anyway.</span></span>

<span data-ttu-id="0e824-334">En tercer lugar, predication solo omite ciertas llamadas.</span><span class="sxs-lookup"><span data-stu-id="0e824-334">Third, predication only skips certain calls.</span></span> <span data-ttu-id="0e824-335">Las llamadas que se omiten son Draw, Clear, Copy, Update, ResolveSubresource y GenerateMips.</span><span class="sxs-lookup"><span data-stu-id="0e824-335">The calls that are skipped are Draw, Clear, Copy, Update, ResolveSubresource and GenerateMips.</span></span> <span data-ttu-id="0e824-336">La configuración de estado, la configuración de IA, la asignación y las llamadas de creación no respetan predication.</span><span class="sxs-lookup"><span data-stu-id="0e824-336">State setting, IA setup, Map, and Create calls do not respect predication.</span></span> <span data-ttu-id="0e824-337">Si hay una gran cantidad de llamadas de configuración de estado alrededor de la llamada a Draw que se va a predicar, estos Estados se establecerán.</span><span class="sxs-lookup"><span data-stu-id="0e824-337">If there are a lot of state setting calls around the draw call to be predicated, these states still will be set.</span></span>

</dd> </dl>

## <a name="geometry-shader"></a><span data-ttu-id="0e824-338">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="0e824-338">Geometry Shader</span></span>

<dl> <dt>

<span data-ttu-id="0e824-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>¿Debo usar el sombreador de geometría para dividirlasr mi (insertar algo aquí)?</span><span class="sxs-lookup"><span data-stu-id="0e824-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Should I use the geometry shader to tessellate my (insert anything here)?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-340">No.</span><span class="sxs-lookup"><span data-stu-id="0e824-340">No.</span></span> <span data-ttu-id="0e824-341">El sombreador de geometría no se debe utilizar para la teselación.</span><span class="sxs-lookup"><span data-stu-id="0e824-341">The geometry shader should NOT be used for tessellation.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>¿Puedo usar el sombreador de geometría para crear geometría?</span><span class="sxs-lookup"><span data-stu-id="0e824-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Can I use the geometry shader to create geometry?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-343">Sí, en escenarios muy limitados.</span><span class="sxs-lookup"><span data-stu-id="0e824-343">Yes, in very limited scenarios.</span></span> <span data-ttu-id="0e824-344">El sombreador de geometría en las partes actuales de D3D10 (2008) no está equipado para controlar la gran expansión.</span><span class="sxs-lookup"><span data-stu-id="0e824-344">The geometry shader in current D3D10 (2008) parts is not equipped to handle much expansion.</span></span> <span data-ttu-id="0e824-345">Esto puede cambiar en el futuro.</span><span class="sxs-lookup"><span data-stu-id="0e824-345">This may change in the future.</span></span> <span data-ttu-id="0e824-346">Los proveedores de tarjetas de vídeo pueden tener una ruta de acceso especial para una o cuatro expansiones debido a un hardware de punto y Sprite existente.</span><span class="sxs-lookup"><span data-stu-id="0e824-346">Video card vendors may have a special path for one to four expansions because of existing point-sprite hardware.</span></span> <span data-ttu-id="0e824-347">Cualquier otra expansión tendría que ser muy limitada.</span><span class="sxs-lookup"><span data-stu-id="0e824-347">Any other expansion would have to be very limited.</span></span> <span data-ttu-id="0e824-348">Los ejemplos de ParticlesGS y PipesGS logran velocidades de fotogramas altas al realizar solo una expansión limitada.</span><span class="sxs-lookup"><span data-stu-id="0e824-348">The ParticlesGS and PipesGS samples achieve high frame rates by only doing limited expansion.</span></span> <span data-ttu-id="0e824-349">Solo se expanden unos cuantos puntos por fotograma.</span><span class="sxs-lookup"><span data-stu-id="0e824-349">Only a few points are expanded per frame.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>¿Para qué se debe usar el sombreador de geometría?</span><span class="sxs-lookup"><span data-stu-id="0e824-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>What should I use the geometry shader for?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-351">Cualquier elemento que requiera operaciones en un primitivo completo, como la detección de siluetas, las coordenadas Barycentric, etc.</span><span class="sxs-lookup"><span data-stu-id="0e824-351">Anything that requires operations on an entire primitive such as silhouette detection, barycentric coordinates, and so on.</span></span> <span data-ttu-id="0e824-352">Úselo también para seleccionar el segmento de una matriz de destino de representación a la que se van a enviar primitivos.</span><span class="sxs-lookup"><span data-stu-id="0e824-352">Also use it to select which slice of a render target array to send primitives to.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>¿Se pueden generar cantidades variables de geometría desde el sombreador de geometría?</span><span class="sxs-lookup"><span data-stu-id="0e824-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Can I output variable amounts of geometry from the geometry shader?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-354">Sí, pero esto puede causar problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="0e824-354">Yes, but this can cause performance issues.</span></span> <span data-ttu-id="0e824-355">Tome el ejemplo de salida de 1 punto para una invocación y 4 puntos para otro.</span><span class="sxs-lookup"><span data-stu-id="0e824-355">Take the example of outputting 1 point for one invocation and 4 points for another.</span></span> <span data-ttu-id="0e824-356">Al ajustarse dentro de las instrucciones de expansión, esto puede hacer que los subprocesos del sombreador de geometría se ejecuten en serie.</span><span class="sxs-lookup"><span data-stu-id="0e824-356">While fitting within the expansion guidelines, this can cause the geometry shader threads to run serially.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>¿Cómo D3D10 sabe cómo generar índices de adyacencia para mi malla?</span><span class="sxs-lookup"><span data-stu-id="0e824-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>How does D3D10 know how to generate adjacency indices for my mesh?</span></span> <span data-ttu-id="0e824-358">O, ¿por qué D3D10 no se representa correctamente cuando se especifica que el sombreador de geometría necesita información de adyacencia.</span><span class="sxs-lookup"><span data-stu-id="0e824-358">Or, why does D3D10 not render correctly when I specify that the geometry shader needs adjacency information.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-359">D3D10 no crea la información de adyacencia, sino que la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0e824-359">The adjacency information is not created by D3D10, but by the application.</span></span> <span data-ttu-id="0e824-360">La aplicación genera índices de adyacencia y debe contener seis índices por primitivo; de los seis, los índices con números impares son los vértices adyacentes del borde.</span><span class="sxs-lookup"><span data-stu-id="0e824-360">Adjacency indices are generated by the application and must contain six indices per primitive; of the six, the odd numbered indices are the edge adjacent vertices.</span></span> <span data-ttu-id="0e824-361">ID3DX10Mesh:: GenerateAdjacencyAndPointsReps se puede usar para generar estos datos.</span><span class="sxs-lookup"><span data-stu-id="0e824-361">ID3DX10Mesh::GenerateAdjacencyAndPointsReps can be used to generate this data.</span></span>

</dd> </dl>

## <a name="hlsl"></a><span data-ttu-id="0e824-362">HLSL</span><span class="sxs-lookup"><span data-stu-id="0e824-362">HLSL</span></span>

<dl> <dt>

<span data-ttu-id="0e824-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>¿Son lentas las instrucciones de tipo entero y bit a bit?</span><span class="sxs-lookup"><span data-stu-id="0e824-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Are integer and bitwise instructions slow?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-364">Pueden ser.</span><span class="sxs-lookup"><span data-stu-id="0e824-364">They can be.</span></span> <span data-ttu-id="0e824-365">Varias tarjetas D3D10 solo pueden emitir operaciones de enteros en un subconjunto de las unidades de ALU disponibles.</span><span class="sxs-lookup"><span data-stu-id="0e824-365">Various D3D10 cards may be able only to issue integer operations on a subset of the available ALU units.</span></span> <span data-ttu-id="0e824-366">Esto depende en gran medida del hardware.</span><span class="sxs-lookup"><span data-stu-id="0e824-366">This is highly dependent on the hardware.</span></span> <span data-ttu-id="0e824-367">Consulte a su proveedor de hardware individual para obtener recomendaciones sobre cómo abordar las operaciones de enteros en ese hardware determinado.</span><span class="sxs-lookup"><span data-stu-id="0e824-367">See your individual hardware vendor for recommendations on how to address integer operations on that particular hardware.</span></span> <span data-ttu-id="0e824-368">Además, preste mucha atención a las conversiones entre tipos.</span><span class="sxs-lookup"><span data-stu-id="0e824-368">Also, be very careful of casts between types.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>¿Qué ha ocurrido con VPOS?</span><span class="sxs-lookup"><span data-stu-id="0e824-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>What happened to VPOS?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-370">Si declara una entrada en el sombreador de píxeles como posición de la VP \_ , obtendrá el mismo comportamiento que la declaración como VPOS.</span><span class="sxs-lookup"><span data-stu-id="0e824-370">If you declare an input to your pixel shader as SV\_POSITION, you will get the same behavior as declaring it as VPOS.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Cómo muestra una textura de MSAA?</span><span class="sxs-lookup"><span data-stu-id="0e824-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>How do I sample an MSAA texture?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-372">En el sombreador, declare la textura como Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="0e824-372">In your shader, declare your texture as Texture2DMS.</span></span> <span data-ttu-id="0e824-373">A continuación, puede capturar ejemplos individuales con los métodos de ejemplo fuera del objeto Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="0e824-373">You then can fetch individual samples using the Sample methods off of the Texture2DMS object.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Cómo saber si se usa realmente una variable de sombreador en un búfer de constantes?</span><span class="sxs-lookup"><span data-stu-id="0e824-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>How do I tell if a shader variable in a constant buffer actually is used?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-375">Fíjese en el \_ struct de la variable de sombreador D3D10 reflejada \_ \_ para esa variable.</span><span class="sxs-lookup"><span data-stu-id="0e824-375">Look at the reflected D3D10\_SHADER\_VARIABLE\_DESC struct for that variable.</span></span> <span data-ttu-id="0e824-376">uFlags debe tener establecido el \_ indicador D3D10 SVF \_ used.</span><span class="sxs-lookup"><span data-stu-id="0e824-376">uFlags should have the D3D10\_SVF\_USED flag set.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Cómo saber si una variable de sombreador en un búfer de constantes está usando FX10?</span><span class="sxs-lookup"><span data-stu-id="0e824-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>How do I tell if a shader variable in a constant buffer actually is using FX10?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-378">Actualmente no es posible usar FX10.</span><span class="sxs-lookup"><span data-stu-id="0e824-378">This currently is not possible using FX10.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>No tengo ningún control sobre los búferes de constantes que crea FX10.</span><span class="sxs-lookup"><span data-stu-id="0e824-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>I have no control over constant buffers that FX10 creates.</span></span> <span data-ttu-id="0e824-380">¿Cómo se crean y actualizan?</span><span class="sxs-lookup"><span data-stu-id="0e824-380">How are they created and updated?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-381">Todos los búferes de constantes administrados por FX10 se crean como \_ \_ recursos predeterminados de uso de D3D10 y se actualizan con UpdateSubresource.</span><span class="sxs-lookup"><span data-stu-id="0e824-381">All FX10-managed constant buffers are created as D3D10\_USAGE\_DEFAULT resources and are updated using UpdateSubresource.</span></span> <span data-ttu-id="0e824-382">Dado que FX10 mantiene una memoria auxiliar de todos los datos constantes, UpdateSubresource es el mejor enfoque para actualizarlos.</span><span class="sxs-lookup"><span data-stu-id="0e824-382">Because FX10 keeps a backing store of all constant data, UpdateSubresource is the best approach for updating these.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Cómo emular la canalización de funciones fijas mediante sombreadores?</span><span class="sxs-lookup"><span data-stu-id="0e824-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>How do I emulate the fixed function pipeline using shaders?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-384">Vea el ejemplo FixedFuncEMU.</span><span class="sxs-lookup"><span data-stu-id="0e824-384">See FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>¿Debo usar las nuevas \[ sugerencias de \] \[ \] \[ compilador, bucle, bifurcación, \] etc.?</span><span class="sxs-lookup"><span data-stu-id="0e824-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Should I use the new \[unroll\], \[loop\], \[branch\], and so on, compiler hints?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-386">En general, no.</span><span class="sxs-lookup"><span data-stu-id="0e824-386">In general, no.</span></span> <span data-ttu-id="0e824-387">El compilador probará a menudo ambos modos y elegirá el más rápido.</span><span class="sxs-lookup"><span data-stu-id="0e824-387">The compiler will often try both ways and choose the fastest one.</span></span> <span data-ttu-id="0e824-388">En algunos casos, puede ser necesario utilizar \[ unroll \] , por ejemplo, cuando una captura de textura dentro de un bucle necesita tener acceso a un degradado.</span><span class="sxs-lookup"><span data-stu-id="0e824-388">In some cases, it may be necessary to use \[unroll\], for example, when a texture fetch inside a loop needs access to a gradient.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>¿La precisión parcial marca una diferencia en D3D10?</span><span class="sxs-lookup"><span data-stu-id="0e824-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Does partial precision make any difference on D3D10?</span></span> <span data-ttu-id="0e824-390">Puedo especificar una precisión parcial en el HLSL D3D9, pero no en mi D3D10 HLSL.</span><span class="sxs-lookup"><span data-stu-id="0e824-390">I can specify partial precision in my D3D9 HLSL, but not in my D3D10 HLSL.</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-391">Todas las operaciones de D3D10 se especifican para ejecutarse en una precisión de punto flotante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0e824-391">All D3D10 operations are specified to run at 32-bit floating point precision.</span></span> <span data-ttu-id="0e824-392">Por lo tanto, la precisión parcial no debe hacer ninguna diferencia en D3D10.</span><span class="sxs-lookup"><span data-stu-id="0e824-392">Therefore, partial precision should not make any difference in D3D10.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>En D3D9, podía realizar el filtrado de sombra PCF de HW enlazando un búfer de profundidad como textura y usando las instrucciones de HLSL tex2d normales.</span><span class="sxs-lookup"><span data-stu-id="0e824-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9, I could do HW PCF shadow filtering by binding a depth buffer as a texture and using regular tex2d hlsl instructions.</span></span> <span data-ttu-id="0e824-394">Cómo hacer esto en D3D10?</span><span class="sxs-lookup"><span data-stu-id="0e824-394">How do I do this on D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-395">Tiene que usar un estado de muestra de comparación y usar instrucciones de SampleCmp.</span><span class="sxs-lookup"><span data-stu-id="0e824-395">You have to use a comparison sampler state and use SampleCmp instructions.</span></span>

</dd> <dt>

<span data-ttu-id="0e824-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>¿Cómo funciona esta palabra clave Register en D3D10?</span><span class="sxs-lookup"><span data-stu-id="0e824-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>How does this register keyword work in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-397">La palabra clave Register de D3D10 se aplica ahora a la ranura a la que está enlazado un recurso determinado.</span><span class="sxs-lookup"><span data-stu-id="0e824-397">The register keyword in D3D10 now applies to which slot a particular resource is bound to.</span></span> <span data-ttu-id="0e824-398">En este caso, el recurso puede ser un búfer (constante o de otro tipo), una textura o una muestra.</span><span class="sxs-lookup"><span data-stu-id="0e824-398">In this case, the resource can be a Buffer (constant or otherwise), Texture, or Sampler.</span></span>

-   <span data-ttu-id="0e824-399">En el caso de los búferes de constantes, use la sintaxis: Register (bN), donde N es la ranura de entrada (0-15)</span><span class="sxs-lookup"><span data-stu-id="0e824-399">For constant buffers, use the syntax: register(bN), where N is the input slot (0-15)</span></span>
-   <span data-ttu-id="0e824-400">En el caso de las texturas, use la sintaxis: Register (tN), donde N es la ranura de entrada (0-127)</span><span class="sxs-lookup"><span data-stu-id="0e824-400">For textures, use the syntax: register(tN), where N is the input slot (0-127)</span></span>
-   <span data-ttu-id="0e824-401">En el caso de los muestreadores, use la sintaxis: Register (sN), donde N es la ranura de entrada (0-127)</span><span class="sxs-lookup"><span data-stu-id="0e824-401">For samplers, use the syntax: register(sN), where N is the input slot (0-127)</span></span>

</dd> <dt>

<span data-ttu-id="0e824-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Cómo colocar una variable dentro de un búfer de constantes si Register solo se usa para especificar dónde se debe enlazar todo el búfer.</span><span class="sxs-lookup"><span data-stu-id="0e824-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>How do I place a variable inside a constant buffer if register is just used to specify where to bind the entire buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="0e824-403">Use la palabra clave packoffset.</span><span class="sxs-lookup"><span data-stu-id="0e824-403">Use the packoffset keyword.</span></span> <span data-ttu-id="0e824-404">El argumento para packoffset tiene el formato c \[ 0-4095 \] . \[ x, y, z, w \] .</span><span class="sxs-lookup"><span data-stu-id="0e824-404">The argument to packoffset is in the form of c\[0-4095\].\[x,y,z,w\].</span></span> <span data-ttu-id="0e824-405">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0e824-405">For example:</span></span>

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

<span data-ttu-id="0e824-406">En este búfer de constantes, IWaste2Floats se coloca en el tercer Float (12 bytes) en el búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-406">In this constant buffer, IWaste2Floats is placed at the third float (12th byte) in the constant buffer.</span></span> <span data-ttu-id="0e824-407">IWasteMore se coloca en el decimotercer FLOAT4 o 52nd Float en el búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="0e824-407">IWasteMore is placed at the 13th float4 or 52nd float in the constant buffer.</span></span>

</dd> </dl>

 

 