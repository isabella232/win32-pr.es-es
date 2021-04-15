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
# <a name="how-to-design-a-hull-shader"></a>Cómo: diseñar un sombreador de casco

Un sombreador de casco es la primera de las tres fases que funcionan conjuntamente para implementar la [teselación](direct3d-11-advanced-stages-tessellation.md) (las otras dos fases son del teselador y un sombreador de dominios). En este tema se muestra cómo diseñar un sombreador de casco.

Un sombreador de casco requiere dos funciones: el sombreador de casco principal y una función de constante patch. El sombreador de casco implementa los cálculos en cada punto de control. el sombreador de casco también llama a la función de la constante patch que implementa los cálculos en cada revisión.

Después de diseñar un sombreador de casco, consulte [Cómo: crear un sombreador de casco](direct3d-11-advanced-stages-hull-shader-create.md) para obtener información sobre cómo crear un sombreador de casco.

**Para diseñar un sombreador de casco**

1.  Definir el control de entrada y los puntos de control de salida del sombreador de casco.

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

    

2.  Defina los datos constantes de la revisión de salida.

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

    

    En el caso de un dominio cuádruple, [VP \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) define 4 factores de teselación perimetral (para dividirlasr los bordes), ya que la función Fixed del teselador debe saber cuánto dividirlas. Los resultados necesarios son diferentes para los dominios de triángulo y Isoline.

    La función Fixed del teselador no examina ninguna otra salida del sombreador de casco, como otros datos de constantes de revisión o cualquiera de los puntos de control. El sombreador de dominios, que se invoca para cada punto que genera la función fija del teselador, verá como su entrada todos los puntos de control de salida del sombreador de casco y todos los datos constantes de la revisión de salida. el sombreador evalúa la revisión en su ubicación.

3.  Defina una función de constante patch. Una función patch Constant se ejecuta una vez para cada revisión con el fin de calcular los datos constantes para toda la revisión (en oposición a los datos de punto de control, que se calculan en el sombreador de casco).

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

    

    Las propiedades de la función de constante patch incluyen:

    -   Una entrada especifica una variable que contiene un identificador de revisión y se identifica mediante el valor del sistema **\_ PrimitiveID VP** (vea [semántica](../direct3dhlsl/dx-graphics-hlsl-semantics.md) en el modelo de sombreador 4).
    -   Un parámetro de entrada es los puntos de control de entrada, declarados en la salida de punto de control de vs en este ejemplo. **\_ \_ \_** Una función patch puede ver todos los puntos de control de entrada de cada revisión; en este ejemplo hay 32 puntos de control por revisión.
    -   Como mínimo, la función debe calcular factores de teselación por revisión para la fase del teselador que se identifican con la [VP \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor). Un dominio cuádruple requiere cuatro factores de teselación para los bordes y dos factores adicionales (identificados por la [VP \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) para teselar en el interior de la revisión. La función Fixed del teselador no examina ninguna otra salida del sombreador de casco (como los datos constantes de la revisión o cualquiera de los puntos de control).
    -   Las salidas normalmente se definen mediante una estructura y se identifican mediante la **\_ salida de \_ datos \_ de constante HS** en este ejemplo; la estructura depende del tipo de dominio y sería diferente para los dominios de trilínea o triángulos.

    Por otro lado, un sombreador de dominio se invoca para cada punto que genera la función del teselador y necesita ver los datos constantes de la revisión de salida y los puntos de control de salida (ambos del sombreador de casco) para evaluar una revisión en su ubicación.

4.  Defina un sombreador de casco. Un sombreador de casco identifica las propiedades de una revisión que incluye una función de constante patch. Un sombreador de casco se invoca una vez para cada punto de control de salida.

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

    -   Atributo de [dominio](/windows/desktop/direct3dhlsl/sm5-attributes-domain) .
    -   Atributo de [particionamiento](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) .
    -   Un atributo [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) .
    -   Un atributo [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) .
    -   Un atributo [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) . Un sombreador de casco calcula los puntos de control de salida, hay 16 puntos de control de Bézier de salida en este ejemplo.

Todos los puntos de control de entrada (identificados por la salida de punto de control de vs) son visibles para cada invocación del sombreador de casco. **\_ \_ \_** En este ejemplo, hay 32 puntos de control de entrada.

Un sombreador de casco se invoca una vez por cada punto de control de salida (identificado con la [VP \_ OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) para cada revisión (identificada con la VP \_ PrimitiveID). El propósito de este sombreador determinado es calcular la salida *i*, que se definió como un punto de control Bézier (este ejemplo tiene 16 puntos de control de salida definidos por outputcontrolpoints).

Un sombreador de casco ejecuta una rutina una vez por revisión (la función de constante patch) para calcular datos constantes de revisión (factores de teselación como mínimo). Por separado, un sombreador de casco ejecuta una función de constante patch (denominada SubDToBezierConstantsHS) en cada revisión para calcular datos constantes de revisión, como factores de teselación para la fase del teselador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Información general sobre teselación](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 