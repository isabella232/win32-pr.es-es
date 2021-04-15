---
description: Un bloque de estado se puede usar para capturar solo el estado del vértice (vea bloques de estado guardar y restaurar estado (Direct3D 9)).
ms.assetid: cb898228-dc45-4a2a-a82e-8d64523e9b85
title: Guardar Estados de vértice con un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c6bc7fd291a2609ef60709f05a04fe8d27f8eb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696093"
---
# <a name="saving-vertex-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="85f86-103">Guardar Estados de vértice con un StateBlock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="85f86-103">Saving Vertex States With a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="85f86-104">Un bloque de estado se puede usar para capturar solo el estado del vértice (vea [bloques de estado guardar y restaurar estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="85f86-104">A state block can be used to capture only vertex state (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="85f86-105">El estado siguiente es el estado del vértice:</span><span class="sxs-lookup"><span data-stu-id="85f86-105">The following state is vertex state:</span></span>

-   <span data-ttu-id="85f86-106">Estado de representación de vértices (vea [canalización de vértices: estado de representación](#vertex-pipeline-render-state)).</span><span class="sxs-lookup"><span data-stu-id="85f86-106">Vertex render state (see [Vertex Pipeline: Render State](#vertex-pipeline-render-state)).</span></span>
-   <span data-ttu-id="85f86-107">Estado del muestrario de vértices (consulte [canalización de vértices: estado de muestra](#vertex-pipeline-sampler-state)).</span><span class="sxs-lookup"><span data-stu-id="85f86-107">Vertex sampler state (see [Vertex Pipeline: Sampler State](#vertex-pipeline-sampler-state)).</span></span>
-   <span data-ttu-id="85f86-108">Estado de textura de vértices (vea [canalización de vértices: estado de textura](#vertex-pipeline-texture-state)).</span><span class="sxs-lookup"><span data-stu-id="85f86-108">Vertex texture state (see [Vertex Pipeline: Texture State](#vertex-pipeline-texture-state)).</span></span>
-   <span data-ttu-id="85f86-109">Los segmentos del modo NPatch de [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="85f86-109">The NPatch mode segments from [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>
-   <span data-ttu-id="85f86-110">Cada luz de [**IDirect3DDevice9:: SetLight**](/windows/desktop/api), así como si la luz está habilitada o no con [**IDirect3DDevice9:: LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="85f86-110">Each light from [**IDirect3DDevice9::SetLight**](/windows/desktop/api), as well as whether or not the light is enabled with [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>
-   <span data-ttu-id="85f86-111">Sombreador de vértices actual y cada una de las constantes de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="85f86-111">The current vertex shader and each of the vertex shader constants.</span></span>
-   <span data-ttu-id="85f86-112">Para cada flujo de vértices, almacene el valor de divisor de [**IDirect3DDevice9:: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="85f86-112">For each vertex stream, store the divider value from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="85f86-113">La declaración de vértice actual.</span><span class="sxs-lookup"><span data-stu-id="85f86-113">The current vertex declaration.</span></span>

<span data-ttu-id="85f86-114">Para capturar el estado del vértice con un bloque de estado, especifique D3DSBT \_ VERTEXSTATE cuando llame a [**IDirect3DDevice9:: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="85f86-114">To capture vertex state with a state block, specify D3DSBT\_VERTEXSTATE when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="vertex-pipeline-render-state"></a><span data-ttu-id="85f86-115">Canalización de vértices: estado de representación</span><span class="sxs-lookup"><span data-stu-id="85f86-115">Vertex Pipeline: Render State</span></span>

<span data-ttu-id="85f86-116">Los Estados de representación de dispositivos afectan al comportamiento de casi todas las partes de la canalización.</span><span class="sxs-lookup"><span data-stu-id="85f86-116">Device render states affect the behavior of almost every part of the pipeline.</span></span> <span data-ttu-id="85f86-117">Los Estados de representación se establecen mediante una llamada a [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="85f86-117">Render states are set by calling [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="85f86-118">En la tabla siguiente se incluyen todos los Estados de representación que establecen el estado del vértice:</span><span class="sxs-lookup"><span data-stu-id="85f86-118">The following table includes all render states that set-up vertex state:</span></span>



| <span data-ttu-id="85f86-119">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="85f86-119">Render States</span></span>                           | <span data-ttu-id="85f86-120">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="85f86-120">Default Value</span></span>          |
|-----------------------------------------|------------------------|
| <span data-ttu-id="85f86-121">D3DRS \_ CULLMODE</span><span class="sxs-lookup"><span data-stu-id="85f86-121">D3DRS\_CULLMODE</span></span>                         | <span data-ttu-id="85f86-122">D3DCULL \_ CCW</span><span class="sxs-lookup"><span data-stu-id="85f86-122">D3DCULL\_CCW</span></span>           |
| <span data-ttu-id="85f86-123">D3DRS \_ FOGCOLOR</span><span class="sxs-lookup"><span data-stu-id="85f86-123">D3DRS\_FOGCOLOR</span></span>                         | <span data-ttu-id="85f86-124">0</span><span class="sxs-lookup"><span data-stu-id="85f86-124">0</span></span>                      |
| <span data-ttu-id="85f86-125">D3DRS \_ FOGTABLEMODE</span><span class="sxs-lookup"><span data-stu-id="85f86-125">D3DRS\_FOGTABLEMODE</span></span>                     | <span data-ttu-id="85f86-126">D3DFOG \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="85f86-126">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="85f86-127">D3DRS \_ FOGSTART</span><span class="sxs-lookup"><span data-stu-id="85f86-127">D3DRS\_FOGSTART</span></span>                         | <span data-ttu-id="85f86-128">0</span><span class="sxs-lookup"><span data-stu-id="85f86-128">0</span></span>                      |
| <span data-ttu-id="85f86-129">D3DRS \_ FOGEND</span><span class="sxs-lookup"><span data-stu-id="85f86-129">D3DRS\_FOGEND</span></span>                           | <span data-ttu-id="85f86-130">1</span><span class="sxs-lookup"><span data-stu-id="85f86-130">1</span></span>                      |
| <span data-ttu-id="85f86-131">D3DRS \_ FOGDENSITY</span><span class="sxs-lookup"><span data-stu-id="85f86-131">D3DRS\_FOGDENSITY</span></span>                       | <span data-ttu-id="85f86-132">1</span><span class="sxs-lookup"><span data-stu-id="85f86-132">1</span></span>                      |
| <span data-ttu-id="85f86-133">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="85f86-133">D3DRS\_RANGEFOGENABLE</span></span>                   | <span data-ttu-id="85f86-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85f86-134">**FALSE**</span></span>              |
| <span data-ttu-id="85f86-135">\_Ambiente D3DRS</span><span class="sxs-lookup"><span data-stu-id="85f86-135">D3DRS\_AMBIENT</span></span>                          | <span data-ttu-id="85f86-136">0</span><span class="sxs-lookup"><span data-stu-id="85f86-136">0</span></span>                      |
| <span data-ttu-id="85f86-137">D3DRS \_ COLORVERTEX</span><span class="sxs-lookup"><span data-stu-id="85f86-137">D3DRS\_COLORVERTEX</span></span>                      | <span data-ttu-id="85f86-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85f86-138">**TRUE**</span></span>               |
| <span data-ttu-id="85f86-139">D3DRS \_ FOGVERTEXMODE</span><span class="sxs-lookup"><span data-stu-id="85f86-139">D3DRS\_FOGVERTEXMODE</span></span>                    | <span data-ttu-id="85f86-140">D3DFOG \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="85f86-140">D3DFOG\_NONE</span></span>           |
| <span data-ttu-id="85f86-141">Recorte de D3DRS \_</span><span class="sxs-lookup"><span data-stu-id="85f86-141">D3DRS\_CLIPPING</span></span>                         | <span data-ttu-id="85f86-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85f86-142">**TRUE**</span></span>               |
| <span data-ttu-id="85f86-143">\_Iluminación D3DRS</span><span class="sxs-lookup"><span data-stu-id="85f86-143">D3DRS\_LIGHTING</span></span>                         | <span data-ttu-id="85f86-144">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85f86-144">**TRUE**</span></span>               |
| <span data-ttu-id="85f86-145">D3DRS \_ LOCALVIEWER</span><span class="sxs-lookup"><span data-stu-id="85f86-145">D3DRS\_LOCALVIEWER</span></span>                      | <span data-ttu-id="85f86-146">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85f86-146">**TRUE**</span></span>               |
| <span data-ttu-id="85f86-147">D3DRS \_ EMISSIVEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="85f86-147">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>           | <span data-ttu-id="85f86-148">\_Material D3DMCS</span><span class="sxs-lookup"><span data-stu-id="85f86-148">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="85f86-149">D3DRS \_ AMBIENTMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="85f86-149">D3DRS\_AMBIENTMATERIALSOURCE</span></span>            | <span data-ttu-id="85f86-150">\_Material D3DMCS</span><span class="sxs-lookup"><span data-stu-id="85f86-150">D3DMCS\_MATERIAL</span></span>       |
| <span data-ttu-id="85f86-151">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="85f86-151">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>            | <span data-ttu-id="85f86-152">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="85f86-152">D3DMCS\_COLOR1</span></span>         |
| <span data-ttu-id="85f86-153">D3DRS \_ SPECULARMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="85f86-153">D3DRS\_SPECULARMATERIALSOURCE</span></span>           | <span data-ttu-id="85f86-154">D3DMCS \_ COLOR2</span><span class="sxs-lookup"><span data-stu-id="85f86-154">D3DMCS\_COLOR2</span></span>         |
| <span data-ttu-id="85f86-155">D3DRS \_ VERTEXBLEND</span><span class="sxs-lookup"><span data-stu-id="85f86-155">D3DRS\_VERTEXBLEND</span></span>                      | <span data-ttu-id="85f86-156">Deshabilitación de D3DVBF \_</span><span class="sxs-lookup"><span data-stu-id="85f86-156">D3DVBF\_DISABLE</span></span>        |
| <span data-ttu-id="85f86-157">D3DRS \_ CLIPPLANEENABLE</span><span class="sxs-lookup"><span data-stu-id="85f86-157">D3DRS\_CLIPPLANEENABLE</span></span>                  | <span data-ttu-id="85f86-158">0</span><span class="sxs-lookup"><span data-stu-id="85f86-158">0</span></span>                      |
| <span data-ttu-id="85f86-159">D3DRS \_ puntuación</span><span class="sxs-lookup"><span data-stu-id="85f86-159">D3DRS\_POINTSIZE</span></span>                        | <span data-ttu-id="85f86-160">Dependiente del controlador</span><span class="sxs-lookup"><span data-stu-id="85f86-160">Driver dependent</span></span>       |
| <span data-ttu-id="85f86-161">D3DRS de \_ puntuación \_ mín.</span><span class="sxs-lookup"><span data-stu-id="85f86-161">D3DRS\_POINTSIZE\_MIN</span></span>                   | <span data-ttu-id="85f86-162">1</span><span class="sxs-lookup"><span data-stu-id="85f86-162">1</span></span>                      |
| <span data-ttu-id="85f86-163">D3DRS \_ POINTSPRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="85f86-163">D3DRS\_POINTSPRITEENABLE</span></span>                | <span data-ttu-id="85f86-164">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85f86-164">**FALSE**</span></span>              |
| <span data-ttu-id="85f86-165">D3DRS \_ POINTSCALEENABLE</span><span class="sxs-lookup"><span data-stu-id="85f86-165">D3DRS\_POINTSCALEENABLE</span></span>                 | <span data-ttu-id="85f86-166">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85f86-166">**FALSE**</span></span>              |
| <span data-ttu-id="85f86-167">D3DRS \_ POINTSCALE \_</span><span class="sxs-lookup"><span data-stu-id="85f86-167">D3DRS\_POINTSCALE\_A</span></span>                    | <span data-ttu-id="85f86-168">1</span><span class="sxs-lookup"><span data-stu-id="85f86-168">1</span></span>                      |
| <span data-ttu-id="85f86-169">D3DRS \_ POINTSCALE \_ B</span><span class="sxs-lookup"><span data-stu-id="85f86-169">D3DRS\_POINTSCALE\_B</span></span>                    | <span data-ttu-id="85f86-170">0</span><span class="sxs-lookup"><span data-stu-id="85f86-170">0</span></span>                      |
| <span data-ttu-id="85f86-171">D3DRS \_ POINTSCALE \_ C</span><span class="sxs-lookup"><span data-stu-id="85f86-171">D3DRS\_POINTSCALE\_C</span></span>                    | <span data-ttu-id="85f86-172">0</span><span class="sxs-lookup"><span data-stu-id="85f86-172">0</span></span>                      |
| <span data-ttu-id="85f86-173">D3DRS \_ MULTISAMPLEANTIALIAS</span><span class="sxs-lookup"><span data-stu-id="85f86-173">D3DRS\_MULTISAMPLEANTIALIAS</span></span>             | <span data-ttu-id="85f86-174">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="85f86-174">**TRUE**</span></span>               |
| <span data-ttu-id="85f86-175">D3DRS \_ MULTISAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="85f86-175">D3DRS\_MULTISAMPLEMASK</span></span>                  | <span data-ttu-id="85f86-176">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="85f86-176">0xffffffff</span></span>             |
| <span data-ttu-id="85f86-177">D3DRS \_ PATCHEDGESTYLE</span><span class="sxs-lookup"><span data-stu-id="85f86-177">D3DRS\_PATCHEDGESTYLE</span></span>                   | <span data-ttu-id="85f86-178">D3DPATCHEDGE \_ discreto</span><span class="sxs-lookup"><span data-stu-id="85f86-178">D3DPATCHEDGE\_DISCRETE</span></span> |
| <span data-ttu-id="85f86-179">D3DRS \_ \_ Max</span><span class="sxs-lookup"><span data-stu-id="85f86-179">D3DRS\_POINTSIZE\_MAX</span></span>                   | <span data-ttu-id="85f86-180">1</span><span class="sxs-lookup"><span data-stu-id="85f86-180">1</span></span>                      |
| <span data-ttu-id="85f86-181">D3DRS \_ INDEXEDVERTEXBLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="85f86-181">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>         | <span data-ttu-id="85f86-182">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85f86-182">**FALSE**</span></span>              |
| <span data-ttu-id="85f86-183">D3DRS \_ TWEENFACTOR</span><span class="sxs-lookup"><span data-stu-id="85f86-183">D3DRS\_TWEENFACTOR</span></span>                      | <span data-ttu-id="85f86-184">0</span><span class="sxs-lookup"><span data-stu-id="85f86-184">0</span></span>                      |
| <span data-ttu-id="85f86-185">D3DRS \_ POSITIONDEGREE</span><span class="sxs-lookup"><span data-stu-id="85f86-185">D3DRS\_POSITIONDEGREE</span></span>                   | <span data-ttu-id="85f86-186">D3DDEGREE \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="85f86-186">D3DDEGREE\_CUBIC</span></span>       |
| <span data-ttu-id="85f86-187">D3DRS \_ NORMALDEGREE</span><span class="sxs-lookup"><span data-stu-id="85f86-187">D3DRS\_NORMALDEGREE</span></span>                     | <span data-ttu-id="85f86-188">\_Lineal D3DDEGREE</span><span class="sxs-lookup"><span data-stu-id="85f86-188">D3DDEGREE\_LINEAR</span></span>      |
| <span data-ttu-id="85f86-189">D3DRS \_ MINTESSELLATIONLEVEL</span><span class="sxs-lookup"><span data-stu-id="85f86-189">D3DRS\_MINTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="85f86-190">1</span><span class="sxs-lookup"><span data-stu-id="85f86-190">1</span></span>                      |
| <span data-ttu-id="85f86-191">D3DRS \_ MAXTESSELLATIONLEVEL</span><span class="sxs-lookup"><span data-stu-id="85f86-191">D3DRS\_MAXTESSELLATIONLEVEL</span></span>             | <span data-ttu-id="85f86-192">1</span><span class="sxs-lookup"><span data-stu-id="85f86-192">1</span></span>                      |
| <span data-ttu-id="85f86-193">D3DRS \_ ADAPTIVETESS \_ X</span><span class="sxs-lookup"><span data-stu-id="85f86-193">D3DRS\_ADAPTIVETESS\_X</span></span>                  | <span data-ttu-id="85f86-194">0</span><span class="sxs-lookup"><span data-stu-id="85f86-194">0</span></span>                      |
| <span data-ttu-id="85f86-195">D3DRS \_ ADAPTIVETESS \_ Y</span><span class="sxs-lookup"><span data-stu-id="85f86-195">D3DRS\_ADAPTIVETESS\_Y</span></span>                  | <span data-ttu-id="85f86-196">0</span><span class="sxs-lookup"><span data-stu-id="85f86-196">0</span></span>                      |
| <span data-ttu-id="85f86-197">D3DRS \_ ADAPTIVETESS \_ Z</span><span class="sxs-lookup"><span data-stu-id="85f86-197">D3DRS\_ADAPTIVETESS\_Z</span></span>                  | <span data-ttu-id="85f86-198">1</span><span class="sxs-lookup"><span data-stu-id="85f86-198">1</span></span>                      |
| <span data-ttu-id="85f86-199">D3DRS \_ ADAPTIVETESS \_ W</span><span class="sxs-lookup"><span data-stu-id="85f86-199">D3DRS\_ADAPTIVETESS\_W</span></span>                  | <span data-ttu-id="85f86-200">0</span><span class="sxs-lookup"><span data-stu-id="85f86-200">0</span></span>                      |
| <span data-ttu-id="85f86-201">D3DRS \_ ENABLEADAPTIVETESSELLATION "/></span><span class="sxs-lookup"><span data-stu-id="85f86-201">D3DRS\_ENABLEADAPTIVETESSELLATION"/></span></span> | <span data-ttu-id="85f86-202">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="85f86-202">**FALSE**</span></span>              |



 

## <a name="vertex-pipeline-sampler-state"></a><span data-ttu-id="85f86-203">Canalización de vértices: estado de muestra</span><span class="sxs-lookup"><span data-stu-id="85f86-203">Vertex Pipeline: Sampler State</span></span>

<span data-ttu-id="85f86-204">Los Estados de muestra controlan temas relacionados con el muestreo, como filtrado, mosaico y modos de dirección de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="85f86-204">Sampler states control sampling related topics such as filtering, tiling, and texture coordinate address modes.</span></span> <span data-ttu-id="85f86-205">Use [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) para configurar el estado de la muestra (incluido el usado en la unidad del teselador para los mapas de desplazamiento de ejemplo).</span><span class="sxs-lookup"><span data-stu-id="85f86-205">Use [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) to set up the sampler state (including the one used in the tessellator unit to sample displacement maps).</span></span> <span data-ttu-id="85f86-206">Se ha cambiado el nombre de los Estados de muestra con un \_ prefijo "D3DSAMP" para habilitar la detección de errores en tiempo de compilación al migrar desde DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="85f86-206">The sampler states have been renamed with a "D3DSAMP\_" prefix to enable compile time error detection when porting from DirectX 8.</span></span>

<span data-ttu-id="85f86-207">En la tabla siguiente se incluyen todos los Estados de muestra que establecen el estado del vértice:</span><span class="sxs-lookup"><span data-stu-id="85f86-207">The following table includes all sampler states that set-up vertex state:</span></span>



| <span data-ttu-id="85f86-208">Estados de muestra</span><span class="sxs-lookup"><span data-stu-id="85f86-208">Sampler States</span></span>      | <span data-ttu-id="85f86-209">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="85f86-209">Default Value</span></span> |
|---------------------|---------------|
| <span data-ttu-id="85f86-210">D3DSAMP \_ DMAPOFFSET</span><span class="sxs-lookup"><span data-stu-id="85f86-210">D3DSAMP\_DMAPOFFSET</span></span> | <span data-ttu-id="85f86-211">256</span><span class="sxs-lookup"><span data-stu-id="85f86-211">256</span></span>           |



 

## <a name="vertex-pipeline-texture-state"></a><span data-ttu-id="85f86-212">Canalización de vértices: estado de textura</span><span class="sxs-lookup"><span data-stu-id="85f86-212">Vertex Pipeline: Texture State</span></span>

<span data-ttu-id="85f86-213">Los Estados de textura controlan las operaciones de combinación de texturas del mezclador de varias texturas.</span><span class="sxs-lookup"><span data-stu-id="85f86-213">Texture states control texture blending operations of the multi-texture blender.</span></span> <span data-ttu-id="85f86-214">Use [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) para configurar los Estados de textura.</span><span class="sxs-lookup"><span data-stu-id="85f86-214">Use [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) to set-up texture states.</span></span> <span data-ttu-id="85f86-215">Use [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para asociar una textura a una fase de muestra.</span><span class="sxs-lookup"><span data-stu-id="85f86-215">Use [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) to associate a texture with a sampler stage.</span></span>

<span data-ttu-id="85f86-216">En la tabla siguiente se incluyen todos los Estados de textura que establecen el estado del vértice:</span><span class="sxs-lookup"><span data-stu-id="85f86-216">The following table includes all the texture states that set-up vertex state:</span></span>



| <span data-ttu-id="85f86-217">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="85f86-217">Texture States</span></span>                | <span data-ttu-id="85f86-218">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="85f86-218">Default Value</span></span>    |
|-------------------------------|------------------|
| <span data-ttu-id="85f86-219">D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="85f86-219">D3DTSS\_TEXCOORDINDEX</span></span>         | <span data-ttu-id="85f86-220">0</span><span class="sxs-lookup"><span data-stu-id="85f86-220">0</span></span>                |
| <span data-ttu-id="85f86-221">D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="85f86-221">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span> | <span data-ttu-id="85f86-222">Deshabilitación de D3DTTFF \_</span><span class="sxs-lookup"><span data-stu-id="85f86-222">D3DTTFF\_DISABLE</span></span> |



 

<span data-ttu-id="85f86-223">D3DTSS \_ TEXCOORDINDEX es un estado de procesamiento de vértice de función fijo.</span><span class="sxs-lookup"><span data-stu-id="85f86-223">D3DTSS\_TEXCOORDINDEX is a fixed function vertex processing state.</span></span> <span data-ttu-id="85f86-224">Si se usa un sombreador de vértices programable, se omite este estado.</span><span class="sxs-lookup"><span data-stu-id="85f86-224">If a programmable vertex shader is used, this state is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85f86-225">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85f86-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85f86-226">Estado de guardado y restauración de bloques de estado</span><span class="sxs-lookup"><span data-stu-id="85f86-226">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
