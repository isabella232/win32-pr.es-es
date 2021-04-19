---
description: Los Estados de efecto se utilizan para inicializar los Estados de la canalización como preparación para el procesamiento de vértices y píxeles.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Estados de efectos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314768"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="bc6dc-103">Estados de efectos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="bc6dc-104">Los Estados de efecto se utilizan para inicializar los Estados de la canalización como preparación para el procesamiento de vértices y píxeles.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="bc6dc-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-105">Where:</span></span>

-   <span data-ttu-id="bc6dc-106">Estado del efecto: similar a los Estados de canalización de funciones fijas tradicionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="bc6dc-107">A continuación se proporciona una lista completa de Estados.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="bc6dc-108">\[\[ \] Índice \] de : Índice de entero opcional.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="bc6dc-109">El Índice identifica un estado determinado dentro de una matriz de Estados de efecto.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="bc6dc-110">Los corchetes externos indican que un índice es opcional.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="bc6dc-111">Si se usa un índice, asegúrese de usar los corchetes internos.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="bc6dc-112">expresión de asignación de estado de expresión.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-112">expression - State assignment expression.</span></span> <span data-ttu-id="bc6dc-113">Vea [expresiones (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="bc6dc-114">Cada Estado tiene un tipo de datos nativo.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-114">Each state has a native data type.</span></span> <span data-ttu-id="bc6dc-115">Este es el tipo de datos en el que el estado espera que los valores estén en cuando el efecto los asigna.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="bc6dc-116">A continuación se enumeran los tipos de datos que espera cada Estado.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="bc6dc-117">Tenga en cuenta que la interfaz de efecto intentará convertir los valores al tipo adecuado lo antes posible.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="bc6dc-118">Los valores literales se pueden convertir en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="bc6dc-119">Los no literales (es decir, las variables regulares) deben convertirse cuando se llama a los métodos de conjunto adecuados.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="bc6dc-120">Por ejemplo, la interfaz de efecto convertirá los valores establecidos mediante [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)y otras funciones similares, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="bc6dc-121">Para mejorar el rendimiento, asegúrese de que los valores que se pasan a la interfaz de efecto ya son del tipo correcto y no necesitan conversión.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="bc6dc-122">Si el tiempo de ejecución no puede convertir un valor, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="bc6dc-123">Los Estados de efecto se pueden dividir en las siguientes categorías:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="bc6dc-124">Estados claros</span><span class="sxs-lookup"><span data-stu-id="bc6dc-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="bc6dc-125">Estados de materiales</span><span class="sxs-lookup"><span data-stu-id="bc6dc-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="bc6dc-126">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="bc6dc-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="bc6dc-127">Estados de representación de canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="bc6dc-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="bc6dc-128">Estados de representación de canalización de vértices</span><span class="sxs-lookup"><span data-stu-id="bc6dc-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="bc6dc-129">Estados de muestra</span><span class="sxs-lookup"><span data-stu-id="bc6dc-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="bc6dc-130">Estados de la fase de muestra</span><span class="sxs-lookup"><span data-stu-id="bc6dc-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="bc6dc-131">Estados del sombreador</span><span class="sxs-lookup"><span data-stu-id="bc6dc-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="bc6dc-132">Estados de constantes del sombreador</span><span class="sxs-lookup"><span data-stu-id="bc6dc-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="bc6dc-133">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="bc6dc-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="bc6dc-134">Estados de la fase de textura</span><span class="sxs-lookup"><span data-stu-id="bc6dc-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="bc6dc-135">Estados de transformación</span><span class="sxs-lookup"><span data-stu-id="bc6dc-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="bc6dc-136">Estados claros</span><span class="sxs-lookup"><span data-stu-id="bc6dc-136">Light States</span></span>

<span data-ttu-id="bc6dc-137">Para permitir el mejor rendimiento para aplicar un efecto, se deben especificar todos los componentes de una luz o un material en el archivo de efectos.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="bc6dc-138">Indica que no se puede declarar que se establece en un valor predeterminado porque no hay ninguna manera de que Direct3D establezca los Estados de luz individualmente.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6dc-139">Estado claro</span><span class="sxs-lookup"><span data-stu-id="bc6dc-139">Light State</span></span>            | <span data-ttu-id="bc6dc-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-140">Type</span></span>   | <span data-ttu-id="bc6dc-141">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="bc6dc-142">LightAmbient \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="bc6dc-143">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-143">float4</span></span> | <span data-ttu-id="bc6dc-144">Vea el miembro de ambiente de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="bc6dc-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="bc6dc-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-146">float</span></span>  | <span data-ttu-id="bc6dc-147">Vea el miembro Attenuation0 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="bc6dc-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="bc6dc-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-149">float</span></span>  | <span data-ttu-id="bc6dc-150">Vea el miembro Attenuation1 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="bc6dc-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="bc6dc-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-152">float</span></span>  | <span data-ttu-id="bc6dc-153">Vea el miembro Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="bc6dc-154">LightDiffuse \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="bc6dc-155">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-155">float4</span></span> | <span data-ttu-id="bc6dc-156">Vea el miembro difuso de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="bc6dc-157">LightDirection \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="bc6dc-158">float3</span><span class="sxs-lookup"><span data-stu-id="bc6dc-158">float3</span></span> | <span data-ttu-id="bc6dc-159">Vea el miembro Direction de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="bc6dc-160">LightEnable \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="bc6dc-161">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-161">bool</span></span>   | <span data-ttu-id="bc6dc-162">**True** o **false**.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="bc6dc-163">Vea el argumento bEnable en [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="bc6dc-164">LightFalloff \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="bc6dc-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-165">float</span></span>  | <span data-ttu-id="bc6dc-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="bc6dc-167">Vea el miembro de difuminación de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="bc6dc-168">LightPhi \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="bc6dc-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-169">float</span></span>  | <span data-ttu-id="bc6dc-170">Vea el miembro de la PHI de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="bc6dc-171">LightPosition \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="bc6dc-172">float3</span><span class="sxs-lookup"><span data-stu-id="bc6dc-172">float3</span></span> | <span data-ttu-id="bc6dc-173">Vea el miembro Position de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="bc6dc-174">LightRange \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-174">LightRange\[n\]</span></span>        | <span data-ttu-id="bc6dc-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-175">float</span></span>  | <span data-ttu-id="bc6dc-176">Vea el miembro de intervalo de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="bc6dc-177">LightSpecular \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="bc6dc-178">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-178">float4</span></span> | <span data-ttu-id="bc6dc-179">Vea el miembro especular de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="bc6dc-180">LightTheta \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="bc6dc-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-181">float</span></span>  | <span data-ttu-id="bc6dc-182">Vea el miembro theta de [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="bc6dc-183">LightType \[ n\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-183">LightType\[n\]</span></span>         | <span data-ttu-id="bc6dc-184">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-184">dword</span></span>  | <span data-ttu-id="bc6dc-185">El mismo valor que la matriz de hasta n valores de [**D3DLIGHTTYPE**](./d3dlighttype.md) sin el \_ prefijo D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="bc6dc-186">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="bc6dc-187">Esto habilitará la iluminación, hará la iluminación puntual del tipo, establecerá la posición de la luz en float3<10.0 f, 1,0 f, 23.0 f> y establecerá el color ambiente en FLOAT4<0,7 f, 0.0 f, 0.0 f, 1,0 f>.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="bc6dc-188">Estados de materiales</span><span class="sxs-lookup"><span data-stu-id="bc6dc-188">Material States</span></span>

<span data-ttu-id="bc6dc-189">Indica que no se puede declarar que se establece en un valor predeterminado porque no hay ninguna manera de que Direct3D establezca los Estados de material de forma individual.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="bc6dc-190">Estado de materiales</span><span class="sxs-lookup"><span data-stu-id="bc6dc-190">Material State</span></span>   | <span data-ttu-id="bc6dc-191">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-191">Type</span></span>   | <span data-ttu-id="bc6dc-192">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-192">Values</span></span>                                         |
| <span data-ttu-id="bc6dc-193">MaterialAmbient</span><span class="sxs-lookup"><span data-stu-id="bc6dc-193">MaterialAmbient</span></span>  | <span data-ttu-id="bc6dc-194">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-194">float4</span></span> | <span data-ttu-id="bc6dc-195">Mismo valor que el [ **ambiente**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="bc6dc-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="bc6dc-196">MaterialDiffuse</span></span>  | <span data-ttu-id="bc6dc-197">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-197">float4</span></span> | <span data-ttu-id="bc6dc-198">El mismo valor que el [ **difuso**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="bc6dc-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="bc6dc-199">MaterialEmissive</span></span> | <span data-ttu-id="bc6dc-200">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-200">float4</span></span> | <span data-ttu-id="bc6dc-201">Mismo valor que [ **emisor**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="bc6dc-202">MaterialPower</span><span class="sxs-lookup"><span data-stu-id="bc6dc-202">MaterialPower</span></span>    | <span data-ttu-id="bc6dc-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-203">float</span></span>  | <span data-ttu-id="bc6dc-204">El mismo valor que [ **Power**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="bc6dc-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="bc6dc-205">MaterialSpecular</span></span> | <span data-ttu-id="bc6dc-206">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-206">float4</span></span> | <span data-ttu-id="bc6dc-207">Mismo valor que [ **especular**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="bc6dc-208">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="bc6dc-209">Esto establecerá el color difuso en FLOAT4<0,7 f, 0.0 f, 0.0 f, 1,0 f> y tomar la eficacia del material 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="bc6dc-210">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="bc6dc-210">Render States</span></span>

<span data-ttu-id="bc6dc-211">Hay dos tipos de Estados de representación:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="bc6dc-212">Estados de representación de canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="bc6dc-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="bc6dc-213">Estados de representación de canalización de vértices</span><span class="sxs-lookup"><span data-stu-id="bc6dc-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="bc6dc-214">Estados de representación de canalización de píxeles</span><span class="sxs-lookup"><span data-stu-id="bc6dc-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="bc6dc-215">Los Estados de representación del archivo de efectos tienen nombres similares a los Estados de canalización de funciones fijas, a menudo con el prefijo quitado.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc6dc-216">Estado de representación</span><span class="sxs-lookup"><span data-stu-id="bc6dc-216">Render State</span></span></td>
<td><span data-ttu-id="bc6dc-217">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-217">Type</span></span></td>
<td><span data-ttu-id="bc6dc-218">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-219">AlphaBlendEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="bc6dc-220">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-220">bool</span></span></td>
<td><span data-ttu-id="bc6dc-221">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-221">True or False.</span></span> <span data-ttu-id="bc6dc-222">Los mismos valores que D3DRS_ALPHABLENDENABLE en <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-223">AlphaFunc</span><span class="sxs-lookup"><span data-stu-id="bc6dc-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="bc6dc-224">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-224">dword</span></span></td>
<td><span data-ttu-id="bc6dc-225">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sin el prefijo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="bc6dc-226">Vea D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-227">AlphaRef</span><span class="sxs-lookup"><span data-stu-id="bc6dc-227">AlphaRef</span></span></td>
<td><span data-ttu-id="bc6dc-228">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-228">dword</span></span></td>
<td><span data-ttu-id="bc6dc-229">Los mismos valores que D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-230">AlphaTestEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="bc6dc-231">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-231">dword</span></span></td>
<td><span data-ttu-id="bc6dc-232">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-232">True or False.</span></span> <span data-ttu-id="bc6dc-233">Vea D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-234">BlendOp</span><span class="sxs-lookup"><span data-stu-id="bc6dc-234">BlendOp</span></span></td>
<td><span data-ttu-id="bc6dc-235">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-235">dword</span></span></td>
<td><span data-ttu-id="bc6dc-236">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> sin el prefijo D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-237">ColorWriteEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="bc6dc-238">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-238">dword</span></span></td>
<td><span data-ttu-id="bc6dc-239">Combinación bit a bit de rojo | VERDE | AZUL | Canal.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="bc6dc-240">Vea D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-241">DepthBias</span><span class="sxs-lookup"><span data-stu-id="bc6dc-241">DepthBias</span></span></td>
<td><span data-ttu-id="bc6dc-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-242">float</span></span></td>
<td><span data-ttu-id="bc6dc-243">Los mismos valores que D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-244">DestBlend</span><span class="sxs-lookup"><span data-stu-id="bc6dc-244">DestBlend</span></span></td>
<td><span data-ttu-id="bc6dc-245">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-245">dword</span></span></td>
<td><span data-ttu-id="bc6dc-246">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sin el prefijo D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-247">DitherEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-247">DitherEnable</span></span></td>
<td><span data-ttu-id="bc6dc-248">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-248">bool</span></span></td>
<td><span data-ttu-id="bc6dc-249">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-249">True or False.</span></span> <span data-ttu-id="bc6dc-250">Los mismos valores que D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-251">FillMode</span><span class="sxs-lookup"><span data-stu-id="bc6dc-251">FillMode</span></span></td>
<td><span data-ttu-id="bc6dc-252">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-252">dword</span></span></td>
<td><span data-ttu-id="bc6dc-253">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> sin el prefijo D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-254">LastPixel</span><span class="sxs-lookup"><span data-stu-id="bc6dc-254">LastPixel</span></span></td>
<td><span data-ttu-id="bc6dc-255">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-255">dword</span></span></td>
<td><span data-ttu-id="bc6dc-256">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-256">True or False.</span></span> <span data-ttu-id="bc6dc-257">Vea D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-258">ShadeMode</span><span class="sxs-lookup"><span data-stu-id="bc6dc-258">ShadeMode</span></span></td>
<td><span data-ttu-id="bc6dc-259">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-259">dword</span></span></td>
<td><span data-ttu-id="bc6dc-260">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sin el prefijo D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-261">SlopeScaleDepthBias</span><span class="sxs-lookup"><span data-stu-id="bc6dc-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="bc6dc-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-262">float</span></span></td>
<td><span data-ttu-id="bc6dc-263">Los mismos valores que D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-264">SrcBlend</span><span class="sxs-lookup"><span data-stu-id="bc6dc-264">SrcBlend</span></span></td>
<td><span data-ttu-id="bc6dc-265">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-265">dword</span></span></td>
<td><span data-ttu-id="bc6dc-266">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sin el prefijo D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-267">SRGBWriteEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="bc6dc-268">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-268">bool</span></span></td>
<td><span data-ttu-id="bc6dc-269">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-269">True or False.</span></span> <span data-ttu-id="bc6dc-270">Los mismos valores que D3DRS_SRGBWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-271">StencilEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-271">StencilEnable</span></span></td>
<td><span data-ttu-id="bc6dc-272">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-272">bool</span></span></td>
<td><span data-ttu-id="bc6dc-273">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-273">True or False.</span></span> <span data-ttu-id="bc6dc-274">Los mismos valores que D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-275">StencilFail</span><span class="sxs-lookup"><span data-stu-id="bc6dc-275">StencilFail</span></span></td>
<td><span data-ttu-id="bc6dc-276">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-276">dword</span></span></td>
<td><span data-ttu-id="bc6dc-277">Los mismos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sin el prefijo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="bc6dc-278">Vea D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-279">StencilFunc</span><span class="sxs-lookup"><span data-stu-id="bc6dc-279">StencilFunc</span></span></td>
<td><span data-ttu-id="bc6dc-280">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-280">dword</span></span></td>
<td><span data-ttu-id="bc6dc-281">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sin el prefijo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="bc6dc-282">Vea D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-283">StencilMask</span><span class="sxs-lookup"><span data-stu-id="bc6dc-283">StencilMask</span></span></td>
<td><span data-ttu-id="bc6dc-284">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-284">dword</span></span></td>
<td><span data-ttu-id="bc6dc-285">Los mismos valores que D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-286">StencilPass</span><span class="sxs-lookup"><span data-stu-id="bc6dc-286">StencilPass</span></span></td>
<td><span data-ttu-id="bc6dc-287">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-287">dword</span></span></td>
<td><span data-ttu-id="bc6dc-288">Los mismos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sin el prefijo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="bc6dc-289">Vea D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-290">StencilRef</span><span class="sxs-lookup"><span data-stu-id="bc6dc-290">StencilRef</span></span></td>
<td><span data-ttu-id="bc6dc-291">int</span><span class="sxs-lookup"><span data-stu-id="bc6dc-291">int</span></span></td>
<td><span data-ttu-id="bc6dc-292">Los mismos valores que D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-293">StencilWriteMask</span><span class="sxs-lookup"><span data-stu-id="bc6dc-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="bc6dc-294">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-294">dword</span></span></td>
<td><span data-ttu-id="bc6dc-295">Los mismos valores que D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-296">StencilZFail</span><span class="sxs-lookup"><span data-stu-id="bc6dc-296">StencilZFail</span></span></td>
<td><span data-ttu-id="bc6dc-297">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-297">dword</span></span></td>
<td><span data-ttu-id="bc6dc-298">Los mismos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sin el prefijo D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="bc6dc-299">Vea D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-300">TextureFactor</span><span class="sxs-lookup"><span data-stu-id="bc6dc-300">TextureFactor</span></span></td>
<td><span data-ttu-id="bc6dc-301">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-301">dword</span></span></td>
<td><span data-ttu-id="bc6dc-302">Los mismos valores que <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="bc6dc-303">Los mismos valores que D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-304">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="bc6dc-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="bc6dc-305">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-305">dword</span></span></td>
<td><span data-ttu-id="bc6dc-306">Los valores son los mismos que los utilizados por D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="bc6dc-307">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="bc6dc-308">COORD0 (que corresponde a D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="bc6dc-309">COORD1 (que corresponde a D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="bc6dc-310">COORD2 (que corresponde a D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="bc6dc-311">COORD3 (que corresponde a D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="bc6dc-312">U (que corresponde a D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="bc6dc-313">V (que corresponde a D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="bc6dc-314">W (que corresponde a D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="bc6dc-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-315">ZEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-315">ZEnable</span></span></td>
<td><span data-ttu-id="bc6dc-316">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-316">dword</span></span></td>
<td><span data-ttu-id="bc6dc-317">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> sin el prefijo D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc6dc-318">ZFunc</span><span class="sxs-lookup"><span data-stu-id="bc6dc-318">ZFunc</span></span></td>
<td><span data-ttu-id="bc6dc-319">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-319">dword</span></span></td>
<td><span data-ttu-id="bc6dc-320">Los mismos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sin el prefijo D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="bc6dc-321">Vea D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc6dc-322">ZWriteEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="bc6dc-323">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-323">bool</span></span></td>
<td><span data-ttu-id="bc6dc-324">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-324">True or False.</span></span> <span data-ttu-id="bc6dc-325">Vea D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bc6dc-326">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="bc6dc-327">Esto habilitará la combinación alfa y hará que todas las geometrías se representen en el alambre.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="bc6dc-328">Estados de representación de canalización de vértices</span><span class="sxs-lookup"><span data-stu-id="bc6dc-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="bc6dc-329">Los Estados de representación del archivo de efectos tienen nombres similares a los Estados de canalización de funciones fijas, a menudo con el prefijo quitado.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6dc-330">Estado de representación</span><span class="sxs-lookup"><span data-stu-id="bc6dc-330">Render State</span></span>             | <span data-ttu-id="bc6dc-331">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-331">Type</span></span>   | <span data-ttu-id="bc6dc-332">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-332">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="bc6dc-333">Ambiente</span><span class="sxs-lookup"><span data-stu-id="bc6dc-333">Ambient</span></span>                  | <span data-ttu-id="bc6dc-334">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-334">float4</span></span> | <span data-ttu-id="bc6dc-335">Los mismos valores que D3DRS \_ ambiente.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="bc6dc-336">AmbientMaterialSource</span><span class="sxs-lookup"><span data-stu-id="bc6dc-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="bc6dc-337">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-337">dword</span></span>  | <span data-ttu-id="bc6dc-338">Los mismos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el \_ prefijo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="bc6dc-339">Vea D3DRS \_ AMBIENTMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="bc6dc-340">Recorte</span><span class="sxs-lookup"><span data-stu-id="bc6dc-340">Clipping</span></span>                 | <span data-ttu-id="bc6dc-341">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-341">bool</span></span>   | <span data-ttu-id="bc6dc-342">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-342">True or False.</span></span> <span data-ttu-id="bc6dc-343">Los mismos valores que el \_ recorte D3DRS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="bc6dc-344">ClipPlaneEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="bc6dc-345">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-345">dword</span></span>  | <span data-ttu-id="bc6dc-346">Combinación bit a bit de las macros D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="bc6dc-347">Vea [**D3DCLIPPLANEn**](d3dclipplanen.md) y D3DRS \_ CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="bc6dc-348">ColorVertex</span><span class="sxs-lookup"><span data-stu-id="bc6dc-348">ColorVertex</span></span>              | <span data-ttu-id="bc6dc-349">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-349">bool</span></span>   | <span data-ttu-id="bc6dc-350">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-350">True or False.</span></span> <span data-ttu-id="bc6dc-351">Los mismos valores que D3DRS \_ COLORVERTEX.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="bc6dc-352">CullMode</span><span class="sxs-lookup"><span data-stu-id="bc6dc-352">CullMode</span></span>                 | <span data-ttu-id="bc6dc-353">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-353">dword</span></span>  | <span data-ttu-id="bc6dc-354">Los mismos valores que [**D3DCULL**](./d3dcull.md) sin el \_ prefijo D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="bc6dc-355">DiffuseMaterialSource</span><span class="sxs-lookup"><span data-stu-id="bc6dc-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="bc6dc-356">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-356">dword</span></span>  | <span data-ttu-id="bc6dc-357">Los mismos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el \_ prefijo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="bc6dc-358">Vea D3DRS \_ DIFFUSEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="bc6dc-359">EmissiveMaterialSource</span><span class="sxs-lookup"><span data-stu-id="bc6dc-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="bc6dc-360">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-360">dword</span></span>  | <span data-ttu-id="bc6dc-361">Los mismos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el \_ prefijo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="bc6dc-362">Vea D3DRS \_ EMISSIVEMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="bc6dc-363">FogColor</span><span class="sxs-lookup"><span data-stu-id="bc6dc-363">FogColor</span></span>                 | <span data-ttu-id="bc6dc-364">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-364">dword</span></span>  | <span data-ttu-id="bc6dc-365">Los mismos valores que [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="bc6dc-366">Vea D3DRS \_ FOGCOLOR.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="bc6dc-367">FogDensity</span><span class="sxs-lookup"><span data-stu-id="bc6dc-367">FogDensity</span></span>               | <span data-ttu-id="bc6dc-368">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-368">float</span></span>  | <span data-ttu-id="bc6dc-369">Los mismos valores que D3DRS \_ FOGDENSITY.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="bc6dc-370">FogEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-370">FogEnable</span></span>                | <span data-ttu-id="bc6dc-371">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-371">bool</span></span>   | <span data-ttu-id="bc6dc-372">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-372">True or False.</span></span> <span data-ttu-id="bc6dc-373">Los mismos valores que D3DRS \_ FOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="bc6dc-374">FogEnd</span><span class="sxs-lookup"><span data-stu-id="bc6dc-374">FogEnd</span></span>                   | <span data-ttu-id="bc6dc-375">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-375">float</span></span>  | <span data-ttu-id="bc6dc-376">Los mismos valores que D3DRS \_ FOGEND.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="bc6dc-377">FogStart</span><span class="sxs-lookup"><span data-stu-id="bc6dc-377">FogStart</span></span>                 | <span data-ttu-id="bc6dc-378">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-378">float</span></span>  | <span data-ttu-id="bc6dc-379">Los mismos valores que D3DRS \_ FOGSTART.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="bc6dc-380">FogTableMode</span><span class="sxs-lookup"><span data-stu-id="bc6dc-380">FogTableMode</span></span>             | <span data-ttu-id="bc6dc-381">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-381">dword</span></span>  | <span data-ttu-id="bc6dc-382">Los mismos valores que [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="bc6dc-383">Consulte D3DRS \_ FOGTABLEMODE en [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="bc6dc-384">FogVertexMode</span><span class="sxs-lookup"><span data-stu-id="bc6dc-384">FogVertexMode</span></span>            | <span data-ttu-id="bc6dc-385">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-385">dword</span></span>  | <span data-ttu-id="bc6dc-386">Los mismos valores que [**D3DFOGMODE**](./d3dfogmode.md) sin el \_ prefijo D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="bc6dc-387">IndexedVertexBlendEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="bc6dc-388">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-388">bool</span></span>   | <span data-ttu-id="bc6dc-389">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-389">True or False.</span></span> <span data-ttu-id="bc6dc-390">Los mismos valores que D3DRS \_ INDEXEDVERTEXBLENDENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="bc6dc-391">Iluminación</span><span class="sxs-lookup"><span data-stu-id="bc6dc-391">Lighting</span></span>                 | <span data-ttu-id="bc6dc-392">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-392">bool</span></span>   | <span data-ttu-id="bc6dc-393">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-393">True or False.</span></span> <span data-ttu-id="bc6dc-394">Los mismos valores que D3DRS \_ Lighting.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="bc6dc-395">LocalViewer</span><span class="sxs-lookup"><span data-stu-id="bc6dc-395">LocalViewer</span></span>              | <span data-ttu-id="bc6dc-396">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-396">bool</span></span>   | <span data-ttu-id="bc6dc-397">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-397">True or False.</span></span> <span data-ttu-id="bc6dc-398">Los mismos valores que D3DRS \_ LOCALVIEWER.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="bc6dc-399">MultiSampleAntialias</span><span class="sxs-lookup"><span data-stu-id="bc6dc-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="bc6dc-400">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-400">bool</span></span>   | <span data-ttu-id="bc6dc-401">Los mismos valores que D3DRS \_ MULTISAMPLEANTIALIAS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="bc6dc-402">MultiSampleMask</span><span class="sxs-lookup"><span data-stu-id="bc6dc-402">MultiSampleMask</span></span>          | <span data-ttu-id="bc6dc-403">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-403">dword</span></span>  | <span data-ttu-id="bc6dc-404">Los mismos valores que D3DRS \_ MULTISAMPLEMASK.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="bc6dc-405">NormalizeNormals</span><span class="sxs-lookup"><span data-stu-id="bc6dc-405">NormalizeNormals</span></span>         | <span data-ttu-id="bc6dc-406">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-406">bool</span></span>   | <span data-ttu-id="bc6dc-407">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-407">True or False.</span></span> <span data-ttu-id="bc6dc-408">Los mismos valores que D3DRS \_ NORMALIZENORMALS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="bc6dc-409">PatchSegments</span><span class="sxs-lookup"><span data-stu-id="bc6dc-409">PatchSegments</span></span>            | <span data-ttu-id="bc6dc-410">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-410">float</span></span>  | <span data-ttu-id="bc6dc-411">Los mismos valores que nSegments en [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="bc6dc-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="bc6dc-412">PointScale \_ A</span><span class="sxs-lookup"><span data-stu-id="bc6dc-412">PointScale\_A</span></span>            | <span data-ttu-id="bc6dc-413">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-413">float</span></span>  | <span data-ttu-id="bc6dc-414">Los mismos valores que D3DRS \_ POINTSCALE \_ A.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="bc6dc-415">PointScale \_ B</span><span class="sxs-lookup"><span data-stu-id="bc6dc-415">PointScale\_B</span></span>            | <span data-ttu-id="bc6dc-416">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-416">float</span></span>  | <span data-ttu-id="bc6dc-417">Los mismos valores que D3DRS \_ POINTSCALE \_ B.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="bc6dc-418">PointScale \_ C</span><span class="sxs-lookup"><span data-stu-id="bc6dc-418">PointScale\_C</span></span>            | <span data-ttu-id="bc6dc-419">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-419">float</span></span>  | <span data-ttu-id="bc6dc-420">Los mismos valores que D3DRS \_ POINTSCALE \_ C.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="bc6dc-421">PointScaleEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-421">PointScaleEnable</span></span>         | <span data-ttu-id="bc6dc-422">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-422">bool</span></span>   | <span data-ttu-id="bc6dc-423">Los mismos valores que D3DRS \_ POINTSCALEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="bc6dc-424">PointSize</span><span class="sxs-lookup"><span data-stu-id="bc6dc-424">PointSize</span></span>                | <span data-ttu-id="bc6dc-425">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-425">float</span></span>  | <span data-ttu-id="bc6dc-426">Los mismos valores que D3DRS \_ .</span><span class="sxs-lookup"><span data-stu-id="bc6dc-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="bc6dc-427">Puntuación \_ mínima</span><span class="sxs-lookup"><span data-stu-id="bc6dc-427">PointSize\_Min</span></span>           | <span data-ttu-id="bc6dc-428">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-428">float</span></span>  | <span data-ttu-id="bc6dc-429">Los mismos valores que D3DRS se \_ puntuación \_ min.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="bc6dc-430">Puntuación \_ máxima</span><span class="sxs-lookup"><span data-stu-id="bc6dc-430">PointSize\_Max</span></span>           | <span data-ttu-id="bc6dc-431">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-431">float</span></span>  | <span data-ttu-id="bc6dc-432">Los mismos valores que D3DRSan \_ \_ Max sin el \_ prefijo D3DRS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="bc6dc-433">PointSpriteEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-433">PointSpriteEnable</span></span>        | <span data-ttu-id="bc6dc-434">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-434">bool</span></span>   | <span data-ttu-id="bc6dc-435">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-435">True or False.</span></span> <span data-ttu-id="bc6dc-436">Los mismos valores que D3DRS \_ POINTSPRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="bc6dc-437">RangeFogEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-437">RangeFogEnable</span></span>           | <span data-ttu-id="bc6dc-438">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-438">bool</span></span>   | <span data-ttu-id="bc6dc-439">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-439">True or False.</span></span> <span data-ttu-id="bc6dc-440">Los mismos valores que D3DRS \_ RANGEFOGENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="bc6dc-441">SpecularEnable</span><span class="sxs-lookup"><span data-stu-id="bc6dc-441">SpecularEnable</span></span>           | <span data-ttu-id="bc6dc-442">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-442">bool</span></span>   | <span data-ttu-id="bc6dc-443">True o False.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-443">True or False.</span></span> <span data-ttu-id="bc6dc-444">Los mismos valores que D3DRS \_ SPECULARENABLE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="bc6dc-445">SpecularMaterialSource</span><span class="sxs-lookup"><span data-stu-id="bc6dc-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="bc6dc-446">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-446">dword</span></span>  | <span data-ttu-id="bc6dc-447">Los mismos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sin el \_ prefijo D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="bc6dc-448">Vea D3DRS \_ SPECULARMATERIALSOURCE.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="bc6dc-449">TweenFactor</span><span class="sxs-lookup"><span data-stu-id="bc6dc-449">TweenFactor</span></span>              | <span data-ttu-id="bc6dc-450">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-450">float</span></span>  | <span data-ttu-id="bc6dc-451">Los mismos valores que D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="bc6dc-452">VertexBlend</span><span class="sxs-lookup"><span data-stu-id="bc6dc-452">VertexBlend</span></span>              | <span data-ttu-id="bc6dc-453">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-453">dword</span></span>  | <span data-ttu-id="bc6dc-454">Los mismos valores que [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sin el \_ prefijo D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="bc6dc-455">Vea D3DRS \_ VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="bc6dc-456">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="bc6dc-457">Esto hará que el color ambiente FLOAT4<0,7 f, 0.0 f, 0.0 f, 1,0 f>, establezca el modo de selección de la cara del aire en el sentido contrario a las agujas del reloj y establezca el color de niebla en rojo.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="bc6dc-458">Estados de muestra</span><span class="sxs-lookup"><span data-stu-id="bc6dc-458">Sampler States</span></span>

<span data-ttu-id="bc6dc-459">Un estado de muestra representa un objeto de muestra.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-459">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="bc6dc-460">State</span><span class="sxs-lookup"><span data-stu-id="bc6dc-460">State</span></span>   | <span data-ttu-id="bc6dc-461">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-461">Type</span></span>    | <span data-ttu-id="bc6dc-462">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-462">Values</span></span>                              |
| <span data-ttu-id="bc6dc-463">Muestra</span><span class="sxs-lookup"><span data-stu-id="bc6dc-463">Sampler</span></span> | <span data-ttu-id="bc6dc-464">muestras</span><span class="sxs-lookup"><span data-stu-id="bc6dc-464">sampler</span></span> | <span data-ttu-id="bc6dc-465">**Null** o un bloque de estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="bc6dc-466">Estados de la fase de muestra</span><span class="sxs-lookup"><span data-stu-id="bc6dc-466">Sampler Stage States</span></span>

<span data-ttu-id="bc6dc-467">Los Estados de la fase de muestra se utilizan para muestrear las texturas.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="bc6dc-468">El estado de muestra determina los tipos de filtrado y los modos de direccionamiento de textura.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-468">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6dc-469">Estado de muestra</span><span class="sxs-lookup"><span data-stu-id="bc6dc-469">Sampler State</span></span>       | <span data-ttu-id="bc6dc-470">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-470">Type</span></span>                         | <span data-ttu-id="bc6dc-471">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-471">Values</span></span>                                                                                                                            |
| <span data-ttu-id="bc6dc-472">AddressU \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-472">AddressU\[16\]</span></span>      | <span data-ttu-id="bc6dc-473">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-473">dword</span></span>                        | <span data-ttu-id="bc6dc-474">Los mismos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el \_ prefijo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="bc6dc-475">Vea D3DSAMP \_ ADDRESSU.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="bc6dc-476">AddressV \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-476">AddressV\[16\]</span></span>      | <span data-ttu-id="bc6dc-477">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-477">dword</span></span>                        | <span data-ttu-id="bc6dc-478">Los mismos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el \_ prefijo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="bc6dc-479">Vea D3DSAMP \_ ADDRESSV.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="bc6dc-480">AddressW \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-480">AddressW\[16\]</span></span>      | <span data-ttu-id="bc6dc-481">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-481">dword</span></span>                        | <span data-ttu-id="bc6dc-482">Los mismos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sin el \_ prefijo D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="bc6dc-483">Vea D3DSAMP \_ ADDRESSW.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="bc6dc-484">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="bc6dc-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="bc6dc-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="bc6dc-486">Los mismos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sin el \_ prefijo D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="bc6dc-487">Vea D3DSAMP \_ BORDERCOLOR.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="bc6dc-488">MagFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="bc6dc-489">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-489">dword</span></span>                        | <span data-ttu-id="bc6dc-490">Los mismos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sin el \_ prefijo D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="bc6dc-491">Vea D3DSAMP \_ MAGFILTER.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="bc6dc-492">MaxAnisotropy \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="bc6dc-493">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-493">dword</span></span>                        | <span data-ttu-id="bc6dc-494">Los mismos valores que D3DSAMP \_ MAXANISOTROPY sin el \_ prefijo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="bc6dc-495">MaxMipLevel \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="bc6dc-496">int</span><span class="sxs-lookup"><span data-stu-id="bc6dc-496">int</span></span>                          | <span data-ttu-id="bc6dc-497">Los mismos valores que D3DSAMP \_ MAXMIPLEVEL sin el \_ prefijo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="bc6dc-498">MinFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="bc6dc-499">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-499">dword</span></span>                        | <span data-ttu-id="bc6dc-500">Los mismos valores que D3DSAMP \_ MINFILTER sin el \_ prefijo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="bc6dc-501">MipFilter \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="bc6dc-502">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-502">dword</span></span>                        | <span data-ttu-id="bc6dc-503">Los mismos valores que D3DSAMP \_ MIPFILTER sin el \_ prefijo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="bc6dc-504">MipMapLodBias \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="bc6dc-505">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-505">float</span></span>                        | <span data-ttu-id="bc6dc-506">Los mismos valores que D3DSAMP \_ MIPMAPLODBIAS sin el \_ prefijo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="bc6dc-507">SRGBTexture</span><span class="sxs-lookup"><span data-stu-id="bc6dc-507">SRGBTexture</span></span>         | <span data-ttu-id="bc6dc-508">bool</span><span class="sxs-lookup"><span data-stu-id="bc6dc-508">bool</span></span>                         | <span data-ttu-id="bc6dc-509">El mismo valor que D3DSAMP \_ SRGBTEXTURE sin el \_ prefijo D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="bc6dc-510">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="bc6dc-511">Esto fija los valores de UVW para que estén entre 0 y 1.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="bc6dc-512">Estados del sombreador</span><span class="sxs-lookup"><span data-stu-id="bc6dc-512">Shader States</span></span>

<span data-ttu-id="bc6dc-513">Solo hay dos Estados de sombreador de efectos: uno asociado a un objeto de sombreador de vértices y el otro asociado a un objeto de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="bc6dc-514">Estado del sombreador</span><span class="sxs-lookup"><span data-stu-id="bc6dc-514">Shader State</span></span> | <span data-ttu-id="bc6dc-515">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-515">Type</span></span>         | <span data-ttu-id="bc6dc-516">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-516">Values</span></span>                                                                      |
| <span data-ttu-id="bc6dc-517">U</span><span class="sxs-lookup"><span data-stu-id="bc6dc-517">PixelShader</span></span>  | <span data-ttu-id="bc6dc-518">u</span><span class="sxs-lookup"><span data-stu-id="bc6dc-518">pixelshader</span></span>  | <span data-ttu-id="bc6dc-519">**Null**, un bloque de ensamblado, un destino de compilación o un parámetro de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="bc6dc-520">VertexShader</span><span class="sxs-lookup"><span data-stu-id="bc6dc-520">VertexShader</span></span> | <span data-ttu-id="bc6dc-521">vertexshader</span><span class="sxs-lookup"><span data-stu-id="bc6dc-521">vertexshader</span></span> | <span data-ttu-id="bc6dc-522">**Null**, un bloque de ensamblado, un destino de compilación o un parámetro de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="bc6dc-523">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="bc6dc-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="bc6dc-524">Esto compilará VSTexture, un sombreador de vértices definido anteriormente en el archivo. FX, en la versión 1,1 del sombreador de vértices y, a continuación, establecerá ese sombreador compilado como sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="bc6dc-525">El sombreador de píxeles se asigna a **null**.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="bc6dc-526">Estados de constantes del sombreador</span><span class="sxs-lookup"><span data-stu-id="bc6dc-526">Shader Constant States</span></span>

<span data-ttu-id="bc6dc-527">Los Estados de constantes del sombreador se usan para tener acceso a los parámetros constantes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-527">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="bc6dc-528">Estado constante del sombreador</span><span class="sxs-lookup"><span data-stu-id="bc6dc-528">Shader Constant State</span></span> | <span data-ttu-id="bc6dc-529">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-529">Type</span></span>            | <span data-ttu-id="bc6dc-530">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-530">Values</span></span>                                       |
| <span data-ttu-id="bc6dc-531">PixelShaderConstant</span><span class="sxs-lookup"><span data-stu-id="bc6dc-531">PixelShaderConstant</span></span>   | <span data-ttu-id="bc6dc-532">Float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="bc6dc-533">m x n matriz de flotantes; m y n son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="bc6dc-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="bc6dc-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="bc6dc-535">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-535">float4</span></span>          | <span data-ttu-id="bc6dc-536">Un valor de 4D float.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-536">One 4D float.</span></span>                                |
| <span data-ttu-id="bc6dc-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="bc6dc-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="bc6dc-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="bc6dc-538">float4x2</span></span>        | <span data-ttu-id="bc6dc-539">Dos floats de 4D.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="bc6dc-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="bc6dc-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="bc6dc-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="bc6dc-541">float4x3</span></span>        | <span data-ttu-id="bc6dc-542">Tres flotantes de 4D.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="bc6dc-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="bc6dc-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-544">float4x4</span></span>        | <span data-ttu-id="bc6dc-545">Cuatro flotantes de 4D.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="bc6dc-546">PixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="bc6dc-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="bc6dc-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="bc6dc-548">matriz de booleanos de m x n; m y n son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="bc6dc-549">PixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="bc6dc-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="bc6dc-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="bc6dc-551">matriz de ints m x n.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-551">m x n array of ints.</span></span> <span data-ttu-id="bc6dc-552">m y n son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-552">m and n are optional.</span></span>   |
| <span data-ttu-id="bc6dc-553">PixelShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="bc6dc-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="bc6dc-554">Float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="bc6dc-555">m x n matriz de flotantes.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-555">m x n array of floats.</span></span> <span data-ttu-id="bc6dc-556">m y n son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-556">m and n are optional.</span></span> |
| <span data-ttu-id="bc6dc-557">VertexShaderConstant</span><span class="sxs-lookup"><span data-stu-id="bc6dc-557">VertexShaderConstant</span></span>  | <span data-ttu-id="bc6dc-558">Float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="bc6dc-559">m x n matriz de flotantes.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-559">m x n array of floats.</span></span> <span data-ttu-id="bc6dc-560">m y n son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-560">m and n are optional.</span></span> |
| <span data-ttu-id="bc6dc-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="bc6dc-561">VertexShaderConstant1</span></span> | <span data-ttu-id="bc6dc-562">float4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-562">float4</span></span>          | <span data-ttu-id="bc6dc-563">Un valor de 4D float.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-563">One 4D float.</span></span>                                |
| <span data-ttu-id="bc6dc-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="bc6dc-564">VertexShaderConstant2</span></span> | <span data-ttu-id="bc6dc-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="bc6dc-565">float4x2</span></span>        | <span data-ttu-id="bc6dc-566">Dos floats de 4D.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="bc6dc-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="bc6dc-567">VertexShaderConstant3</span></span> | <span data-ttu-id="bc6dc-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="bc6dc-568">float4x3</span></span>        | <span data-ttu-id="bc6dc-569">Tres flotantes de 4D.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="bc6dc-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-570">VertexShaderConstant4</span></span> | <span data-ttu-id="bc6dc-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-571">float4x4</span></span>        | <span data-ttu-id="bc6dc-572">Cuatro flotantes de 4D.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="bc6dc-573">VertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="bc6dc-573">VertexShaderConstantB</span></span> | <span data-ttu-id="bc6dc-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="bc6dc-575">matriz de booleanos de m x n.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-575">m x n array of bools.</span></span> <span data-ttu-id="bc6dc-576">m y n son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-576">m and n are optional.</span></span>  |
| <span data-ttu-id="bc6dc-577">VertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="bc6dc-577">VertexShaderConstantI</span></span> | <span data-ttu-id="bc6dc-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="bc6dc-579">matriz de ints m x n.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-579">m x n array of ints.</span></span> <span data-ttu-id="bc6dc-580">m y n son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-580">m and n are optional.</span></span>   |
| <span data-ttu-id="bc6dc-581">VertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="bc6dc-581">VertexShaderConstantF</span></span> | <span data-ttu-id="bc6dc-582">Float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="bc6dc-583">m x n matriz de flotantes.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-583">m x n array of floats.</span></span> <span data-ttu-id="bc6dc-584">m y n son opcionales.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="bc6dc-585">Estados de textura</span><span class="sxs-lookup"><span data-stu-id="bc6dc-585">Texture States</span></span>

<span data-ttu-id="bc6dc-586">Los Estados de textura inicializan las texturas utilizadas por el mezclador multitexture.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-586">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="bc6dc-587">Estado de textura</span><span class="sxs-lookup"><span data-stu-id="bc6dc-587">Texture State</span></span> | <span data-ttu-id="bc6dc-588">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-588">Type</span></span>    | <span data-ttu-id="bc6dc-589">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-589">Values</span></span>                            |
| <span data-ttu-id="bc6dc-590">Textura \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-590">Texture\[8\]</span></span>  | <span data-ttu-id="bc6dc-591">textura</span><span class="sxs-lookup"><span data-stu-id="bc6dc-591">texture</span></span> | <span data-ttu-id="bc6dc-592">**Null** o un parámetro de textura.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="bc6dc-593">Estados de la fase de textura</span><span class="sxs-lookup"><span data-stu-id="bc6dc-593">Texture Stage States</span></span>

<span data-ttu-id="bc6dc-594">Los Estados de la fase de textura establecen texturas y las fases de textura en el mezclador multitextura.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6dc-595">Estado de la fase de textura</span><span class="sxs-lookup"><span data-stu-id="bc6dc-595">Texture Stage State</span></span>        | <span data-ttu-id="bc6dc-596">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-596">Type</span></span>  | <span data-ttu-id="bc6dc-597">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-597">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="bc6dc-598">AlphaOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="bc6dc-599">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-599">dword</span></span> | <span data-ttu-id="bc6dc-600">Igual que [**D3DTEXTUREOP**](./d3dtextureop.md) sin el \_ prefijo D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="bc6dc-601">Vea D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="bc6dc-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="bc6dc-603">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-603">dword</span></span> | <span data-ttu-id="bc6dc-604">Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bc6dc-605">Vea D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="bc6dc-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="bc6dc-607">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-607">dword</span></span> | <span data-ttu-id="bc6dc-608">Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bc6dc-609">Vea D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="bc6dc-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="bc6dc-611">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-611">dword</span></span> | <span data-ttu-id="bc6dc-612">Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bc6dc-613">Vea D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="bc6dc-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="bc6dc-615">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-615">dword</span></span> | <span data-ttu-id="bc6dc-616">Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bc6dc-617">Vea D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="bc6dc-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="bc6dc-619">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-619">dword</span></span> | <span data-ttu-id="bc6dc-620">Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bc6dc-621">Vea D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="bc6dc-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="bc6dc-623">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-623">dword</span></span> | <span data-ttu-id="bc6dc-624">Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bc6dc-625">Vea D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="bc6dc-626">ColorOp \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="bc6dc-627">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-627">dword</span></span> | <span data-ttu-id="bc6dc-628">Igual que [**D3DTEXTUREOP**](./d3dtextureop.md) sin el \_ prefijo D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="bc6dc-629">Vea D3DTSS \_ COLOROP.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="bc6dc-630">BumpEnvLScale \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="bc6dc-631">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-631">float</span></span> | <span data-ttu-id="bc6dc-632">Los mismos valores que D3DTSS \_ BUMPENVLSCALE sin el \_ prefijo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="bc6dc-633">BumpEnvLOffset \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="bc6dc-634">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-634">float</span></span> | <span data-ttu-id="bc6dc-635">Los mismos valores que D3DTSS \_ BUMPENVLOFFSET sin el \_ prefijo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="bc6dc-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="bc6dc-637">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-637">float</span></span> | <span data-ttu-id="bc6dc-638">Los mismos valores que D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="bc6dc-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="bc6dc-640">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-640">float</span></span> | <span data-ttu-id="bc6dc-641">Los mismos valores que D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="bc6dc-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="bc6dc-643">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-643">float</span></span> | <span data-ttu-id="bc6dc-644">Los mismos valores que D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="bc6dc-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="bc6dc-646">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bc6dc-646">float</span></span> | <span data-ttu-id="bc6dc-647">Los mismos valores que D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="bc6dc-648">ResultArg \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="bc6dc-649">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-649">dword</span></span> | <span data-ttu-id="bc6dc-650">Igual que [D3DTA](d3dta.md) sin el \_ prefijo D3DTA.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="bc6dc-651">Vea D3DTSS \_ RESULTARG.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="bc6dc-652">TexCoordIndex \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="bc6dc-653">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-653">dword</span></span> | <span data-ttu-id="bc6dc-654">Los mismos valores que D3DTSS \_ TEXCOORDINDEX sin el \_ prefijo D3DTSS TCI.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="bc6dc-655">TextureTransformFlags \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="bc6dc-656">dword</span><span class="sxs-lookup"><span data-stu-id="bc6dc-656">dword</span></span> | <span data-ttu-id="bc6dc-657">Los mismos valores que los valores de [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) sin el \_ prefijo D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="bc6dc-658">Vea D3DTSS \_ TEXTURETRANSFORMFLAGS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="bc6dc-659">Estados de transformación</span><span class="sxs-lookup"><span data-stu-id="bc6dc-659">Transform States</span></span>

<span data-ttu-id="bc6dc-660">Establezca los Estados de transformación para inicializar las matrices de transformación.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="bc6dc-661">Los efectos usan matrices transpuestas para mejorar la eficacia.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="bc6dc-662">Puede proporcionar matrices transpuestas a un efecto o un efecto transformará automáticamente las matrices antes de utilizarlas.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc6dc-663">Estado de transformación</span><span class="sxs-lookup"><span data-stu-id="bc6dc-663">Transform State</span></span>       | <span data-ttu-id="bc6dc-664">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc6dc-664">Type</span></span>     | <span data-ttu-id="bc6dc-665">Valores</span><span class="sxs-lookup"><span data-stu-id="bc6dc-665">Values</span></span>                                                                                                                          |
| <span data-ttu-id="bc6dc-666">ProjectionTransform</span><span class="sxs-lookup"><span data-stu-id="bc6dc-666">ProjectionTransform</span></span>   | <span data-ttu-id="bc6dc-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-667">float4x4</span></span> | <span data-ttu-id="bc6dc-668">Matriz 4x4 de flotantes.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="bc6dc-669">Los mismos valores que \_ la proyección D3DTS sin el \_ prefijo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="bc6dc-670">TextureTransform \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="bc6dc-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="bc6dc-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-671">float4x4</span></span> | <span data-ttu-id="bc6dc-672">Matriz 4x4 de flotantes.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="bc6dc-673">Los mismos valores que [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sin el \_ prefijo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="bc6dc-674">ViewTransform</span><span class="sxs-lookup"><span data-stu-id="bc6dc-674">ViewTransform</span></span>         | <span data-ttu-id="bc6dc-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-675">float4x4</span></span> | <span data-ttu-id="bc6dc-676">Matriz 4x4 de flotantes.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="bc6dc-677">Los mismos valores que D3DTS \_ vista sin el \_ prefijo D3DTS.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="bc6dc-678">WorldTransform</span><span class="sxs-lookup"><span data-stu-id="bc6dc-678">WorldTransform</span></span>        | <span data-ttu-id="bc6dc-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="bc6dc-679">float4x4</span></span> | <span data-ttu-id="bc6dc-680">Matriz 4x4 de flotantes.</span><span class="sxs-lookup"><span data-stu-id="bc6dc-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="bc6dc-681">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc6dc-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc6dc-682">Formato de efecto</span><span class="sxs-lookup"><span data-stu-id="bc6dc-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
