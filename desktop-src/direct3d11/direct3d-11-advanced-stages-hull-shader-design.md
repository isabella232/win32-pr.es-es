---
title: Cómo diseñar un sombreador de casco
description: En este tema se muestra cómo diseñar un sombreador de casco.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997056"
---
# <a name="how-to-design-a-hull-shader"></a><span data-ttu-id="2e6aa-103">Cómo: diseñar un sombreador de casco</span><span class="sxs-lookup"><span data-stu-id="2e6aa-103">How To: Design a Hull Shader</span></span>

<span data-ttu-id="2e6aa-104">Un sombreador de casco es la primera de las tres fases que funcionan conjuntamente para implementar la [teselación](direct3d-11-advanced-stages-tessellation.md) (las otras dos fases son del teselador y un sombreador de dominios).</span><span class="sxs-lookup"><span data-stu-id="2e6aa-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md) (the other two stages are the tessellator and a domain shader).</span></span> <span data-ttu-id="2e6aa-105">En este tema se muestra cómo diseñar un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-105">This topics shows how to design a hull shader.</span></span>

<span data-ttu-id="2e6aa-106">Un sombreador de casco requiere dos funciones: el sombreador de casco principal y una función de constante patch.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-106">A hull shader requires two functions, the main hull shader and a patch constant function.</span></span> <span data-ttu-id="2e6aa-107">El sombreador de casco implementa los cálculos en cada punto de control. el sombreador de casco también llama a la función de la constante patch que implementa los cálculos en cada revisión.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-107">The hull shader implements calculations on each control point; the hull shader also calls the patch constant function which implements calculations on each patch.</span></span>

<span data-ttu-id="2e6aa-108">Después de diseñar un sombreador de casco, consulte [Cómo: crear un sombreador de casco](direct3d-11-advanced-stages-hull-shader-create.md) para obtener información sobre cómo crear un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-108">After you have designed a hull shader, see [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md) to learn how to create a hull shader.</span></span>

<span data-ttu-id="2e6aa-109">**Para diseñar un sombreador de casco**</span><span class="sxs-lookup"><span data-stu-id="2e6aa-109">**To design a hull shader**</span></span>

1.  <span data-ttu-id="2e6aa-110">Definir el control de entrada y los puntos de control de salida del sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-110">Define hull shader input control and output control points.</span></span>

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  <span data-ttu-id="2e6aa-111">Defina los datos constantes de la revisión de salida.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-111">Define output patch constant data.</span></span>

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    <span data-ttu-id="2e6aa-112">En el caso de un dominio cuádruple, [VP \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) define 4 factores de teselación perimetral (para dividirlasr los bordes), ya que la función Fixed del teselador debe saber cuánto dividirlas.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-112">For a quad domain, [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) defines 4 edge tessellation factors (to tessellate the edges), since the fixed function tessellator needs to know how much to tessellate.</span></span> <span data-ttu-id="2e6aa-113">Los resultados necesarios son diferentes para los dominios de triángulo y Isoline.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-113">The required outputs are different for the triangle and isoline domains.</span></span>

    <span data-ttu-id="2e6aa-114">La función Fixed del teselador no examina ninguna otra salida del sombreador de casco, como otros datos de constantes de revisión o cualquiera de los puntos de control.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-114">The fixed function tessellator doesn't look at any other hull shader outputs, such as other patch constant data or any of the control points.</span></span> <span data-ttu-id="2e6aa-115">El sombreador de dominios, que se invoca para cada punto que genera la función fija del teselador, verá como su entrada todos los puntos de control de salida del sombreador de casco y todos los datos constantes de la revisión de salida. el sombreador evalúa la revisión en su ubicación.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-115">The domain shader -- which is invoked for each point the fixed function tessellator generates -- will see as its input all the hull shader's output control points and all the output patch constant data; the shader evaluates the patch at its location.</span></span>

3.  <span data-ttu-id="2e6aa-116">Defina una función de constante patch.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-116">Define a patch constant function.</span></span> <span data-ttu-id="2e6aa-117">Una función patch Constant se ejecuta una vez para cada revisión con el fin de calcular los datos constantes para toda la revisión (en oposición a los datos de punto de control, que se calculan en el sombreador de casco).</span><span class="sxs-lookup"><span data-stu-id="2e6aa-117">A patch constant function executes once for each patch to calculate any data that is constant for the entire patch (as opposed to per-control point data, which is computed in the hull shader).</span></span>

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    <span data-ttu-id="2e6aa-118">Las propiedades de la función de constante patch incluyen:</span><span class="sxs-lookup"><span data-stu-id="2e6aa-118">Properties of the patch constant function include:</span></span>

    -   <span data-ttu-id="2e6aa-119">Una entrada especifica una variable que contiene un identificador de revisión y se identifica mediante el valor del sistema **\_ PrimitiveID VP** (vea [semántica](../direct3dhlsl/dx-graphics-hlsl-semantics.md) en el modelo de sombreador 4).</span><span class="sxs-lookup"><span data-stu-id="2e6aa-119">One input specifies a variable containing a patch id, and is identified by the **SV\_PrimitiveID** system value (see [semantics](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in shader model 4).</span></span>
    -   <span data-ttu-id="2e6aa-120">Un parámetro de entrada es los puntos de control de entrada, declarados en la salida de punto de control de vs en este ejemplo. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2e6aa-120">One input parameter is the input control points, declared in **VS\_CONTROL\_POINT\_OUTPUT** in this example.</span></span> <span data-ttu-id="2e6aa-121">Una función patch puede ver todos los puntos de control de entrada de cada revisión; en este ejemplo hay 32 puntos de control por revisión.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-121">A patch function can see all the input control points for each patch, there are 32 control points per patch in this example.</span></span>
    -   <span data-ttu-id="2e6aa-122">Como mínimo, la función debe calcular factores de teselación por revisión para la fase del teselador que se identifican con la [VP \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span><span class="sxs-lookup"><span data-stu-id="2e6aa-122">As a minimum, the function must calculate per-patch tessellation factors for the tessellator stage which are identified with [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span></span> <span data-ttu-id="2e6aa-123">Un dominio cuádruple requiere cuatro factores de teselación para los bordes y dos factores adicionales (identificados por la [VP \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) para teselar en el interior de la revisión.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-123">A quad domain requires four tessellation factors for the edges and two additional factors (identified by [SV\_InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) for tessellating the inside of the patch.</span></span> <span data-ttu-id="2e6aa-124">La función Fixed del teselador no examina ninguna otra salida del sombreador de casco (como los datos constantes de la revisión o cualquiera de los puntos de control).</span><span class="sxs-lookup"><span data-stu-id="2e6aa-124">The fixed function tessellator doesn't look at any other hull shader outputs (such as the patch constant data or any of the control points).</span></span>
    -   <span data-ttu-id="2e6aa-125">Las salidas normalmente se definen mediante una estructura y se identifican mediante la **\_ salida de \_ datos \_ de constante HS** en este ejemplo; la estructura depende del tipo de dominio y sería diferente para los dominios de trilínea o triángulos.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-125">The outputs are usually defined by a structure and is identified by **HS\_CONSTANT\_DATA\_OUTPUT** in this example; the structure depends on the domain type and would be different for triangle or isoline domains.</span></span>

    <span data-ttu-id="2e6aa-126">Por otro lado, un sombreador de dominio se invoca para cada punto que genera la función del teselador y necesita ver los datos constantes de la revisión de salida y los puntos de control de salida (ambos del sombreador de casco) para evaluar una revisión en su ubicación.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-126">A domain shader on the other hand is invoked for each point the fixed function tessellator generates and needs to see the output control points and the output patch constant data (both from the hull shader) to evaluate a patch at its location.</span></span>

4.  <span data-ttu-id="2e6aa-127">Defina un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-127">Define a hull shader.</span></span> <span data-ttu-id="2e6aa-128">Un sombreador de casco identifica las propiedades de una revisión que incluye una función de constante patch.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-128">A hull shader identifies the properties of a patch including a patch constant function.</span></span> <span data-ttu-id="2e6aa-129">Un sombreador de casco se invoca una vez para cada punto de control de salida.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-129">A hull shader is invoked once for each output control point.</span></span>

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    <span data-ttu-id="2e6aa-130">Un sombreador de casco usa los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="2e6aa-130">A hull shader uses the following attributes:</span></span>

    -   <span data-ttu-id="2e6aa-131">Atributo de [dominio](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .</span><span class="sxs-lookup"><span data-stu-id="2e6aa-131">A [domain](/windows/desktop/direct3dhlsl/sm5-attributes-domain) attribute.</span></span>
    -   <span data-ttu-id="2e6aa-132">Atributo de [particionamiento](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .</span><span class="sxs-lookup"><span data-stu-id="2e6aa-132">A [partitioning](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) attribute.</span></span>
    -   <span data-ttu-id="2e6aa-133">Un atributo [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .</span><span class="sxs-lookup"><span data-stu-id="2e6aa-133">An [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) attribute.</span></span>
    -   <span data-ttu-id="2e6aa-134">Un atributo [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .</span><span class="sxs-lookup"><span data-stu-id="2e6aa-134">An [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) attribute.</span></span>
    -   <span data-ttu-id="2e6aa-135">Un atributo [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) .</span><span class="sxs-lookup"><span data-stu-id="2e6aa-135">A [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) attribute.</span></span> <span data-ttu-id="2e6aa-136">Un sombreador de casco calcula los puntos de control de salida, hay 16 puntos de control de Bézier de salida en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-136">A hull shader calculates output control points, there are 16 output Bezier control points in this example.</span></span>

<span data-ttu-id="2e6aa-137">Todos los puntos de control de entrada (identificados por la salida de punto de control de vs) son visibles para cada invocación del sombreador de casco. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2e6aa-137">All the input control points (identified by **VS\_CONTROL\_POINT\_OUTPUT**) are visible to each hull shader invocation.</span></span> <span data-ttu-id="2e6aa-138">En este ejemplo, hay 32 puntos de control de entrada.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-138">In this example, there are 32 input control points.</span></span>

<span data-ttu-id="2e6aa-139">Un sombreador de casco se invoca una vez por cada punto de control de salida (identificado con la [VP \_ OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) para cada revisión (identificada con la VP \_ PrimitiveID).</span><span class="sxs-lookup"><span data-stu-id="2e6aa-139">A hull shader is invoked once per output control point (identified with [SV\_OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) for each patch (identified with SV\_PrimitiveID).</span></span> <span data-ttu-id="2e6aa-140">El propósito de este sombreador determinado es calcular la salida *i*, que se definió como un punto de control Bézier (este ejemplo tiene 16 puntos de control de salida definidos por outputcontrolpoints).</span><span class="sxs-lookup"><span data-stu-id="2e6aa-140">The purpose of this particular shader is to calculate output *i*, which was defined to be a BEZIER control point (this example has 16 output control points defined by outputcontrolpoints).</span></span>

<span data-ttu-id="2e6aa-141">Un sombreador de casco ejecuta una rutina una vez por revisión (la función de constante patch) para calcular datos constantes de revisión (factores de teselación como mínimo).</span><span class="sxs-lookup"><span data-stu-id="2e6aa-141">A hull shader runs a routine once per patch (the patch constant function) to compute patch-constant data (tessellation factors as a minimum).</span></span> <span data-ttu-id="2e6aa-142">Por separado, un sombreador de casco ejecuta una función de constante patch (denominada SubDToBezierConstantsHS) en cada revisión para calcular datos constantes de revisión, como factores de teselación para la fase del teselador.</span><span class="sxs-lookup"><span data-stu-id="2e6aa-142">Separately, a hull shader runs a patch constant function (called SubDToBezierConstantsHS) on each patch to compute patch-constant data such as tessellation factors for the tessellator stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e6aa-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e6aa-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e6aa-144">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="2e6aa-144">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="2e6aa-145">Información general sobre teselación</span><span class="sxs-lookup"><span data-stu-id="2e6aa-145">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 