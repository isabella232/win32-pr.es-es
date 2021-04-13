---
description: Use la colección SasHostParameterValue para definir la colección de valores de la aplicación host, así como sus tipos y miembros, expuestos a efectos.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Enlace de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104359907"
---
# <a name="data-binding"></a><span data-ttu-id="3a18a-103">Enlace de datos</span><span class="sxs-lookup"><span data-stu-id="3a18a-103">Data Binding</span></span>

<span data-ttu-id="3a18a-104">Use la [colección SasHostParameterValue](#sashostparametervalue-collection) para definir la colección de valores de la aplicación host, así como sus tipos y miembros, expuestos a efectos.</span><span class="sxs-lookup"><span data-stu-id="3a18a-104">Use [SasHostParameterValue Collection](#sashostparametervalue-collection) to define the collection of host application values, as well as their type and members, exposed to effects.</span></span> <span data-ttu-id="3a18a-105">Use la anotación [SasBindAddress](#sasbindaddress) en un archivo de efectos para asociar un parámetro de efecto a su parámetro correspondiente en la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="3a18a-105">Use the [SasBindAddress](#sasbindaddress) annotation in an effect file to associate an effect parameter with its corresponding parameter in the host application.</span></span>

## <a name="sashostparametervalue-collection"></a><span data-ttu-id="3a18a-106">Colección SasHostParameterValue</span><span class="sxs-lookup"><span data-stu-id="3a18a-106">SasHostParameterValue Collection</span></span>

<span data-ttu-id="3a18a-107">SasHostParameterValue se define mediante la sintaxis de archivo de efectos (. FX).</span><span class="sxs-lookup"><span data-stu-id="3a18a-107">The SasHostParameterValue is defined using effect file (.fx) syntax.</span></span> <span data-ttu-id="3a18a-108">Aunque la sintaxis es muy similar a la sintaxis del archivo de efectos, existen algunas diferencias.</span><span class="sxs-lookup"><span data-stu-id="3a18a-108">While the syntax is very similar to the effect file syntax, some differences exist.</span></span> <span data-ttu-id="3a18a-109">Por ejemplo, los tipos de objeto, como texture2d, muestreadores y cadenas, no son válidos en los archivos de efectos reales, sino que son válidos en SasHostParameterValue.</span><span class="sxs-lookup"><span data-stu-id="3a18a-109">For example, object types, such as texture2d, samplers, and strings, are not valid in actual effect files, but are valid in the SasHostParameterValue.</span></span> <span data-ttu-id="3a18a-110">Una aplicación host puede implementar SasHostParameterValue de cualquier manera, siempre y cuando se ajuste a la descripción siguiente; la definición real se encuentra en el archivo de inclusión del efecto estándar DXSAS (/Utilities/Source/SAS/SAS.fxh de la \[ raíz del SDK \] ).</span><span class="sxs-lookup"><span data-stu-id="3a18a-110">A host application can implement SasHostParameterValue in any way so long as it conforms to the description below; the actual definition is located in the DXSAS standard effect include file (\[SDK Root\]/Utilities/Source/Sas/Sas.fxh).</span></span>

<span data-ttu-id="3a18a-111">Tenga en cuenta que las matrices de SasHostParameterValue, como las luces o las cámaras, tienen una longitud sin enlazar.</span><span class="sxs-lookup"><span data-stu-id="3a18a-111">Note that arrays in the SasHostParameterValue such as Lights or Cameras have unbounded length.</span></span> <span data-ttu-id="3a18a-112">Esto significa que los efectos se pueden enlazar a cualquier índice arbitrario de esas matrices y las aplicaciones host deben proporcionar valores predeterminados significativos en los casos en los que no se puede proporcionar ningún valor de aplicación.</span><span class="sxs-lookup"><span data-stu-id="3a18a-112">This means that effects can bind to any arbitrary index in those arrays and host applications must provide meaningful defaults in the cases where no application value can be provided.</span></span>

<span data-ttu-id="3a18a-113">Algunos tipos y constantes deben definirse en el estándar DXSAS, como se indica en la definición de la inclusión estándar.</span><span class="sxs-lookup"><span data-stu-id="3a18a-113">Some types and constants are required to be defined in the DXSAS standard include, as noted in the definition of the standard include.</span></span> <span data-ttu-id="3a18a-114">Esto permite que los efectos enlacen fácilmente los valores agregados de SasHostParameterValue a los parámetros de efectos estructurados.</span><span class="sxs-lookup"><span data-stu-id="3a18a-114">This allows effects to easily bind aggregated values from the SasHostParameterValue to structured effect parameters.</span></span>



| <span data-ttu-id="3a18a-115">Colección SasHostParameterValue</span><span class="sxs-lookup"><span data-stu-id="3a18a-115">SasHostParameterValue Collection</span></span>    | <span data-ttu-id="3a18a-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="3a18a-116">Type</span></span>            | <span data-ttu-id="3a18a-117">Miembro</span><span class="sxs-lookup"><span data-stu-id="3a18a-117">Member</span></span>                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [<span data-ttu-id="3a18a-118">Time</span><span class="sxs-lookup"><span data-stu-id="3a18a-118">Time</span></span>](#time)                       | <span data-ttu-id="3a18a-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3a18a-119">float</span></span>           | <span data-ttu-id="3a18a-120">SAS. Time. Now</span><span class="sxs-lookup"><span data-stu-id="3a18a-120">Sas.Time.Now</span></span>                                 |
|                                     | <span data-ttu-id="3a18a-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3a18a-121">float</span></span>           | <span data-ttu-id="3a18a-122">SAS. Time. Last</span><span class="sxs-lookup"><span data-stu-id="3a18a-122">Sas.Time.Last</span></span>                                |
|                                     | <span data-ttu-id="3a18a-123">int</span><span class="sxs-lookup"><span data-stu-id="3a18a-123">int</span></span>             | <span data-ttu-id="3a18a-124">SAS. Time. Númeromarco</span><span class="sxs-lookup"><span data-stu-id="3a18a-124">Sas.Time.FrameNumber</span></span>                         |
| [<span data-ttu-id="3a18a-125">Mapa de entorno</span><span class="sxs-lookup"><span data-stu-id="3a18a-125">Environment Map</span></span>](#environment-map) | <span data-ttu-id="3a18a-126">textureCUBE</span><span class="sxs-lookup"><span data-stu-id="3a18a-126">textureCUBE</span></span>     | <span data-ttu-id="3a18a-127">SAS. EnvironmentMap</span><span class="sxs-lookup"><span data-stu-id="3a18a-127">Sas.EnvironmentMap</span></span>                           |
| [<span data-ttu-id="3a18a-128">Cámara</span><span class="sxs-lookup"><span data-stu-id="3a18a-128">Camera</span></span>](#camera)                   | <span data-ttu-id="3a18a-129">SasCamera</span><span class="sxs-lookup"><span data-stu-id="3a18a-129">SasCamera</span></span>       | <span data-ttu-id="3a18a-130">SAS. Camera</span><span class="sxs-lookup"><span data-stu-id="3a18a-130">Sas.Camera</span></span>                                   |
|                                     | <span data-ttu-id="3a18a-131">float4x4</span><span class="sxs-lookup"><span data-stu-id="3a18a-131">float4x4</span></span>        | <span data-ttu-id="3a18a-132">SAS. Camera. WorldToView</span><span class="sxs-lookup"><span data-stu-id="3a18a-132">Sas.Camera.WorldToView</span></span>                       |
|                                     | <span data-ttu-id="3a18a-133">float4x4</span><span class="sxs-lookup"><span data-stu-id="3a18a-133">float4x4</span></span>        | <span data-ttu-id="3a18a-134">SAS. Camera. Projection</span><span class="sxs-lookup"><span data-stu-id="3a18a-134">Sas.Camera.Projection</span></span>                        |
|                                     | <span data-ttu-id="3a18a-135">float2</span><span class="sxs-lookup"><span data-stu-id="3a18a-135">float2</span></span>          | <span data-ttu-id="3a18a-136">SAS. Camera. NearFarClipping</span><span class="sxs-lookup"><span data-stu-id="3a18a-136">Sas.Camera.NearFarClipping</span></span>                   |
| [<span data-ttu-id="3a18a-137">Claro</span><span class="sxs-lookup"><span data-stu-id="3a18a-137">Light</span></span>](#light)                     | <span data-ttu-id="3a18a-138">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="3a18a-138">SasAmbientLight</span></span> | <span data-ttu-id="3a18a-139">AmbientLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="3a18a-139">AmbientLight\[ZeroOrMore\];</span></span>                  |
|                                     | <span data-ttu-id="3a18a-140">int</span><span class="sxs-lookup"><span data-stu-id="3a18a-140">int</span></span>             | <span data-ttu-id="3a18a-141">SAS. NumAmbientLights</span><span class="sxs-lookup"><span data-stu-id="3a18a-141">Sas.NumAmbientLights</span></span>                         |
|                                     | <span data-ttu-id="3a18a-142">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="3a18a-142">SasAmbientLight</span></span> | <span data-ttu-id="3a18a-143">DirectionalLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="3a18a-143">DirectionalLight\[ZeroOrMore\];</span></span>              |
|                                     | <span data-ttu-id="3a18a-144">int</span><span class="sxs-lookup"><span data-stu-id="3a18a-144">int</span></span>             | <span data-ttu-id="3a18a-145">SAS. NumDirectionalLights</span><span class="sxs-lookup"><span data-stu-id="3a18a-145">Sas.NumDirectionalLights</span></span>                     |
|                                     | <span data-ttu-id="3a18a-146">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="3a18a-146">SasAmbientLight</span></span> | <span data-ttu-id="3a18a-147">PointLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="3a18a-147">PointLight\[ZeroOrMore\];</span></span>                    |
|                                     | <span data-ttu-id="3a18a-148">int</span><span class="sxs-lookup"><span data-stu-id="3a18a-148">int</span></span>             | <span data-ttu-id="3a18a-149">SAS. NumPointLights</span><span class="sxs-lookup"><span data-stu-id="3a18a-149">Sas.NumPointLights</span></span>                           |
|                                     | <span data-ttu-id="3a18a-150">SasAmbientLight</span><span class="sxs-lookup"><span data-stu-id="3a18a-150">SasAmbientLight</span></span> | <span data-ttu-id="3a18a-151">SpotLight \[ ZeroOrMore \] ;</span><span class="sxs-lookup"><span data-stu-id="3a18a-151">SpotLight\[ZeroOrMore\];</span></span>                     |
|                                     | <span data-ttu-id="3a18a-152">int</span><span class="sxs-lookup"><span data-stu-id="3a18a-152">int</span></span>             | <span data-ttu-id="3a18a-153">SAS. NumSpotLights</span><span class="sxs-lookup"><span data-stu-id="3a18a-153">Sas.NumSpotLights</span></span>                            |
| [<span data-ttu-id="3a18a-154">Shadow</span><span class="sxs-lookup"><span data-stu-id="3a18a-154">Shadow</span></span>](#shadow)                   | <span data-ttu-id="3a18a-155">float4x4</span><span class="sxs-lookup"><span data-stu-id="3a18a-155">float4x4</span></span>        | <span data-ttu-id="3a18a-156">SAS. Shadow \[ ZeroOrMore \] . WorldToShadow</span><span class="sxs-lookup"><span data-stu-id="3a18a-156">Sas.Shadow\[ZeroOrMore\].WorldToShadow</span></span>       |
|                                     | <span data-ttu-id="3a18a-157">texture2D</span><span class="sxs-lookup"><span data-stu-id="3a18a-157">texture2D</span></span>       | <span data-ttu-id="3a18a-158">SAS. Shadow \[ ZeroOrMore \] . ShadowMap</span><span class="sxs-lookup"><span data-stu-id="3a18a-158">Sas.Shadow\[ZeroOrMore\].ShadowMap</span></span>           |
| [<span data-ttu-id="3a18a-159">Esqueleto</span><span class="sxs-lookup"><span data-stu-id="3a18a-159">Skeleton</span></span>](#skeleton)               | <span data-ttu-id="3a18a-160">float4x4</span><span class="sxs-lookup"><span data-stu-id="3a18a-160">float4x4</span></span>        | <span data-ttu-id="3a18a-161">SAS. esqueleto. MeshToJointToWorld \[ OneOrMore\]</span><span class="sxs-lookup"><span data-stu-id="3a18a-161">Sas.Skeleton.MeshToJointToWorld\[OneOrMore\]</span></span> |
|                                     | <span data-ttu-id="3a18a-162">int</span><span class="sxs-lookup"><span data-stu-id="3a18a-162">int</span></span>             | <span data-ttu-id="3a18a-163">SAS. esqueleto. NumJoints</span><span class="sxs-lookup"><span data-stu-id="3a18a-163">Sas.Skeleton.NumJoints</span></span>                       |



 

### <a name="time"></a><span data-ttu-id="3a18a-164">Hora</span><span class="sxs-lookup"><span data-stu-id="3a18a-164">Time</span></span>

<span data-ttu-id="3a18a-165">El valor de reloj virtual o de hora de la aplicación host.</span><span class="sxs-lookup"><span data-stu-id="3a18a-165">The host application's virtual clock or time value.</span></span> <span data-ttu-id="3a18a-166">Los miembros incluyen:</span><span class="sxs-lookup"><span data-stu-id="3a18a-166">Members include:</span></span>

-   <span data-ttu-id="3a18a-167">SAS. Time. Now: el valor del reloj virtual de la aplicación host en el punto en el que se representará el efecto.</span><span class="sxs-lookup"><span data-stu-id="3a18a-167">Sas.Time.Now - the value of the host application virtual clock at the point at which the effect will be rendered.</span></span>
-   <span data-ttu-id="3a18a-168">SAS. Time. Last: el valor de Now en la representación anterior.</span><span class="sxs-lookup"><span data-stu-id="3a18a-168">Sas.Time.Last - the value of Now at the previous render.</span></span>
-   <span data-ttu-id="3a18a-169">SAS. Time. Númeromarco: el valor del contador que se incrementa una vez por cada fotograma representado.</span><span class="sxs-lookup"><span data-stu-id="3a18a-169">Sas.Time.FrameNumber - the counter value that is incremented once per rendered frame.</span></span>

<span data-ttu-id="3a18a-170">Los efectos deben controlar correctamente el hecho de que los valores de estos miembros pueden ajustarse potencialmente en los tiempos de ejecución extremadamente largos.</span><span class="sxs-lookup"><span data-stu-id="3a18a-170">Effects must properly handle the fact that the values of these members can potentially wrap around during extremely long execution times.</span></span> <span data-ttu-id="3a18a-171">Ahora y el último pueden tener valores muy grandes.</span><span class="sxs-lookup"><span data-stu-id="3a18a-171">Now and Last may have very large values.</span></span>

### <a name="environment-map"></a><span data-ttu-id="3a18a-172">Mapa de entorno</span><span class="sxs-lookup"><span data-stu-id="3a18a-172">Environment Map</span></span>

<span data-ttu-id="3a18a-173">Un mapa de entorno cúbico.</span><span class="sxs-lookup"><span data-stu-id="3a18a-173">A cubic environment map.</span></span> <span data-ttu-id="3a18a-174">Las aplicaciones host deben proporcionar una textura de cubo válida si un efecto intenta enlazar a SAS. EnvironmentMap.</span><span class="sxs-lookup"><span data-stu-id="3a18a-174">Host applications must provide a valid cube texture if an effect attempts to bind to Sas.EnvironmentMap.</span></span>

### <a name="camera"></a><span data-ttu-id="3a18a-175">Cámara</span><span class="sxs-lookup"><span data-stu-id="3a18a-175">Camera</span></span>

<span data-ttu-id="3a18a-176">Cámara que se está representando actualmente.</span><span class="sxs-lookup"><span data-stu-id="3a18a-176">The camera currently being rendered.</span></span> <span data-ttu-id="3a18a-177">Los miembros incluyen:</span><span class="sxs-lookup"><span data-stu-id="3a18a-177">Members include:</span></span>

-   <span data-ttu-id="3a18a-178">SAS. Camera. WorldToView: la matriz de vista universal compuesta de la cámara.</span><span class="sxs-lookup"><span data-stu-id="3a18a-178">Sas.Camera.WorldToView - the composite world-view matrix for the camera.</span></span>
-   <span data-ttu-id="3a18a-179">SAS. Camera. Projection: la matriz de proyección de la cámara.</span><span class="sxs-lookup"><span data-stu-id="3a18a-179">Sas.Camera.Projection - the projection matrix for the camera.</span></span>
-   <span data-ttu-id="3a18a-180">SAS. Camera. NearFarClipping: los valores de los planos de recorte Near y Far.</span><span class="sxs-lookup"><span data-stu-id="3a18a-180">Sas.Camera.NearFarClipping - the values of the near and far clipping planes.</span></span>

### <a name="light"></a><span data-ttu-id="3a18a-181">Claro</span><span class="sxs-lookup"><span data-stu-id="3a18a-181">Light</span></span>

<span data-ttu-id="3a18a-182">Una o más luces de la escena.</span><span class="sxs-lookup"><span data-stu-id="3a18a-182">One or more scene lights.</span></span> <span data-ttu-id="3a18a-183">La colección de luces se declara como una matriz donde:</span><span class="sxs-lookup"><span data-stu-id="3a18a-183">The collection of lights is declared as an array where:</span></span>

-   <span data-ttu-id="3a18a-184">Color: color RGB.</span><span class="sxs-lookup"><span data-stu-id="3a18a-184">Color - an RGB color.</span></span> <span data-ttu-id="3a18a-185">El valor predeterminado es (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="3a18a-185">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="3a18a-186">Dirección: la dirección de la luz.</span><span class="sxs-lookup"><span data-stu-id="3a18a-186">Direction - the light direction.</span></span> <span data-ttu-id="3a18a-187">El valor predeterminado es (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="3a18a-187">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="3a18a-188">Intervalo: la distancia desde la luz en la que los rayos de luz no tienen ningún efecto en la escena.</span><span class="sxs-lookup"><span data-stu-id="3a18a-188">Range - the distance from the light where the light rays have no effect on the scene.</span></span> <span data-ttu-id="3a18a-189">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="3a18a-189">The default value is 0.</span></span>
-   <span data-ttu-id="3a18a-190">Theta: el ángulo de cono interior de un foco, medido en radianes.</span><span class="sxs-lookup"><span data-stu-id="3a18a-190">Theta - the inner cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="3a18a-191">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="3a18a-191">The default value is 0.</span></span>
-   <span data-ttu-id="3a18a-192">Phi: el ángulo de cono exterior de un foco, medido en radianes.</span><span class="sxs-lookup"><span data-stu-id="3a18a-192">Phi - the outer cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="3a18a-193">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="3a18a-193">The default value is 0.</span></span>

<span data-ttu-id="3a18a-194">El número de luces debe establecerse en el número de luces enlazadas a la matriz asociada.</span><span class="sxs-lookup"><span data-stu-id="3a18a-194">The number of lights must be set to the number of lights bound into the associated array.</span></span> <span data-ttu-id="3a18a-195">Los efectos pueden optar por omitir el número de luces y enlazar a cualquier elemento de una de las matrices ligeras.</span><span class="sxs-lookup"><span data-stu-id="3a18a-195">Effects can choose to ignore the number of lights and bind to any element of one of the light arrays.</span></span> <span data-ttu-id="3a18a-196">Por lo tanto, las aplicaciones host deben proporcionar un enlace válido para los elementos más allá del número de luces de la matriz.</span><span class="sxs-lookup"><span data-stu-id="3a18a-196">Therefore, host applications must provide a valid binding for elements beyond the number of lights in the array.</span></span>

<span data-ttu-id="3a18a-197">ZeroOrMore implica que la matriz puede tener cualquier número de elementos.</span><span class="sxs-lookup"><span data-stu-id="3a18a-197">ZeroOrMore implies that the array may have any number of elements.</span></span>

### <a name="shadow"></a><span data-ttu-id="3a18a-198">Shadow</span><span class="sxs-lookup"><span data-stu-id="3a18a-198">Shadow</span></span>

<span data-ttu-id="3a18a-199">Búferes de instantáneas que constan de:</span><span class="sxs-lookup"><span data-stu-id="3a18a-199">Shadow buffers which consists of:</span></span>

-   <span data-ttu-id="3a18a-200">WorldToShadow: una matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="3a18a-200">WorldToShadow - an array of matrices.</span></span>
-   <span data-ttu-id="3a18a-201">ShadowMap: un archivo de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="3a18a-201">ShadowMap - a 2D texture file.</span></span>

<span data-ttu-id="3a18a-202">ZeroOrMore implica que la matriz puede tener cualquier número de elementos (cero significa una matriz vacía).</span><span class="sxs-lookup"><span data-stu-id="3a18a-202">ZeroOrMore implies that the array may have any number of elements (zero means an empty array).</span></span>

<span data-ttu-id="3a18a-203">Un efecto declararía una muestra de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3a18a-203">An effect would declare a sampler as follows:</span></span>


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a><span data-ttu-id="3a18a-204">Esqueleto</span><span class="sxs-lookup"><span data-stu-id="3a18a-204">Skeleton</span></span>

<span data-ttu-id="3a18a-205">Conjunto de marcos que componen el objeto que se está procesando actualmente.</span><span class="sxs-lookup"><span data-stu-id="3a18a-205">The set of frames that compose the currently rendering object.</span></span> <span data-ttu-id="3a18a-206">Los ejemplos de fotogramas son huesos y transformaciones.</span><span class="sxs-lookup"><span data-stu-id="3a18a-206">Frame examples are bones and transforms.</span></span> <span data-ttu-id="3a18a-207">Esto incluye:</span><span class="sxs-lookup"><span data-stu-id="3a18a-207">This includes:</span></span>

-   <span data-ttu-id="3a18a-208">MeshToJointToWorld: una matriz de matrices.</span><span class="sxs-lookup"><span data-stu-id="3a18a-208">MeshToJointToWorld - an array of matrices.</span></span>
-   <span data-ttu-id="3a18a-209">NumJoints: el número de uniones en el esqueleto.</span><span class="sxs-lookup"><span data-stu-id="3a18a-209">NumJoints - the number of joints in the skeleton.</span></span>

<span data-ttu-id="3a18a-210">OneOrMore implica que la matriz tiene al menos un elemento y puede contener cualquier número de elementos.</span><span class="sxs-lookup"><span data-stu-id="3a18a-210">OneOrMore implies that the array has at least one and may contain any number of elements.</span></span>

<span data-ttu-id="3a18a-211">La definición admite objetos de malla rígidas y estratificados mediante el mismo conjunto de valores de [colección SasHostParameterValue](#sashostparametervalue-collection) con una interpretación diferente.</span><span class="sxs-lookup"><span data-stu-id="3a18a-211">The definition supports both rigid and skinned mesh objects using the same set of [SasHostParameterValue Collection](#sashostparametervalue-collection) values with different interpretation.</span></span>

## <a name="sasbindaddress"></a><span data-ttu-id="3a18a-212">SasBindAddress</span><span class="sxs-lookup"><span data-stu-id="3a18a-212">SasBindAddress</span></span>

<span data-ttu-id="3a18a-213">Esta anotación se agrega a la parte superior de un archivo de efectos para asociar un parámetro de efecto a su parámetro correspondiente definido en la [colección SasHostParameterValue](#sashostparametervalue-collection).</span><span class="sxs-lookup"><span data-stu-id="3a18a-213">This annotation is added to the top of an effect file to associate an effect parameter with its corresponding parameter defined in the [SasHostParameterValue Collection](#sashostparametervalue-collection).</span></span> <span data-ttu-id="3a18a-214">La anotación se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3a18a-214">The annotation is declared like this:</span></span>


```
string SasBindAddress = "SasHostParameterValue";
```



<span data-ttu-id="3a18a-215">En este ejemplo se enlaza la matriz del mundo del efecto a la matriz de MeshToJointToWorld:</span><span class="sxs-lookup"><span data-stu-id="3a18a-215">This example binds the effect world matrix to the MeshToJointToWorld matrix:</span></span>


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



<span data-ttu-id="3a18a-216">Esta anotación indica a la aplicación host que necesita establecer el valor de la matriz del efecto mundial con los datos de la matriz MeshToJointToWorld.</span><span class="sxs-lookup"><span data-stu-id="3a18a-216">This annotation tells the host application that it needs to set the value of the effect world matrix using the data in the MeshToJointToWorld matrix.</span></span>

<span data-ttu-id="3a18a-217">La sintaxis de la anotación de dirección de enlace se definió para ser muy similar a la sintaxis que usa [**ID3DXEffect**](id3dxeffect.md) para obtener y establecer los parámetros de efecto.</span><span class="sxs-lookup"><span data-stu-id="3a18a-217">The bind address annotation syntax was defined to be very similar with the syntax used by [**ID3DXEffect**](id3dxeffect.md) to get and set effect parameters.</span></span> <span data-ttu-id="3a18a-218">La única diferencia entre los métodos DXSAS gramatical y **ID3DXEffect** es la adición del token de índice de asterisco.</span><span class="sxs-lookup"><span data-stu-id="3a18a-218">The only difference between the DXSAS grammar and **ID3DXEffect** methods is the addition of the asterisk index token.</span></span> <span data-ttu-id="3a18a-219">Este es otro ejemplo que usa el índice de asterisco:</span><span class="sxs-lookup"><span data-stu-id="3a18a-219">Here is another example using the asterisk index:</span></span>


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



<span data-ttu-id="3a18a-220">El token de índice de asterisco denota que todos los elementos de la matriz de valores de envirnmant de host determinada (color en este caso) se deben enlazar en el parámetro asociado.</span><span class="sxs-lookup"><span data-stu-id="3a18a-220">The asterisk index token denotes that all elements of the particular host envirnmant value array (color in this case) should be bound in the associated parameter.</span></span> <span data-ttu-id="3a18a-221">Varios tokens de índice de asterisco permiten que los efectos se enlacen a subelementos de una matriz de estructuras sin necesidad de enlazar la propia estructura.</span><span class="sxs-lookup"><span data-stu-id="3a18a-221">Multiple asterisk index tokens allow effects to bind to sub-elements of an array of structures without the need to bind the entire structure itself.</span></span> <span data-ttu-id="3a18a-222">En este ejemplo se enlazan los valores de color de las seis primeras luces a un parámetro de efecto.</span><span class="sxs-lookup"><span data-stu-id="3a18a-222">This example binds the color values of the first six lights to an effect parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a18a-223">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a18a-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a18a-224">Referencia de las anotaciones y semánticas estándar de DirectX</span><span class="sxs-lookup"><span data-stu-id="3a18a-224">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



