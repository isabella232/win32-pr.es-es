---
description: Transferencia de base precalcalada (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Transferencia de base precalcalada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc18eff66dab9a696a3e441d894a327890c53888da008d72a5f143ca0d345a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798763"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Transferencia de base precalcalada (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Uso de la transferencia de radiancia precalcalada

Hay varias formas de complejidad presentes en escenas interesantes, incluida la forma en que se modela el entorno de iluminación (es decir, los modelos de iluminación de área frente a los de punto/direccional) y qué tipo de efectos globales se modela (por ejemplo, sombras, interreferencias, dispersión de subsuperficie). Las técnicas de representación interactiva tradicionales modela una cantidad limitada de esta complejidad. PRT habilita estos efectos con algunas restricciones significativas:

-   Se supone que los objetos son rígidas (es decir, sin degradaciones).
-   Es un enfoque centrado en objetos (a menos que los objetos se mueven juntos, estos efectos globales no se mantienen entre ellos).
-   Solo se modela la iluminación de baja frecuencia (lo que da lugar a sombras suave). En el caso de las luces de alta frecuencia (sombras nítidas), se tendrían que emplear técnicas tradicionales.

PRT requiere una de las siguientes opciones, pero no ambas:

-   modelos muy teselados y frente a \_ \_ 1 1
-   ps \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Iluminación difusa estándar frente a PRT

La ilustración siguiente se representa mediante el modelo de iluminación tradicional (n · l). Las sombras nítidas se pueden habilitar mediante otro paso y algún tipo de técnica de sombreado (mapas de profundidad de sombra o volúmenes de sombra). Agregar varias luces requeriría varios pases (si se van a usar sombras) o sombreadores más complejos con técnicas tradicionales.

![captura de pantalla de una ilustración que se representa mediante el modelo de iluminación tradicional](images/prt-diffuse-cropped.png)

La siguiente ilustración se representa con PRT con la mejor aproximación de una sola luz direccional que puede resolver. Esto da como resultado sombras débiles que serían difíciles de producir con técnicas tradicionales. Dado que PRT siempre modela entornos de iluminación completos que agregan varias luces o usan un mapa de entorno, solo cambiaría los valores (pero no el número) de constantes utilizadas por el sombreador.

![captura de pantalla de una ilustración que se representa mediante prt](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT con interreferencias

La iluminación directa llega a la superficie directamente desde la luz. Las interreferencias son luz que llega a la superficie después de saltar alguna otra superficie varias veces. PRT puede modelar este comportamiento sin cambiar el rendimiento en tiempo de ejecución simplemente ejecutando el simulador con parámetros diferentes.

La siguiente ilustración se crea usando solo PRT directo (0 saltos sin interreferencias).

![captura de pantalla de una ilustración que se representa solo mediante prt directo](images/prt-nointerreflections.png)

La siguiente ilustración se crea mediante PRT con interreferencias (2 saltos con interreferencias).

![captura de pantalla de una ilustración que se representa mediante prt con interreferencias](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT con dispersión de subsuelo

La dispersión de subsuperficie es una técnica que modela cómo pasa la luz a través de ciertos materiales. Por ejemplo, presione una linterna de luz contra la mano. La luz de la bombilla pasa por la mano, salta (cambia de color en el proceso) y sale del otro lado de la mano. También se puede modelar con cambios sencillos en el simulador y sin cambios en el tiempo de ejecución.

En la ilustración siguiente se muestra el PRT con dispersión de subsuperficie.

![captura de pantalla de una ilustración que se representa mediante prt con dispersión de subsuperficie](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Funcionamiento del PRT

Los términos siguientes son útiles para comprender cómo funciona el PRT, como se muestra en el diagrama siguiente.

Radiance de origen: el radiance de origen representa el entorno de iluminación en su conjunto. En PRT, se aproxima un entorno arbitrario mediante la base de armónica esférica: se supone que esta iluminación es lejana con respecto al objeto (la misma suposición que se realiza con los mapas de entorno).

Radiance de salida: el radiance de salida es la luz que sale de un punto de la superficie desde cualquier origen posible (radiancia reflejada, dispersión de subsuperficie, emisión).

Vectores de transferencia: los vectores de transferencia asignan el radiance de origen al radiance de salida y se precalutan sin conexión mediante una simulación de transporte de luz compleja.

![diagrama de cómo funciona prt](images/prt-lightingpicture.png)

PRT factorización del proceso de representación en dos fases, como se muestra en el diagrama siguiente:

1.  Una simulación de transporte ligero costosa precompute los coeficientes de transferencia que se pueden usar en tiempo de ejecución.
2.  En primer lugar, una fase en tiempo de ejecución relativamente ligera se aproxima al entorno de iluminación mediante la base de armónica esférica y, a continuación, usa estos coeficientes de iluminación y los coeficientes de transferencia precalutados (de la fase 1) con un sombreador simple, lo que da lugar a un brillo de salida (la luz que sale del objeto).

![diagrama de flujo de datos prt](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Uso de la API de PRT

1.  Calcule los vectores de transferencia con uno de los... Métodos [**de ID3DXPRTEngine**](id3dxprtengine.md).

    Trabajar directamente con estos vectores de transferencia requiere una cantidad significativa de memoria y cálculo del sombreador. La compresión reduce significativamente la cantidad de memoria y el cálculo del sombreador necesarios.

    Los valores de iluminación finales se calculan en un sombreador de vértices que implementa la siguiente ecuación de representación comprimida.

    ![ecuación de representación prt](images/prt-shaderequation.png)

    Donde:

    

    | Parámetro      | Descripción                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | Rp             | Un único canal de radiancia de salida en el vértice p y se evalúa en cada vértice de la malla.                     |
    | Mk             | La media del clúster k. Se trata de un vector Ordermiento de coeficientes.                                               |
    | k              | Identificador del clúster para el vértice p.                                                                                    |
    | L<sup>'</sup>  | Aproximación de la base de origen en las funciones de base SH. Se trata de un vector Ordermiento de coeficientes. |
    | j              | Entero que suma el número de vectores pcA.                                                            |
    | w<sub>pj</sub> | Peso de PCA jth para el punto p. Se trata de un coeficiente único.                                                   |
    | B<sub>kj</sub> | Vector de base de PCA jth para el clúster k. Se trata de un vector Ordermiento de coeficientes.                               |

    

     

    La extracción... Los métodos [**de ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) proporcionan acceso a los datos comprimidos de la simulación.

2.  Calcule el radiance de origen.

    Hay varias funciones auxiliares en la API para controlar una variedad de escenarios de iluminación comunes.

    

    | Función                                                         | Finalidad                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Aproxima una luz direccional convencional.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Aproxima las fuentes de luz esféricas locales. (Tenga en cuenta que PRT solo funciona con entornos de iluminación de distancia). |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Se aproxima a una fuente de luz de área lejana. Un ejemplo sería el sol (ángulo de cono muy pequeño).              |
    | [**D3DXSHEvalRriisphereLight**](d3dxshevalhemispherelight.md)   | Evalúa una luz que es una interpolación lineal entre dos colores (uno en cada polo de una esfera).         |

    

     

3.  Calcule el radiance de salida.

    La ecuación 1 ahora debe evaluarse en cada punto mediante un sombreador de vértices o píxeles. Antes de que se pueda evaluar el sombreador, las constantes se deben precalutar y cargar en la tabla constante (consulte el ejemplo de [demostración de PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) para obtener más información). El propio sombreador es una implementación sencilla de esta ecuación.

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

Para obtener más información sobre PRT y armónicos esféricos, vea los siguientes artículos:


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

[Ecuaciones PRT (Direct3D 9)](prt-equations.md)
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

[Funciones de transferencia de radiancia precalutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



