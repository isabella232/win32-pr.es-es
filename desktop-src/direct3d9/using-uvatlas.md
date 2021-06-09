---
description: Muchas técnicas de representación y generación de contenido requieren un mapa único y no superpuesto de una señal 2D (como una textura) en una malla.
ms.assetid: 0ec19e8c-2a14-4392-93de-7ab832784085
title: Uso de UVAtlas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8faeaa0a416f6f062c81c4101ff47d5222ca75d
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826333"
---
# <a name="using-uvatlas-direct3d-9"></a><span data-ttu-id="7c16b-103">Uso de UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7c16b-103">Using UVAtlas (Direct3D 9)</span></span>

> [!NOTE]
> <span data-ttu-id="7c16b-104">UVAtlas se envió originalmente en la biblioteca de utilidad D3DX9 ahora en desuso.</span><span class="sxs-lookup"><span data-stu-id="7c16b-104">UVAtlas was originally shipped in the now-deprecated D3DX9 utilty library.</span></span> <span data-ttu-id="7c16b-105">La versión más reciente está disponible en [UV Atlas Command-Line Tool (uvatlas.exe).](https://github.com/Microsoft/UVAtlas)</span><span class="sxs-lookup"><span data-stu-id="7c16b-105">The latest version is available at [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas).</span></span>

<span data-ttu-id="7c16b-106">Muchas técnicas de representación y generación de contenido requieren un mapa único y no superpuesto de una señal 2D (como una textura) en una malla.</span><span class="sxs-lookup"><span data-stu-id="7c16b-106">Many rendering and content generation techniques require a unique, non-overlapping map of a 2D signal (such as a texture) onto a mesh.</span></span> <span data-ttu-id="7c16b-107">Estas técnicas incluyen:</span><span class="sxs-lookup"><span data-stu-id="7c16b-107">Such techniques include:</span></span>

-   <span data-ttu-id="7c16b-108">Asignación normal o de desplazamiento</span><span class="sxs-lookup"><span data-stu-id="7c16b-108">Normal/displacement mapping</span></span>
-   <span data-ttu-id="7c16b-109">Simulaciones de PRT de espacio de textura y mapas claros</span><span class="sxs-lookup"><span data-stu-id="7c16b-109">Texture-space PRT simulations and light maps</span></span>
-   <span data-ttu-id="7c16b-110">Cuadro de superficie</span><span class="sxs-lookup"><span data-stu-id="7c16b-110">Surface painting</span></span>
-   <span data-ttu-id="7c16b-111">Iluminación de espacio de textura</span><span class="sxs-lookup"><span data-stu-id="7c16b-111">Texture-space lighting</span></span>

<span data-ttu-id="7c16b-112">La generación manual de una asignación DE UV única suele llevar mucho tiempo y tediosa. esto es especialmente cierto cuando la geometría de entrada es compleja y se desea una utilización de espacio de textura eficaz o de baja distorsión.</span><span class="sxs-lookup"><span data-stu-id="7c16b-112">Generating a unique UV mapping manually is often time-consuming and tedious; this is especially true when the input geometry is complex and efficient/low-distortion texture-space utilization is desired.</span></span> <span data-ttu-id="7c16b-113">En la ilustración siguiente se muestra una malla de ejemplo y su atlas de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7c16b-113">The following illustration shows an example mesh and its corresponding texture atlas.</span></span>

![Muestra una malla de ejemplo y su atlas de textura correspondiente.](images/uvatlas1.jpg)

<span data-ttu-id="7c16b-115">En este ejemplo se muestra una malla (a la izquierda) y el mapa normal de espacio UV correspondiente (a la derecha).</span><span class="sxs-lookup"><span data-stu-id="7c16b-115">This example shows a mesh (on the left) and the corresponding UV-space normal map (on the right).</span></span> <span data-ttu-id="7c16b-116">Observe que el atlas de textura contiene varios grupos o clústeres de datos; Cada clúster se denomina gráfico y, en el ejemplo anterior, las pantallas contienen los datos normales de una parte de la malla.</span><span class="sxs-lookup"><span data-stu-id="7c16b-116">Notice that the texture atlas contains several groups or clusters of data; each cluster is called a chart and in the example above, displays contains the normal data for a portion of the mesh.</span></span>

<span data-ttu-id="7c16b-117">Las API de UVAtlas de D3DX generan automáticamente un atlas de textura óptimo y no superpuesto.</span><span class="sxs-lookup"><span data-stu-id="7c16b-117">The D3DX UVAtlas APIs automatically generate an optimal, non-overlapping texture atlas.</span></span> <span data-ttu-id="7c16b-118">Las API proporcionan parámetros de entrada que le permiten:</span><span class="sxs-lookup"><span data-stu-id="7c16b-118">The APIs provide input parameters that allow you to:</span></span>

-   <span data-ttu-id="7c16b-119">Minimice la extensión de textura, la distorsión y el submuestreo.</span><span class="sxs-lookup"><span data-stu-id="7c16b-119">Minimize texture stretch, distortion, and undersampling.</span></span>
-   <span data-ttu-id="7c16b-120">Maximice la densidad de empaquetado del espacio de textura para un uso eficaz de la memoria.</span><span class="sxs-lookup"><span data-stu-id="7c16b-120">Maximize texture-space packing density for efficient use of memory.</span></span>
-   <span data-ttu-id="7c16b-121">Proporcione un muestreo uniforme en la malla, lo que minimiza las discontinuidades en la frecuencia de muestreo.</span><span class="sxs-lookup"><span data-stu-id="7c16b-121">Provide an even sampling across the mesh, minimizing discontinuities in sampling frequency.</span></span>

## <a name="how-uvatlas-works"></a><span data-ttu-id="7c16b-122">Funcionamiento de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="7c16b-122">How UVAtlas Works</span></span>

<span data-ttu-id="7c16b-123">Las API de UVAtlas (consulte FUNCIONES DE [UVAtlas)](dx9-graphics-reference-d3dx-functions-uvatlas.md)generan un atlas de textura mediante la creación de particiones de una superficie en gráficos y el empaquetado de los gráficos en un atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="7c16b-123">The UVAtlas APIs (see [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md)) generate a texture atlas by partitioning a surface into charts and packing the charts into a texture atlas.</span></span> <span data-ttu-id="7c16b-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) y [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) para realizar estos pasos por separado; o use [**D3DXUVAtlasCreate para**](d3dxuvatlascreate.md) crear particiones, parametrizar y empaquetar en una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="7c16b-124">Use [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md) and [**D3DXUVAtlasPack**](d3dxuvatlaspack.md) to perform these steps separately; or use [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md) to partition, parameterize and pack in a single call.</span></span>

-   [<span data-ttu-id="7c16b-125">Creación de particiones y parametrización de una malla</span><span class="sxs-lookup"><span data-stu-id="7c16b-125">Partitioning and Parameterizing a Mesh</span></span>](#partitioning-and-parameterizing-a-mesh)
-   [<span data-ttu-id="7c16b-126">Uso de tensores de métricas integrados para controlar la parametrización</span><span class="sxs-lookup"><span data-stu-id="7c16b-126">Using Integrated Metric Tensors to Control Parameterization</span></span>](#using-integrated-metric-tensors-to-control-parameterization)
-   [<span data-ttu-id="7c16b-127">Usar datos de adyacencia para los creases especificados por el usuario</span><span class="sxs-lookup"><span data-stu-id="7c16b-127">Using Adjacency Data for User Specified Creases</span></span>](#using-adjacency-data-for-user-specified-creases)
-   [<span data-ttu-id="7c16b-128">Empaquetado de gráficos en un atlas</span><span class="sxs-lookup"><span data-stu-id="7c16b-128">Packing Charts Into an Atlas</span></span>](#packing-charts-into-an-atlas)

### <a name="partitioning-and-parameterizing-a-mesh"></a><span data-ttu-id="7c16b-129">Creación de particiones y parametrización de una malla</span><span class="sxs-lookup"><span data-stu-id="7c16b-129">Partitioning and Parameterizing a Mesh</span></span>

<span data-ttu-id="7c16b-130">En primer lugar, la malla se divide en gráficos y, a continuación, cada gráfico se parametriza en su propio \[ espacio UV 0,1. \]</span><span class="sxs-lookup"><span data-stu-id="7c16b-130">First, the mesh is partitioned into charts, then each chart is parameterized into its own \[0,1\] UV-space.</span></span> <span data-ttu-id="7c16b-131">Un cilindro se puede parametrizar mediante un gráfico; Por otro lado, una esfera requerirá dos gráficos, como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c16b-131">A cylinder can be parameterized by one chart; a sphere on the other hand will require two charts, as shown in the following illustration.</span></span>

![ilustración de una esfera particionada en dos gráficos](images/uvatlas3.jpg)

<span data-ttu-id="7c16b-133">Una malla que se puede parametrizar con un solo gráfico se clasifica como "homeórfico en un disco", lo que significa que podría extender un disco infinitamente flexible y infinitamente flexible sobre el gráfico y cubrir perfectamente la geometría.</span><span class="sxs-lookup"><span data-stu-id="7c16b-133">A mesh which can be parameterized with a single chart is classified as "homeomorphic to a disk", meaning you could spread out an infinitely flexible, infinitely stretchable disk over the chart and cover the geometry perfectly.</span></span> <span data-ttu-id="7c16b-134">Esta extensión, denominada homeomorfismo, es una función bidireccional; lo que significa que puede pasar de una parametrización a otra sin perder información.</span><span class="sxs-lookup"><span data-stu-id="7c16b-134">This stretching, called a homeomorphism, is a bidirectional function; which means you can go from one parameterization to the other without losing information.</span></span>

<span data-ttu-id="7c16b-135">Muy pocas mallas reales se pueden parametrizar en dos dimensiones sin separar la malla en clústeres o gráficos.</span><span class="sxs-lookup"><span data-stu-id="7c16b-135">Very few real-world meshes can be parameterized into two dimensions without separating the mesh into clusters, or charts.</span></span> <span data-ttu-id="7c16b-136">En la ilustración siguiente se muestra otra malla de ejemplo y su atlas de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7c16b-136">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![Muestra una malla de ejemplo con diferentes formas y su atlas de textura correspondiente.](images/uvatlas2.jpg)

<span data-ttu-id="7c16b-138">Hay dos parámetros que determinan el número de gráficos creados:</span><span class="sxs-lookup"><span data-stu-id="7c16b-138">There are two parameters that determine the number of charts created:</span></span>

-   <span data-ttu-id="7c16b-139">El número máximo de gráficos permitido para el atlas</span><span class="sxs-lookup"><span data-stu-id="7c16b-139">The maximum number of charts allowed for the atlas</span></span>
-   <span data-ttu-id="7c16b-140">La cantidad máxima de stretch permitida para cada gráfico</span><span class="sxs-lookup"><span data-stu-id="7c16b-140">The maximum amount of stretch allowed for each chart</span></span>

<span data-ttu-id="7c16b-141">La cantidad de stretch determinará el número de gráficos que se generan y la calidad general del muestreo.</span><span class="sxs-lookup"><span data-stu-id="7c16b-141">The amount of stretch will determine the number of charts that are generated, and the overall quality of the sampling.</span></span> <span data-ttu-id="7c16b-142">Stretch va de 0,0 (sin stretch) a 1,0 (cualquier cantidad de stretch).</span><span class="sxs-lookup"><span data-stu-id="7c16b-142">Stretch ranges from 0.0 (no stretch) to 1.0 (any amount of stretch).</span></span> <span data-ttu-id="7c16b-143">D3DXUVAtlasCreate y D3DXUVAtlasPartition devuelven el stretch máximo generado por el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="7c16b-143">D3DXUVAtlasCreate and D3DXUVAtlasPartition return the maximum stretch generated by the algorithm.</span></span> <span data-ttu-id="7c16b-144">En la ilustración siguiente se muestra otra malla de ejemplo y su atlas de textura correspondiente.</span><span class="sxs-lookup"><span data-stu-id="7c16b-144">The following illustration shows another example mesh and its corresponding texture atlas.</span></span>

![ilustración de una malla de ejemplo y su atlas de textura correspondiente](images/uvatlas4.jpg)

### <a name="using-integrated-metric-tensors-to-control-parameterization"></a><span data-ttu-id="7c16b-146">Uso de tensores de métricas integrados para controlar la parametrización</span><span class="sxs-lookup"><span data-stu-id="7c16b-146">Using Integrated Metric Tensors to Control Parameterization</span></span>

<span data-ttu-id="7c16b-147">La priorización del espacio de textura se puede especificar por triángulo.</span><span class="sxs-lookup"><span data-stu-id="7c16b-147">Texture-space prioritization can be specified on a per-triangle basis.</span></span> <span data-ttu-id="7c16b-148">Se pueden proporcionar tensores de métricas integrados para controlar cómo se extienden los triángulos en el atlas de espacio de textura resultante.</span><span class="sxs-lookup"><span data-stu-id="7c16b-148">Integrated Metric Tensors can be provided to control how triangles are stretched in the resulting texture-space atlas.</span></span> <span data-ttu-id="7c16b-149">Las IMT se pueden especificar directamente o calcular en función de una señal de entrada mediante las funciones de cálculo D3DX IMT.</span><span class="sxs-lookup"><span data-stu-id="7c16b-149">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions.</span></span> <span data-ttu-id="7c16b-150">Un tensor de métricas integrado (o IMT) es una matriz simétrica de 2x2 que describe cómo se extiende un triángulo en el atlas.</span><span class="sxs-lookup"><span data-stu-id="7c16b-150">An integrated metric tensor (or IMT) is a symmetrical 2x2 matrix that describes how a triangle is stretched in the atlas.</span></span> <span data-ttu-id="7c16b-151">Cada IMT se define mediante 3 flotantes, llámelos (a,b,c).</span><span class="sxs-lookup"><span data-stu-id="7c16b-151">Each IMT is defined by 3 floats, call them (a,b,c).</span></span> <span data-ttu-id="7c16b-152">Se pueden organizar en una matriz simétrica de 2x2 como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="7c16b-152">They can be arranged in a symmetric 2x2 matrix like this:</span></span>


```
a b
b c
```



<span data-ttu-id="7c16b-153">A continuación, se puede usar IMT para buscar la distancia entre dos vectores.</span><span class="sxs-lookup"><span data-stu-id="7c16b-153">Then the IMT can be used to find the distance between two vectors.</span></span> <span data-ttu-id="7c16b-154">Dados dos vectores v1 y v2, donde :</span><span class="sxs-lookup"><span data-stu-id="7c16b-154">Given two vectors v1 and v2, where :</span></span>


```
vector v1
vector v2 = v1 + (s,t)
```



<span data-ttu-id="7c16b-155">La distancia entre v1 y v2 se puede calcular como:</span><span class="sxs-lookup"><span data-stu-id="7c16b-155">The distance between v1 and v2 can be calculated as:</span></span>


```
sqrt((s, t) * M * (s, t)^T)
```



<span data-ttu-id="7c16b-156">En otras palabras, el vector (s,t) podría ser la magnitud del stretch en una dirección arbitraria en el espacio u-v.</span><span class="sxs-lookup"><span data-stu-id="7c16b-156">In other words, the vector (s,t) could be the magnitude of the stretch in an arbitrary direction in u-v space.</span></span> <span data-ttu-id="7c16b-157">En este caso, el vector de es una dirección desde el primero al segundo vértice, y t es el producto cruzado de los valores normales y s.</span><span class="sxs-lookup"><span data-stu-id="7c16b-157">In this case, the s vector is a direction from the first to the second vertex, and t is the cross product of the normal and s.</span></span> <span data-ttu-id="7c16b-158">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7c16b-158">For instance:</span></span>


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



<span data-ttu-id="7c16b-159">Las IMT se pueden especificar directamente o calcular en función de una señal de entrada mediante las funciones de cálculo D3DX IMT: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal y D3DXComputeIMTFromTexture. \_</span><span class="sxs-lookup"><span data-stu-id="7c16b-159">IMT's can be specified directly or computed based on an input signal using the D3DX IMT computation functions: D3DXComputeIMTFromPerVertexSignal, D3DXComputeIMTFromPerTexelSignal, D3DXComputeIMTFromSignal, and D3DXComputeIMTFromTexture\_graphics.</span></span>

<span data-ttu-id="7c16b-160">Especifique los datos de IMT directamente si desea controlar cómo se asigna el espacio de textura a triángulos individuales.</span><span class="sxs-lookup"><span data-stu-id="7c16b-160">Specify IMT data directly if you want to control how texture-space is allocated to individual triangles.</span></span> <span data-ttu-id="7c16b-161">Al hacerlo, asigne más área en el atlas a áreas importantes de una malla (como la cara de un carácter o el logotipo del logotipo del logotipo de un logotipo o regiones de una escena cerca de la ruta de acceso de un jugador).</span><span class="sxs-lookup"><span data-stu-id="7c16b-161">By doing so, allocate more area in the atlas to important areas of a mesh (such as a character's face or chest logo, or regions of a scene near a player's walking-path).</span></span> <span data-ttu-id="7c16b-162">Al especificar IMT que son múltiplo de la matriz de identidad, los triángulos resultantes se escalarán uniformemente en el espacio de textura.</span><span class="sxs-lookup"><span data-stu-id="7c16b-162">By specifying IMT's that are multiples of the identity matrix, the resulting triangles will be scaled uniformly in texture space.</span></span>

<span data-ttu-id="7c16b-163">Por ejemplo, dado un mapa normal de alta resolución, puede calcular IMT para proporcionar más espacio de textura a las áreas de señal de mayor frecuencia en el mapa normal.</span><span class="sxs-lookup"><span data-stu-id="7c16b-163">For example, given a high-resolution normal map, you can compute IMT to provide more texture-space to areas of higher frequency signal in the normal map.</span></span> <span data-ttu-id="7c16b-164">Los triángulos que son "planos" (que se asignan a regiones constantes del mapa normal original) recibirán menos espacio de textura.</span><span class="sxs-lookup"><span data-stu-id="7c16b-164">Triangles that are "flat" (that mapped to constant regions of the original normal map) will receive less texture space.</span></span> <span data-ttu-id="7c16b-165">Los triángulos que contienen una gran cantidad de detalles del mapa normal recibirán más área de textura en el resultado final.</span><span class="sxs-lookup"><span data-stu-id="7c16b-165">Triangles that contain a great deal of normal-map detail will receive more texture area in the final result.</span></span> <span data-ttu-id="7c16b-166">A continuación, puede volver a muestrear el mapa normal en una textura más pequeña, pero mantener los detalles, o puede volver a compilar el mapa normal con la asignación UV más óptima.</span><span class="sxs-lookup"><span data-stu-id="7c16b-166">You can then resample the normal map into a smaller texture but maintain detail, or you can recompute the normal map with the more optimal UV mapping.</span></span>

### <a name="using-adjacency-data-for-user-specified-creases"></a><span data-ttu-id="7c16b-167">Usar datos de adyacencia para los creases especificados por el usuario</span><span class="sxs-lookup"><span data-stu-id="7c16b-167">Using Adjacency Data for User Specified Creases</span></span>

<span data-ttu-id="7c16b-168">Se puede proporcionar información de adyacencia definida por el usuario a la función de creación de particiones para describir los contornos predefinidos en la malla y, por tanto, definir un límite de gráfico entre las caras adyacentes.</span><span class="sxs-lookup"><span data-stu-id="7c16b-168">User-defined adjacency information can be provided to the partitioning function to describe pre-defined creases in the mesh, and thus define a chart boundary between adjacent faces.</span></span> <span data-ttu-id="7c16b-169">Se trata de una manera sencilla de que el autor de la llamada especifique su propia creación de particiones de gráfico como entrada en el algoritmo, lo que refinará aún más los gráficos para que el ajuste sea inferior al máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="7c16b-169">This is a simple way for the caller to specify their own chart partitioning as input into the algorithm, which will further refine charts to bring the stretch under the maximum allowed.</span></span>

### <a name="example"></a><span data-ttu-id="7c16b-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7c16b-170">Example</span></span>

<span data-ttu-id="7c16b-171">En este ejemplo se muestra cómo podría usar las API uvatlas y el visor de DirectX (Dxviewer.exe) para buscar y corregir discontinuidades en el modelo que pueden afectar drásticamente al tamaño del atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="7c16b-171">This example illustrates how you might use the UVAtlas APIs and the DirectX Viewer (Dxviewer.exe) to find and fix discontinuities in your model that can dramatically affect the size of your texture atlas.</span></span> <span data-ttu-id="7c16b-172">Puede obtener información Dxviewer.exe y obtener información al respecto desde el SDK de DirectX.</span><span class="sxs-lookup"><span data-stu-id="7c16b-172">You can get Dxviewer.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="7c16b-173">Dxviewer.exe se quitó del SDK de DirectX después de la versión de agosto de 2009, por lo que para obtenerlo necesitará al menos el SDK de DirectX de agosto de 2009.</span><span class="sxs-lookup"><span data-stu-id="7c16b-173">Dxviewer.exe was removed from the DirectX SDK after the August 2009 version so to get it you'll need at least the August 2009 DirectX SDK.</span></span> <span data-ttu-id="7c16b-174">Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="7c16b-174">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="7c16b-175">Suponga que ha empezado con algún modelo en su software de generación de contenido favorito (en este ejemplo se usa un modelo principal de un pequeño árbol que se creó en Maya).</span><span class="sxs-lookup"><span data-stu-id="7c16b-175">Assume you started with some model in your favorite content generation software (this example uses a dwarf head model that was created in Maya).</span></span> <span data-ttu-id="7c16b-176">Exporte el modelo con textura a un archivo .x y cree un atlas de textura con D3DXUVAtlasCreate.</span><span class="sxs-lookup"><span data-stu-id="7c16b-176">Export the textured model to an .x file and create a texture atlas with D3DXUVAtlasCreate.</span></span> <span data-ttu-id="7c16b-177">El atlas de textura resultante tendría un aspecto parecido al de la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c16b-177">The resulting texture atlas would look something like the following illustration.</span></span>

![ilustración de un atlas para un modelo de árboles](images/uvatlas5.jpg)

<span data-ttu-id="7c16b-179">El atlas tiene 22 gráficos y un máximo de 0,994.</span><span class="sxs-lookup"><span data-stu-id="7c16b-179">The atlas has 22 charts and a maximum stretch of 0.994.</span></span>

<span data-ttu-id="7c16b-180">Ahora, mire el modelo con textura para ver qué tan bien se asigna el atlas de textura a la geometría.</span><span class="sxs-lookup"><span data-stu-id="7c16b-180">Now look at the textured model to see how well the texture atlas maps to the geometry.</span></span> <span data-ttu-id="7c16b-181">Para ello, cargue el modelo en la herramienta de visor:</span><span class="sxs-lookup"><span data-stu-id="7c16b-181">To do this, load the model into the viewer tool:</span></span>

-   <span data-ttu-id="7c16b-182">Abra la herramienta visor desde Utilidades de DirectX.</span><span class="sxs-lookup"><span data-stu-id="7c16b-182">Open the viewer tool from the DirectX Utilities.</span></span>
-   <span data-ttu-id="7c16b-183">Cargue el archivo .x haciendo clic en el botón Abrir.</span><span class="sxs-lookup"><span data-stu-id="7c16b-183">Load the .x file by clicking the Open button.</span></span>
-   <span data-ttu-id="7c16b-184">Para habilitar la opción de visualización de crease, haga clic en el botón Ver y seleccione Creases en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="7c16b-184">Enabling the crease viewing option by clicking the view button and selecting Creases from popup.</span></span>

<span data-ttu-id="7c16b-185">En la ilustración siguiente se muestra lo que debería ver en la herramienta de visor.</span><span class="sxs-lookup"><span data-stu-id="7c16b-185">The following illustration shows what you should see in the viewer tool.</span></span>

![ilustración de una malla con textura en la herramienta de visor](images/uvatlas6c.jpg)

<span data-ttu-id="7c16b-187">Cada línea es un crease que es un borde adyacente entre dos gráficos del atlas de textura.</span><span class="sxs-lookup"><span data-stu-id="7c16b-187">Each line is a crease which is an adjacent edge between two charts in the texture atlas.</span></span> <span data-ttu-id="7c16b-188">El número de gráficos generados por el algoritmo se debe a ligeras diferencias, quizás debido a discontinuidades en las normales.</span><span class="sxs-lookup"><span data-stu-id="7c16b-188">The number of charts generated by the algorithm is caused by slight differences perhaps due to discontinuities in the normals.</span></span> <span data-ttu-id="7c16b-189">Estas pequeñas diferencias se pueden reducir mediante datos desaseados, es decir, forzando datos que son casi iguales para ser iguales.</span><span class="sxs-lookup"><span data-stu-id="7c16b-189">These small differences can be reduced by welding data, that is, forcing data that is nearly equal to be equal.</span></span> <span data-ttu-id="7c16b-190">Para cambiar los normales y los pesos de máscara:</span><span class="sxs-lookup"><span data-stu-id="7c16b-190">To weld the normals and the skinweights:</span></span>

-   <span data-ttu-id="7c16b-191">Ejecute la herramienta DirectX Ops (dxops.exe) con la siguiente línea de comandos en la malla (reemplazando "modelName.x" por el nombre del modelo):</span><span class="sxs-lookup"><span data-stu-id="7c16b-191">Run the DirectX Ops (dxops.exe) tool with the following command line on the mesh (replacing 'modelName.x' with the name of your model):</span></span>
    ```
    Dxops.exe -s "load 'modelName.x'; Optimize n:2.01 w:2.01 uv0:0.01;  save 'newModelName.x';"
    ```

    

<span data-ttu-id="7c16b-192">Esto compara los normales y los pesos de máscara, y donde difieren en el valor en menos de 2,01, los datos se hacen iguales.</span><span class="sxs-lookup"><span data-stu-id="7c16b-192">This compares the normals and skinweights, and where they differ in value by less than 2.01, the data is made equal.</span></span> <span data-ttu-id="7c16b-193">En las ilustraciones siguientes se muestra un primer lugar en el ojo para ver los creases antes de la deserción (a la izquierda) y los creas después de la conserción (a la derecha):</span><span class="sxs-lookup"><span data-stu-id="7c16b-193">The following illustrations shows a close up of the eye to see the creases before welding (on the left) and the creases after welding (on the right):</span></span>

![ilustración de los creases antes de la desapleción](images/uvatlas6a.jpg)![ilustración de los creases después de la desapleción](images/uvatlas6b.jpg)

<span data-ttu-id="7c16b-196">Figura 7: Eliminación de los creases por ingles</span><span class="sxs-lookup"><span data-stu-id="7c16b-196">Figure 7: Removing creases by welding</span></span>

<span data-ttu-id="7c16b-197">En este ejemplo, elimina 86 vértices de la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="7c16b-197">In this example, welding removed 86 vertices from the input mesh.</span></span> <span data-ttu-id="7c16b-198">Con menos creases en la malla, puede volver a generar el atlas, como se muestra en la ilustración siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c16b-198">With fewer creases in the mesh, you can regenerate the atlas, as the following illustration shows.</span></span>

![ilustración del nuevo atlas con los creases quitados](images/uvatlas8.jpg)

<span data-ttu-id="7c16b-200">El atlas solo tiene 7 gráficos y un máximo de aproximadamente 0,0776.</span><span class="sxs-lookup"><span data-stu-id="7c16b-200">The atlas only has 7 charts and a maximum stretch of approximately 0.0776.</span></span> <span data-ttu-id="7c16b-201">El nuevo atlas ahora encaja en una textura más pequeña (aproximadamente un 30 % más pequeña en este ejemplo).</span><span class="sxs-lookup"><span data-stu-id="7c16b-201">The new atlas now fits into a smaller texture (approximately 30% smaller in this example).</span></span>

### <a name="packing-charts-into-an-atlas"></a><span data-ttu-id="7c16b-202">Empaquetado de gráficos en un atlas</span><span class="sxs-lookup"><span data-stu-id="7c16b-202">Packing Charts Into an Atlas</span></span>

<span data-ttu-id="7c16b-203">Una vez que una malla se ha particionado en gráficos con parámetros individuales, los gráficos deben empaquetarse de forma eficaz en un único mapa de textura.</span><span class="sxs-lookup"><span data-stu-id="7c16b-203">Once a mesh has been partitioned into individually-parameterized charts, the charts need to be packed efficiently into a single texture map.</span></span> <span data-ttu-id="7c16b-204">Esto se realiza como el segundo paso de D3DXUVAtlasCreate o se puede invocar explícitamente llamando a D3DXUVAtlasPack.</span><span class="sxs-lookup"><span data-stu-id="7c16b-204">This is performed as the second step of D3DXUVAtlasCreate or can be invoked explicitly by calling D3DXUVAtlasPack.</span></span>

<span data-ttu-id="7c16b-205">Los gráficos empaquetados están separados por un ancho de canalón especificado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="7c16b-205">Packed charts are separated by a user-specified gutter width.</span></span> <span data-ttu-id="7c16b-206">El ancho del medianía es la cantidad de separación entre los gráficos y permite la interpolación bilineal y la asignación de mip para evitar la representación de artefactos en los límites del gráfico.</span><span class="sxs-lookup"><span data-stu-id="7c16b-206">The gutter width is the amount of separation between charts, and allows for bilinear interpolation and mip-mapping to avoid rendering artifacts at chart boundaries.</span></span> <span data-ttu-id="7c16b-207">D3DX proporciona una interfaz para rellenar automáticamente estos canales; vea [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7c16b-207">D3DX provides an interface for automatically filling in these gutters - see [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) for more information.</span></span>

## <a name="integrating-uvatlas-into-your-pipeline"></a><span data-ttu-id="7c16b-208">Integración de UVAtlas en la canalización</span><span class="sxs-lookup"><span data-stu-id="7c16b-208">Integrating UVAtlas Into Your Pipeline</span></span>

<span data-ttu-id="7c16b-209">Además de ser invocadas por el autor antes de pintar texturas, estas funciones se pueden integrar en una canalización de arte automatizada.</span><span class="sxs-lookup"><span data-stu-id="7c16b-209">In addition to being artist-invoked prior to texture painting, these functions can be integrated into an automated art pipeline.</span></span> <span data-ttu-id="7c16b-210">Por ejemplo, una llamada UVAtlas se puede emitir automáticamente después de actualizar un recurso, antes de realizar una simulación de PRT o un paso de asignación normal.</span><span class="sxs-lookup"><span data-stu-id="7c16b-210">For example, a UVAtlas call can be issued automatically after an asset is updated, prior to performing a PRT simulation or normal mapping pass.</span></span> <span data-ttu-id="7c16b-211">Esto evita la necesidad de reparar manualmente la asignación UV de un objeto si se ha modificado la topología de la malla.</span><span class="sxs-lookup"><span data-stu-id="7c16b-211">This avoids any need to manually manual repair of an object's UV mapping if the mesh's topology has been modified.</span></span>

<span data-ttu-id="7c16b-212">Consulte la [herramienta de Command-Line UV Atlas (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) para ver un ejemplo de uso de las funciones UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="7c16b-212">See the [UV Atlas Command-Line Tool (uvatlas.exe)](https://github.com/Microsoft/UVAtlas) for example usage of the UVAtlas functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c16b-213">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c16b-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c16b-214">Temas avanzados</span><span class="sxs-lookup"><span data-stu-id="7c16b-214">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
