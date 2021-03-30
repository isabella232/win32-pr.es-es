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
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Transferencia Radiance precalculada (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Usar la transferencia Radiance precalculada

Hay varias formas de complejidad presentes en escenas interesantes, como la forma en que se modela el entorno de iluminación (es decir, modelos de iluminación de área frente a puntos o direccionales) y qué tipo de efectos globales se modelan (por ejemplo, sombras, interflexiones, dispersión de subsuperficies). Las técnicas de representación interactivas tradicionales modelan una cantidad limitada de esta complejidad. PRT permite estos efectos con algunas restricciones importantes:

-   Se supone que los objetos son rígidos (es decir, ninguna desformación).
-   Se trata de un enfoque centrado en objetos (a menos que los objetos se muevan juntos; estos efectos globales no se mantienen entre ellos).
-   Solo se modela la iluminación de baja frecuencia (lo que da lugar a sombras flexibles). En el caso de las luces de alta frecuencia (sombras vivas), se tendrían que emplear técnicas tradicionales.

PRT requiere una de las siguientes opciones, pero no ambas:

-   modelos de teselación alta y vs \_ 1 \_ 1
-   PS \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Iluminación difusa estándar frente a PRT

La siguiente ilustración se representa con el modelo de iluminación tradicional (n · l). Las sombras nítidas se pueden habilitar con otro paso y alguna forma de técnica de sombreado (mapas de profundidad de sombra o volúmenes de instantáneas). Agregar varias luces requeriría varios pasos (si se van a usar sombras) o sombreadores más complejos con técnicas tradicionales.

![captura de pantalla de una ilustración representada mediante el modelo de iluminación tradicional](images/prt-diffuse-cropped.png)

La siguiente ilustración se representa con PRT con la mejor aproximación de una luz direccional única que puede resolver. Esto da como resultado sombras flexibles que serían difíciles de producir con técnicas tradicionales. Dado que PRT siempre modela entornos de iluminación completos agregando varias luces o usando un mapa de entorno, solo cambiaría los valores (pero no el número) de constantes que usa el sombreador.

![captura de pantalla de una ilustración representada mediante PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT con interflexiones

La iluminación directa alcanza la superficie directamente de la luz. Las interflexiones son claras al alcanzar la superficie después de rebotar alguna otra superficie un número determinado de veces. PRT puede modelar este comportamiento sin cambiar el rendimiento en tiempo de ejecución simplemente ejecutando el simulador con distintos parámetros.

La siguiente ilustración se crea solo con Direct PRT (0 rebota sin interacciones).

![captura de pantalla de una ilustración presentada solo con Direct PRT](images/prt-nointerreflections.png)

La siguiente ilustración se crea con PRT con interflexiones (2 rebotas con interacciones).

![captura de pantalla de una ilustración representada mediante PRT con interflexiones](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT con dispersión de subsuperficies

La dispersión de subsuperficies es una técnica que modela cómo pasa la luz a través de determinados materiales. Por ejemplo, presione una linterna iluminada en la palma de la mano. La luz de la linterna pasa a través de la mano, rebota (cambiar el color en el proceso) y sale del otro lado de la mano. También se puede modelar con cambios sencillos en el simulador y sin cambios en el tiempo de ejecución.

En la ilustración siguiente se muestra PRT con dispersión de subsuperficies.

![captura de pantalla de una ilustración representada mediante PRT con dispersión de subsuperficies](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Cómo funciona PRT

Los siguientes términos son útiles para comprender cómo funciona PRT, tal como se muestra en el diagrama siguiente.

Source Radiance: el Radiance de origen representa el entorno de iluminación en conjunto. En PRT, se aproxima un entorno arbitrario mediante la base de armónico esférico: se supone que se trata de una iluminación lejana respecto al objeto (la misma suposición que se realiza con mapas de entorno).

Exit Radiance: Exit Radiance es la luz que sale de un punto de la superficie de cualquier origen posible (reflejado radiance, dispersión de subsuperficies, emisión).

Vectores de transferencia: los vectores de transferencia asignan el origen Radiance a la salida Radiance y se calculan previamente sin conexión mediante una simulación de transporte ligero complejo.

![diagrama de cómo funciona PRT](images/prt-lightingpicture.png)

PRT factores el proceso de representación en dos fases, tal como se muestra en el diagrama siguiente:

1.  Una simulación de transporte de luz costosa calcula previamente los coeficientes de transferencia que se pueden usar en tiempo de ejecución.
2.  En primer lugar, una fase de tiempo de ejecución relativamente ligera aproxima el entorno de iluminación con el modelo armónico esférico y luego usa estos coeficientes de iluminación y los coeficientes de transferencia precalculados (de la fase 1) con un sombreador simple, lo que da lugar a la salida de Radiance (la luz que sale del objeto).

![diagrama del flujo de datos de PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Cómo usar la API de PRT

1.  Calcular los vectores de transferencia con uno de los tipos de proceso... métodos de [**ID3DXPRTEngine**](id3dxprtengine.md).

    Tratar directamente con estos vectores de transferencia requiere una cantidad significativa de memoria y cálculo del sombreador. La compresión reduce significativamente la cantidad de memoria y el cálculo del sombreador necesarios.

    Los valores de iluminación finales se calculan en un sombreador de vértices que implementa la siguiente ecuación de representación comprimida.

    ![ecuación de la representación de PRT](images/prt-shaderequation.png)

    Donde:

    

    | Parámetro      | Descripción                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | RP             | Un solo canal de salida radiance en el vértice p y se evalúa en cada vértice de la malla.                     |
    | MK             | La media del clúster k. Este es un vector de pedido ² de coeficientes.                                               |
    | k              | El identificador de clúster para el vértice p.                                                                                    |
    | L<sup>'</sup>  | La aproximación de la Radiance de origen en las funciones de base de SH. Este es un vector de pedido ² de coeficientes. |
    | j              | Entero que suma el número de vectores PCA.                                                            |
    | en<sub>blanco</sub> | Peso del PCA de JTH para el punto p. Se trata de un único coeficiente.                                                   |
    | B<sub>KJ</sub> | Vector de base del PCA de JTH para el clúster k. Este es un vector de pedido ² de coeficientes.                               |

    

     

    El extracto... los métodos de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) proporcionan acceso a los datos comprimidos desde la simulación.

2.  Calcule el Radiance de origen.

    Hay varias funciones auxiliares en la API para controlar diversos escenarios de iluminación comunes.

    

    | Función                                                         | Finalidad                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Aproxima una luz direccional convencional.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Se aproxima a las fuentes de luz esféricas locales. (Tenga en cuenta que PRT solo funciona con entornos de iluminación de distancia). |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Aproxima una fuente de luz de área distante. Un ejemplo sería el sol (ángulo de cono muy pequeño).              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | Evalúa una luz que es una interpolación lineal entre dos colores (uno en cada polo de una esfera).         |

    

     

3.  Calcule el Radiance de salida.

    La ecuación 1 ahora debe evaluarse en cada punto mediante un sombreador de vértices o de píxeles. Antes de que se pueda evaluar el sombreador, las constantes deben calcularse previamente y cargarse en la tabla de constantes (vea el [ejemplo de demostración de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) para obtener más detalles). El propio sombreador es una implementación sencilla de esta ecuación.

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

    

## <a name="references"></a>Referencias

Para obtener más información acerca de PRT y armónicos esféricos, consulte los siguientes documentos:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas avanzados](advanced-topics.md)
</dt> <dt>

[Ecuaciones de PRT (Direct3D 9)](prt-equations.md)
</dt> <dt>

[Representar PRT con texturas (Direct3D 9)](representing-prt-with-textures.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTEngine**](id3dxprtengine.md)
</dt> <dt>

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)
</dt> <dt>

[Funciones de transferencia Radiance precalculadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



