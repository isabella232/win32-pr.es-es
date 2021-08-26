---
title: Planos de recorte de usuario en hardware de nivel 9 de características
description: A partir de Windows 8, el Lenguaje de sombreador de alto nivel (HLSL) de Microsoft admite una sintaxis que se puede usar con la API de Microsoft Direct3D 11 para especificar planos de recorte de usuario en el nivel de característica 9 x y \_ superior.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6ffd624e688dbe5e3591e10ee5c005a9d4564dc5a536e9c89cfcee50067c2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948975"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>Planos de recorte de usuario en hardware de nivel 9 de características

A partir de Windows 8, el Lenguaje de sombreador de alto nivel (HLSL) de Microsoft admite una sintaxis que se puede usar con la API de Microsoft Direct3D 11 para especificar planos de recorte de usuario en el nivel [de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) característica 9 x y \_ superior. Puede usar esta sintaxis de planos de recorte para escribir un sombreador y, a continuación, usar ese objeto de sombreador con la API de Direct3D 11 para ejecutarse en todos los niveles de características de Direct3D.

-   [Información preliminar](#background-reading)
-   [Sintaxis](#syntax)
-   [Creación de planos de recorte en el espacio de recorte en el nivel de característica 9 y superior](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [Lectura en segundo plano](#background-reading)
    -   [Niveles de características 10Level9](#10level9-feature-levels)
    -   [Cálculo matemático de plano de recorte](#clip-plane-math)
    -   [Recorte en el espacio de vista](#clipping-in-view-space)
    -   [Matriz de proyección](#projection-matrix)
    -   [Plano de recorte del espacio de recorte](#clip-space-clip-plane)
-   [Temas relacionados](#related-topics)

## <a name="background"></a>Información previa

Puede acceder a los planos de recorte de usuario en la API de Microsoft Direct3D 9 a través de los métodos [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) e [**IDirect3DDevice9::GetClipPlane.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) En Microsoft Direct3D 10 y versiones posteriores, puede acceder a planos de recorte de usuario a través de la [semántica \_ SV ClipDistance.](dx-graphics-hlsl-semantics.md) Pero antes Windows 8, SV ClipDistance no estaba disponible para el hardware x de nivel de característica 9 en las \_ API de [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ Direct3D 10 o Direct3D 11. Por lo tanto, antes Windows 8, la única manera de acceder a los planos de recorte de usuario con hardware de nivel de característica 9 x era a través de la \_ API de Direct3D 9. Las aplicaciones Windows Store de Direct3D no pueden usar la API de Direct3D 9. Aquí se describe la sintaxis que puede usar para acceder a planos de recorte de usuario a través de la API de Direct3D 11 en el nivel de característica 9 \_ x y superior.

Las aplicaciones usan planos de recorte para definir un conjunto de planos invisibles dentro del mundo 3D que recortan (desejen) todas las primitivas dibujadas. Windows dibujará ningún píxel que esté en el lado negativo de los planos de recorte. A continuación, las aplicaciones pueden usar planos de recorte para representar las reflexión planas.

## <a name="syntax"></a>Syntax

Use esta sintaxis para declarar planos de recorte como atributos de función en una [declaración de función](dx-graphics-hlsl-function-syntax.md). Por ejemplo, aquí usamos la sintaxis en un fragmento del sombreador de vértices:

``` syntax
cbuffer ClipPlaneConstantBuffer 
{
       float4 clipPlane1;
       float4 clipPlane2;
};

[clipplanes(clipPlane1,clipPlane2)]
VertexShaderOutput main(VertexShaderInput input)
{
       // the rest of the vertex shader doesn't refer to the clip plane
 
       …
 
       return output;
}
```

Este ejemplo para un fragmento de sombreador de vértices denota dos planos de recorte. Muestra que debe colocar el nuevo atributo **clipplanes** entre corchetes inmediatamente antes del valor devuelto del sombreador de vértices. Entre paréntesis después del atributo **clipplanes,** se proporciona una lista de hasta 6 constantes **float4** que definen los coeficientes de plano para cada plano de recorte activo. En el ejemplo también se muestra que debe hacer que los coeficientes de cada plano residan en un búfer constante.

> [!Note]  
> No hay ninguna sintaxis disponible para deshabilitar dinámicamente un plano de recorte. Debe volver a compilar un sombreador idéntico sin ningún atributo **clipplanes,** o bien la aplicación puede establecer los coeficientes del búfer constante en cero para que el plano ya no afecte a ninguna geometría.

 

Esta sintaxis está disponible para cualquier destino de sombreador de vértices 4.0 o posterior, que incluye \_ 4 \_ 0 \_ nivel 9 1 y \_ 4 0 nivel \_ \_ \_ \_ \_ 9 \_ 3.

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>Creación de planos de recorte en el espacio de recorte en el nivel de característica 9 y superior

Aquí se muestra cómo crear planos de recorte en el espacio de recorte en [el nivel](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de característica 9 x \_ y superior.

### <a name="background-reading"></a>Lectura en segundo plano

"Introduction to 3D Game Programming with DirectX 10" (Introducción a la programación de juegos en 3D con DirectX 10) de Frank D. Luna explica el fondo matemático de gráficos (capítulos 1, 2 y 3) que necesita y las diversas transformaciones de espacios y espacios que se producen en el sombreador de vértices (secciones 5.6 y 5.8).

### <a name="10level9-feature-levels"></a>Niveles de características 10Level9

En Direct3D 10 y versiones posteriores, puede recortar en cualquier espacio que tenga sentido, a menudo en el espacio del mundo o en el espacio de vista. Pero Direct3D 9 usa el espacio de recorte, que es el espacio de proyección de división de perspectiva previa. Los vectores están en el espacio de recorte cuando el sombreador de vértices los pasa a las fases siguientes en la canalización [de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).

Al escribir una aplicación de Windows Store, debe usar los niveles de características 10Level9[(nivel](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de característica 9 x) para que la aplicación se pueda ejecutar en el nivel de característica 9 x y \_ hardware \_ superior. Dado que la aplicación admite el nivel de característica 9 x y superior, también debe usar la funcionalidad común de aplicar planos de \_ recorte en el espacio de recorte.

Al compilar un sombreador de vértices con frente a 4 0 nivel 9 1 o posterior, ese sombreador de vértices puede \_ \_ usar el atributo \_ \_ \_ **clipplanes.** Un objeto Direct3D 10 o posterior tiene un producto de punto del vértice emitido que contiene cada una de las constantes globales **float4** especificadas en el atributo . El objeto Direct3D 9 tiene suficientes metadatos para hacer que el entorno de ejecución 10Level9 emita las llamadas adecuadas a [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).

### <a name="clip-plane-math"></a>Cálculo matemático de plano de recorte

Un plano de recorte se define mediante un vector con 4 componentes. Los tres primeros componentes definen un vector x, y, z que se origina en el espacio que se quiere recortar. Este vector implica un plano, uno al vector y otro que se ejecuta a través del origen. Windows mantiene todos los píxeles en el lado vectorial del plano y recorta todos los píxeles detrás del plano. El componente forth w inserta el plano hacia atrás y hace que Windows recorte menos (un w negativo hace que Windows recorte más) a lo largo de la línea vectorial. Si los componentes x, y, z componen un vector de unidad (normalizado), w vuelve a insertar el plano con unidades.

La matemática que realiza la unidad de procesamiento gráfico (GPU) para determinar que el recorte es un producto de punto simple entre el vector de vértice (x, y, z, 1) y el vector del plano de recorte. Esta operación matemática crea una longitud de proyección en el vector del plano de recorte. Un producto de punto negativo muestra que el vértice está en el lado recortado del plano.

### <a name="clipping-in-view-space"></a>Recorte en el espacio de vista

Este es nuestro vértice en el espacio de vista:

![vértice en el espacio de vista](images/vertex-clip.png)

Este es nuestro plano de recorte en el espacio de vista:

![plano de recorte en el espacio de vista](images/clip-plane-view.png)

Este es el producto de punto del vértice y el plano de recorte en el espacio de vista:

ClipDistance = **v** · **C**  =  *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub>  +  *v*<sub>z</sub>*C*<sub>z</sub>  +  *C*<sub>w</sub>

Esta operación matemática funciona para un objeto Direct3D 10 o posterior, pero no funcionará para un objeto Direct3D 9. Para Direct3D 9, primero debemos pasar a través de la transformación de proyección en espacio de recorte.

### <a name="projection-matrix"></a>Matriz de proyección

Una matriz de proyección transforma un vértice del espacio de vista (donde el origen es el ojo del visor, +x está a la derecha, +y está hacia arriba y +z está directamente delante) en un espacio de recorte. La matriz de proyección lee el vértice para el recorte de hardware y la fase [de rasterización](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage). Esta es una matriz de perspectiva estándar (otras proyecciones requieren matemáticas diferentes):

<dl> *Proporción de r*   de ancho y alto de la ventana  
*α*   ángulo de visualización  
*f*   distancia desde el visor hasta el plano lejano  
*n*   distancia desde el visor hasta el plano cercano
</dl>![Matriz de proyección](images/projection-matrix.png)

La siguiente matriz es una versión simplificada de la matriz anterior. Mostramos la matriz simplificada para que podamos usarla más adelante en la operación de multiplicación de matriz.

![Matriz de proyección simplificada](images/projection-matrix2.png)

Ahora transformamos el vértice del espacio de vista en un espacio de recorte con una matriz multiplicada:

![multiplicación de matrices](images/matrix-multiply.png)

En la operación de multiplicación de matriz, los componentes x e y solo se ajustan ligeramente, pero los componentes z y w están bastante desajustados. El plano de recorte ya no nos dará lo que queremos.

### <a name="clip-space-clip-plane"></a>Plano de recorte del espacio de recorte

Aquí queremos crear un plano de recorte de espacio de recorte cuyo producto de punto con el vértice del espacio de recorte nos da el mismo valor que **v · C** en la [sección Recorte en el espacio de](#clipping-in-view-space) vista.

![plano de recorte](images/clip-space-clip-plane.png)

**v** · **C**  =  **v P** · **C**<sub>P</sub>

*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub>  +  *v*<sub>z</sub>*C*<sub>z</sub>  +  *C*<sub>w</sub>  =  *v* ₓ *P* ₓ *C*<sub>Pₓ</sub>  + *v*<sub>y</sub>P <sub>y</sub>*C* P <sub><sub>y</sub></sub>  +  *v v*<sub>z</sub>*A*<sub>y</sub>*C* P <sub><sub>z</sub></sub>  +  *BC* P <sub><sub>z</sub></sub>  +  *v*<sub>z</sub>*C* P <sub><sub>w</sub></sub>

Ahora podemos dividir la operación matemática anterior por componente de vértice en cuatro ecuaciones independientes:

![Componente de vértice x del producto de plano de recorte](images/clip-space-clip-plane-equ1.png)

![Componente de vértice y del producto de plano de recorte](images/clip-space-clip-plane-equ2.png)

![w componente de vértice del producto de plano de recorte](images/clip-space-clip-plane-equ3.png)

![Componente de vértice z del producto de plano de recorte](images/clip-space-clip-plane-equ4.png)

El plano de recorte del espacio de vista y la matriz de proyección derivan y nos dan el plano de recorte del espacio de recorte.

![plano de recorte del espacio de recorte](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Sintaxis de declaración de funciones](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 