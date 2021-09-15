---
title: Cómo diseñar un sombreador de casco
description: En este tema se muestra cómo diseñar un sombreador de casco.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566236"
---
# <a name="how-to-design-a-hull-shader"></a>Cómo: Diseñar un sombreador de casco

Un sombreador de casco es la primera de las tres fases que funcionan conjuntamente para implementar la teselación (las otras dos [fases](direct3d-11-advanced-stages-tessellation.md) son el teselador y un sombreador de dominio). En este tema se muestra cómo diseñar un sombreador de casco.

Un sombreador de casco requiere dos funciones, el sombreador de casco principal y una función constante de revisión. El sombreador de casco implementa cálculos en cada punto de control; El sombreador de casco también llama a la función de constante de revisión que implementa cálculos en cada revisión.

Después de diseñar un sombreador de casco, consulte [Cómo:](direct3d-11-advanced-stages-hull-shader-create.md) Crear un sombreador de casco para aprender a crear un sombreador de casco.

**Para diseñar un sombreador de casco**

1.  Defina el control de entrada del sombreador de casco y los puntos de control de salida.

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

    

2.  Defina los datos constantes de revisión de salida.

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

    

    En el caso de un dominio quad, [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) define 4 factores de teselación de borde (para teselar los bordes), ya que el teselador de función fija debe saber cuánto se debe tesentar. Las salidas necesarias son diferentes para los dominios triángulo e isolínea.

    El teselador de función fija no observa ninguna otra salida del sombreador de casco, como otros datos constantes de revisión o ninguno de los puntos de control. El sombreador de dominio , que se invoca para cada punto que genera el teselador de función fija, verá como entrada todos los puntos de control de salida del sombreador de casco y todos los datos constantes de revisión de salida. el sombreador evalúa la revisión en su ubicación.

3.  Defina una función de constante de revisión. Una función de constante de revisión se ejecuta una vez por cada revisión para calcular los datos que son constantes para toda la revisión (en lugar de los datos por punto de control, que se calculan en el sombreador de casco).

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

    

    Las propiedades de la función de constante de revisión incluyen:

    -   Una entrada especifica una variable que contiene un identificador de revisión y se identifica mediante el valor del sistema **SV \_ PrimitiveID** (vea [semántica en](../direct3dhlsl/dx-graphics-hlsl-semantics.md) el modelo de sombreador 4).
    -   Un parámetro de entrada son los puntos de control de entrada, declarados en **VS \_ CONTROL POINT \_ \_ OUTPUT** en este ejemplo. Una función de revisión puede ver todos los puntos de control de entrada de cada revisión; hay 32 puntos de control por revisión en este ejemplo.
    -   Como mínimo, la función debe calcular los factores de teselación por revisión para la fase del teselador que se identifican con [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor). Un dominio quad requiere cuatro factores de teselación para los bordes y dos factores adicionales (identificados por [SV \_ InsideTessFactor)](/windows/desktop/direct3dhlsl/sv-insidetessfactor)para la teselación del interior de la revisión. El teselador de función fija no observa ninguna otra salida del sombreador de casco (como los datos constantes de revisión o cualquiera de los puntos de control).
    -   Las salidas normalmente se definen mediante una estructura y se identifican mediante **HS \_ CONSTANT DATA \_ \_ OUTPUT** en este ejemplo; la estructura depende del tipo de dominio y sería diferente para los dominios triángulo o isolínea.

    Por otro lado, se invoca un sombreador de dominio para cada punto que el teselador de función fija genera y necesita ver los puntos de control de salida y los datos constantes de revisión de salida (ambos del sombreador de casco) para evaluar una revisión en su ubicación.

4.  Defina un sombreador de casco. Un sombreador de casco identifica las propiedades de una revisión, incluida una función de constante de revisión. Se invoca un sombreador de casco una vez para cada punto de control de salida.

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

    

    Un sombreador de casco usa los siguientes atributos:

    -   Atributo [de](/windows/desktop/direct3dhlsl/sm5-attributes-domain) dominio.
    -   Atributo [de creación de](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) particiones.
    -   Atributo [outputtopology.](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology)
    -   Atributo [outputcontrolpoints.](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints)
    -   Atributo [patchconstantfunc.](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) Un sombreador de casco calcula los puntos de control de salida; en este ejemplo hay 16 puntos de control Bézier de salida.

Todos los puntos de control de entrada (identificados **por VS CONTROL POINT \_ \_ \_ OUTPUT)** son visibles para cada invocación del sombreador de casco. En este ejemplo, hay 32 puntos de control de entrada.

Un sombreador de casco se invoca una vez por punto de control de salida (identificado con [SV \_ OutputControlPointID)](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)para cada revisión (identificado con SV \_ PrimitiveID). El propósito de este sombreador concreto es calcular la salida *i*, que se definió como un punto de control BEZIER (este ejemplo tiene 16 puntos de control de salida definidos por los puntos de control de salida).

Un sombreador de casco ejecuta una rutina una vez por revisión (la función de constante de revisión) para calcular los datos de constante de revisión (factores de teselación como mínimo). Por separado, un sombreador de casco ejecuta una función de constante de revisión (denominada SubDToBezierConstantsHS) en cada revisión para calcular datos constantes de revisión, como factores de teselación para la fase del teselador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Introducción a la teselación](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 