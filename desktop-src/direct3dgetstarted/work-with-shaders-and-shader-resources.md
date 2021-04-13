---
title: Trabajar con sombreadores y recursos del sombreador
description: Es el momento de aprender a trabajar con sombreadores y recursos del sombreador en el desarrollo de un juego de Microsoft DirectX para Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420912"
---
# <a name="work-with-shaders-and-shader-resources"></a><span data-ttu-id="ca8bb-103">Trabajar con sombreadores y recursos del sombreador</span><span class="sxs-lookup"><span data-stu-id="ca8bb-103">Work with shaders and shader resources</span></span>

<span data-ttu-id="ca8bb-104">Es el momento de aprender a trabajar con sombreadores y recursos del sombreador en el desarrollo de un juego de Microsoft DirectX para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-104">It's time to learn how to work with shaders and shader resources in developing your Microsoft DirectX game for Windows 8.</span></span> <span data-ttu-id="ca8bb-105">Hemos visto cómo configurar el dispositivo de gráficos y los recursos, y es posible que incluso haya empezado a modificar su canalización.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-105">We've seen how to set up the graphics device and resources, and perhaps you've even started modifying its pipeline.</span></span> <span data-ttu-id="ca8bb-106">Ahora vamos a echar un vistazo a los sombreadores de píxeles y vértices.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-106">So now let's look at pixel and vertex shaders.</span></span>

<span data-ttu-id="ca8bb-107">Si no está familiarizado con los idiomas del sombreador, una explicación rápida está en orden.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-107">If you aren't familiar with shader languages, a quick discussion is in order.</span></span> <span data-ttu-id="ca8bb-108">Los sombreadores son programas pequeños y de bajo nivel que se compilan y ejecutan en fases específicas de la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-108">Shaders are small, low-level programs that are compiled and run at specific stages in the graphics pipeline.</span></span> <span data-ttu-id="ca8bb-109">Su especialidad es una operación matemática de punto flotante muy rápida.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-109">Their specialty is very fast floating-point mathematical operations.</span></span> <span data-ttu-id="ca8bb-110">Los programas de sombreador más comunes son:</span><span class="sxs-lookup"><span data-stu-id="ca8bb-110">The most common shader programs are:</span></span>

-   <span data-ttu-id="ca8bb-111">**Sombreador de vértices**: se ejecuta para cada vértice de una escena.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-111">**Vertex shader**—Executed for each vertex in a scene.</span></span> <span data-ttu-id="ca8bb-112">Este sombreador opera en los elementos de búfer de vértices proporcionados por la aplicación que realiza la llamada y, como mínimo, da como resultado un vector de posición de cuatro componentes que se rasterizará en una posición en píxeles.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-112">This shader operates on vertex buffer elements provided to it by the calling app, and minimally results in a 4-component position vector that will be rasterized into a pixel position.</span></span>
-   <span data-ttu-id="ca8bb-113">**Sombreador de píxeles**: se ejecuta para cada píxel de un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-113">**Pixel shader**—Executed for each pixel in a render target.</span></span> <span data-ttu-id="ca8bb-114">Este sombreador recibe coordenadas rasterizadas de las fases del sombreador anterior (en las canalizaciones más simples, esto sería el sombreador de vértices) y devuelve un color (u otro valor de 4 componentes) para esa posición en píxeles, que se escribe en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-114">This shader receives rasterized coordinates from previous shader stages (in the simplest pipelines, this would be the vertex shader) and returns a color (or other 4-component value) for that pixel position, which is then written into a render target.</span></span>

<span data-ttu-id="ca8bb-115">En este ejemplo se incluyen sombreadores de vértices y píxeles muy básicos que solo dibujan geometría y sombreadores más complejos que agregan cálculos de iluminación básicos.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-115">This example includes very basic vertex and pixel shaders that only draw geometry, and more complex shaders that add basic lighting calculations.</span></span>

<span data-ttu-id="ca8bb-116">Los programas del sombreador están escritos en el lenguaje HLSL (Microsoft High Level Shader Language).</span><span class="sxs-lookup"><span data-stu-id="ca8bb-116">Shader programs are written in Microsoft High Level Shader Language (HLSL).</span></span> <span data-ttu-id="ca8bb-117">La sintaxis de HLSL tiene un aspecto muy similar a C, pero sin los punteros.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-117">HLSL syntax looks a lot like C, but without the pointers.</span></span> <span data-ttu-id="ca8bb-118">Los programas del sombreador deben ser muy compactos y eficaces.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-118">Shader programs must be very compact and efficient.</span></span> <span data-ttu-id="ca8bb-119">Si el sombreador se compila con demasiadas instrucciones, no se puede ejecutar y se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-119">If your shader compiles to too many instructions, it cannot be run and an error is returned.</span></span> <span data-ttu-id="ca8bb-120">(Tenga en cuenta que el número exacto de instrucciones permitidas forma parte del [nivel de características de Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)).</span><span class="sxs-lookup"><span data-stu-id="ca8bb-120">(Note that the exact number of instructions allowed is part of the [Direct3D feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)</span></span>

<span data-ttu-id="ca8bb-121">En Direct3D, los sombreadores no se compilan en tiempo de ejecución; se compilan cuando se compila el resto del programa.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-121">In Direct3D, shaders are not compiled at run time; they are compiled when the rest of the program is compiled.</span></span> <span data-ttu-id="ca8bb-122">Al compilar la aplicación con Microsoft Visual Studio 2013, los archivos HLSL se compilan en archivos CSO (. CSO) que la aplicación debe cargar y colocar en la memoria de GPU antes del dibujo.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-122">When you compile your app with Microsoft Visual Studio 2013, the HLSL files are compiled to CSO (.cso) files that your app must load and place in GPU memory prior to drawing.</span></span> <span data-ttu-id="ca8bb-123">Asegúrese de incluir estos archivos CSO en la aplicación al empaquetarla. se trata de recursos como mallas y texturas.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-123">Make sure you include these CSO files with your app when you package it; they are assets just like meshes and textures.</span></span>

## <a name="understand-hlsl-semantics"></a><span data-ttu-id="ca8bb-124">Descripción de la semántica de HLSL</span><span class="sxs-lookup"><span data-stu-id="ca8bb-124">Understand HLSL semantics</span></span>

<span data-ttu-id="ca8bb-125">Es importante dedicar un momento a analizar la semántica de HLSL antes de continuar, ya que a menudo son un punto de confusión para los nuevos desarrolladores de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-125">It's important to take a moment to discuss HLSL semantics before we continue, because they are often a point of confusion for new Direct3D developers.</span></span> <span data-ttu-id="ca8bb-126">La semántica de HLSL son cadenas que identifican un valor pasado entre la aplicación y un programa de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-126">HLSL semantics are strings that identify a value passed between the app and a shader program.</span></span> <span data-ttu-id="ca8bb-127">Aunque pueden ser cualquiera de las diversas cadenas posibles, el procedimiento recomendado es usar una cadena como `POSITION` o `COLOR` que indique el uso.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-127">Although they can be any of a variety of possible strings, the best practice is to use a string like `POSITION` or `COLOR` that indicates the usage.</span></span> <span data-ttu-id="ca8bb-128">Esta semántica se asigna cuando se crea un búfer de constantes o un diseño de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-128">You assign these semantics when you are constructing a constant buffer or input layout.</span></span> <span data-ttu-id="ca8bb-129">Puedes anexar un número entre 0 y 7 a la semántica para usar registros distintos para valores similares.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-129">You can also append a number between 0 and 7 to the semantic so that you use separate registers for similar values.</span></span> <span data-ttu-id="ca8bb-130">Por ejemplo: COLOR0, COLOR1, COLOR2...</span><span class="sxs-lookup"><span data-stu-id="ca8bb-130">For example: COLOR0, COLOR1, COLOR2...</span></span>

<span data-ttu-id="ca8bb-131">La semántica que tiene el prefijo "SV \_ " es la semántica *del valor del sistema* que escribe el programa del sombreador; el propio juego (que se ejecuta en la CPU) no puede modificarla.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-131">Semantics that are prefixed with "SV\_" are *system value* semantics that are written to by your shader program; your game itself (running on the CPU) cannot modify them.</span></span> <span data-ttu-id="ca8bb-132">Normalmente, esta semántica contiene valores que son entradas o salidas de otra fase del sombreador en la canalización de gráficos, o que la GPU genera completamente.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-132">Typically, these semantics contain values that are inputs or outputs from another shader stage in the graphics pipeline, or that are generated entirely by the GPU.</span></span>

<span data-ttu-id="ca8bb-133">Además, `SV_` la semántica tiene comportamientos diferentes cuando se usan para especificar la entrada o la salida de una fase del sombreador.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-133">Additionally, `SV_` semantics have different behaviors when they are used to specify input to or output from a shader stage.</span></span> <span data-ttu-id="ca8bb-134">Por ejemplo, `SV_POSITION` (salida) contiene los datos de vértice transformados durante la fase del sombreador de vértices y `SV_POSITION` (*entrada*) contiene los valores de posición en píxeles interpolados por la GPU durante la fase de rasterización.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-134">For example, `SV_POSITION` (output) contains the vertex data transformed during the vertex shader stage, and `SV_POSITION` (*input*) contains the pixel position values that were interpolated by the GPU during the rasterization stage.</span></span>

<span data-ttu-id="ca8bb-135">A continuación se muestran algunas semánticas de HLSL comunes:</span><span class="sxs-lookup"><span data-stu-id="ca8bb-135">Here are a few common HLSL semantics:</span></span>

-   <span data-ttu-id="ca8bb-136">`POSITION`(*n*) para los datos de búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-136">`POSITION`(*n*) for vertex buffer data.</span></span> <span data-ttu-id="ca8bb-137">`SV_POSITION` proporciona una posición en píxeles para el sombreador de píxeles y no se puede escribir en el juego.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-137">`SV_POSITION` provides a pixel position to the pixel shader and cannot be written by your game.</span></span>
-   <span data-ttu-id="ca8bb-138">`NORMAL`(*n*) para los datos normales proporcionados por el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-138">`NORMAL`(*n*) for normal data provided by the vertex buffer.</span></span>
-   <span data-ttu-id="ca8bb-139">`TEXCOORD`(*n*) para los datos de coordenadas UV de textura que se proporcionan a un sombreador.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-139">`TEXCOORD`(*n*) for texture UV coordinate data supplied to a shader.</span></span>
-   <span data-ttu-id="ca8bb-140">`COLOR`(n) para los datos de color RGBA proporcionados a un sombreador.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-140">`COLOR`(n) for RGBA color data supplied to a shader.</span></span> <span data-ttu-id="ca8bb-141">Tenga en cuenta que se trata de forma idéntica para coordinar los datos, incluida la interpolación del valor durante la rasterización; la semántica simplemente le ayuda a identificar que se trata de datos de color.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-141">Note that it is treated identically to coordinate data, including interpolating the value during rasterization; the semantic simply helps you identify that it is color data.</span></span>
-   <span data-ttu-id="ca8bb-142">`SV_Target`\[n \] para escribir de un sombreador de píxeles en una textura de destino u otro búfer de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-142">`SV_Target`\[n\] for writing from a pixel shader to a target texture or other pixel buffer.</span></span>

<span data-ttu-id="ca8bb-143">Veremos algunos ejemplos de la semántica de HLSL mientras revisamos el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-143">We'll see some examples of HLSL semantics as we review the example.</span></span>

## <a name="read-from-the-constant-buffers"></a><span data-ttu-id="ca8bb-144">Leer de los búferes de constantes</span><span class="sxs-lookup"><span data-stu-id="ca8bb-144">Read from the constant buffers</span></span>

<span data-ttu-id="ca8bb-145">Cualquier sombreador puede leer desde un búfer de constantes si ese búfer se adjunta a su fase como un recurso.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-145">Any shader can read from a constant buffer if that buffer is attached to its stage as a resource.</span></span> <span data-ttu-id="ca8bb-146">En este ejemplo, solo se asigna un búfer de constantes al sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-146">In this example, only the vertex shader is assigned a constant buffer.</span></span>

<span data-ttu-id="ca8bb-147">El búfer de constantes se declara en dos lugares: en el código de C++ y en los archivos HLSL correspondientes que tendrán acceso a él.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-147">The constant buffer is declared in two places: in the C++ code, and in the corresponding HLSL files that will access it.</span></span>

<span data-ttu-id="ca8bb-148">Aquí se muestra cómo se declara el struct de búfer de constantes en el código de C++.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-148">Here's how the constant buffer struct is declared in the C++ code.</span></span>


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



<span data-ttu-id="ca8bb-149">Al declarar la estructura para el búfer de constantes en el código de C++, asegúrese de que todos los datos se alineen correctamente a lo largo de los límites de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-149">When declaring the structure for the constant buffer in your C++ code, ensure that all of the data is correctly aligned along 16-byte boundaries.</span></span> <span data-ttu-id="ca8bb-150">La forma más fácil de hacerlo es usar tipos de [DirectXMath](/windows/desktop/dxmath/directxmath-portal) , como **XMFLOAT4** o **XMFLOAT4X4**, tal como se ha detectado en el código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-150">The easiest way to do this is to use [DirectXMath](/windows/desktop/dxmath/directxmath-portal) types, like **XMFLOAT4** or **XMFLOAT4X4**, as seen in the example code.</span></span> <span data-ttu-id="ca8bb-151">También puede protegerse frente a búferes desalineados mediante la declaración de una aserción estática:</span><span class="sxs-lookup"><span data-stu-id="ca8bb-151">You can also guard against misaligned buffers by declaring a static assert:</span></span>


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



<span data-ttu-id="ca8bb-152">Esta línea de código producirá un error en tiempo de compilación si **ConstantBufferStruct** no tiene una alineación de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-152">This line of code will cause an error at compile time if **ConstantBufferStruct** is not 16-byte aligned.</span></span> <span data-ttu-id="ca8bb-153">Para obtener más información sobre la alineación y el empaquetado de búferes constantes, consulte [reglas de empaquetado para variables constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="ca8bb-153">For more information about constant buffer alignment and packing, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

<span data-ttu-id="ca8bb-154">Ahora, aquí se muestra cómo se declara el búfer de constantes en el HLSL del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-154">Now, here's how the constant buffer is declared in the vertex shader HLSL.</span></span>


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



<span data-ttu-id="ca8bb-155">Todos los búferes (constantes, texturas, muestreador u otros) deben tener un registro definido para que la GPU pueda acceder a ellos.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-155">All buffers—constant, texture, sampler, or other—must have a register defined so the GPU can access them.</span></span> <span data-ttu-id="ca8bb-156">Cada fase del sombreador permite hasta 15 búferes de constantes y cada búfer puede contener hasta 4.096 variables constantes.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-156">Each shader stage allows up to 15 constant buffers, and each buffer can hold up to 4,096 constant variables.</span></span> <span data-ttu-id="ca8bb-157">La sintaxis de la declaración de uso de registro es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ca8bb-157">The register-usage declaration syntax is as follows:</span></span>

-   <span data-ttu-id="ca8bb-158">**b \* \* *\#* : un registro para un búfer de constantes (** CBuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="ca8bb-158">**b\*\**\#*: A register for a constant buffer (** cbuffer\*\*).</span></span>
-   <span data-ttu-id="ca8bb-159">**t \* \* *\#* : un registro para un búfer de textura (** tbuffer \* \*).</span><span class="sxs-lookup"><span data-stu-id="ca8bb-159">**t\*\**\#*: A register for a texture buffer (** tbuffer\*\*).</span></span>
-   <span data-ttu-id="ca8bb-160">**s \* \#** \*: registro de una muestra.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-160">\**s\*\*\*\#*: A register for a sampler.</span></span> <span data-ttu-id="ca8bb-161">(Una muestra define el comportamiento de búsqueda de textura en el recurso de textura).</span><span class="sxs-lookup"><span data-stu-id="ca8bb-161">(A sampler defines the lookup behavior for texels in the texture resource.)</span></span>

<span data-ttu-id="ca8bb-162">Por ejemplo, el HLSL de un sombreador de píxeles podría tomar una textura y una muestra como entrada con una declaración como esta.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-162">For example, the HLSL for a pixel shader might take a texture and a sampler as input with a declaration like this.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

<span data-ttu-id="ca8bb-163">Depende de usted asignar búferes de constantes a los registros; al configurar la canalización, debe adjuntar un búfer de constantes a la misma ranura a la que se asignó en el archivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-163">It's up to you to assign constant buffers to registers—when you set up the pipeline, you attach a constant buffer to the same slot you assigned it to in the HLSL file.</span></span> <span data-ttu-id="ca8bb-164">Por ejemplo, en el tema anterior, la llamada a [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indica "0" para el primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-164">For example, in the previous topic the call to [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indicates '0' for the first parameter.</span></span> <span data-ttu-id="ca8bb-165">Esto indica a Direct3D que debe adjuntar el recurso de búfer de constante al registro 0, que coincide con la asignación del búfer para **registrar (b0)** en el archivo HLSL.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-165">That tells Direct3D to attach the constant buffer resource to register 0, which matches the buffer's assignment to **register(b0)** in the HLSL file.</span></span>

## <a name="read-from-the-vertex-buffers"></a><span data-ttu-id="ca8bb-166">Leer de los búferes de vértices</span><span class="sxs-lookup"><span data-stu-id="ca8bb-166">Read from the vertex buffers</span></span>

<span data-ttu-id="ca8bb-167">El búfer de vértices proporciona los datos de triángulo para los objetos de escena a los sombreadores de vértices.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-167">The vertex buffer supplies the triangle data for the scene objects to the vertex shader(s).</span></span> <span data-ttu-id="ca8bb-168">Al igual que con el búfer de constantes, el struct de búfer de vértices se declara en el código de C++, mediante reglas de empaquetado similares.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-168">As with the constant buffer, the vertex buffer struct is declared in the C++ code, using similar packing rules.</span></span>


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



<span data-ttu-id="ca8bb-169">No hay ningún formato estándar para los datos de vértices en Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-169">There is no standard format for vertex data in Direct3D 11.</span></span> <span data-ttu-id="ca8bb-170">En su lugar, se define nuestro propio diseño de datos de vértices con un descriptor. los campos de datos se definen mediante una matriz de estructuras [**\_ DESC del \_ elemento \_ de entrada D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) .</span><span class="sxs-lookup"><span data-stu-id="ca8bb-170">Instead, we define our own vertex data layout using a descriptor; the data fields are defined using an array of [**D3D11\_INPUT\_ELEMENT\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) structures.</span></span> <span data-ttu-id="ca8bb-171">Aquí se muestra un diseño de entrada simple que describe el mismo formato de vértice que el struct anterior:</span><span class="sxs-lookup"><span data-stu-id="ca8bb-171">Here, we show a simple input layout that describes the same vertex format as the preceding struct:</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



<span data-ttu-id="ca8bb-172">Si agrega datos al formato de vértice al modificar el código de ejemplo, asegúrese de actualizar también el diseño de entrada o el sombreador no podrá interpretarlo.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-172">If you add data to the vertex format when modifying the example code, be sure to update the input layout as well, or the shader will not be able to interpret it.</span></span> <span data-ttu-id="ca8bb-173">Puede modificar el diseño de vértices de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="ca8bb-173">You might modify the vertex layout like this:</span></span>


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



<span data-ttu-id="ca8bb-174">En ese caso, debe modificar la definición de diseño de entrada como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-174">In that case, you'd modify the input-layout definition as follows.</span></span>


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



<span data-ttu-id="ca8bb-175">Cada una de las definiciones de elementos de diseño de entrada tiene como prefijo una cadena, como "POSITION" o "NORMAL", que es la semántica que se explicó anteriormente en este tema.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-175">Each of the input-layout element definitions is prefixed with a string, like "POSITION" or "NORMAL"—that is the semantic we discussed earlier in this topic.</span></span> <span data-ttu-id="ca8bb-176">Es como un identificador que ayuda a la GPU a identificar ese elemento al procesar el vértice.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-176">It's like a handle that helps the GPU identify that element when processing the vertex.</span></span> <span data-ttu-id="ca8bb-177">Elija nombres comunes y significativos para los elementos de vértice.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-177">Choose common, meaningful names for your vertex elements.</span></span>

<span data-ttu-id="ca8bb-178">Al igual que con el búfer de constantes, el sombreador de vértices tiene una definición de búfer correspondiente para los elementos de vértices entrantes.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-178">Just as with the constant buffer, the vertex shader has a corresponding buffer definition for incoming vertex elements.</span></span> <span data-ttu-id="ca8bb-179">(Este es el motivo por el que se proporciona una referencia al recurso de sombreador de vértices al crear el diseño de entrada: Direct3D valida el diseño de datos por vértice con la estructura de entrada del sombreador). Observe cómo la semántica coincide entre la definición de diseño de entrada y esta declaración de búfer de HLSL.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-179">(That's why we provided a reference to the vertex shader resource when creating the input layout - Direct3D validates the per-vertex data layout with the shader's input struct.) Note how the semantics match between the input layout definition and this HLSL buffer declaration.</span></span> <span data-ttu-id="ca8bb-180">Sin embargo, `COLOR` tiene un "0" anexado.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-180">However, `COLOR` has a "0" appended to it.</span></span> <span data-ttu-id="ca8bb-181">No es necesario agregar 0 si solo tiene un `COLOR` elemento declarado en el diseño, pero es aconsejable anexarlo en caso de que decida agregar más elementos de color en el futuro.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-181">It isn't necessary to add the 0 if you have only one `COLOR` element declared in the layout, but it's a good practice to append it in case you you choose to add more color elements in the future.</span></span>


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a><span data-ttu-id="ca8bb-182">Pasar datos entre sombreadores</span><span class="sxs-lookup"><span data-stu-id="ca8bb-182">Pass data between shaders</span></span>

<span data-ttu-id="ca8bb-183">Los sombreadores toman tipos de entrada y devuelven los tipos de salida de sus funciones principales tras su ejecución.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-183">Shaders take input types and return output types from their main functions upon execution.</span></span> <span data-ttu-id="ca8bb-184">Para el sombreador de vértices definido en la sección anterior, el tipo de entrada era la estructura de entrada de VS \_ y hemos definido un diseño de entrada y una estructura de C++ coincidentes.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-184">For the vertex shader defined in the previous section, the input type was the VS\_INPUT structure, and we defined a matching input layout and C++ struct.</span></span> <span data-ttu-id="ca8bb-185">Una matriz de este struct se usa para crear un búfer de vértices en el método **CreateCube** .</span><span class="sxs-lookup"><span data-stu-id="ca8bb-185">An array of this struct is used to create a vertex buffer in the **CreateCube** method.</span></span>

<span data-ttu-id="ca8bb-186">El sombreador de vértices devuelve una estructura de entrada de PS \_ , que debe contener mínimamente la posición del vértice final de 4 componentes (FLOAT4).</span><span class="sxs-lookup"><span data-stu-id="ca8bb-186">The vertex shader returns a PS\_INPUT structure, which must minimally contain the 4-component (float4) final vertex position.</span></span> <span data-ttu-id="ca8bb-187">Este valor de posición debe tener la semántica del valor del sistema, `SV_POSITION` , que se declara para que la GPU tenga los datos que necesita para realizar el siguiente paso del dibujo.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-187">This position value must have the system value semantic, `SV_POSITION`, declared for it so the GPU has the data it needs to perform the next drawing step.</span></span> <span data-ttu-id="ca8bb-188">Observe que no hay una correspondencia 1:1 entre la salida del sombreador de vértices y la entrada del sombreador de píxeles; el sombreador de vértices devuelve una estructura para cada vértice, pero el sombreador de píxeles se ejecuta una vez para cada píxel.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-188">Notice that there is not a 1:1 correspondence between vertex shader output and pixel shader input; the vertex shader returns one structure for each vertex it is given, but the pixel shader runs once for each pixel.</span></span> <span data-ttu-id="ca8bb-189">Esto se debe a que los datos por vértice primero pasan a través de la fase de rasterización.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-189">That's because the per-vertex data first passes through the rasterization stage.</span></span> <span data-ttu-id="ca8bb-190">En esta fase se decide qué píxeles "cubren" la geometría que se está dibujando, se calculan los datos interpolados por vértice para cada píxel y, a continuación, se llama al sombreador de píxeles una vez para cada uno de esos píxeles.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-190">This stage decides which pixels "cover" the geometry you're drawing, computes interpolated per-vertex data for each pixel, and then calls the pixel shader once for each of those pixels.</span></span> <span data-ttu-id="ca8bb-191">La interpolación es el comportamiento predeterminado cuando se rasterizan los valores de salida y es esencial en concreto para el procesamiento correcto de los datos de vectores de salida (vectores ligeros, normalización por vértice y tangentes y otros).</span><span class="sxs-lookup"><span data-stu-id="ca8bb-191">Interpolation is the default behavior when rasterizing output values, and is essential in particular for the correct processing of output vector data (light vectors, per-vertex normals and tangents, and others).</span></span>


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a><span data-ttu-id="ca8bb-192">Revisar el sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ca8bb-192">Review the vertex shader</span></span>

<span data-ttu-id="ca8bb-193">El sombreador de vértices de ejemplo es muy sencillo: tomar un vértice (posición y color), transformar la posición de las coordenadas del modelo en coordenadas proyectadas de perspectiva y devolverla (junto con el color) al rasterizador.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-193">The example vertex shader is very simple: take in a vertex (position and color), transform the position from model coordinates into perspective projected coordinates, and return it (along with the color) to the rasterizer.</span></span> <span data-ttu-id="ca8bb-194">Observe que el valor de color se interpola a la derecha junto con los datos de la posición, lo que proporciona un valor diferente para cada píxel aunque el sombreador de vértices no haya realizado ningún cálculo en el valor de color.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-194">Notice that the color value is interpolated right along with the position data, providing a different value for each pixel even though the vertex shader didn't perform any calculations on the color value.</span></span>


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



<span data-ttu-id="ca8bb-195">Un sombreador de vértices más complejo, como uno que configura los vértices de un objeto para el sombreado de Phong, podría ser más parecido a esto.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-195">A more complex vertex shader, such as one that sets up an object's vertices for Phong shading, might look more like this.</span></span> <span data-ttu-id="ca8bb-196">En este caso, estamos aprovechando el hecho de que los vectores y las normales se interpolan para aproximarse a una superficie de aspecto suave.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-196">In this case, we're taking advantage of the fact that the vectors and normals are interpolated to approximate a smooth-looking surface.</span></span>

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a><span data-ttu-id="ca8bb-197">Revisar el sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ca8bb-197">Review the pixel shader</span></span>

<span data-ttu-id="ca8bb-198">Este sombreador de píxeles en este ejemplo es probablemente la cantidad mínima absoluta de código que puede tener en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-198">This pixel shader in this example is quite possibly the absolute minimum amount of code you can have in a pixel shader.</span></span> <span data-ttu-id="ca8bb-199">Toma los datos de color de los píxeles interpolados generados durante la rasterización y los devuelve como salida, donde se escribirá en un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-199">It takes the interpolated pixel color data generated during rasterization and returns it as output, where it will be written to a render target.</span></span> <span data-ttu-id="ca8bb-200">¿Cómo aburri!</span><span class="sxs-lookup"><span data-stu-id="ca8bb-200">How boring!</span></span>


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



<span data-ttu-id="ca8bb-201">La parte importante es la `SV_TARGET` semántica del valor del sistema en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-201">The important part is the `SV_TARGET` system-value semantic on the return value.</span></span> <span data-ttu-id="ca8bb-202">Indica que la salida se va a escribir en el destino de representación principal, que es el búfer de textura proporcionado a la cadena de intercambio para su presentación.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-202">It indicates that the output is to be written to the primary render target, which is the texture buffer supplied to the swap chain for display.</span></span> <span data-ttu-id="ca8bb-203">Esto es necesario para los sombreadores de píxeles: sin los datos de color del sombreador de píxeles, Direct3D no tendría nada que mostrar.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-203">This is required for pixel shaders - without the color data from the pixel shader, Direct3D wouldn't have anything to display!</span></span>

<span data-ttu-id="ca8bb-204">Un ejemplo de un sombreador de píxeles más complejo para realizar el sombreado de Phong podría ser similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-204">An example of a more complex pixel shader to perform Phong shading might look like this.</span></span> <span data-ttu-id="ca8bb-205">Dado que los vectores y las normales se interpolaron, no tenemos que calcularlos por píxel.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-205">Since the vectors and normals were interpolated, we don't have to compute them on a per-pixel basis.</span></span> <span data-ttu-id="ca8bb-206">Sin embargo, es necesario volver a normalizarlas debido a cómo funciona la interpolación; conceptualmente, es necesario "girar" gradualmente el vector de la dirección en el vértice a hasta la dirección del vértice B, manteniendo su longitud: la interpolación wheras se corta en lugar de una línea recta entre los dos extremos de vector.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-206">However, we do have to re-normalize them because of how interpolation works; conceptually, we need to gradually "spin" the vector from direction at vertex A to direction at vertex B, maintaining its length—wheras interpolation instead cuts across a straight line between the two vector endpoints.</span></span>

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

<span data-ttu-id="ca8bb-207">En otro ejemplo, el sombreador de píxeles toma sus propios búferes de constantes que contienen información de luz y material.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-207">In another example, the pixel shader takes its own constant buffers that contain light and material information.</span></span> <span data-ttu-id="ca8bb-208">El diseño de entrada en el sombreador de vértices se expandirá para incluir datos normales y se espera que la salida de ese sombreador de vértices incluya vectores transformados para el vértice, la luz y el vértice normal en el sistema de coordenadas de la vista.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-208">The input layout in the vertex shader would be expanded to include normal data, and the output from that vertex shader is expected to include transformed vectors for the vertex, the light, and the vertex normal in the view coordinate system.</span></span>

<span data-ttu-id="ca8bb-209">Si tiene búferes de textura y muestreadores con registros asignados (**t** y **s**, respectivamente), puede tener acceso a ellos también en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-209">If you have texture buffers and samplers with assigned registers (**t** and **s**, respectively), you can access them in the pixel shader also.</span></span>

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

<span data-ttu-id="ca8bb-210">Los sombreadores son herramientas muy eficaces que se pueden usar para generar recursos de procedimientos como mapas de sombras o texturas de ruido.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-210">Shaders are very powerful tools that can be used to generate procedural resources like shadow maps or noise textures.</span></span> <span data-ttu-id="ca8bb-211">De hecho, las técnicas avanzadas requieren que se creen texturas más abstractas, no como elementos visuales, sino como búferes.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-211">In fact, advanced techniques require that you think of textures more abstractly, not as visual elements but as buffers.</span></span> <span data-ttu-id="ca8bb-212">Contienen datos como la información de alto u otros datos que se pueden muestrear en el paso final del sombreador de píxeles o en ese fotograma determinado como parte de un paso de efectos de varias fases.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-212">They hold data like height information, or other data that can be sampled in the final pixel shader pass or in that particular frame as part of a multi-stage effects pass.</span></span> <span data-ttu-id="ca8bb-213">El muestreo múltiple es una herramienta eficaz y la red troncal de muchos efectos visuales modernos.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-213">Multi-sampling is a powerful tool and the backbone of many modern visual effects.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ca8bb-214">Pasos siguientes</span><span class="sxs-lookup"><span data-stu-id="ca8bb-214">Next steps</span></span>

<span data-ttu-id="ca8bb-215">Espero que esté familiarizado con DirectX 11at este punto y esté listo para empezar a trabajar en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="ca8bb-215">Hopefully, you're comfortable with DirectX 11at this point and are ready to start working on your project.</span></span> <span data-ttu-id="ca8bb-216">Estos son algunos vínculos que le ayudarán a responder a otras preguntas que puede tener sobre el desarrollo con DirectX y C++:</span><span class="sxs-lookup"><span data-stu-id="ca8bb-216">Here are some links to help answer other questions you may have about development with DirectX and C++:</span></span>

-   <span data-ttu-id="ca8bb-217">[Desarrollar juegos](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ca8bb-217">[Developing games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="ca8bb-218">[Usar Visual Studio Tools para la programación de juegos de DirectX](/previous-versions/windows/apps/dn166877(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ca8bb-218">[Use Visual Studio tools for DirectX game programming](/previous-versions/windows/apps/dn166877(v=win.10))</span></span>
-   <span data-ttu-id="ca8bb-219">[Tutoriales de ejemplo y desarrollo de juegos de DirectX](/previous-versions/windows/apps/hh465149(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ca8bb-219">[DirectX game development and sample walkthroughs](/previous-versions/windows/apps/hh465149(v=win.10))</span></span>
-   <span data-ttu-id="ca8bb-220">[Recursos adicionales de programación de juegos](/previous-versions/windows/apps/dn194515(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ca8bb-220">[Additional game programming resources](/previous-versions/windows/apps/dn194515(v=win.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca8bb-221">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ca8bb-221">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca8bb-222">Trabajar con recursos de dispositivos DirectX</span><span class="sxs-lookup"><span data-stu-id="ca8bb-222">Work with DirectX device resources</span></span>](work-with-dxgi.md)
</dt> <dt>

[<span data-ttu-id="ca8bb-223">Descripción de la canalización de representación de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ca8bb-223">Understand the Direct3D 11 rendering pipeline</span></span>](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 