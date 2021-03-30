---
description: Transferencia Radiance precalculada (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Transferencia Radiance precalculada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553572"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a><span data-ttu-id="f3f5c-103">Transferencia Radiance precalculada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f3f5c-103">Precomputed Radiance Transfer (Direct3D 9)</span></span>

## <a name="using-precomputed-radiance-transfer"></a><span data-ttu-id="f3f5c-104">Usar la transferencia Radiance precalculada</span><span class="sxs-lookup"><span data-stu-id="f3f5c-104">Using Precomputed Radiance Transfer</span></span>

<span data-ttu-id="f3f5c-105">Hay varias formas de complejidad presentes en escenas interesantes, como la forma en que se modela el entorno de iluminación (es decir, modelos de iluminación de área frente a puntos o direccionales) y qué tipo de efectos globales se modelan (por ejemplo, sombras, interflexiones, dispersión de subsuperficies). Las técnicas de representación interactivas tradicionales modelan una cantidad limitada de esta complejidad.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-105">There are several forms of complexity present in interesting scenes, including how the lighting environment is modeled (that is, area lighting models versus point/directional ones) and what kind of global effects are modeled (for example, shadows, interreflections, subsurface scattering.) Traditional interactive rendering techniques model a limited amount of this complexity.</span></span> <span data-ttu-id="f3f5c-106">PRT permite estos efectos con algunas restricciones importantes:</span><span class="sxs-lookup"><span data-stu-id="f3f5c-106">PRT enables these effects with some significant restrictions:</span></span>

-   <span data-ttu-id="f3f5c-107">Se supone que los objetos son rígidos (es decir, ninguna desformación).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-107">Objects are assumed to be rigid (that is, no deformations).</span></span>
-   <span data-ttu-id="f3f5c-108">Se trata de un enfoque centrado en objetos (a menos que los objetos se muevan juntos; estos efectos globales no se mantienen entre ellos).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-108">It is an object-centric approach (unless objects are moved together, these global effects are not maintained between them).</span></span>
-   <span data-ttu-id="f3f5c-109">Solo se modela la iluminación de baja frecuencia (lo que da lugar a sombras flexibles). En el caso de las luces de alta frecuencia (sombras vivas), se tendrían que emplear técnicas tradicionales.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-109">Only low-frequency lighting is modeled (resulting in soft shadows.) For high-frequency lights (sharp shadows), traditional techniques would have to be employed.</span></span>

<span data-ttu-id="f3f5c-110">PRT requiere una de las siguientes opciones, pero no ambas:</span><span class="sxs-lookup"><span data-stu-id="f3f5c-110">PRT requires either of the following, but not both:</span></span>

-   <span data-ttu-id="f3f5c-111">modelos de teselación alta y vs \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f3f5c-111">highly-tessellated models and vs\_1\_1</span></span>
-   <span data-ttu-id="f3f5c-112">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f3f5c-112">ps\_2\_0</span></span>

### <a name="standard-diffuse-lighting-versus-prt"></a><span data-ttu-id="f3f5c-113">Iluminación difusa estándar frente a PRT</span><span class="sxs-lookup"><span data-stu-id="f3f5c-113">Standard Diffuse Lighting versus PRT</span></span>

<span data-ttu-id="f3f5c-114">La siguiente ilustración se representa con el modelo de iluminación tradicional (n · l).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-114">The following illustration is rendered using the traditional (n · l) lighting model.</span></span> <span data-ttu-id="f3f5c-115">Las sombras nítidas se pueden habilitar con otro paso y alguna forma de técnica de sombreado (mapas de profundidad de sombra o volúmenes de instantáneas).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-115">Sharp shadows could be enabled using another pass and some form of shadowing technique (shadow depth maps or shadow volumes).</span></span> <span data-ttu-id="f3f5c-116">Agregar varias luces requeriría varios pasos (si se van a usar sombras) o sombreadores más complejos con técnicas tradicionales.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-116">Adding multiple lights would require either multiple passes (if shadows are to be used) or more complex shaders with traditional techniques.</span></span>

![captura de pantalla de una ilustración representada mediante el modelo de iluminación tradicional](images/prt-diffuse-cropped.png)

<span data-ttu-id="f3f5c-118">La siguiente ilustración se representa con PRT con la mejor aproximación de una luz direccional única que puede resolver.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-118">The next illustration is rendered with PRT using the best approximation of a single directional light that it can resolve.</span></span> <span data-ttu-id="f3f5c-119">Esto da como resultado sombras flexibles que serían difíciles de producir con técnicas tradicionales.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-119">This results in soft shadows that would be difficult to produce with traditional techniques.</span></span> <span data-ttu-id="f3f5c-120">Dado que PRT siempre modela entornos de iluminación completos agregando varias luces o usando un mapa de entorno, solo cambiaría los valores (pero no el número) de constantes que usa el sombreador.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-120">Because PRT always models complete lighting environments adding multiple lights or using an environment map, you would only change the values (but not the number) of constants used by the shader.</span></span>

![captura de pantalla de una ilustración representada mediante PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a><span data-ttu-id="f3f5c-122">PRT con interflexiones</span><span class="sxs-lookup"><span data-stu-id="f3f5c-122">PRT with Interreflections</span></span>

<span data-ttu-id="f3f5c-123">La iluminación directa alcanza la superficie directamente de la luz.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-123">Direct lighting reaches the surface directly from the light.</span></span> <span data-ttu-id="f3f5c-124">Las interflexiones son claras al alcanzar la superficie después de rebotar alguna otra superficie un número determinado de veces.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-124">Interreflections are light reaching the surface after bouncing off some other surface some number of times.</span></span> <span data-ttu-id="f3f5c-125">PRT puede modelar este comportamiento sin cambiar el rendimiento en tiempo de ejecución simplemente ejecutando el simulador con distintos parámetros.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-125">PRT can model this behavior without changing the performance at run time by simply running the simulator with different parameters.</span></span>

<span data-ttu-id="f3f5c-126">La siguiente ilustración se crea solo con Direct PRT (0 rebota sin interacciones).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-126">The following illustration is created using direct PRT only (0 bounces with no interreflections).</span></span>

![captura de pantalla de una ilustración presentada solo con Direct PRT](images/prt-nointerreflections.png)

<span data-ttu-id="f3f5c-128">La siguiente ilustración se crea con PRT con interflexiones (2 rebotas con interacciones).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-128">The following illustration is created using PRT with interreflections (2 bounces with interreflections).</span></span>

![captura de pantalla de una ilustración representada mediante PRT con interflexiones](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a><span data-ttu-id="f3f5c-130">PRT con dispersión de subsuperficies</span><span class="sxs-lookup"><span data-stu-id="f3f5c-130">PRT with Subsurface Scattering</span></span>

<span data-ttu-id="f3f5c-131">La dispersión de subsuperficies es una técnica que modela cómo pasa la luz a través de determinados materiales.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-131">Subsurface scattering is a technique that models how light passes through certain materials.</span></span> <span data-ttu-id="f3f5c-132">Por ejemplo, presione una linterna iluminada en la palma de la mano.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-132">As an example, press a lit flashlight against the palm of your hand.</span></span> <span data-ttu-id="f3f5c-133">La luz de la linterna pasa a través de la mano, rebota (cambiar el color en el proceso) y sale del otro lado de la mano.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-133">The light from the flashlight passes through your hand, bounces around (changing color in the process), and exits from the other side of your hand.</span></span> <span data-ttu-id="f3f5c-134">También se puede modelar con cambios sencillos en el simulador y sin cambios en el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-134">This can also be modeled with simple changes to the simulator and no changes to the runtime.</span></span>

<span data-ttu-id="f3f5c-135">En la ilustración siguiente se muestra PRT con dispersión de subsuperficies.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-135">The following illustration demonstrates PRT with subsurface scattering.</span></span>

![captura de pantalla de una ilustración representada mediante PRT con dispersión de subsuperficies](images/prt-subsurface.png)

## <a name="how-prt-works"></a><span data-ttu-id="f3f5c-137">Cómo funciona PRT</span><span class="sxs-lookup"><span data-stu-id="f3f5c-137">How PRT Works</span></span>

<span data-ttu-id="f3f5c-138">Los siguientes términos son útiles para comprender cómo funciona PRT, tal como se muestra en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-138">The following terms are useful for understanding how PRT works, as illustrated in the following diagram.</span></span>

<span data-ttu-id="f3f5c-139">Source Radiance: el Radiance de origen representa el entorno de iluminación en conjunto.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-139">Source Radiance: The source radiance represents the lighting environment as a whole.</span></span> <span data-ttu-id="f3f5c-140">En PRT, se aproxima un entorno arbitrario mediante la base de armónico esférico: se supone que se trata de una iluminación lejana respecto al objeto (la misma suposición que se realiza con mapas de entorno).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-140">In PRT an arbitrary environment is approximated using the spherical harmonic basis - this lighting is assumed to be distant relative to the object (the same assumption that is made with environment maps.)</span></span>

<span data-ttu-id="f3f5c-141">Exit Radiance: Exit Radiance es la luz que sale de un punto de la superficie de cualquier origen posible (reflejado radiance, dispersión de subsuperficies, emisión).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-141">Exit Radiance: Exit radiance is the light leaving from a point on the surface from any possible source (reflected radiance, subsurface scattering, emission).</span></span>

<span data-ttu-id="f3f5c-142">Vectores de transferencia: los vectores de transferencia asignan el origen Radiance a la salida Radiance y se calculan previamente sin conexión mediante una simulación de transporte ligero complejo.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-142">Transfer Vectors: Transfer vectors map Source Radiance into exit radiance and are precomputed offline using a complex light transport simulation.</span></span>

![diagrama de cómo funciona PRT](images/prt-lightingpicture.png)

<span data-ttu-id="f3f5c-144">PRT factores el proceso de representación en dos fases, tal como se muestra en el diagrama siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3f5c-144">PRT factors the rendering process into two stages, as shown in the following diagram:</span></span>

1.  <span data-ttu-id="f3f5c-145">Una simulación de transporte de luz costosa calcula previamente los coeficientes de transferencia que se pueden usar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-145">An expensive light transport simulation precomputes transfer coefficients that can be used at run time.</span></span>
2.  <span data-ttu-id="f3f5c-146">En primer lugar, una fase de tiempo de ejecución relativamente ligera aproxima el entorno de iluminación con el modelo armónico esférico y luego usa estos coeficientes de iluminación y los coeficientes de transferencia precalculados (de la fase 1) con un sombreador simple, lo que da lugar a la salida de Radiance (la luz que sale del objeto).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-146">A relatively lightweight run-time stage first approximates the lighting environment using the spherical harmonic basis, then uses these lighting coefficients and the precomputed transfer coefficients (from stage 1) with a simple shader, resulting in exit radiance (the light leaving the object).</span></span>

![diagrama del flujo de datos de PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a><span data-ttu-id="f3f5c-148">Cómo usar la API de PRT</span><span class="sxs-lookup"><span data-stu-id="f3f5c-148">How to Use the PRT API</span></span>

1.  <span data-ttu-id="f3f5c-149">Calcular los vectores de transferencia con uno de los tipos de proceso... métodos de [**ID3DXPRTEngine**](id3dxprtengine.md).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-149">Compute the transfer vectors with one of the Compute... methods of [**ID3DXPRTEngine**](id3dxprtengine.md).</span></span>

    <span data-ttu-id="f3f5c-150">Tratar directamente con estos vectores de transferencia requiere una cantidad significativa de memoria y cálculo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-150">Directly dealing with these transfer vectors requires a significant amount of memory and shader computation.</span></span> <span data-ttu-id="f3f5c-151">La compresión reduce significativamente la cantidad de memoria y el cálculo del sombreador necesarios.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-151">Compression significantly reduces the amount of memory and shader computation required.</span></span>

    <span data-ttu-id="f3f5c-152">Los valores de iluminación finales se calculan en un sombreador de vértices que implementa la siguiente ecuación de representación comprimida.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-152">The final lighting values are calculated in a vertex shader that implements the following compressed rendering equation.</span></span>

    ![ecuación de la representación de PRT](images/prt-shaderequation.png)

    <span data-ttu-id="f3f5c-154">Donde:</span><span class="sxs-lookup"><span data-stu-id="f3f5c-154">Where:</span></span>

    

    | <span data-ttu-id="f3f5c-155">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f3f5c-155">Parameter</span></span>      | <span data-ttu-id="f3f5c-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3f5c-156">Description</span></span>                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f3f5c-157">RP</span><span class="sxs-lookup"><span data-stu-id="f3f5c-157">Rₚ</span></span>             | <span data-ttu-id="f3f5c-158">Un solo canal de salida radiance en el vértice p y se evalúa en cada vértice de la malla.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-158">A single channel of exit radiance at vertex p and is evaluated at every vertex on the mesh.</span></span>                     |
    | <span data-ttu-id="f3f5c-159">MK</span><span class="sxs-lookup"><span data-stu-id="f3f5c-159">Mₖ</span></span>             | <span data-ttu-id="f3f5c-160">La media del clúster k.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-160">The mean for cluster k.</span></span> <span data-ttu-id="f3f5c-161">Este es un vector de pedido ² de coeficientes.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-161">This is an Order² vector of coefficients.</span></span>                                               |
    | <span data-ttu-id="f3f5c-162">k</span><span class="sxs-lookup"><span data-stu-id="f3f5c-162">k</span></span>              | <span data-ttu-id="f3f5c-163">El identificador de clúster para el vértice p.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-163">The cluster ID for vertex p.</span></span>                                                                                    |
    | <span data-ttu-id="f3f5c-164">L<sup>'</sup></span><span class="sxs-lookup"><span data-stu-id="f3f5c-164">L<sup>'</sup></span></span>  | <span data-ttu-id="f3f5c-165">La aproximación de la Radiance de origen en las funciones de base de SH.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-165">The approximation of the source radiance into the SH basis functions.</span></span> <span data-ttu-id="f3f5c-166">Este es un vector de pedido ² de coeficientes.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-166">This is an Order² vector of coefficients.</span></span> |
    | <span data-ttu-id="f3f5c-167">j</span><span class="sxs-lookup"><span data-stu-id="f3f5c-167">j</span></span>              | <span data-ttu-id="f3f5c-168">Entero que suma el número de vectores PCA.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-168">An integer that sums over the number of PCA vectors.</span></span>                                                            |
    | <span data-ttu-id="f3f5c-169">en<sub>blanco</sub></span><span class="sxs-lookup"><span data-stu-id="f3f5c-169">w<sub>pj</sub></span></span> | <span data-ttu-id="f3f5c-170">Peso del PCA de JTH para el punto p.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-170">The jth PCA weight for point p.</span></span> <span data-ttu-id="f3f5c-171">Se trata de un único coeficiente.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-171">This is a single coefficient.</span></span>                                                   |
    | <span data-ttu-id="f3f5c-172">B<sub>KJ</sub></span><span class="sxs-lookup"><span data-stu-id="f3f5c-172">B<sub>kj</sub></span></span> | <span data-ttu-id="f3f5c-173">Vector de base del PCA de JTH para el clúster k.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-173">The jth PCA basis vector for cluster k.</span></span> <span data-ttu-id="f3f5c-174">Este es un vector de pedido ² de coeficientes.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-174">This is an Order² vector of coefficients.</span></span>                               |

    

     

    <span data-ttu-id="f3f5c-175">El extracto... los métodos de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) proporcionan acceso a los datos comprimidos desde la simulación.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-175">The Extract... methods of [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) provide access to compressed data from the simulation.</span></span>

2.  <span data-ttu-id="f3f5c-176">Calcule el Radiance de origen.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-176">Compute the source radiance.</span></span>

    <span data-ttu-id="f3f5c-177">Hay varias funciones auxiliares en la API para controlar diversos escenarios de iluminación comunes.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-177">There are several helper functions in the API to handle a variety of common lighting scenarios.</span></span>

    

    | <span data-ttu-id="f3f5c-178">Función</span><span class="sxs-lookup"><span data-stu-id="f3f5c-178">Function</span></span>                                                         | <span data-ttu-id="f3f5c-179">Finalidad</span><span class="sxs-lookup"><span data-stu-id="f3f5c-179">Purpose</span></span>                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="f3f5c-180">**D3DXSHEvalDirectionalLight**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-180">**D3DXSHEvalDirectionalLight**</span></span>](d3dxshevaldirectionallight.md) | <span data-ttu-id="f3f5c-181">Aproxima una luz direccional convencional.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-181">Approximates a conventional directional light.</span></span>                                                              |
    | [<span data-ttu-id="f3f5c-182">**D3DXSHEvalSphericalLight**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-182">**D3DXSHEvalSphericalLight**</span></span>](d3dxshevalsphericallight.md)     | <span data-ttu-id="f3f5c-183">Se aproxima a las fuentes de luz esféricas locales.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-183">Approximates local spherical light sources.</span></span> <span data-ttu-id="f3f5c-184">(Tenga en cuenta que PRT solo funciona con entornos de iluminación de distancia).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-184">(Note that PRT only works with distance lighting environments.)</span></span> |
    | [<span data-ttu-id="f3f5c-185">**D3DXSHEvalConeLight**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-185">**D3DXSHEvalConeLight**</span></span>](d3dxshevalconelight.md)               | <span data-ttu-id="f3f5c-186">Aproxima una fuente de luz de área distante.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-186">Approximates a distant area light source.</span></span> <span data-ttu-id="f3f5c-187">Un ejemplo sería el sol (ángulo de cono muy pequeño).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-187">An example would be the sun (very small cone angle).</span></span>              |
    | [<span data-ttu-id="f3f5c-188">**D3DXSHEvalHemisphereLight**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-188">**D3DXSHEvalHemisphereLight**</span></span>](d3dxshevalhemispherelight.md)   | <span data-ttu-id="f3f5c-189">Evalúa una luz que es una interpolación lineal entre dos colores (uno en cada polo de una esfera).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-189">Evaluates a light that is a linear interpolation between two colors (one on each pole of a sphere).</span></span>         |

    

     

3.  <span data-ttu-id="f3f5c-190">Calcule el Radiance de salida.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-190">Compute the exit radiance.</span></span>

    <span data-ttu-id="f3f5c-191">La ecuación 1 ahora debe evaluarse en cada punto mediante un sombreador de vértices o de píxeles.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-191">Equation 1 now has to be evaluated at every point using either a vertex or pixel shader.</span></span> <span data-ttu-id="f3f5c-192">Antes de que se pueda evaluar el sombreador, las constantes deben calcularse previamente y cargarse en la tabla de constantes (vea el [ejemplo de demostración de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) para obtener más detalles).</span><span class="sxs-lookup"><span data-stu-id="f3f5c-192">Before the shader can be evaluated, constants have to be precomputed and loaded into the constant table (see the [PRT Demo Sample](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) for details).</span></span> <span data-ttu-id="f3f5c-193">El propio sombreador es una implementación sencilla de esta ecuación.</span><span class="sxs-lookup"><span data-stu-id="f3f5c-193">The shader itself is a straightforward implementation of this equation.</span></span>

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a><span data-ttu-id="f3f5c-194">Referencias</span><span class="sxs-lookup"><span data-stu-id="f3f5c-194">References</span></span>

<span data-ttu-id="f3f5c-195">Para obtener más información acerca de PRT y armónicos esféricos, consulte los siguientes documentos:</span><span class="sxs-lookup"><span data-stu-id="f3f5c-195">For more information about PRT and spherical harmonics, see the following papers:</span></span>


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a><span data-ttu-id="f3f5c-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3f5c-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3f5c-197">Temas avanzados</span><span class="sxs-lookup"><span data-stu-id="f3f5c-197">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="f3f5c-198">Ecuaciones de PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f3f5c-198">PRT Equations (Direct3D 9)</span></span>](prt-equations.md)
</dt> <dt>

[<span data-ttu-id="f3f5c-199">Representar PRT con texturas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f3f5c-199">Representing PRT With Textures (Direct3D 9)</span></span>](representing-prt-with-textures.md)
</dt> <dt>

[<span data-ttu-id="f3f5c-200">**ID3DXPRTBuffer**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-200">**ID3DXPRTBuffer**</span></span>](id3dxprtbuffer.md)
</dt> <dt>

[<span data-ttu-id="f3f5c-201">**ID3DXPRTCompBuffer**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-201">**ID3DXPRTCompBuffer**</span></span>](id3dxprtcompbuffer.md)
</dt> <dt>

[<span data-ttu-id="f3f5c-202">**ID3DXPRTEngine**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-202">**ID3DXPRTEngine**</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="f3f5c-203">**ID3DXTextureGutterHelper**</span><span class="sxs-lookup"><span data-stu-id="f3f5c-203">**ID3DXTextureGutterHelper**</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="f3f5c-204">Funciones de transferencia Radiance precalculadas</span><span class="sxs-lookup"><span data-stu-id="f3f5c-204">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[<span data-ttu-id="f3f5c-205">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f3f5c-205">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



