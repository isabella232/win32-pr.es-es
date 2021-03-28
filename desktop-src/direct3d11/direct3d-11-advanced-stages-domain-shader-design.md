---
title: Cómo diseñar un sombreador de dominios
description: En este tema se muestra cómo diseñar un sombreador de dominios.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d6b006c5ffe3afa355abe5e662cb96aa1391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149422"
---
# <a name="how-to-design-a-domain-shader"></a>Cómo: diseñar un sombreador de dominios

Un sombreador de dominios es el tercero de tres fases que funcionan conjuntamente para implementar la [teselación](direct3d-11-advanced-stages-tessellation.md). El sombreador de dominios genera la geometría de la superficie a partir de los puntos de control transformados de un sombreador de casco y las coordenadas UV. En este tema se muestra cómo diseñar un sombreador de dominios.

Un sombreador de dominio se invoca una vez para cada punto generado por la función Fixed del teselador. Las entradas son las \[ coordenadas UV \] del punto de la revisión, así como todos los datos de salida del sombreador de casco, incluidos los puntos de control y las constantes de revisión. El resultado es un vértice definido de la forma que se desee. Si el resultado se envía al sombreador de píxeles, la salida debe incluir una posición (indicada con una semántica de posición de la VP \_ ).

**Para diseñar un sombreador de dominios**

1.  Defina el atributo de dominio.

    ```
    [domain("quad")]
    ```

    

    El dominio se define para una revisión cuádruple.

2.  Declare la ubicación en el casco con el valor del sistema de [Ubicación del dominio](/windows/desktop/direct3dhlsl/sv-domainlocation) .

    -   Para una revisión cuádruple, use un float2.
    -   En el caso de una triple revisión, use float3 (para las coordenadas Barycentric).
    -   Para una isolínea, use un float2.

    Por lo tanto, la ubicación de dominio para una revisión cuádruple tiene el siguiente aspecto:

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Defina las demás entradas.

    Las demás entradas proceden del sombreador de casco y están definidas por el usuario. Esto incluye los puntos de control de entrada para la revisión, de los cuales puede estar entre 1 y 32 puntos, y datos constantes de la revisión de entrada.

    Los puntos de control están definidos por el usuario, normalmente con una estructura como esta (definida en [Cómo: diseñar un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Los datos constantes de revisión también están definidos por el usuario y podrían parecerse a este (definido en [Cómo: diseñar un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Agregue código definido por el usuario para calcular las salidas; crea el cuerpo del sombreador de dominios.

    Esta estructura contiene las salidas del sombreador de dominios definidas por el usuario.

    ```
    struct DS_OUTPUT
    {
        float3 vNormal    : NORMAL;
        float2 vUV        : TEXCOORD;
        float3 vTangent   : TANGENT;
        float3 vBiTangent : BITANGENT;
        
        float4 vPosition  : SV_POSITION;
    };
    ```

    

    La función toma cada UV de entrada (desde el del teselador) y evalúa el parche de Bézier en esta posición.

    ```
    [domain("quad")]
    DS_OUTPUT BezierEvalDS( HS_CONSTANT_DATA_OUTPUT input, 
                            float2 UV : SV_DomainLocation,
                            const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch )
    {
        DS_OUTPUT Output;

        // Insert code to compute the output here.

        return Output;    
    }
    ```

    

    La función se invoca una vez para cada punto generado por la función Fixed del teselador. Dado que en este ejemplo se usa un cuádruple parche, la ubicación del dominio de entrada ([VP \_ DomainLocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) es un float2 (UV); un tri patch tendría una ubicación de entrada FLOAT3 (coordenadas UVW Barycentric) y una isolínea tendría una ubicación de dominio de entrada float2.

    Las demás entradas de la función proceden directamente del sombreador de casco. En este ejemplo, es 16 puntos de control cada uno de los cuales es un **\_ \_ punto de control Bézier**, así como datos constantes de revisión (**\_ \_ \_ salida de datos constante HS**). El resultado es un vértice que contiene los datos de **\_ salida de DS** deseado en este ejemplo.

Después de diseñar un sombreador de dominios, consulte [Cómo: crear un sombreador de dominios](direct3d-11-advanced-stages-domain-shader-create.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Información general sobre teselación](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 