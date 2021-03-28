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
# <a name="user-clip-planes-on-feature-level-9-hardware"></a><span data-ttu-id="741ea-103">Planos de clip de usuario en hardware de nivel de característica 9</span><span class="sxs-lookup"><span data-stu-id="741ea-103">User clip planes on feature level 9 hardware</span></span>

<span data-ttu-id="741ea-104">A partir de Windows 8, el lenguaje de sombreador de alto nivel (HLSL) de Microsoft admite una sintaxis que se puede usar con la API de Microsoft Direct3D 11 para especificar los planos de clip de usuario en el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="741ea-104">Starting with Windows 8, Microsoft High Level Shader Language (HLSL) supports a syntax that you can use with the Microsoft Direct3D 11 API to specify user clip planes on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="741ea-105">Puede usar esta sintaxis de planos de clips para escribir un sombreador y, a continuación, usar ese objeto de sombreador con la API de Direct3D 11 para ejecutarlo en todos los niveles de características de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="741ea-105">You can use this clip-planes syntax to write a shader, and then use that shader object with the Direct3D 11 API to run on all Direct3D feature levels.</span></span>

-   [<span data-ttu-id="741ea-106">Información preliminar</span><span class="sxs-lookup"><span data-stu-id="741ea-106">Background</span></span>](#background-reading)
-   [<span data-ttu-id="741ea-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="741ea-107">Syntax</span></span>](#syntax)
-   [<span data-ttu-id="741ea-108">Crear planos de clips en el espacio de recorte en el nivel de característica 9 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="741ea-108">Creating clip planes in clip space on feature level 9 and higher</span></span>](#creating-clip-planes-in-clip-space-on-feature-level-9-and-higher)
    -   [<span data-ttu-id="741ea-109">Lectura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="741ea-109">Background reading</span></span>](#background-reading)
    -   [<span data-ttu-id="741ea-110">niveles de características de 10Level9</span><span class="sxs-lookup"><span data-stu-id="741ea-110">10Level9 feature levels</span></span>](#10level9-feature-levels)
    -   [<span data-ttu-id="741ea-111">Matemáticas del plano de recorte</span><span class="sxs-lookup"><span data-stu-id="741ea-111">Clip plane math</span></span>](#clip-plane-math)
    -   [<span data-ttu-id="741ea-112">Recorte en el espacio de la vista</span><span class="sxs-lookup"><span data-stu-id="741ea-112">Clipping in view space</span></span>](#clipping-in-view-space)
    -   [<span data-ttu-id="741ea-113">Matriz de proyección</span><span class="sxs-lookup"><span data-stu-id="741ea-113">Projection matrix</span></span>](#projection-matrix)
    -   [<span data-ttu-id="741ea-114">Plano de recorte del espacio de recorte</span><span class="sxs-lookup"><span data-stu-id="741ea-114">Clip space clip plane</span></span>](#clip-space-clip-plane)
-   [<span data-ttu-id="741ea-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="741ea-115">Related topics</span></span>](#related-topics)

## <a name="background"></a><span data-ttu-id="741ea-116">Información previa</span><span class="sxs-lookup"><span data-stu-id="741ea-116">Background</span></span>

<span data-ttu-id="741ea-117">Puede tener acceso a los planos de clips del usuario en la API de Microsoft Direct3D 9 a través de los métodos [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) y [**IDirect3DDevice9:: GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) .</span><span class="sxs-lookup"><span data-stu-id="741ea-117">You can access user clip planes in the Microsoft Direct3D 9 API via [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane) and [**IDirect3DDevice9::GetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane) methods.</span></span> <span data-ttu-id="741ea-118">En Microsoft Direct3D 10 y versiones posteriores, puede tener acceso a los planos de clips del usuario a través de la semántica de [ \_ ClipDistance VP](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="741ea-118">In Microsoft Direct3D 10 and later, you can access user clip planes through the [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="741ea-119">Pero antes de Windows 8, la VP \_ ClipDistance no estaba disponible para el hardware de [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x en las API de Direct3D 10 o Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="741ea-119">But before Windows 8, SV\_ClipDistance was not available for [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x hardware in the Direct3D 10 or Direct3D 11 APIs.</span></span> <span data-ttu-id="741ea-120">Por lo tanto, antes de Windows 8, la única manera de tener acceso a los planos de clips del usuario con el hardware de nivel de característica 9 \_ x era a través de la API de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="741ea-120">So, before Windows 8, the only way to access user clip planes with feature level 9\_x hardware was through the Direct3D 9 API.</span></span> <span data-ttu-id="741ea-121">Las aplicaciones de la tienda Windows de Direct3D no pueden usar la API de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="741ea-121">Direct3D Windows Store apps can't use the Direct3D 9 API.</span></span> <span data-ttu-id="741ea-122">Aquí se describe la sintaxis que puede usar para acceder a los planos de clips del usuario a través de la API de Direct3D 11 en el nivel de característica 9 \_ x y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="741ea-122">Here we describe the syntax that you can use to access user clip planes through the Direct3D 11 API on feature level 9\_x and higher.</span></span>

<span data-ttu-id="741ea-123">Las aplicaciones usan planos de recortes para definir un conjunto de planos invisibles dentro del mundo 3D que recortan (descartan) todos los primitivos trazados.</span><span class="sxs-lookup"><span data-stu-id="741ea-123">Apps use clip planes to define a set of invisible planes within the 3D world that clip (throw away) all drawn primitives.</span></span> <span data-ttu-id="741ea-124">Windows no dibujará ningún píxel que esté en el lado negativo de los planos de clips.</span><span class="sxs-lookup"><span data-stu-id="741ea-124">Windows won't draw any pixel that is on the negative side of any clip planes.</span></span> <span data-ttu-id="741ea-125">Las aplicaciones pueden usar planos de recortes para representar reflexiones planas.</span><span class="sxs-lookup"><span data-stu-id="741ea-125">Apps can then use clip planes to render planar reflections.</span></span>

## <a name="syntax"></a><span data-ttu-id="741ea-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="741ea-126">Syntax</span></span>

<span data-ttu-id="741ea-127">Use esta sintaxis para declarar planos de clips como atributos de función en una [declaración de función](dx-graphics-hlsl-function-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="741ea-127">Use this syntax to declare clip planes as function attributes in a [function declaration](dx-graphics-hlsl-function-syntax.md).</span></span> <span data-ttu-id="741ea-128">Por ejemplo, aquí usamos la sintaxis en un fragmento de sombreador de vértices:</span><span class="sxs-lookup"><span data-stu-id="741ea-128">For example, here we use the syntax on a vertex shader fragment:</span></span>

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

<span data-ttu-id="741ea-129">Este ejemplo para un fragmento del sombreador de vértices denota dos planos de clips.</span><span class="sxs-lookup"><span data-stu-id="741ea-129">This example for a vertex shader fragment denotes two clip planes.</span></span> <span data-ttu-id="741ea-130">Muestra que es necesario colocar el nuevo atributo **clipplanes** entre corchetes inmediatamente antes del valor devuelto del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="741ea-130">It shows that you need to place the new **clipplanes** attribute within square brackets immediately before the return value of the vertex shader.</span></span> <span data-ttu-id="741ea-131">Entre paréntesis después del atributo **clipplanes** , se proporciona una lista de hasta 6 constantes de **FLOAT4** que definen los coeficientes de plano para cada plano de recorte activo.</span><span class="sxs-lookup"><span data-stu-id="741ea-131">Within parentheses after the **clipplanes** attribute, you provide a list of up to 6 **float4** constants that define the plane coefficients for each active clip plane.</span></span> <span data-ttu-id="741ea-132">En el ejemplo también se muestra que es necesario que los coeficientes de cada plano residan en un búfer de constantes.</span><span class="sxs-lookup"><span data-stu-id="741ea-132">The example also shows that you need to make the coefficients of each plane reside in a constant buffer.</span></span>

> [!Note]  
> <span data-ttu-id="741ea-133">No hay ninguna sintaxis disponible para deshabilitar dinámicamente un plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="741ea-133">There is no syntax available to disable a clip plane dynamically.</span></span> <span data-ttu-id="741ea-134">Debe volver a compilar un sombreador idéntico de otro modo sin ningún atributo **clipplanes** o la aplicación puede establecer los coeficientes en el búfer de constantes en cero para que el plano ya no afecte a ninguna geometría.</span><span class="sxs-lookup"><span data-stu-id="741ea-134">You must either recompile an otherwise identical shader with no **clipplanes** attribute, or your app can set the coefficients in your constant buffer to zero so that the plane no longer affects any geometry.</span></span>

 

<span data-ttu-id="741ea-135">Esta sintaxis está disponible para cualquier destino del sombreador de vértices 4,0 o posterior, que incluye vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1 y vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 3.</span><span class="sxs-lookup"><span data-stu-id="741ea-135">This syntax is available for any 4.0 or later vertex shader target, which includes vs\_4\_0\_level\_9\_1 and vs\_4\_0\_level\_9\_3.</span></span>

## <a name="creating-clip-planes-in-clip-space-on-feature-level-9-and-higher"></a><span data-ttu-id="741ea-136">Crear planos de clips en el espacio de recorte en el nivel de característica 9 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="741ea-136">Creating clip planes in clip space on feature level 9 and higher</span></span>

<span data-ttu-id="741ea-137">Aquí se muestra cómo crear planos de clips en el espacio de recorte en el [nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="741ea-137">Here we show how to create clip planes in clip space on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

### <a name="background-reading"></a><span data-ttu-id="741ea-138">Lectura en segundo plano</span><span class="sxs-lookup"><span data-stu-id="741ea-138">Background reading</span></span>

<span data-ttu-id="741ea-139">"Introducción a la programación de juegos 3D con DirectX 10" de Frank D. Luna explica el fondo de matemáticas de gráficos (capítulos 1, 2 y 3) que necesita y los distintos espacios y transformaciones de espacio que se producen en el sombreador de vértices (secciones 5,6 y 5,8).</span><span class="sxs-lookup"><span data-stu-id="741ea-139">"Introduction to 3D Game Programming with DirectX 10" by Frank D. Luna explains the graphics math background (chapters 1, 2 and 3) you need, and the various spaces and space transformations that occur in the vertex shader (sections 5.6 and 5.8).</span></span>

### <a name="10level9-feature-levels"></a><span data-ttu-id="741ea-140">niveles de características de 10Level9</span><span class="sxs-lookup"><span data-stu-id="741ea-140">10Level9 feature levels</span></span>

<span data-ttu-id="741ea-141">En Direct3D 10 y versiones posteriores, puede recortar cualquier espacio que tenga sentido, a menudo en el espacio universal o en el espacio de la vista.</span><span class="sxs-lookup"><span data-stu-id="741ea-141">In Direct3D 10 and later, you can clip in any space that makes sense, often in world space or view space.</span></span> <span data-ttu-id="741ea-142">Pero Direct3D 9 usa el espacio de recorte, que es la perspectiva previa dividir el espacio de proyección.</span><span class="sxs-lookup"><span data-stu-id="741ea-142">But Direct3D 9 uses clip space, which is pre perspective divide projection space.</span></span> <span data-ttu-id="741ea-143">Los vectores están en el espacio de recorte cuando el sombreador de vértices los pasa a las fases siguientes en la [canalización de gráficos](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span><span class="sxs-lookup"><span data-stu-id="741ea-143">Vectors are in clip space when the vertex shader passes them to stages that follow in the [graphics pipeline](/windows/desktop/direct3d11/overviews-direct3d-11-graphics-pipeline).</span></span>

<span data-ttu-id="741ea-144">Al escribir una aplicación de la tienda Windows, debe usar los niveles de características de 10Level9 ([nivel de característica](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x) para que la aplicación se pueda ejecutar en el nivel de características 9 \_ x y el hardware superior.</span><span class="sxs-lookup"><span data-stu-id="741ea-144">When you write a Windows Store app, you must use 10Level9 feature levels ([feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x) so the app can run on feature level 9\_x and higher hardware.</span></span> <span data-ttu-id="741ea-145">Dado que la aplicación admite el nivel \_ de características 9 x y versiones posteriores, también debe usar la funcionalidad común de aplicar planos de clips en el espacio de recorte.</span><span class="sxs-lookup"><span data-stu-id="741ea-145">Because your app supports feature level 9\_x and higher, you must also use the common capability of applying clip planes in clip space.</span></span>

<span data-ttu-id="741ea-146">Al compilar un sombreador de vértices con vs \_ 4 \_ 0 \_ nivel \_ 9 \_ 1 o posterior, ese sombreador de vértices puede usar el atributo **clipplanes** .</span><span class="sxs-lookup"><span data-stu-id="741ea-146">When you compile a vertex shader with vs\_4\_0\_level\_9\_1 or later, that vertex shader can use the **clipplanes** attribute.</span></span> <span data-ttu-id="741ea-147">Un objeto de Direct3D 10 o posterior tiene un producto de punto del vértice emitido que contiene cada una de las constantes globales de **FLOAT4** especificadas en el atributo.</span><span class="sxs-lookup"><span data-stu-id="741ea-147">A Direct3D 10 or later object has a dot product of the emitted vertex that contains each of the **float4** global constants specified in the attribute.</span></span> <span data-ttu-id="741ea-148">El objeto de Direct3D 9 tiene suficientes metadatos para hacer que el tiempo de ejecución de 10Level9 emita las llamadas adecuadas a [**IDirect3DDevice9:: SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span><span class="sxs-lookup"><span data-stu-id="741ea-148">The Direct3D 9 object has enough meta data to cause the 10Level9 runtime to issue the appropriate calls to [**IDirect3DDevice9::SetClipPlane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane).</span></span>

### <a name="clip-plane-math"></a><span data-ttu-id="741ea-149">Matemáticas del plano de recorte</span><span class="sxs-lookup"><span data-stu-id="741ea-149">Clip plane math</span></span>

<span data-ttu-id="741ea-150">Un plano de recorte se define mediante un vector con 4 componentes.</span><span class="sxs-lookup"><span data-stu-id="741ea-150">A clip plane is defined by a vector with 4 components.</span></span> <span data-ttu-id="741ea-151">Los tres primeros componentes definen un vector x, y, z que emana del origen en el espacio que queremos recortar.</span><span class="sxs-lookup"><span data-stu-id="741ea-151">The first three components define an x, y, z vector that emanates from the origin in the space we want to clip.</span></span> <span data-ttu-id="741ea-152">Este vector implica un plano, perpendicular al vector y que se ejecuta a través del origen.</span><span class="sxs-lookup"><span data-stu-id="741ea-152">This vector implies a plane, perpendicular to the vector and running through the origin.</span></span> <span data-ttu-id="741ea-153">Windows mantiene todos los píxeles en el lado vectorial del plano y recorta todos los píxeles detrás del plano.</span><span class="sxs-lookup"><span data-stu-id="741ea-153">Windows keeps all pixels on the vector side of the plane and clips all pixels behind the plane.</span></span> <span data-ttu-id="741ea-154">El componente en adelante inserta el plano y hace que Windows se recorte menos (un negativo w hace que Windows se recorte más) a lo largo de la línea vectorial.</span><span class="sxs-lookup"><span data-stu-id="741ea-154">The forth w component pushes the plane back and causes Windows to clip less (a negative w causes Windows to clip more) along the vector line.</span></span> <span data-ttu-id="741ea-155">Si los componentes x, y, z componen un vector de unidad (normalizado), w envía las unidades de plano hacia atrás.</span><span class="sxs-lookup"><span data-stu-id="741ea-155">If the x, y, z components compose a unit (normalized) vector, w pushes the plane w units back.</span></span>

<span data-ttu-id="741ea-156">Los cálculos que la unidad de procesamiento de gráficos (GPU) realiza para determinar el recorte son un producto punto sencillo entre el vector de vértice (x, y, z, 1) y el vector del plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="741ea-156">The math that the graphics processing unit (GPU) performs to determine clipping is a simple dot product between the vertex vector (x, y, z, 1) and the clipping plane vector.</span></span> <span data-ttu-id="741ea-157">Esta operación matemática crea una longitud de proyección en el vector del plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="741ea-157">This math operation creates a projection length on the clip plane vector.</span></span> <span data-ttu-id="741ea-158">Un producto de punto negativo muestra el vértice que se encuentra en el lado recortado del plano.</span><span class="sxs-lookup"><span data-stu-id="741ea-158">A negative dot product shows the vertex to be on the clipped side of the plane.</span></span>

### <a name="clipping-in-view-space"></a><span data-ttu-id="741ea-159">Recorte en el espacio de la vista</span><span class="sxs-lookup"><span data-stu-id="741ea-159">Clipping in view space</span></span>

<span data-ttu-id="741ea-160">Este es el vértice en el espacio de la vista:</span><span class="sxs-lookup"><span data-stu-id="741ea-160">Here is our vertex in view space:</span></span>

![vértice en el espacio de la vista](images/vertex-clip.png)

<span data-ttu-id="741ea-162">Este es nuestro plano de recorte en el espacio de la vista:</span><span class="sxs-lookup"><span data-stu-id="741ea-162">Here is our clip plane in view space:</span></span>

![plano de recorte en el espacio de la vista](images/clip-plane-view.png)

<span data-ttu-id="741ea-164">Este es el producto de punto de vértice y plano de recorte en el espacio de la vista:</span><span class="sxs-lookup"><span data-stu-id="741ea-164">Here is the dot product of vertex and clip plane in view space:</span></span>

<span data-ttu-id="741ea-165">ClipDistance = **v** · **C**  =  *v* ₓ *c* ₓ +*v*<sub>y</sub>*c*<sub>y</sub>  +  *v*<sub>z</sub>*z c*<sub>z</sub>  +  <sub></sub></span><span class="sxs-lookup"><span data-stu-id="741ea-165">ClipDistance = **v** · **C** = *v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub></span></span>

<span data-ttu-id="741ea-166">Esta operación matemática funciona para un objeto de Direct3D 10 o posterior, pero no funciona para un objeto de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="741ea-166">This math operation works for a Direct3D 10 or later object but won't work for a Direct3D 9 object.</span></span> <span data-ttu-id="741ea-167">Para Direct3D 9, primero debemos obtener nuestra transformación de proyección en el espacio de recorte.</span><span class="sxs-lookup"><span data-stu-id="741ea-167">For Direct3D 9, we must first get through our projection transform into clip space.</span></span>

### <a name="projection-matrix"></a><span data-ttu-id="741ea-168">Matriz de proyección</span><span class="sxs-lookup"><span data-stu-id="741ea-168">Projection matrix</span></span>

<span data-ttu-id="741ea-169">Una matriz de proyección transforma un vértice del espacio de la vista (donde el origen es el ojo del espectador, + x está a la derecha, + y está activo y + z es recto) en el espacio de recorte.</span><span class="sxs-lookup"><span data-stu-id="741ea-169">A projection matrix transforms a vertex from view space (where the origin is the viewer's eye, +x is to the right, +y is up, and +z is straight ahead) into clip space.</span></span> <span data-ttu-id="741ea-170">La matriz de proyección lee el vértice para el recorte de hardware y la [fase de rasterización](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span><span class="sxs-lookup"><span data-stu-id="741ea-170">The projection matrix readies the vertex for hardware clipping and the [rasterization stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage).</span></span> <span data-ttu-id="741ea-171">Esta es una matriz de perspectiva estándar (otras proyecciones requieren cálculos diferentes):</span><span class="sxs-lookup"><span data-stu-id="741ea-171">Here is a standard perspective matrix (other projections require different math):</span></span>

<dl> <span data-ttu-id="741ea-172">   proporción de r de ancho/alto de ventana</span><span class="sxs-lookup"><span data-stu-id="741ea-172">*r*  ratio of window width/height</span></span>  
<span data-ttu-id="741ea-173">ángulo de visualización de *α*  </span><span class="sxs-lookup"><span data-stu-id="741ea-173">*α*  viewing angle</span></span>  
<span data-ttu-id="741ea-174">*f*   distancia desde el visor hasta el plano lejano</span><span class="sxs-lookup"><span data-stu-id="741ea-174">*f*  distance from the viewer to the far plane</span></span>  
<span data-ttu-id="741ea-175">*n*   distancia desde el visor hasta el plano próximo</span><span class="sxs-lookup"><span data-stu-id="741ea-175">*n*  distance from the viewer to the near plane</span></span>
</dl><span data-ttu-id="741ea-176">![matriz de proyección](images/projection-matrix.png)</span><span class="sxs-lookup"><span data-stu-id="741ea-176">![projection matrix](images/projection-matrix.png)</span></span>

<span data-ttu-id="741ea-177">La siguiente matriz es una versión simplificada de la matriz anterior.</span><span class="sxs-lookup"><span data-stu-id="741ea-177">The next matrix is a simplified version of the previous matrix.</span></span> <span data-ttu-id="741ea-178">Mostramos la matriz simplificada para poder usarla más adelante en la operación de multiplicación de la matriz.</span><span class="sxs-lookup"><span data-stu-id="741ea-178">We show the matrix simplified so we can use it later in the matrix multiply operation.</span></span>

![matriz de proyección simplificada](images/projection-matrix2.png)

<span data-ttu-id="741ea-180">Ahora transformaremos el vértice del espacio de la vista en el espacio de recorte con una multiplicación de matriz:</span><span class="sxs-lookup"><span data-stu-id="741ea-180">Now we transform our view space vertex into clip space with a matrix multiply:</span></span>

![multiplicación de matriz](images/matrix-multiply.png)

<span data-ttu-id="741ea-182">En la operación de multiplicación de la matriz, los componentes x e y solo se ajustan ligeramente, pero los componentes z y w son muy alterados.</span><span class="sxs-lookup"><span data-stu-id="741ea-182">In our matrix multiply operation, our x and y components are only slightly adjusted, but our z and w components are quite mangled.</span></span> <span data-ttu-id="741ea-183">Nuestro plano de recorte no nos proporcionará lo que queremos más.</span><span class="sxs-lookup"><span data-stu-id="741ea-183">Our clip plane won't give us what we want any more.</span></span>

### <a name="clip-space-clip-plane"></a><span data-ttu-id="741ea-184">Plano de recorte del espacio de recorte</span><span class="sxs-lookup"><span data-stu-id="741ea-184">Clip space clip plane</span></span>

<span data-ttu-id="741ea-185">Aquí queremos crear un plano de clip de espacio de recorte cuyo producto de punto con nuestro vértice de espacio de recorte nos proporcione el mismo valor que **v · C** en la sección [recorte en el espacio de la vista](#clipping-in-view-space) .</span><span class="sxs-lookup"><span data-stu-id="741ea-185">Here we want to create a clip space clip plane whose dot product with our clip space vertex gives us the same value as **v · C** in the [Clipping in view space](#clipping-in-view-space) section.</span></span>

![plano de recorte](images/clip-space-clip-plane.png)

<span data-ttu-id="741ea-187">**v** · **C**  =  **v P** · **C**<sub>P</sub></span><span class="sxs-lookup"><span data-stu-id="741ea-187">**v** · **C** = **v P** · **C**<sub>P</sub></span></span>

<span data-ttu-id="741ea-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*c*<sub></sub>  +  <sub>z z</sub><sub>c z</sub>  +  *c*<sub>w</sub>  =  *v* ₓ *P* ₓ *c*<sub>p ₓ</sub>  + *v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>p <sub>y</sub></sub>  +  *v*<sub>z</sub>*A*<sub>y</sub>*c*<sub>p <sub>z z</sub></sub>  +  <sub><sub></sub></sub>  +  <sub></sub><sub><sub></sub></sub> z p z p z</span><span class="sxs-lookup"><span data-stu-id="741ea-188">*v* ₓ *C* ₓ +*v*<sub>y</sub>*C*<sub>y</sub> + *v*<sub>z</sub>*C*<sub>z</sub> + *C*<sub>w</sub> = *v* ₓ *P* ₓ *C*<sub>Pₓ</sub> +*v*<sub>y</sub>*P*<sub>y</sub>*C*<sub>P <sub>y</sub></sub> + *v*<sub>z</sub>*A*<sub>y</sub>*C*<sub>P <sub>z</sub></sub> + *BC*<sub>P <sub>z</sub></sub> + *v*<sub>z</sub>*C*<sub>P<sub>w</sub></sub></span></span>

<span data-ttu-id="741ea-189">Ahora podemos dividir la operación matemática anterior por componente de vértice en cuatro ecuaciones independientes:</span><span class="sxs-lookup"><span data-stu-id="741ea-189">Now we can break the preceding math operation up by vertex component into four separate equations:</span></span>

![componente de vértice x del producto del plano de recorte](images/clip-space-clip-plane-equ1.png)

![componente de vértice y del producto de plano de recorte](images/clip-space-clip-plane-equ2.png)

![componente de vértice w del producto del plano de recorte](images/clip-space-clip-plane-equ3.png)

![componente de vértice z del producto del plano de recorte](images/clip-space-clip-plane-equ4.png)

<span data-ttu-id="741ea-194">Nuestro plano de recorte de espacio de vista y nuestra matriz de proyección derivan y nos proporcionan nuestro plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="741ea-194">Our view space clip plane and our projection matrix derive and give us our clip space clip plane.</span></span>

![plano de recorte del espacio de recorte](images/clip-space-clip-plane-matrix.png)

## <a name="related-topics"></a><span data-ttu-id="741ea-196">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="741ea-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="741ea-197">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="741ea-197">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> <dt>

[<span data-ttu-id="741ea-198">Sintaxis de declaración de funciones</span><span class="sxs-lookup"><span data-stu-id="741ea-198">Function Declaration Syntax</span></span>](dx-graphics-hlsl-function-syntax.md)
</dt> </dl>

 

 