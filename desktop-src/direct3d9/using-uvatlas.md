---
description: Muchas técnicas de representación y generación de contenido requieren un mapa único y no superpuesto de una señal 2D (como una textura) en una malla.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Usar UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b335dd6ea94a3db0c0760b0d07a0b8df3fe4c7c
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279709"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="beb6d-103">Usar UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="beb6d-103">Using UVAtlas (Direct3D 9)</span></span>

<span data-ttu-id="beb6d-104">Muchas técnicas de representación y generación de contenido requieren un mapa único y no superpuesto de una señal 2D (como una textura) en una malla.</span><span class="sxs-lookup"><span data-stu-id="beb6d-104">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="beb6d-105">Estas técnicas incluyen:</span><span class="sxs-lookup"><span data-stu-id="beb6d-105">Such techniques include:</span></span>

-   <span data-ttu-id="beb6d-106">Asignación normal/de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="beb6d-106">Normal/displacement mapping</span></span>
-   <span data-ttu-id="beb6d-107">Simulaciones de PRT de espacio de textura y mapas ligeros</span><span class="sxs-lookup"><span data-stu-id="beb6d-107">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="beb6d-108">Dibujo de Surface</span><span class="sxs-lookup"><span data-stu-id="beb6d-108">Surface painting</span></span>
-   <span data-ttu-id="beb6d-109">Iluminación de espacio de textura</span><span class="sxs-lookup"><span data-stu-id="beb6d-109">Texture-space lighting</span></span>

<span data-ttu-id="beb6d-110">La generación manual de una asignación UV es a menudo lenta y tediosa. Esto es especialmente cierto cuando la geometría de entrada es una utilización de espacio de textura compleja y eficiente y de baja distorsión.</span><span class="sxs-lookup"><span data-stu-id="beb6d-110">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="beb6d-111">En la ilustración siguiente se muestra un ejemplo de malla y su Atlas de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="beb6d-111">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Muestra una malla de ejemplo y su Atlas de textura correspondiente.](images/uvatlas1.jpg)

<span data-ttu-id="beb6d-113">Este ejemplo muestra una malla (a la izquierda) y el mapa normal de espacio UV correspondiente (a la derecha).</span><span class="sxs-lookup"><span data-stu-id="beb6d-113">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="beb6d-114">Tenga en cuenta que el Atlas de textura contiene varios grupos o clústeres de datos. cada clúster se denomina gráfico y en el ejemplo anterior, muestra contiene los datos normales de una parte de la malla.</span><span class="sxs-lookup"><span data-stu-id="beb6d-114">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="beb6d-115">Las API de D3DX UVAtlas generan automáticamente un Atlas de texturas no superpuestos óptima.</span><span class="sxs-lookup"><span data-stu-id="beb6d-115">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="beb6d-116">Las API proporcionan parámetros de entrada que le permiten:</span><span class="sxs-lookup"><span data-stu-id="beb6d-116">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="beb6d-117">Minimizar el estiramiento de textura, la distorsión y el submuestreo.</span><span class="sxs-lookup"><span data-stu-id="beb6d-117">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="beb6d-118">Maximice la densidad de empaquetado de espacio de textura para un uso eficaz de la memoria.</span><span class="sxs-lookup"><span data-stu-id="beb6d-118">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="beb6d-119">Proporcionar un muestreo uniforme en la malla, lo que minimiza las discontinuidades en la frecuencia de muestreo.</span><span class="sxs-lookup"><span data-stu-id="beb6d-119">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="beb6d-120">Cómo funciona UVAtlas</span><span class="sxs-lookup"><span data-stu-id="beb6d-120">How UVAtlas Works</span></span>

<span data-ttu-id="beb6d-121">Las API de UVAtlas (consulte [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generan un Atlas de textura mediante la creación de particiones de una superficie en los gráficos y el empaquetado de los gráficos en un Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="beb6d-121">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="beb6d-122">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) y [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) para realizar estos pasos por separado. o bien, use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) para particionar, parametrizar y empaquetar en una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="beb6d-122">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="beb6d-123">Creación de particiones y parametrización de una malla</span><span class="sxs-lookup"><span data-stu-id="beb6d-123">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="beb6d-124">Usar decenas de métricas integradas para controlar la parametrización</span><span class="sxs-lookup"><span data-stu-id="beb6d-124">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="beb6d-125">Usar datos de proximidad para las arrugas especificadas por el usuario</span><span class="sxs-lookup"><span data-stu-id="beb6d-125">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="beb6d-126">Empaquetar gráficos en un Atlas</span><span class="sxs-lookup"><span data-stu-id="beb6d-126">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="beb6d-127">Creación de particiones y parametrización de una malla</span><span class="sxs-lookup"><span data-stu-id="beb6d-127">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="beb6d-128">En primer lugar, la malla está dividida en gráficos y, a continuación, cada gráfico tiene parámetros en su propio \[ \] espacio de UV de 0, 1.</span><span class="sxs-lookup"><span data-stu-id="beb6d-128">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="beb6d-129">Un cilindro puede incluir parámetros en un gráfico; por otra parte, una esfera necesitará dos gráficos, como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="beb6d-129">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![Ilustración de una esfera dividida en dos gráficos](images/uvatlas3.jpg)

<span data-ttu-id="beb6d-131">Una malla que se puede parametrizar con un solo gráfico se clasifica como "homeomorphic a un disco", lo que significa que se puede repartir un disco infinitamente flexible y estirable en el gráfico y cubrir la geometría perfectamente.</span><span class="sxs-lookup"><span data-stu-id="beb6d-131">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="beb6d-132">Esta ampliación, denominada homeomorphism, es una función bidireccional. lo que significa que puede pasar de una parametrización a otra sin perder información.</span><span class="sxs-lookup"><span data-stu-id="beb6d-132">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="beb6d-133">Muy pocas mallas del mundo real se pueden parametrizar en dos dimensiones sin separar la malla en clústeres o gráficos.</span><span class="sxs-lookup"><span data-stu-id="beb6d-133">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="beb6d-134">En la ilustración siguiente se muestra otra malla de ejemplo y su Atlas de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="beb6d-134">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Muestra una malla de ejemplo con diferentes formas y su Atlas de textura correspondiente.](images/uvatlas2.jpg)

<span data-ttu-id="beb6d-136">Hay dos parámetros que determinan el número de gráficos creados:</span><span class="sxs-lookup"><span data-stu-id="beb6d-136">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="beb6d-137">El número máximo de gráficos permitidos para Atlas</span><span class="sxs-lookup"><span data-stu-id="beb6d-137">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="beb6d-138">La cantidad máxima de stretch permitida para cada gráfico</span><span class="sxs-lookup"><span data-stu-id="beb6d-138">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="beb6d-139">La cantidad de stretch determinará el número de gráficos que se generan y la calidad general del muestreo.</span><span class="sxs-lookup"><span data-stu-id="beb6d-139">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="beb6d-140">Estire los intervalos desde 0,0 (sin Stretch) hasta 1,0 (cualquier cantidad de Stretch).</span><span class="sxs-lookup"><span data-stu-id="beb6d-140">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="beb6d-141">D3DXUVAtlasCreate y D3DXUVAtlasPartition devuelven el estiramiento máximo generado por el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="beb6d-141">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="beb6d-142">En la ilustración siguiente se muestra otra malla de ejemplo y su Atlas de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="beb6d-142">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Ilustración de una malla de ejemplo y su Atlas de textura correspondiente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="beb6d-144">Usar decenas de métricas integradas para controlar la parametrización</span><span class="sxs-lookup"><span data-stu-id="beb6d-144">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="beb6d-145">La priorización del espacio de textura se puede especificar por triángulo.</span><span class="sxs-lookup"><span data-stu-id="beb6d-145">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="beb6d-146">Se pueden proporcionar decenas de métricas integradas para controlar cómo se ajustan los triángulos en el Atlas de espacio de textura resultante.</span><span class="sxs-lookup"><span data-stu-id="beb6d-146">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="beb6d-147">IMT se puede especificar directamente o calcular según una señal de entrada mediante las funciones de cálculo de D3DX IMT.</span><span class="sxs-lookup"><span data-stu-id="beb6d-147">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="beb6d-148">Una métrica integrada tensores (o IMT) es una matriz de 2x2 simétrica que describe cómo se ajusta un triángulo en el Atlas.</span><span class="sxs-lookup"><span data-stu-id="beb6d-148">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="beb6d-149">Cada IMT se define mediante 3 flotantes, se llama (a, b, c).</span><span class="sxs-lookup"><span data-stu-id="beb6d-149">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="beb6d-150">Se pueden organizar en una matriz de 2x2 simétrica como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="beb6d-150">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="beb6d-151">A continuación, se puede usar IMT para encontrar la distancia entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="beb6d-151">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="beb6d-152">Dados dos vectores v1 y V2, donde:</span><span class="sxs-lookup"><span data-stu-id="beb6d-152">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="beb6d-153">La distancia entre V1 y V2 puede calcularse como:</span><span class="sxs-lookup"><span data-stu-id="beb6d-153">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="beb6d-154">En otras palabras, el vector (s, t) podría ser la magnitud de stretch en una dirección arbitraria en el espacio u-v.</span><span class="sxs-lookup"><span data-stu-id="beb6d-154">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="beb6d-155">En este caso, el vector s es una dirección entre el primero y el segundo, y t es el producto cruzado de la normal y s.</span><span class="sxs-lookup"><span data-stu-id="beb6d-155">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="beb6d-156">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="beb6d-156">For instance:</span></span>


```
(1,1) * (1,1) = (2,2)
        (1,1)
IMT(1,1,1) scales by 2
```




```
(1,-1) * (1,1) = (0,0)
         (1,1)
IMT(2,0,2) scales by 2 with no shearing
```



<span data-ttu-id="beb6d-157">IMT se puede especificar directamente o calcular según una señal de entrada mediante las funciones de cálculo de D3DX IMT: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal y D3DXComputeIMTFromTexture \_ Graphics.</span><span class="sxs-lookup"><span data-stu-id="beb6d-157">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="beb6d-158">Especifique los datos de IMT directamente si desea controlar cómo se asigna el espacio de textura a los triángulos individuales.</span><span class="sxs-lookup"><span data-stu-id="beb6d-158">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="beb6d-159">Al hacerlo, asigne más área en el Atlas a las áreas importantes de una malla (como el logotipo o la esfera de un carácter o las regiones de una escena cerca de la ruta de acceso de un jugador).</span><span class="sxs-lookup"><span data-stu-id="beb6d-159">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="beb6d-160">Al especificar IMT que son múltiplos de la matriz de identidad, los triángulos resultantes se escalarán uniformemente en el espacio de textura.</span><span class="sxs-lookup"><span data-stu-id="beb6d-160">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="beb6d-161">Por ejemplo, dado un mapa normal de alta resolución, puede calcular IMT para proporcionar más espacio de textura a áreas de señal de mayor frecuencia en el mapa normal.</span><span class="sxs-lookup"><span data-stu-id="beb6d-161">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="beb6d-162">Los triángulos que son "planos" (que se asignan a las regiones constantes del mapa normal original) recibirán menos espacio de textura.</span><span class="sxs-lookup"><span data-stu-id="beb6d-162">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="beb6d-163">Los triángulos que contienen una gran cantidad de detalles de mapa normal recibirán más área de textura en el resultado final.</span><span class="sxs-lookup"><span data-stu-id="beb6d-163">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="beb6d-164">Después, puede volver a muestrear el mapa normal en una textura más pequeña pero mantener los detalles, o bien puede volver a calcular el mapa normal con la asignación UV más óptima.</span><span class="sxs-lookup"><span data-stu-id="beb6d-164">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="beb6d-165">Usar datos de proximidad para las arrugas especificadas por el usuario</span><span class="sxs-lookup"><span data-stu-id="beb6d-165">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="beb6d-166">Se puede proporcionar información de adyacencia definida por el usuario a la función de particionamiento para describir las arrugas predefinidas en la malla y, por tanto, definir un límite de gráfico entre caras adyacentes.</span><span class="sxs-lookup"><span data-stu-id="beb6d-166">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="beb6d-167">Esta es una manera sencilla de que el autor de la llamada especifique su propia creación de particiones de gráfico como entrada en el algoritmo, lo que perfeccionará aún más los gráficos para aumentar el tamaño en el máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="beb6d-167">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="beb6d-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="beb6d-168">Example</span></span>

<span data-ttu-id="beb6d-169">En este ejemplo se muestra cómo podría usar las API de UVAtlas y el visor de DirectX (Dxviewer.exe) para buscar y corregir discontinuidades en el modelo que puede afectar drásticamente al tamaño de su Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="beb6d-169">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="beb6d-170">Puede obtener Dxviewer.exe y obtener información sobre él desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="beb6d-170">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="beb6d-171">Dxviewer.exe se quitó del SDK de DirectX después de la versión de agosto de 2009, por lo que necesitará al menos el SDK de DirectX de agosto de 2009.</span><span class="sxs-lookup"><span data-stu-id="beb6d-171">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="beb6d-172">Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="beb6d-172">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="beb6d-173">Supongamos que comenzó con algún modelo en su software de generación de contenido favorito (en este ejemplo se usa un modelo de encabezado Dwarf creado en Maya).</span><span class="sxs-lookup"><span data-stu-id="beb6d-173">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="beb6d-174">Exporte el modelo con textura a un archivo. x y cree un Atlas de textura con D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="beb6d-174">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="beb6d-175">El Atlas de textura resultante tendría un aspecto similar al de la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="beb6d-175">The resulting texture atlas would look something like the following illustration.</span></span>

![Ilustración de un Atlas para un modelo Dwarf](images/uvatlas5.jpg)

<span data-ttu-id="beb6d-177">El Atlas tiene 22 gráficos y un ajuste máximo de 0,994.</span><span class="sxs-lookup"><span data-stu-id="beb6d-177">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="beb6d-178">Ahora Fíjese en el modelo con textura para ver hasta qué grado se asigna el Atlas de textura a la geometría.</span><span class="sxs-lookup"><span data-stu-id="beb6d-178">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="beb6d-179">Para ello, cargue el modelo en la herramienta Visor:</span><span class="sxs-lookup"><span data-stu-id="beb6d-179">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="beb6d-180">Abra la herramienta visor desde las utilidades de DirectX.</span><span class="sxs-lookup"><span data-stu-id="beb6d-180">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="beb6d-181">Cargue el archivo. x haciendo clic en el botón abrir.</span><span class="sxs-lookup"><span data-stu-id="beb6d-181">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="beb6d-182">Habilitar la opción de visualización de arrugas haciendo clic en el botón ver y seleccionando arrugas en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="beb6d-182">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="beb6d-183">En la ilustración siguiente se muestra lo que debería ver en la herramienta visor.</span><span class="sxs-lookup"><span data-stu-id="beb6d-183">The following illustration shows what you should see in the viewer tool.</span></span>

![Ilustración de una malla con textura en la herramienta Visor](images/uvatlas6c.jpg)

<span data-ttu-id="beb6d-185">Cada línea es una arruga que es un borde adyacente entre dos gráficos en el Atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="beb6d-185">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="beb6d-186">El número de gráficos generados por el algoritmo está causado por pequeñas diferencias, quizás debido a discontinuidades en las normales.</span><span class="sxs-lookup"><span data-stu-id="beb6d-186">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="beb6d-187">Estas pequeñas diferencias se pueden reducir con los datos de soldadura, es decir, forzar que los datos que son casi iguales sean iguales.</span><span class="sxs-lookup"><span data-stu-id="beb6d-187">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="beb6d-188">Para soldar las normales y skinweights:</span><span class="sxs-lookup"><span data-stu-id="beb6d-188">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="beb6d-189">Ejecute la herramienta de operaciones de DirectX (dxops.exe) con la siguiente línea de comandos en la malla (reemplace "modelName. x" por el nombre del modelo):</span><span class="sxs-lookup"><span data-stu-id="beb6d-189">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="beb6d-190">Con esto se comparan los valores normales y skinweights, y donde se diferencian por un valor inferior a 2,01, los datos se hacen iguales.</span><span class="sxs-lookup"><span data-stu-id="beb6d-190">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="beb6d-191">En las ilustraciones siguientes se muestra un cierre del ojo para ver las arrugas antes de la soldadura (a la izquierda) y las arrugas después de la soldadura (a la derecha):</span><span class="sxs-lookup"><span data-stu-id="beb6d-191">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![Ilustración de dobleces antes de la soldadura](images/uvatlas6a.jpg)![Ilustración de arrugas tras la soldadura](images/uvatlas6b.jpg)

<span data-ttu-id="beb6d-194">Figura 7: eliminación de dobleces por soldadura</span><span class="sxs-lookup"><span data-stu-id="beb6d-194">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="beb6d-195">En este ejemplo, la soldadura quitó 86 vértices de la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="beb6d-195">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="beb6d-196">Con menos arrugas en la malla, puede volver a generar el Atlas, tal como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="beb6d-196">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![Ilustración del nuevo Atlas con dobleces quitados](images/uvatlas8.jpg)

<span data-ttu-id="beb6d-198">El Atlas solo tiene 7 gráficos y un ajuste máximo de aproximadamente 0,0776.</span><span class="sxs-lookup"><span data-stu-id="beb6d-198">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="beb6d-199">El nuevo Atlas ahora se ajusta a una textura más pequeña (aproximadamente un 30% más pequeño en este ejemplo).</span><span class="sxs-lookup"><span data-stu-id="beb6d-199">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="beb6d-200">Empaquetar gráficos en un Atlas</span><span class="sxs-lookup"><span data-stu-id="beb6d-200">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="beb6d-201">Una vez que se ha particionado una malla en gráficos con parámetros individuales, los gráficos deben empaquetarse de forma eficaz en un único mapa de textura.</span><span class="sxs-lookup"><span data-stu-id="beb6d-201">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="beb6d-202">Esto se realiza como el segundo paso de D3DXUVAtlasCreate o se puede invocar explícitamente mediante una llamada a D3DXUVAtlasPack.</span><span class="sxs-lookup"><span data-stu-id="beb6d-202">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="beb6d-203">Los gráficos empaquetados están separados por un ancho de medianil especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="beb6d-203">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="beb6d-204">El ancho del medianil es la cantidad de separación entre los gráficos y permite la interpolación bilineal y la asignación de MIP para evitar la representación de artefactos en los límites del gráfico.</span><span class="sxs-lookup"><span data-stu-id="beb6d-204">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="beb6d-205">D3DX proporciona una interfaz para rellenar automáticamente estos medianils; consulte [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="beb6d-205">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="beb6d-206">Integración de UVAtlas en la canalización</span><span class="sxs-lookup"><span data-stu-id="beb6d-206">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="beb6d-207">Además de ser invocado por el artista antes del dibujo de texturas, estas funciones se pueden integrar en una canalización de arte automatizada.</span><span class="sxs-lookup"><span data-stu-id="beb6d-207">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="beb6d-208">Por ejemplo, una llamada a UVAtlas se puede emitir automáticamente después de actualizar un recurso, antes de realizar una simulación de PRT o un paso de asignación normal.</span><span class="sxs-lookup"><span data-stu-id="beb6d-208">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="beb6d-209">Esto evita la necesidad de reparar manualmente la asignación UV de un objeto si se ha modificado la topología de la malla.</span><span class="sxs-lookup"><span data-stu-id="beb6d-209">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="beb6d-210">Consulte la [herramienta de Command-Line de Atlas de UV (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) para obtener un ejemplo del uso de las funciones de UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="beb6d-210">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="beb6d-211">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="beb6d-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beb6d-212">Temas avanzados</span><span class="sxs-lookup"><span data-stu-id="beb6d-212">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
