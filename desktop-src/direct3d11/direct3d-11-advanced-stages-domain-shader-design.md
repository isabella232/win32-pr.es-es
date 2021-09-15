---
title: Cómo diseñar un sombreador de dominio
description: En este tema se muestra cómo diseñar un sombreador de dominio.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d6b006c5ffe3afa355abe5e662cb96aa1391
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566237"
---
# <a name="how-to-design-a-domain-shader"></a>Cómo: Diseñar un sombreador de dominio

Un sombreador de dominio es la tercera de las tres fases que funcionan conjuntamente para implementar [la teselación](direct3d-11-advanced-stages-tessellation.md). El sombreador de dominio genera la geometría de la superficie a partir de los puntos de control transformados a partir de un sombreador de casco y las coordenadas UV. En este tema se muestra cómo diseñar un sombreador de dominio.

Un sombreador de dominio se invoca una vez por cada punto generado por el teselador de función fija. Las entradas son las coordenadas UV W del punto de la revisión, así como todos los datos de salida del sombreador de casco, incluidos los puntos de control y las constantes \[ \] de revisión. La salida es un vértice definido de la manera deseada. Si la salida se envía al sombreador de píxeles, la salida debe incluir una posición (que se indica con una semántica de posición \_ SV).

**Para diseñar un sombreador de dominio**

1.  Defina el atributo de dominio.

    ```
    [domain("quad")]
    ```

    

    El dominio se define para una revisión de cuatro.

2.  Declare la ubicación en el casco con el valor [del sistema de ubicación](/windows/desktop/direct3dhlsl/sv-domainlocation) de dominio.

    -   Para una revisión de cuatro, use float2.
    -   Para una revisión tri, use float3 (para coordenadas baricéntricas)
    -   Para una isolínea, use float2.

    Por lo tanto, la ubicación del dominio para una revisión de cuatro es similar a la siguiente:

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Defina las demás entradas.

    Las demás entradas proceden del sombreador de casco y están definidas por el usuario. Esto incluye los puntos de control de entrada para la revisión, de los cuales puede haber entre 1 y 32 puntos, y datos constantes de revisión de entrada.

    Los puntos de control están definidos por el usuario, normalmente con una estructura como esta (definida en Cómo: Diseñar [un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Los datos de constante de revisión también están definidos por el usuario y podrían ser parecidos a este (definido en Cómo: Diseñar [un sombreador de casco](direct3d-11-advanced-stages-hull-shader-design.md)):

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Agregue código definido por el usuario para calcular las salidas; esto forma el cuerpo del sombreador de dominio.

    Esta estructura contiene salidas del sombreador de dominio definidas por el usuario.

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

    

    La función toma cada UV de entrada (del teselador) y evalúa la revisión de Bézier en esta posición.

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

    

    La función se invoca una vez para cada punto generado por el teselador de función fija. Dado que en este ejemplo se usa una revisión cuadránea, la ubicación del dominio de entrada[(SV \_ DomainLocation)](/windows/desktop/direct3dhlsl/sv-domainlocation)es float2 (UV); una revisión tri tendría una ubicación de entrada float3 (coordenadas baricéntricas de UVW) y una isolínea tendría una ubicación de dominio de entrada float2.

    Las demás entradas de la función proceden directamente del sombreador de casco. En este ejemplo, son 16 puntos de control cada uno de los que son UN PUNTO **\_ DE CONTROL \_ BEZIER,** así como datos constantes de revisión (**HS \_ CONSTANT DATA \_ \_ OUTPUT**). La salida es un vértice que contiene los datos deseados: **DS \_ OUTPUT** en este ejemplo.

Después de diseñar un sombreador de dominio, [vea Cómo: Crear un sombreador de dominio.](direct3d-11-advanced-stages-domain-shader-create.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Introducción a la teselación](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 