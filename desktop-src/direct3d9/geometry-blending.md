---
description: Direct3D permite que una aplicación aumente el realismo de sus escenas mediante la representación de objetos poligonales segmentados (especialmente caracteres) que tienen uniones mezcladas sin problemas.
ms.assetid: 190d5865-c45b-42ea-8a16-10a4f0bda743
title: Combinación de geometría (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a19daa40f7d7d8193ae486640bc613dd7a666ec7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805186"
---
# <a name="geometry-blending-direct3d-9"></a><span data-ttu-id="d1fd0-103">Combinación de geometría (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d1fd0-103">Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="d1fd0-104">Direct3D permite que una aplicación aumente el realismo de sus escenas mediante la representación de objetos poligonales segmentados (especialmente caracteres) que tienen uniones mezcladas sin problemas.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-104">Direct3D enables an application to increase the realism of its scenes by rendering segmented polygonal objects - especially characters - that have smoothly blended joints.</span></span> <span data-ttu-id="d1fd0-105">Estos efectos se denominan a menudo como aspectos.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-105">These effects are often referred to as skinning.</span></span> <span data-ttu-id="d1fd0-106">Para lograr este efecto, el sistema aplica matrices de transformación universal adicionales a un único conjunto de vértices para crear varios resultados y, a continuación, realiza una mezcla lineal entre los vértices resultantes para crear un único conjunto de geometría para la representación.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-106">The system achieves this effect by applying additional world transformation matrices to a single set of vertices to create multiple results, and then performing a linear blend between the resultant vertices to create a single set of geometry for rendering.</span></span> <span data-ttu-id="d1fd0-107">En la siguiente ilustración de un plátano se muestra este proceso.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-107">The following illustration of a banana shows this process.</span></span>

![Ilustración del proceso para fusionar dos objetos con textura de banana](images/geometry-blend.png)

<span data-ttu-id="d1fd0-109">En la ilustración anterior se muestra cómo puede imaginarse el proceso de combinación de geometría.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-109">The preceding illustration shows how you might imagine the geometry-blending process.</span></span> <span data-ttu-id="d1fd0-110">En una única llamada de representación, el sistema toma los vértices del banana, los transforma dos veces (una vez sin modificación) y una vez con una rotación simple, y combina los resultados para crear una banana doblada.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-110">In a single rendering call, the system takes the vertices for the banana, transforms them twice - once without modification, and once with a simple rotation - and blends the results to create a bent banana.</span></span> <span data-ttu-id="d1fd0-111">El sistema combina la posición del vértice, así como el vértice normal cuando se habilita la iluminación.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-111">The system blends the vertex position, as well as the vertex normal when lighting is enabled.</span></span> <span data-ttu-id="d1fd0-112">Las aplicaciones no se limitan a dos rutas de acceso de mezcla; Direct3D puede fusionar la geometría entre un máximo de cuatro matrices mundiales, incluida la matriz mundial del mundo, [**D3DTS \_ World**](d3dts-world.md).</span><span class="sxs-lookup"><span data-stu-id="d1fd0-112">Applications are not limited to two blending paths; Direct3D can blend geometry between as many as four world matrices, including the standard world matrix, [**D3DTS\_WORLD**](d3dts-world.md).</span></span>

> [!Note]
>
> <span data-ttu-id="d1fd0-113">Cuando se habilita la iluminación, las normales de vértice se transforman mediante una matriz de vista mundial inversa correspondiente, ponderada de la misma manera que los cálculos de posición de vértices.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-113">When lighting is enabled, vertex normals are transformed by a corresponding inverse world-view matrix, weighted in the same way as the vertex position computations.</span></span> <span data-ttu-id="d1fd0-114">El sistema normaliza el vector normal resultante si el estado de \_ representación de D3DRS NORMALIZENORMALS se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-114">The system normalizes the resulting normal vector if the D3DRS\_NORMALIZENORMALS render state is set to **TRUE**.</span></span>

 

<span data-ttu-id="d1fd0-115">Sin la combinación de geometría, los modelos dinámicos articulados a menudo se representan en segmentos.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-115">Without geometry blending, dynamic articulated models are often rendered in segments.</span></span> <span data-ttu-id="d1fd0-116">Por ejemplo, considere un modelo 3D del brazo humano.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-116">For instance, consider a 3D model of the human arm.</span></span> <span data-ttu-id="d1fd0-117">En la vista más simple, un brazo tiene dos partes: el brazo superior que se conecta al cuerpo y el brazo inferior, que se conecta a la mano.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-117">In the simplest view, an arm has two parts: the upper arm which connects to the body, and the lower arm, which connects to the hand.</span></span> <span data-ttu-id="d1fd0-118">Los dos están conectados en el codo y el brazo inferior gira en ese punto.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-118">The two are connected at the elbow, and the lower arm rotates at that point.</span></span> <span data-ttu-id="d1fd0-119">Una aplicación que representa un brazo podría conservar los datos de vértice para el brazo superior e inferior, cada uno con una matriz de transformación internacional independiente.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-119">An application that renders an arm might retain vertex data for the upper and lower arm, each with a separate world transformation matrix.</span></span> <span data-ttu-id="d1fd0-120">En el siguiente ejemplo código se muestra cómo hacerlo.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-120">The following code example illustrates this.</span></span>


```
typedef struct _Arm
{
    VERTEX upper_arm_verts[200];
    D3DMATRIX matWorld_Upper;

    VERTEX lower_arm_verts[200];
    D3DMATRIX matWorld_Lower;
} ARM, *LPARM;

ARM MyArm; // This needs to be initialized.
```



<span data-ttu-id="d1fd0-121">Para representar el ARM, se realizan dos llamadas de representación, como se muestra en el código siguiente.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-121">To render the arm, two rendering calls are made, as shown in the following code.</span></span>


```
// Render the upper arm.
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Upper );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );

// Render the lower arm, updating its world matrix to articulate
// the arm by pi/4 radians (45 degrees) at the elbow.
MyArm.matWorld_Lower = RotateMyArm(MyArm.matWorld, pi/4);
d3dDevice->SetTransform( D3DTS_WORLD, &MyArm.matWorld_Lower );
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, numFaces );
```



<span data-ttu-id="d1fd0-122">La siguiente ilustración es un plátano, modificado para usar esta técnica.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-122">The following illustration is a banana, modified to use this technique.</span></span>

![Ilustración de un plátano mezclado sin combinación de geometría](images/noblend.png)

<span data-ttu-id="d1fd0-124">Las diferencias entre la geometría combinada y la geometría no fusionada son obvias.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-124">The differences between the blended geometry and the nonblended geometry are obvious.</span></span> <span data-ttu-id="d1fd0-125">Este ejemplo es algo extremo.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-125">This example is somewhat extreme.</span></span> <span data-ttu-id="d1fd0-126">En una aplicación real, las uniones de modelos segmentados están diseñadas para que las costuras no sean tan obvias.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-126">In a real-world application, the joints of segmented models are designed so that seams are not as obvious.</span></span> <span data-ttu-id="d1fd0-127">Sin embargo, las costuras son visibles en ocasiones, lo que presenta desafíos constantes para los diseñadores de modelos.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-127">However, seams are visible at times, which presents constant challenges for model designers.</span></span>

<span data-ttu-id="d1fd0-128">La combinación de geometría en Direct3D presenta una alternativa al escenario de modelado segmentado clásico.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-128">Geometry blending in Direct3D presents an alternative to the classic segmented-modeling scenario.</span></span> <span data-ttu-id="d1fd0-129">Sin embargo, la calidad visual mejorada de los objetos segmentados se refiere al costo de los cálculos de mezcla durante la representación.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-129">However, the improved visual quality of segmented objects comes at the cost of the blending computations during rendering.</span></span> <span data-ttu-id="d1fd0-130">Para minimizar el impacto de estas operaciones adicionales, la canalización de geometría de Direct3D está optimizada para fusionar la geometría con la menor sobrecarga posible.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-130">To minimize the impact of these additional operations, the Direct3D geometry pipeline is optimized to blend geometry with the least possible overhead.</span></span> <span data-ttu-id="d1fd0-131">Las aplicaciones que usan de forma inteligente los servicios de combinación de geometría que ofrece Direct3D pueden mejorar el realismo de sus caracteres a la vez que evitan repercusiones graves en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-131">Applications that intelligently use the geometry blending services offered by Direct3D can improve the realism of their characters while avoiding serious performance repercussions.</span></span>

## <a name="blending-transform-and-render-states"></a><span data-ttu-id="d1fd0-132">Mezcla de Estados de transformación y representación</span><span class="sxs-lookup"><span data-stu-id="d1fd0-132">Blending Transform and Render States</span></span>

<span data-ttu-id="d1fd0-133">El método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) reconoce las macros [**D3DTS \_ World**](d3dts-world.md) y [**D3DTS \_ worldan**](d3dts-worldn.md) , que corresponden a los valores que se pueden definir mediante la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="d1fd0-133">The [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method recognizes the [**D3DTS\_WORLD**](d3dts-world.md) and [**D3DTS\_WORLDn**](d3dts-worldn.md) macros, which correspond to values that can be defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro.</span></span> <span data-ttu-id="d1fd0-134">Estas macros se utilizan para identificar las matrices entre las que se combinará Geometry.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-134">These macros are used to identify the matrices between which geometry will be blended.</span></span>

<span data-ttu-id="d1fd0-135">El tipo enumerado [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) incluye el estado de representación de D3DRS \_ VERTEXBLEND para habilitar y controlar la combinación de geometría.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-135">The [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) enumerated type includes the D3DRS\_VERTEXBLEND render state to enable and control geometry blending.</span></span> <span data-ttu-id="d1fd0-136">Los valores válidos para este estado de representación se definen mediante el tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="d1fd0-136">Valid values for this render state are defined by the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="d1fd0-137">Si está habilitada la combinación de geometría, el formato de vértice debe incluir el número adecuado de pesos de fusión.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-137">If geometry blending is enabled, the vertex format must include the appropriate number of blending weights.</span></span>

## <a name="blending-weights"></a><span data-ttu-id="d1fd0-138">Pesos de fusión</span><span class="sxs-lookup"><span data-stu-id="d1fd0-138">Blending Weights</span></span>

<span data-ttu-id="d1fd0-139">Un peso de fusión, que a veces se denomina peso beta, controla la medida en que una matriz universal determinada afecta a un vértice.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-139">A blending weight, sometimes called a beta weight, controls the extent to which a given world matrix affects a vertex.</span></span> <span data-ttu-id="d1fd0-140">Los pesos de la mezcla son valores de punto flotante que van de 0,0 a 1,0, codificados en formato de vértice, donde un valor de 0,0 significa que el vértice no se combina con esa matriz y 1,0 significa que el vértice se ve afectado por la matriz.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-140">Blending weights are floating-point values that range from 0.0 to 1.0, encoded in the vertex format, where a value of 0.0 means the vertex is not blended with that matrix, and 1.0 means that the vertex is affected in full by the matrix.</span></span>

<span data-ttu-id="d1fd0-141">Los pesos de la combinación de geometría se codifican en el formato de vértices, que aparecen inmediatamente después de la posición de cada vértice, como se describe en [códigos FVF de función fija (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d1fd0-141">Geometry blending weights are encoded in the vertex format, appearing immediately after the position for each vertex, as described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span> <span data-ttu-id="d1fd0-142">Para comunicar el número de pesos de fusión en el formato de vértice, incluya una de las [constantes FVF](d3dfvf.md) en la descripción del vértice que proporcione a los métodos de representación.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-142">You communicate the number of blending weights in the vertex format by including one of the [FVF constants](d3dfvf.md) in the vertex description that you provide to the rendering methods.</span></span>

<span data-ttu-id="d1fd0-143">El sistema realiza una mezcla lineal entre los resultados ponderados de las matrices de Blend.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-143">The system performs a linear blend between the weighted results of the blend matrices.</span></span> <span data-ttu-id="d1fd0-144">La siguiente ecuación es la fórmula de combinación completa.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-144">The following equation is the complete blending formula.</span></span>

![ecuación de combinación lineal con matrices de transformación universal](images/vert-blend-formula.png)

<span data-ttu-id="d1fd0-146">En la ecuación anterior, vBlend es el vértice de salida, los elementos v son los vértices producidos por la matriz universal aplicada ([**D3DTS \_ worlda**](d3dts-worldn.md)).</span><span class="sxs-lookup"><span data-stu-id="d1fd0-146">In the preceding equation, vBlend is the output vertex, the v-elements are the vertices produced by the applied world matrix ([**D3DTS\_WORLDn**](d3dts-worldn.md)).</span></span> <span data-ttu-id="d1fd0-147">Los elementos W son los valores de peso correspondientes en el formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-147">The W elements are the corresponding weight values within the vertex format.</span></span> <span data-ttu-id="d1fd0-148">Un vértice mezclado entre n matrices puede tener-1 valores de peso de fusión, uno para cada matriz de mezcla, excepto el último.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-148">A vertex blended between n matrices can have - 1 blending weight values, one for each blending matrix, except the last.</span></span> <span data-ttu-id="d1fd0-149">El sistema genera automáticamente el peso de la matriz del último mundo, de modo que la suma de todos los pesos sea 1,0, expresada en la notación Sigma aquí.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-149">The system automatically generates the weight for the last world matrix so that the sum of all weights is 1.0, expressed in sigma notation here.</span></span> <span data-ttu-id="d1fd0-150">Esta fórmula se puede simplificar para cada uno de los casos que admite Direct3D, que se muestra en las siguientes ecuaciones.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-150">This formula can be simplified for each of the cases supported by Direct3D, which is shown in the following equations.</span></span>

![ecuaciones de combinación lineal para tres casos de combinación](images/vert-blend-formulas-simple.png)

<span data-ttu-id="d1fd0-152">Estas son las formas simplificadas de la fórmula de combinación completa para los dos, tres y cuatro casos de matriz de mezcla.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-152">These are the simplified forms of the complete blending formula for the two, three, and four blend matrix cases.</span></span>

> [!Note]  
> <span data-ttu-id="d1fd0-153">Aunque Direct3D incluye descriptores de FVF para definir vértices que contengan hasta cinco pesos de fusión, solo se pueden usar tres en esta versión de DirectX.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-153">Although Direct3D includes FVF descriptors to define vertices that contain up to five blending weights, only three can be used in this release of DirectX.</span></span>

 

<span data-ttu-id="d1fd0-154">En los temas siguientes se incluye información adicional.</span><span class="sxs-lookup"><span data-stu-id="d1fd0-154">Additional information is contained in the following topics.</span></span>

-   [<span data-ttu-id="d1fd0-155">Usar la combinación de geometría (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d1fd0-155">Using Geometry Blending (Direct3D 9)</span></span>](using-geometry-blending.md)
-   [<span data-ttu-id="d1fd0-156">Fusión de vértices indizados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d1fd0-156">Indexed Vertex Blending (Direct3D 9)</span></span>](indexed-vertex-blending.md)
-   [<span data-ttu-id="d1fd0-157">Interpolación de vértices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d1fd0-157">Vertex Tweening (Direct3D 9)</span></span>](vertex-tweening.md)

## <a name="related-topics"></a><span data-ttu-id="d1fd0-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1fd0-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1fd0-159">Canalización de vértices</span><span class="sxs-lookup"><span data-stu-id="d1fd0-159">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
