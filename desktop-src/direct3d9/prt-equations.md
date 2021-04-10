---
description: Para entender completamente un sombreador que implementa PRT, es útil derivar la fórmula que utiliza el sombreador para calcular el Radiance de salida.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Ecuaciones de PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152435"
---
# <a name="prt-equations-direct3d-9"></a><span data-ttu-id="dab42-103">Ecuaciones de PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="dab42-103">PRT Equations (Direct3D 9)</span></span>

<span data-ttu-id="dab42-104">Para entender completamente un sombreador que implementa PRT, es útil derivar la fórmula que utiliza el sombreador para calcular el Radiance de salida.</span><span class="sxs-lookup"><span data-stu-id="dab42-104">To fully understand a shader that implements PRT, it is useful to derive the formula the shader uses to calculate exit radiance.</span></span>

<span data-ttu-id="dab42-105">Para empezar, la siguiente ecuación es la ecuación general para calcular las radiances de salida resultantes de la iluminación directa en un objeto difuso con iluminación distanl arbitraria.</span><span class="sxs-lookup"><span data-stu-id="dab42-105">To start off, the following equation is the general equation to calculate exit radiance resulting from direct lighting on a diffuse object with arbitrary distant lighting.</span></span>

![ecuación del Radiance de salida resultante de la iluminación directa en un objeto difuso con iluminación distanl arbitraria](images/prt-theory-eq1.png)

<span data-ttu-id="dab42-107">donde:</span><span class="sxs-lookup"><span data-stu-id="dab42-107">where:</span></span>



| <span data-ttu-id="dab42-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dab42-108">Parameter</span></span>     | <span data-ttu-id="dab42-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab42-109">Description</span></span>                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab42-110">RP</span><span class="sxs-lookup"><span data-stu-id="dab42-110">Rₚ</span></span>            | <span data-ttu-id="dab42-111">El Radiance de salida en el vértice p.</span><span class="sxs-lookup"><span data-stu-id="dab42-111">The exit radiance at vertex p.</span></span> <span data-ttu-id="dab42-112">Se evalúa en cada vértice de la malla.</span><span class="sxs-lookup"><span data-stu-id="dab42-112">Evaluated at every vertex on the mesh.</span></span>                                   |
| <span data-ttu-id="dab42-113">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="dab42-113">p<sub>d</sub></span></span> | <span data-ttu-id="dab42-114">Albedo de la superficie.</span><span class="sxs-lookup"><span data-stu-id="dab42-114">The albedo of the surface.</span></span>                                                                              |
| <span data-ttu-id="dab42-115">pi</span><span class="sxs-lookup"><span data-stu-id="dab42-115">pi</span></span>            | <span data-ttu-id="dab42-116">Constante que se usa como factor de normalización de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="dab42-116">A constant, used as an energy conservation normalization factor.</span></span>                                        |
| <span data-ttu-id="dab42-117">L (s)</span><span class="sxs-lookup"><span data-stu-id="dab42-117">L(s)</span></span>          | <span data-ttu-id="dab42-118">Entorno de iluminación (Radiance de origen).</span><span class="sxs-lookup"><span data-stu-id="dab42-118">The lighting environment (source radiance).</span></span>                                                             |
| <span data-ttu-id="dab42-119">VP ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="dab42-119">Vₚ₍ₛ₎</span></span>         | <span data-ttu-id="dab42-120">Una función de visibilidad binaria para el punto p.</span><span class="sxs-lookup"><span data-stu-id="dab42-120">A binary visibility function for point p.</span></span> <span data-ttu-id="dab42-121">Es 1 si el punto puede ver la luz, 0 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="dab42-121">It is 1 if the point can see the light, 0 if not.</span></span>             |
| <span data-ttu-id="dab42-122">HNP ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="dab42-122">Hₙₚ₍ₛ₎</span></span>        | <span data-ttu-id="dab42-123">El término del coseno de la ley de Lambert.</span><span class="sxs-lookup"><span data-stu-id="dab42-123">The cosine term from Lambert's law.</span></span> <span data-ttu-id="dab42-124">Igual a Max ((NP · s), 0), donde NP es la superficie normal en el punto p.</span><span class="sxs-lookup"><span data-stu-id="dab42-124">Equal to max((Nₚ· s), 0) where Nₚ is the surface normal at point p.</span></span> |
| <span data-ttu-id="dab42-125">s</span><span class="sxs-lookup"><span data-stu-id="dab42-125">s</span></span>             | <span data-ttu-id="dab42-126">La variable que se integra en la esfera.</span><span class="sxs-lookup"><span data-stu-id="dab42-126">The variable that integrates over the sphere.</span></span>                                                           |



 

<span data-ttu-id="dab42-127">Con las funciones de base esféricas, como los armónicos esféricos, la ecuación siguiente se aproxima al entorno de iluminación.</span><span class="sxs-lookup"><span data-stu-id="dab42-127">Using spherical basis functions, such as spherical harmonics, the following equation approximates the lighting environment.</span></span>

![ecuación del entorno de iluminación](images/prt-theory-eq2.png)

<span data-ttu-id="dab42-129">donde:</span><span class="sxs-lookup"><span data-stu-id="dab42-129">where:</span></span>



| <span data-ttu-id="dab42-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dab42-130">Parameter</span></span>        | <span data-ttu-id="dab42-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab42-131">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="dab42-132">L (s)</span><span class="sxs-lookup"><span data-stu-id="dab42-132">L(s)</span></span>             | <span data-ttu-id="dab42-133">Entorno de iluminación (Radiance de origen).</span><span class="sxs-lookup"><span data-stu-id="dab42-133">The lighting environment (source radiance).</span></span>              |
| <span data-ttu-id="dab42-134">i</span><span class="sxs-lookup"><span data-stu-id="dab42-134">i</span></span>                | <span data-ttu-id="dab42-135">Entero que suma el número de funciones de base.</span><span class="sxs-lookup"><span data-stu-id="dab42-135">An integer that sums over the number of basis functions.</span></span> |
| <span data-ttu-id="dab42-136">O</span><span class="sxs-lookup"><span data-stu-id="dab42-136">O</span></span>                | <span data-ttu-id="dab42-137">El orden de los armónicos esféricos.</span><span class="sxs-lookup"><span data-stu-id="dab42-137">The order of spherical harmonics.</span></span>                        |
| <span data-ttu-id="dab42-138">l<sub>i</sub></span><span class="sxs-lookup"><span data-stu-id="dab42-138">l<sub>i</sub></span></span>    | <span data-ttu-id="dab42-139">Un coeficiente.</span><span class="sxs-lookup"><span data-stu-id="dab42-139">A coefficient.</span></span>                                           |
| <span data-ttu-id="dab42-140">Y<sub>i (s)</sub></span><span class="sxs-lookup"><span data-stu-id="dab42-140">Y<sub>i(s)</sub></span></span> | <span data-ttu-id="dab42-141">Función de base en la esfera.</span><span class="sxs-lookup"><span data-stu-id="dab42-141">Some basis function over the sphere.</span></span>                     |



 

<span data-ttu-id="dab42-142">La colección de estos coeficientes, L ', proporciona una aproximación óptima para las funciones L (s) con las funciones de base Y.</span><span class="sxs-lookup"><span data-stu-id="dab42-142">The collection of these coefficients, L', provides the optimal approximation for function L(s) with the basis functions Y(s).</span></span> <span data-ttu-id="dab42-143">Al sustituir y distribuir, se produce la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="dab42-143">Substituting and distributing yields the following equation.</span></span>

![ecuación del Radiance de salida después de sustituir l (s) y distribuir](images/prt-theory-eq3.png)

<span data-ttu-id="dab42-145">La parte entera de Y<sub>i (s)</sub>VP ₍ s ₎ HNP ₍ s ₎ es un coeficiente de transferencia t<sub>PI</sub> que el simulador calcula para cada vértice de la malla.</span><span class="sxs-lookup"><span data-stu-id="dab42-145">The integral of Y<sub>i(s)</sub>Vₚ₍ₛ₎Hₙₚ₍ₛ₎ is a transfer coefficient t<sub>pi</sub> that the simulator precomputes for every vertex on the mesh.</span></span> <span data-ttu-id="dab42-146">Al sustituir esto, se produce la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="dab42-146">Substituting this yields the following equation.</span></span>

![ecuación del Radiance de salida después de sustituir el coeficiente de transferencia](images/prt-theory-eq4.png)

<span data-ttu-id="dab42-148">Si se cambia a notación vectorial, se produce la siguiente ecuación sin comprimir para calcular el Radiance de salida de cada canal.</span><span class="sxs-lookup"><span data-stu-id="dab42-148">Changing this to vector notation yields the following uncompressed equation to calculate exit radiance for each channel.</span></span>

![ecuación del Radiance de salida después de cambiar a notación vectorial](images/prt-theory-eq5.png)

<span data-ttu-id="dab42-150">donde:</span><span class="sxs-lookup"><span data-stu-id="dab42-150">where:</span></span>



| <span data-ttu-id="dab42-151">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dab42-151">Parameter</span></span>     | <span data-ttu-id="dab42-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab42-152">Description</span></span>                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab42-153">RP</span><span class="sxs-lookup"><span data-stu-id="dab42-153">Rₚ</span></span>            | <span data-ttu-id="dab42-154">El Radiance de salida en el vértice p.</span><span class="sxs-lookup"><span data-stu-id="dab42-154">The exit radiance at vertex p.</span></span>                                                                                                                                                      |
| <span data-ttu-id="dab42-155">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="dab42-155">p<sub>d</sub></span></span> | <span data-ttu-id="dab42-156">Albedo de la superficie.</span><span class="sxs-lookup"><span data-stu-id="dab42-156">The albedo of the surface.</span></span>                                                                                                                                                          |
| <span data-ttu-id="dab42-157">CG</span><span class="sxs-lookup"><span data-stu-id="dab42-157">L'</span></span>            | <span data-ttu-id="dab42-158">Vector de l<sub>i</sub>y es la proyección de la Radiance de origen en las funciones de base de armónico esférica.</span><span class="sxs-lookup"><span data-stu-id="dab42-158">The vector of l<sub>i</sub>, and is the projection of the source radiance into the spherical harmonic basis functions.</span></span> <span data-ttu-id="dab42-159">Se trata de un vector de pedido ² de coeficientees armónicos esféricos.</span><span class="sxs-lookup"><span data-stu-id="dab42-159">This is an order² vector of spherical harmonic coefficients.</span></span> |
| <span data-ttu-id="dab42-160">Supervisor</span><span class="sxs-lookup"><span data-stu-id="dab42-160">Tₚ</span></span>            | <span data-ttu-id="dab42-161">Vector de transferencia de pedido ² para el vértice p.</span><span class="sxs-lookup"><span data-stu-id="dab42-161">An order² transfer vector for vertex p.</span></span> <span data-ttu-id="dab42-162">El simulador divide los coeficientes de transferencia por p.</span><span class="sxs-lookup"><span data-stu-id="dab42-162">The simulator divides the transfer coefficients by p.</span></span>                                                                                       |



 

<span data-ttu-id="dab42-163">Ambos vectores son un vector de pedido ² de coeficientees armónicos esféricos, por lo que se debe tener en cuenta que se trata simplemente de un producto punto.</span><span class="sxs-lookup"><span data-stu-id="dab42-163">Both of these vectors are an order² vector of spherical harmonic coefficients, so notice that this is simply a dot product.</span></span> <span data-ttu-id="dab42-164">Dependiendo del orden, el punto puede ser caro, por lo que se puede usar la compresión.</span><span class="sxs-lookup"><span data-stu-id="dab42-164">Depending on the order, the dot can be expensive so compression can be used.</span></span> <span data-ttu-id="dab42-165">Un algoritmo denominado análisis de componentes principales en clúster (CPCA) comprime de forma eficaz los datos.</span><span class="sxs-lookup"><span data-stu-id="dab42-165">An algorithm called Clustered Principal Component Analysis (CPCA) efficiently compresses the data.</span></span> <span data-ttu-id="dab42-166">Esto permite el uso de una aproximación armónica esférica de orden superior, lo que da como resultado sombras más nítidas.</span><span class="sxs-lookup"><span data-stu-id="dab42-166">This enables the use of a higher-order spherical harmonic approximation which results in sharper shadows.</span></span>

<span data-ttu-id="dab42-167">CPCA proporciona la siguiente ecuación para aproximarse al vector de transferencia.</span><span class="sxs-lookup"><span data-stu-id="dab42-167">CPCA provides the following equation to approximate the transfer vector.</span></span>

![ecuación del vector de transferencia aproximado](images/prt-theory-eq6.png)

<span data-ttu-id="dab42-169">donde:</span><span class="sxs-lookup"><span data-stu-id="dab42-169">where:</span></span>



| <span data-ttu-id="dab42-170">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dab42-170">Parameter</span></span>      | <span data-ttu-id="dab42-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab42-171">Description</span></span>                                          |
|----------------|------------------------------------------------------|
| <span data-ttu-id="dab42-172">Supervisor</span><span class="sxs-lookup"><span data-stu-id="dab42-172">Tₚ</span></span>             | <span data-ttu-id="dab42-173">Vector de transferencia para el vértice p.</span><span class="sxs-lookup"><span data-stu-id="dab42-173">The transfer vector for vertex p.</span></span>                    |
| <span data-ttu-id="dab42-174">MK</span><span class="sxs-lookup"><span data-stu-id="dab42-174">Mₖ</span></span>             | <span data-ttu-id="dab42-175">La media del clúster k.</span><span class="sxs-lookup"><span data-stu-id="dab42-175">The mean for cluster k.</span></span>                              |
| <span data-ttu-id="dab42-176">j</span><span class="sxs-lookup"><span data-stu-id="dab42-176">j</span></span>              | <span data-ttu-id="dab42-177">Entero que suma el número de vectores PCA.</span><span class="sxs-lookup"><span data-stu-id="dab42-177">An integer that sums over the number of PCA vectors.</span></span> |
| <span data-ttu-id="dab42-178">N</span><span class="sxs-lookup"><span data-stu-id="dab42-178">N</span></span>              | <span data-ttu-id="dab42-179">El número de vectores PCA.</span><span class="sxs-lookup"><span data-stu-id="dab42-179">The number of PCA vectors.</span></span>                           |
| <span data-ttu-id="dab42-180">en<sub>blanco</sub></span><span class="sxs-lookup"><span data-stu-id="dab42-180">w<sub>pj</sub></span></span> | <span data-ttu-id="dab42-181">Peso del PCA de JTH para el punto p.</span><span class="sxs-lookup"><span data-stu-id="dab42-181">The jth PCA weight for point p.</span></span>                      |
| <span data-ttu-id="dab42-182">B<sub>KJ</sub></span><span class="sxs-lookup"><span data-stu-id="dab42-182">B<sub>kj</sub></span></span> | <span data-ttu-id="dab42-183">Vector de base del PCA de JTH para el clúster k.</span><span class="sxs-lookup"><span data-stu-id="dab42-183">The jth PCA basis vector for cluster k.</span></span>              |



 

<span data-ttu-id="dab42-184">Un clúster es simplemente un número de vértices que comparten el mismo vector medio.</span><span class="sxs-lookup"><span data-stu-id="dab42-184">A cluster is simply some number of vertices that share the same mean vector.</span></span> <span data-ttu-id="dab42-185">A continuación se describe cómo obtener la media del clúster, las ponderaciones del PCA, los vectores de base del PCA y los identificadores de clúster de los vértices.</span><span class="sxs-lookup"><span data-stu-id="dab42-185">How to get the cluster mean, the PCA weights, the PCA basis vectors, and the cluster ids for the vertices is discussed below.</span></span>

<span data-ttu-id="dab42-186">La sustitución de estas dos ecuaciones produce:</span><span class="sxs-lookup"><span data-stu-id="dab42-186">Substituting these two equations yields:</span></span>

![ecuación del Radiance de salida después de sustituir el vector de transferencia](images/prt-theory-eq7.png)

<span data-ttu-id="dab42-188">A continuación, la distribución del producto DOT produce la siguiente ecuación.</span><span class="sxs-lookup"><span data-stu-id="dab42-188">Then distributing the dot product yields the following equation.</span></span>

![ecuación del Radiance de salida después de distribuir el producto de punto](images/prt-theory-eq8.png)

<span data-ttu-id="dab42-190">Dado que ambos (MK · L ') y (B<sub>KJ</sub>· L ') son constantes por vértice, el ejemplo calcula estos valores con la CPU y los pasa como constantes en el sombreador de vértices; Dado que los cambios en w<sub>PJ</sub> para cada vértice, el ejemplo almacena estos datos por vértice en el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="dab42-190">Because both (Mₖ· L') and (B<sub>kj</sub>· L') are constant per vertex, the sample calculates these values with the CPU and passes them as constants into the vertex shader; because w<sub>pj</sub> changes for each vertex, the sample stores this per-vertex data in the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dab42-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dab42-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab42-192">Transferencia Radiance precalculada</span><span class="sxs-lookup"><span data-stu-id="dab42-192">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



