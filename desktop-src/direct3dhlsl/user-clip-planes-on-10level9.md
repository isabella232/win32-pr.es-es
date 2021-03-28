---
title: Planos de clip de usuario en hardware de nivel de característica 9
description: A partir de Windows 8, el lenguaje de sombreador de alto nivel (HLSL) de Microsoft admite una sintaxis que se puede usar con la API de Microsoft Direct3D 11 para especificar los planos de clip de usuario en el nivel de característica 9 \_ x y versiones posteriores.
ms.assetid: C51FB0E5-94C3-4E7F-AC33-E5F0F26EDC11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968831ca39f2501a44b00f202fd8dfda1f92d1e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359119"
---
# <a name="user-clip-planes-on-feature-level-9-hardware"></a>Planos de clip de usuario en hardware de nivel de característica 9

A partir de Windows 8, el lenguaje de sombreador de alto nivel (HLSL) de Microsoft admite una sintaxis que se puede usar con la API de Microsoft Direct3D 11 para especificar los planos de clip de usuario en el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x y versiones posteriores. Puede usar esta sintaxis de planos de clips para escribir un sombreador y, a continuación, usar ese objeto de sombreador con la API de Direct3D 11 para ejecutarlo en todos los niveles de características de Direct3D.

-   [Información preliminar](#background-reading)
-   [Sintaxis](#syntax)
-   [Crear planos de clips en el espacio de recorte en el nivel de característica 9 y versiones posteriores](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [Lectura en segundo plano](#background-reading)
    -   [niveles de características de 10Level9](#10level9-feature-levels)
    -   [Matemáticas del plano de recorte](#clip-plane-math)
    -   [Recorte en el espacio de la vista](#clipping-in-view-space)
    -   [Matriz de proyección](#projection-matrix)
    -   [Plano de recorte del espacio de recorte](#clip-space-clip-plane)
-   [Temas relacionados](#related-topics)

## <a name="background"></a>Información previa

Puede tener acceso a los planos de clips del usuario en la API de Microsoft Direct3D 9 a través de los métodos [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) y [**IDirect3DDevice9:: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) . En Microsoft Direct3D 10 y versiones posteriores, puede tener acceso a los planos de clips del usuario a través de la semántica de [ \_ ClipDistance VP](dx-graphics-hlsl-semantics.md) . Pero antes de Windows 8, la VP \_ ClipDistance no estaba disponible para el hardware de [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x en las API de Direct3D 10 o Direct3D 11. Por lo tanto, antes de Windows 8, la única manera de tener acceso a los planos de clips del usuario con el hardware de nivel de característica 9 \_ x era a través de la API de Direct3D 9. Las aplicaciones de la tienda Windows de Direct3D no pueden usar la API de Direct3D 9. Aquí se describe la sintaxis que puede usar para acceder a los planos de clips del usuario a través de la API de Direct3D 11 en el nivel de característica 9 \_ x y versiones posteriores.

Las aplicaciones usan planos de recortes para definir un conjunto de planos invisibles dentro del mundo 3D que recortan (descartan) todos los primitivos trazados. Windows no dibujará ningún píxel que esté en el lado negativo de los planos de clips. Las aplicaciones pueden usar planos de recortes para representar reflexiones planas.

## <a name="syntax"></a>Sintaxis

Use esta sintaxis para declarar planos de clips como atributos de función en una [declaración de función](dx-graphics-hlsl-function-syntax.md). Por ejemplo, aquí usamos la sintaxis en un fragmento de sombreador de vértices:

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

Este ejemplo para un fragmento del sombreador de vértices denota dos planos de clips. Muestra que es necesario colocar el nuevo atributo **clipplanes** entre corchetes inmediatamente antes del valor devuelto del sombreador de vértices. Entre paréntesis después del atributo **clipplanes** , se proporciona una lista de hasta 6 constantes de **FLOAT4** que definen los coeficientes de plano para cada plano de recorte activo. En el ejemplo también se muestra que es necesario que los coeficientes de cada plano residan en un búfer de constantes.

> [!Note]  
> No hay ninguna sintaxis disponible para deshabilitar dinámicamente un plano de recorte. Debe volver a compilar un sombreador idéntico de otro modo sin ningún atributo **clipplanes** o la aplicación puede establecer los coeficientes en el búfer de constantes en cero para que el plano ya no afecte a ninguna geometría.

 

Esta sintaxis está disponible para cualquier destino del sombreador de vértices 4,0 o posterior, que incluye vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1 y vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 3.

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a>Crear planos de clips en el espacio de recorte en el nivel de característica 9 y versiones posteriores

Aquí se muestra cómo crear planos de clips en el espacio de recorte en el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x y versiones posteriores.

### <a name="background-reading"></a>Lectura en segundo plano

"Introducción a la programación de juegos 3D con DirectX 10" de Frank D. Luna explica el fondo de matemáticas de gráficos (capítulos 1, 2 y 3) que necesita y los distintos espacios y transformaciones de espacio que se producen en el sombreador de vértices (secciones 5,6 y 5,8).

### <a name="10level9-feature-levels"></a>niveles de características de 10Level9

En Direct3D 10 y versiones posteriores, puede recortar cualquier espacio que tenga sentido, a menudo en el espacio universal o en el espacio de la vista. Pero Direct3D 9 usa el espacio de recorte, que es la perspectiva previa dividir el espacio de proyección. Los vectores están en el espacio de recorte cuando el sombreador de vértices los pasa a las fases siguientes en la [canalización de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).

Al escribir una aplicación de la tienda Windows, debe usar los niveles de características de 10Level9 ([nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) para que la aplicación se pueda ejecutar en el nivel de características 9 \_ x y el hardware superior. Dado que la aplicación admite el nivel \_ de características 9 x y versiones posteriores, también debe usar la funcionalidad común de aplicar planos de clips en el espacio de recorte.

Al compilar un sombreador de vértices con vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1 o posterior, ese sombreador de vértices puede usar el atributo **clipplanes** . Un objeto de Direct3D 10 o posterior tiene un producto de punto del vértice emitido que contiene cada una de las constantes globales de **FLOAT4** especificadas en el atributo. El objeto de Direct3D 9 tiene suficientes metadatos para hacer que el tiempo de ejecución de 10Level9 emita las llamadas adecuadas a [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).

### <a name="clip-plane-math"></a>Matemáticas del plano de recorte

Un plano de recorte se define mediante un vector con 4 componentes. Los tres primeros componentes definen un vector x, y, z que emana del origen en el espacio que queremos recortar. Este vector implica un plano, perpendicular al vector y que se ejecuta a través del origen. Windows mantiene todos los píxeles en el lado vectorial del plano y recorta todos los píxeles detrás del plano. El componente en adelante inserta el plano y hace que Windows se recorte menos (un negativo w hace que Windows se recorte más) a lo largo de la línea vectorial. Si los componentes x, y, z componen un vector de unidad (normalizado), w envía las unidades de plano hacia atrás.

Los cálculos que la unidad de procesamiento de gráficos (GPU) realiza para determinar el recorte son un producto punto sencillo entre el vector de vértice (x, y, z, 1) y el vector del plano de recorte. Esta operación matemática crea una longitud de proyección en el vector del plano de recorte. Un producto de punto negativo muestra el vértice que se encuentra en el lado recortado del plano.

### <a name="clipping-in-view-space"></a>Recorte en el espacio de la vista

Este es el vértice en el espacio de la vista:

![vértice en el espacio de la vista](images/vertex-clip.png)

Este es nuestro plano de recorte en el espacio de la vista:

![plano de recorte en el espacio de la vista](images/clip-plane-view.png)

Este es el producto de punto de vértice y plano de recorte en el espacio de la vista:

ClipDistance = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*z c*<sub>z</sub>  +  <sub></sub>

Esta operación matemática funciona para un objeto de Direct3D 10 o posterior, pero no funciona para un objeto de Direct3D 9. Para Direct3D 9, primero debemos obtener nuestra transformación de proyección en el espacio de recorte.

### <a name="projection-matrix"></a>Matriz de proyección

Una matriz de proyección transforma un vértice del espacio de la vista (donde el origen es el ojo del espectador, + x está a la derecha, + y está activo y + z es recto) en el espacio de recorte. La matriz de proyección lee el vértice para el recorte de hardware y la [fase de rasterización](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage). Esta es una matriz de perspectiva estándar (otras proyecciones requieren cálculos diferentes):

<dl>    proporción de r de ancho/alto de ventana  
ángulo de visualización de *α*    
*f*   distancia desde el visor hasta el plano lejano  
*n*   distancia desde el visor hasta el plano próximo
</dl>![matriz de proyección](images/projection-matrix.png)

La siguiente matriz es una versión simplificada de la matriz anterior. Mostramos la matriz simplificada para poder usarla más adelante en la operación de multiplicación de la matriz.

![matriz de proyección simplificada](images/projection-matrix2.png)

Ahora transformaremos el vértice del espacio de la vista en el espacio de recorte con una multiplicación de matriz:

![multiplicación de matriz](images/matrix-multiply.png)

En la operación de multiplicación de la matriz, los componentes x e y solo se ajustan ligeramente, pero los componentes z y w son muy alterados. Nuestro plano de recorte no nos proporcionará lo que queremos más.

### <a name="clip-space-clip-plane"></a>Plano de recorte del espacio de recorte

Aquí queremos crear un plano de clip de espacio de recorte cuyo producto de punto con nuestro vértice de espacio de recorte nos proporcione el mismo valor que **v · C** en la sección [recorte en el espacio de la vista](#clipping-in-view-space) .

![plano de recorte](images/clip-space-clip-plane.png)

**v** · **C**  =  **v P** · **C**<sub>P</sub>

*v* ₓ *C* ₓ +*v*<sub>y</sub>*c*<sub></sub>  +  <sub>z z</sub><sub>c z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *P* ₓ *c*<sub>p ₓ</sub>  + *v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z z</sub></sub>  +  <sub><sub></sub></sub>  +  <sub></sub><sub><sub></sub></sub> z p z p z

Ahora podemos dividir la operación matemática anterior por componente de vértice en cuatro ecuaciones independientes:

![componente de vértice x del producto del plano de recorte](images/clip-space-clip-plane-equ1.png)

![componente de vértice y del producto de plano de recorte](images/clip-space-clip-plane-equ2.png)

![componente de vértice w del producto del plano de recorte](images/clip-space-clip-plane-equ3.png)

![componente de vértice z del producto del plano de recorte](images/clip-space-clip-plane-equ4.png)

Nuestro plano de recorte de espacio de vista y nuestra matriz de proyección derivan y nos proporcionan nuestro plano de recorte.

![plano de recorte del espacio de recorte](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[Sintaxis de declaración de funciones](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 