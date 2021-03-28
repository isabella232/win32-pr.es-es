---
title: Escribir sombreadores HLSL en Direct3D 9
description: Escribir sombreadores HLSL en Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078140"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a><span data-ttu-id="1d1c6-103">Escribir sombreadores HLSL en Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="1d1c6-103">Writing HLSL Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="1d1c6-104">Conceptos básicos del sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="1d1c6-104">Vertex-Shader Basics</span></span>](#vertex-shader-basics)
-   [<span data-ttu-id="1d1c6-105">Conceptos básicos del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="1d1c6-105">Pixel-Shader Basics</span></span>](#pixel-shader-basics)
    -   [<span data-ttu-id="1d1c6-106">Estados de muestra y fase de textura</span><span class="sxs-lookup"><span data-stu-id="1d1c6-106">Texture Stage and Sampler States</span></span>](#texture-stage-and-sampler-states)
    -   [<span data-ttu-id="1d1c6-107">Entradas del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="1d1c6-107">Pixel Shader Inputs</span></span>](#pixel-shader-inputs)
    -   [<span data-ttu-id="1d1c6-108">Salidas del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="1d1c6-108">Pixel Shader Outputs</span></span>](#pixel-shader-outputs)
-   [<span data-ttu-id="1d1c6-109">Entradas de sombreador y variables de sombreador</span><span class="sxs-lookup"><span data-stu-id="1d1c6-109">Shader Inputs and Shader Variables</span></span>](#shader-inputs-and-shader-variables)
    -   [<span data-ttu-id="1d1c6-110">Declarar variables de sombreador</span><span class="sxs-lookup"><span data-stu-id="1d1c6-110">Declaring Shader Variables</span></span>](#declaring-shader-variables)
    -   [<span data-ttu-id="1d1c6-111">Entradas uniformes del sombreador</span><span class="sxs-lookup"><span data-stu-id="1d1c6-111">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
    -   [<span data-ttu-id="1d1c6-112">Variables y semánticas de sombreador variables</span><span class="sxs-lookup"><span data-stu-id="1d1c6-112">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
    -   [<span data-ttu-id="1d1c6-113">Muestras y objetos de textura</span><span class="sxs-lookup"><span data-stu-id="1d1c6-113">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)
-   [<span data-ttu-id="1d1c6-114">Escribir funciones</span><span class="sxs-lookup"><span data-stu-id="1d1c6-114">Writing Functions</span></span>](#writing-functions)
-   [<span data-ttu-id="1d1c6-115">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="1d1c6-115">Flow Control</span></span>](#flow-control)
-   [<span data-ttu-id="1d1c6-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d1c6-116">Related topics</span></span>](#related-topics)

## <a name="vertex-shader-basics"></a><span data-ttu-id="1d1c6-117">Aspectos básicos de Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="1d1c6-117">Vertex-Shader Basics</span></span>

<span data-ttu-id="1d1c6-118">Cuando está en funcionamiento, un sombreador de vértices programable reemplaza el procesamiento de vértices realizado por la canalización de gráficos de Microsoft Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-118">When in operation, a programmable vertex shader replaces the vertex processing done by the Microsoft Direct3D graphics pipeline.</span></span> <span data-ttu-id="1d1c6-119">Al usar un sombreador de vértices, la canalización de funciones fijas omite la información de estado relativa a las operaciones de transformación e iluminación.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-119">While using a vertex shader, state information regarding transformation and lighting operations is ignored by the fixed function pipeline.</span></span> <span data-ttu-id="1d1c6-120">Cuando se deshabilita el sombreador de vértices y se devuelve el procesamiento de funciones fijas, se aplican todos los valores de estado actuales.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-120">When the vertex shader is disabled and fixed function processing is returned, all current state settings apply.</span></span>

<span data-ttu-id="1d1c6-121">La teselación de primitivas de orden superior debe realizarse antes de que se ejecute el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-121">Tessellation of high-order primitives should be done before the vertex shader executes.</span></span> <span data-ttu-id="1d1c6-122">Las implementaciones que realizan la teselación superficial después del procesamiento del sombreador deben hacerlo de una manera que no es aparente en el código del sombreador y la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-122">Implementations that perform surface tessellation after the shader processing must do so in a way that is not apparent to the application and shader code.</span></span>

<span data-ttu-id="1d1c6-123">Como mínimo, un sombreador de vértices debe generar la posición del vértice en el espacio de recorte homogéneo.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-123">As a minimum, a vertex shader must output vertex position in homogeneous clip space.</span></span> <span data-ttu-id="1d1c6-124">Opcionalmente, el sombreador de vértices puede generar coordenadas de textura, color de vértice, iluminación de vértices, factores de niebla, etc.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-124">Optionally, the vertex shader can output texture coordinates, vertex color, vertex lighting, fog factors, and so on.</span></span>

## <a name="pixel-shader-basics"></a><span data-ttu-id="1d1c6-125">Aspectos básicos de Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="1d1c6-125">Pixel-Shader Basics</span></span>

<span data-ttu-id="1d1c6-126">El procesamiento de píxeles se realiza mediante sombreadores de píxeles en píxeles individuales.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-126">Pixel processing is performed by pixel shaders on individual pixels.</span></span> <span data-ttu-id="1d1c6-127">Los sombreadores de píxeles funcionan en conjunto con los sombreadores de vértices; la salida de un sombreador de vértices proporciona las entradas para un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-127">Pixel shaders work in concert with vertex shaders; the output of a vertex shader provides the inputs for a pixel shader.</span></span> <span data-ttu-id="1d1c6-128">Otras operaciones de píxeles (mezcla de niebla, operaciones de estarcido y mezcla de destino de representación) se producen después de la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-128">Other pixel operations (fog blending, stencil operations, and render-target blending) occur after execution of the shader.</span></span>

### <a name="texture-stage-and-sampler-states"></a><span data-ttu-id="1d1c6-129">Estados de muestra y fase de textura</span><span class="sxs-lookup"><span data-stu-id="1d1c6-129">Texture Stage and Sampler States</span></span>

<span data-ttu-id="1d1c6-130">Un sombreador de píxeles reemplaza completamente la funcionalidad de combinación de píxeles especificada por el mezclador de varias texturas, incluidas las operaciones definidas previamente por los Estados de la fase de textura.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-130">A pixel shader completely replaces the pixel-blending functionality specified by the multi-texture blender including operations previously defined by the texture stage states.</span></span> <span data-ttu-id="1d1c6-131">Las operaciones de filtrado y muestreo de textura que se controlan mediante los Estados de fase de textura estándar para minificación, la ampliación, el filtrado de MIP y los modos de direccionamiento de encapsulado se pueden inicializar en sombreadores.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-131">Texture sampling and filtering operations which were controlled by the standard texture stage states for minification, magnification, mip filtering, and the wrap addressing modes, can be initialized in shaders.</span></span> <span data-ttu-id="1d1c6-132">La aplicación es gratuita para cambiar estos Estados sin necesidad de la regeneración del sombreador enlazado actualmente.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-132">The application is free to change these states without requiring the regeneration of the currently bound shader.</span></span> <span data-ttu-id="1d1c6-133">El establecimiento del estado puede ser más fácil si los sombreadores están diseñados dentro de un efecto.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-133">Setting state can be made even easier if your shaders are designed within an effect.</span></span>

### <a name="pixel-shader-inputs"></a><span data-ttu-id="1d1c6-134">Entradas del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="1d1c6-134">Pixel Shader Inputs</span></span>

<span data-ttu-id="1d1c6-135">En el caso de las versiones de sombreador de píxeles PS \_ 1 \_ 1-PS \_ 2 \_ 0, los colores difusos y especulares se saturan (se fijan) en el intervalo de 0 a 1 antes de que los use el sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-135">For pixel shader versions ps\_1\_1 - ps\_2\_0, diffuse and specular colors are saturated (clamped) in the range 0 to 1 before use by the shader.</span></span>

<span data-ttu-id="1d1c6-136">Los valores de color especificados para el sombreador de píxeles son correctos para la perspectiva, pero esto no se garantiza (para todo el hardware).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-136">Color values input to the pixel shader are assumed to be perspective correct, but this is not guaranteed (for all hardware).</span></span> <span data-ttu-id="1d1c6-137">Los colores muestreados a partir de coordenadas de textura se repiten de manera correcta y se fijan en el intervalo de 0 a 1 durante la iteración.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-137">Colors sampled from texture coordinates are iterated in a perspective correct manner, and are clamped to the 0 to 1 range during iteration.</span></span>

### <a name="pixel-shader-outputs"></a><span data-ttu-id="1d1c6-138">Salidas del sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="1d1c6-138">Pixel Shader Outputs</span></span>

<span data-ttu-id="1d1c6-139">En el caso de las versiones del sombreador de píxeles PS \_ 1 \_ 1-PS \_ 1 \_ 4, el resultado emitido por el sombreador de píxeles es el contenido de Register R0.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-139">For pixel shader versions ps\_1\_1 - ps\_1\_4, the result emitted by the pixel shader is the contents of register r0.</span></span> <span data-ttu-id="1d1c6-140">Lo que contenga cuando el sombreador complete el procesamiento se envía a la fase de niebla y a la mezcla de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-140">Whatever it contains when the shader completes processing is sent to the fog stage and render-target blender.</span></span>

<span data-ttu-id="1d1c6-141">En el caso de las versiones de sombreador de píxeles PS \_ 2 \_ 0 y superiores, el color de salida se emite desde OC0-oC4.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-141">For pixel shader versions ps\_2\_0 and above, output color is emitted from oC0 - oC4.</span></span>

## <a name="shader-inputs-and-shader-variables"></a><span data-ttu-id="1d1c6-142">Entradas de sombreador y variables de sombreador</span><span class="sxs-lookup"><span data-stu-id="1d1c6-142">Shader Inputs and Shader Variables</span></span>

-   [<span data-ttu-id="1d1c6-143">Declarar variables de sombreador</span><span class="sxs-lookup"><span data-stu-id="1d1c6-143">Declaring Shader Variables</span></span>](#declaring-shader-variables)
-   [<span data-ttu-id="1d1c6-144">Entradas uniformes del sombreador</span><span class="sxs-lookup"><span data-stu-id="1d1c6-144">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
-   [<span data-ttu-id="1d1c6-145">Variables y semánticas de sombreador variables</span><span class="sxs-lookup"><span data-stu-id="1d1c6-145">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
-   [<span data-ttu-id="1d1c6-146">Muestras y objetos de textura</span><span class="sxs-lookup"><span data-stu-id="1d1c6-146">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a><span data-ttu-id="1d1c6-147">Declarar variables de sombreador</span><span class="sxs-lookup"><span data-stu-id="1d1c6-147">Declaring Shader Variables</span></span>

<span data-ttu-id="1d1c6-148">La declaración de variable más sencilla incluye un tipo y un nombre de variable, como esta declaración de punto flotante:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-148">The simplest variable declaration includes a type and a variable name, such as this floating-point declaration:</span></span>


```
float fVar;
```



<span data-ttu-id="1d1c6-149">Puede inicializar una variable en la misma instrucción.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-149">You can initialize a variable in the same statement.</span></span>


```
float fVar = 3.1f;
```



<span data-ttu-id="1d1c6-150">Se puede declarar una matriz de variables,</span><span class="sxs-lookup"><span data-stu-id="1d1c6-150">An array of variables can be declared,</span></span>


```
int iVar[3];
```



<span data-ttu-id="1d1c6-151">o se declaran e inicializan en la misma instrucción.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-151">or declared and initialized in the same statement.</span></span>


```
int iVar[3] = {1,2,3};
```



<span data-ttu-id="1d1c6-152">Estas son algunas declaraciones que muestran muchas de las características de las variables del lenguaje de sombreado de alto nivel (HLSL):</span><span class="sxs-lookup"><span data-stu-id="1d1c6-152">Here are a few declarations that demonstrate many of the characteristics of high-level shader language (HLSL) variables:</span></span>


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



<span data-ttu-id="1d1c6-153">Las declaraciones de datos pueden usar cualquier tipo válido, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-153">Data declarations can use any valid type including:</span></span>

-   [<span data-ttu-id="1d1c6-154">Tipos de datos (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-154">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
-   [<span data-ttu-id="1d1c6-155">Tipo de vector (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-155">Vector Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-vector.md)
-   [<span data-ttu-id="1d1c6-156">Tipo de matriz (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-156">Matrix Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-matrix.md)
-   [<span data-ttu-id="1d1c6-157">Tipo de sombreador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-157">Shader Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-shader.md)
-   [<span data-ttu-id="1d1c6-158">Tipo de muestra (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-158">Sampler Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-sampler.md)
-   [<span data-ttu-id="1d1c6-159">Tipo definido por el usuario (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-159">User-Defined Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-user-defined.md)

<span data-ttu-id="1d1c6-160">Un sombreador puede tener variables, argumentos y funciones de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-160">A shader can have top-level variables, arguments, and functions.</span></span>


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



<span data-ttu-id="1d1c6-161">Las variables de nivel superior se declaran fuera de todas las funciones.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-161">Top-level variables are declared outside of all functions.</span></span> <span data-ttu-id="1d1c6-162">Los argumentos de nivel superior son parámetros para una función de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-162">Top-level arguments are parameters to a top-level function.</span></span> <span data-ttu-id="1d1c6-163">Una función de nivel superior es cualquier función a la que llama la aplicación (en lugar de una función a la que llama otra función).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-163">A top-level function is any function called by the application (as opposed to a function that is called by another function).</span></span>

### <a name="uniform-shader-inputs"></a><span data-ttu-id="1d1c6-164">Entradas uniformes del sombreador</span><span class="sxs-lookup"><span data-stu-id="1d1c6-164">Uniform Shader Inputs</span></span>

<span data-ttu-id="1d1c6-165">Los sombreadores de vértices y píxeles aceptan dos tipos de datos de entrada: variables y uniformes.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-165">Vertex and pixel shaders accept two kinds of input data: varying and uniform.</span></span> <span data-ttu-id="1d1c6-166">La entrada variable son los datos que son únicos para cada ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-166">The varying input is the data that is unique to each execution of the shader.</span></span> <span data-ttu-id="1d1c6-167">En el caso de un sombreador de vértices, los datos variables (por ejemplo: Position, normal, etc.) proceden de las secuencias de vértices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-167">For a vertex shader, the varying data (for example: position, normal, etc.) comes from the vertex streams.</span></span> <span data-ttu-id="1d1c6-168">Los datos uniformes (por ejemplo: color del material, transformación del mundo, etc.) son constantes para varias ejecuciones de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-168">The uniform data (for example: material color, world transform, etc.) is constant for multiple executions of a shader.</span></span> <span data-ttu-id="1d1c6-169">Para aquellos que estén familiarizados con los modelos de sombreador de ensamblado, los datos uniformes se especifican mediante registros constantes y datos variables por los registros v y t.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-169">For those familiar with the assembly shader models, uniform data is specified by constant registers and varying data by the v and t registers.</span></span>

<span data-ttu-id="1d1c6-170">Los datos uniformes pueden especificarse mediante dos métodos.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-170">Uniform data can be specified by two methods.</span></span> <span data-ttu-id="1d1c6-171">El método más común consiste en declarar las variables globales y usarlas en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-171">The most common method is to declare global variables and use them within a shader.</span></span> <span data-ttu-id="1d1c6-172">Cualquier uso de variables globales dentro de un sombreador producirá la adición de esa variable a la lista de variables uniformes que requiere ese sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-172">Any use of global variables within a shader will result in adding that variable to the list of uniform variables required by that shader.</span></span> <span data-ttu-id="1d1c6-173">El segundo método consiste en marcar un parámetro de entrada de la función de sombreador de nivel superior como uniforme.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-173">The second method is to mark an input parameter of the top-level shader function as uniform.</span></span> <span data-ttu-id="1d1c6-174">Este marcado especifica que la variable especificada debe agregarse a la lista de variables uniformes.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-174">This marking specifies that the given variable should be added to the list of uniform variables.</span></span>

<span data-ttu-id="1d1c6-175">Las variables uniformes usadas por un sombreador se comunican de nuevo a la aplicación a través de la tabla de constantes.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-175">Uniform variables used by a shader are communicated back to the application via the constant table.</span></span> <span data-ttu-id="1d1c6-176">La tabla Constant es el nombre de la tabla de símbolos que define cómo se ajustan las variables uniformes usadas por un sombreador en los registros de constantes.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-176">The constant table is the name for the symbol table that defines how the uniform variables used by a shader fit into the constant registers.</span></span> <span data-ttu-id="1d1c6-177">Los parámetros de función uniformes aparecen en la tabla de constantes antepuesto con un signo de dólar ($), a diferencia de las variables globales.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-177">The uniform function parameters appear in the constant table prepended with a dollar sign ($), unlike the global variables.</span></span> <span data-ttu-id="1d1c6-178">El signo de dólar es necesario para evitar colisiones de nombres entre las entradas uniformes locales y las variables globales del mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-178">The dollar sign is required to avoid name collisions between local uniform inputs and global variables of the same name.</span></span>

<span data-ttu-id="1d1c6-179">La tabla Constant contiene las ubicaciones de registro constantes de todas las variables uniformes utilizadas por el sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-179">The constant table contains the constant register locations of all uniform variables used by the shader.</span></span> <span data-ttu-id="1d1c6-180">La tabla también incluye la información de tipo y el valor predeterminado, si se especifica.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-180">The table also includes the type information and the default value, if specified.</span></span>

### <a name="varying-shader-inputs-and-semantics"></a><span data-ttu-id="1d1c6-181">Variables y semánticas de sombreador variables</span><span class="sxs-lookup"><span data-stu-id="1d1c6-181">Varying Shader Inputs and Semantics</span></span>

<span data-ttu-id="1d1c6-182">Los distintos parámetros de entrada (de una función de sombreador de nivel superior) se deben marcar con una palabra clave semántica o uniforme que indique que el valor es constante para la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-182">Varying input parameters (of a top-level shader function) must be marked either with a semantic or uniform keyword indicating the value is constant for the execution of the shader.</span></span> <span data-ttu-id="1d1c6-183">Si una entrada de sombreador de nivel superior no está marcada con una palabra clave semántica o uniforme, el sombreador no se compilará.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-183">If a top-level shader input is not marked with a semantic or uniform keyword, then the shader will fail to compile.</span></span>

<span data-ttu-id="1d1c6-184">La semántica de entrada es un nombre que se usa para vincular la entrada especificada a una salida de la parte anterior de la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-184">The input semantic is a name used to link the given input to an output of the previous part of the graphics pipeline.</span></span> <span data-ttu-id="1d1c6-185">Por ejemplo, los sombreadores de vértices usan la semántica de entrada POSITION0 para especificar dónde se deben vincular los datos de posición del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-185">For example, the input semantic POSITION0 is used by the vertex shaders to specify where the position data from the vertex buffer should be linked.</span></span>

<span data-ttu-id="1d1c6-186">Los sombreadores de píxeles y vértices tienen diferentes conjuntos de semántica de entrada debido a las distintas partes de la canalización de gráficos que se alimentan en cada unidad de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-186">Pixel and vertex shaders have different sets of input semantics due to the different parts of the graphics pipeline that feed into each shader unit.</span></span> <span data-ttu-id="1d1c6-187">La semántica de entrada del sombreador de vértices describe la información por vértice (por ejemplo: posición, normal, coordenadas de textura, color, tangente, binormalización, etc.) que se va a cargar desde un búfer de vértices en un formato que el sombreador de vértices puede consumir.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-187">Vertex shader input semantics describe the per-vertex information (for example: position, normal, texture coordinates, color, tangent, binormal, etc.) to be loaded from a vertex buffer into a form that can be consumed by the vertex shader.</span></span> <span data-ttu-id="1d1c6-188">La semántica de entrada se asigna directamente al uso de la declaración de vértices y al índice de uso.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-188">The input semantics directly map to the vertex declaration usage and the usage index.</span></span>

<span data-ttu-id="1d1c6-189">La semántica de entrada del sombreador de píxeles describe la información que la unidad de rasterización proporciona por píxel.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-189">Pixel shader input semantics describe the information that is provided per pixel by the rasterization unit.</span></span> <span data-ttu-id="1d1c6-190">Los datos se generan mediante la interpolación entre las salidas del sombreador de vértices para cada vértice de la primitiva actual.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-190">The data is generated by interpolating between outputs of the vertex shader for each vertex of the current primitive.</span></span> <span data-ttu-id="1d1c6-191">La semántica de entrada del sombreador de píxeles básico vincula el color de salida y la información de coordenadas de textura con los parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-191">The basic pixel shader input semantics link the output color and texture coordinate information to input parameters.</span></span>

<span data-ttu-id="1d1c6-192">La semántica de entrada se puede asignar a la entrada del sombreador mediante dos métodos:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-192">Input semantics can be assigned to shader input by two methods:</span></span>

-   <span data-ttu-id="1d1c6-193">Anexar un signo de dos puntos y el nombre semántico a la declaración del parámetro.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-193">Appending a colon and the semantic name to the parameter declaration.</span></span>
-   <span data-ttu-id="1d1c6-194">Definir una estructura de entrada con semántica de entrada asignada a cada miembro de la estructura.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-194">Defining an input structure with input semantics assigned to each structure member.</span></span>

<span data-ttu-id="1d1c6-195">Los sombreadores de vértices y píxeles proporcionan datos de salida a la siguiente fase de canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-195">Vertex and pixel shaders provide output data to the subsequent graphics pipeline stage.</span></span> <span data-ttu-id="1d1c6-196">La semántica de salida se usa para especificar cómo se deben vincular los datos generados por el sombreador a las entradas de la siguiente fase.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-196">Output semantics are used to specify how data generated by the shader should be linked to the inputs of the next stage.</span></span> <span data-ttu-id="1d1c6-197">Por ejemplo, la semántica de salida de un sombreador de vértices se usa para vincular las salidas de los interpoladores en el rasterizador para generar los datos de entrada para el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-197">For example, the output semantics for a vertex shader are used to link the outputs of the interpolators in the rasterizer to generate the input data for the pixel shader.</span></span> <span data-ttu-id="1d1c6-198">Las salidas del sombreador de píxeles son los valores proporcionados a la unidad de combinación alfa para cada uno de los destinos de representación o el valor de profundidad escrito en el búfer de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-198">The pixel shader outputs are the values provided to the alpha blending unit for each of the render targets or the depth value written to the depth buffer.</span></span>

<span data-ttu-id="1d1c6-199">La semántica de salida del sombreador de vértices se usa para vincular el sombreador con el sombreador de píxeles y con la fase de rasterizador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-199">Vertex shader output semantics are used to link the shader both to the pixel shader and to the rasterizer stage.</span></span> <span data-ttu-id="1d1c6-200">Un sombreador de vértices utilizado por el rasterizador y no expuesto al sombreador de píxeles debe generar los datos de la posición como mínimo.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-200">A vertex shader that is consumed by the rasterizer and not exposed to the pixel shader must generate position data as a minimum.</span></span> <span data-ttu-id="1d1c6-201">Los sombreadores de vértices que generan datos de color y coordenada de textura proporcionan los datos a un sombreador de píxeles una vez realizada la interpolación.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-201">Vertex shaders that generate texture coordinate and color data provide that data to a pixel shader after interpolation is done.</span></span>

<span data-ttu-id="1d1c6-202">La semántica de salida del sombreador de píxeles enlaza los colores de salida de un sombreador de píxeles con el destino de representación correcto.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-202">Pixel shader output semantics bind the output colors of a pixel shader with the correct render target.</span></span> <span data-ttu-id="1d1c6-203">El color de salida del sombreador de píxeles se vincula a la fase de mezcla alfa, que determina cómo se modifican los destinos de representación de destino.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-203">The pixel shader output color is linked to the alpha blend stage, which determines how the destination render targets are modified.</span></span> <span data-ttu-id="1d1c6-204">La salida de profundidad del sombreador de píxeles se puede usar para cambiar los valores de profundidad de destino en la ubicación de la cuadrícula actual.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-204">The pixel shader depth output can be used to change the destination depth values at the current raster location.</span></span> <span data-ttu-id="1d1c6-205">La salida de profundidad y varios destinos de representación solo se admiten con algunos modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-205">The depth output and multiple render targets are only supported with some shader models.</span></span>

<span data-ttu-id="1d1c6-206">La sintaxis de la semántica de salida es idéntica a la sintaxis para especificar la semántica de entrada.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-206">The syntax for output semantics is identical to the syntax for specifying input semantics.</span></span> <span data-ttu-id="1d1c6-207">La semántica se puede especificar directamente en los parámetros declarados como parámetros "out" o asignados durante la definición de una estructura que se devuelve como un parámetro "out" o el valor devuelto de una función.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-207">The semantics can be either specified directly on parameters declared as "out" parameters or assigned during the definition of a structure that either returned as an "out" parameter or the return value of a function.</span></span>

<span data-ttu-id="1d1c6-208">La semántica identifica de dónde proceden los datos.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-208">Semantics identify where data comes from.</span></span> <span data-ttu-id="1d1c6-209">La semántica son identificadores opcionales que identifican las entradas y salidas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-209">Semantics are optional identifiers that identify shader inputs and outputs.</span></span> <span data-ttu-id="1d1c6-210">La semántica aparece en una de tres ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-210">Semantics appear in one of three places:</span></span>

-   <span data-ttu-id="1d1c6-211">Después de un miembro de estructura.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-211">After a structure member.</span></span>
-   <span data-ttu-id="1d1c6-212">Después de un argumento de la lista de argumentos de entrada de una función.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-212">After an argument in a function's input argument list.</span></span>
-   <span data-ttu-id="1d1c6-213">Después de la lista de argumentos de entrada de la función.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-213">After the function's input argument list.</span></span>

<span data-ttu-id="1d1c6-214">En este ejemplo se usa una estructura para proporcionar una o más entradas del sombreador de vértices y otra estructura para proporcionar una o más salidas del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-214">This example uses a structure to provide one or more vertex shader inputs, and another structure to provide one or more vertex shader outputs.</span></span> <span data-ttu-id="1d1c6-215">Cada uno de los miembros de la estructura utiliza una semántica.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-215">Each of the structure members uses a semantic.</span></span>


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



<span data-ttu-id="1d1c6-216">La estructura de entrada identifica los datos del búfer de vértice que proporcionará las entradas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-216">The input structure identifies the data from the vertex buffer that will provide the shader inputs.</span></span> <span data-ttu-id="1d1c6-217">Este sombreador asigna los datos de los elementos Position, normal y blendweight del búfer de vértices en los registros del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-217">This shader maps the data from the position, normal, and blendweight elements of the vertex buffer into vertex shader registers.</span></span> <span data-ttu-id="1d1c6-218">El tipo de datos de entrada no tiene que coincidir exactamente con el tipo de datos de declaración de vértices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-218">The input data type does not have to exactly match the vertex declaration data type.</span></span> <span data-ttu-id="1d1c6-219">Si no coincide exactamente, los datos del vértice se convertirán automáticamente al tipo de datos de HLSL cuando se escriban en los registros del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-219">If it doesn't exactly match, the vertex data will automatically be converted into the HLSL's data type when it is written into the shader registers.</span></span> <span data-ttu-id="1d1c6-220">Por ejemplo, si los datos normales se definieron como de tipo UINT por la aplicación, se convertiría en un float3 cuando lo leyó el sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-220">For instance, if the normal data were defined to be of type UINT by the application, it would be converted into a float3 when read by the shader.</span></span>

<span data-ttu-id="1d1c6-221">Si los datos de la secuencia de vértices contienen menos componentes que el tipo de datos del sombreador correspondiente, los componentes que faltan se inicializarán en 0 (excepto en w, que se inicializa en 1).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-221">If the data in the vertex stream contains fewer components than the corresponding shader data type, the missing components will be initialized to 0 (except for w, which is initialized to 1).</span></span>

<span data-ttu-id="1d1c6-222">La semántica de entrada es similar a los valores de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-222">Input semantics are similar to the values in the [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span>

<span data-ttu-id="1d1c6-223">La estructura de salida identifica los parámetros de salida del sombreador de vértices de posición y color.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-223">The output structure identifies the vertex shader output parameters of position and color.</span></span> <span data-ttu-id="1d1c6-224">La canalización usará estas salidas para la rasterización del triángulo (en el procesamiento primitivo).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-224">These outputs will be used by the pipeline for triangle rasterization (in primitive processing).</span></span> <span data-ttu-id="1d1c6-225">La salida marcada como datos de posición denota la posición de un vértice en un espacio homogéneo.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-225">The output marked as position data denotes the position of a vertex in homogeneous space.</span></span> <span data-ttu-id="1d1c6-226">Como mínimo, un sombreador de vértices debe generar datos de posición.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-226">As a minimum, a vertex shader must generate position data.</span></span> <span data-ttu-id="1d1c6-227">La posición del espacio de la pantalla se calcula una vez que se completa el sombreador de vértices dividiendo la coordenada (x, y, z) entre w.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-227">The screen space position is computed after the vertex shader completes by dividing the (x, y, z) coordinate by w.</span></span> <span data-ttu-id="1d1c6-228">En el espacio de pantalla,-1 y 1 son los valores x e y máximo y mínimo de los límites de la ventanilla, mientras que z se usa para las pruebas de búfer z.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-228">In screen space, -1 and 1 are the minimum and maximum x and y values of the boundaries of the viewport, while z is used for z-buffer testing.</span></span>

<span data-ttu-id="1d1c6-229">La semántica de salida también es similar a los valores de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-229">Output semantics are also similar to the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span> <span data-ttu-id="1d1c6-230">En general, una estructura de salida de un sombreador de vértices también se puede usar como la estructura de entrada de un sombreador de píxeles, siempre que el sombreador de píxeles no lea las variables marcadas con la posición, el tamaño del punto o la semántica de niebla.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-230">In general, an output structure for a vertex shader can also be used as the input structure for a pixel shader, provided the pixel shader does not read from any variable marked with the position, point size, or fog semantics.</span></span> <span data-ttu-id="1d1c6-231">Estas semánticas están asociadas a valores escalares por vértice que no se utilizan en un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-231">These semantics are associated with per-vertex scalar values that are not used by a pixel shader.</span></span> <span data-ttu-id="1d1c6-232">Si estos valores son necesarios para el sombreador de píxeles, se pueden copiar en otra variable de salida que utiliza una semántica de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-232">If these values are needed for the pixel shader, they can be copied into another output variable that uses a pixel shader semantic.</span></span>

<span data-ttu-id="1d1c6-233">El compilador asigna automáticamente las variables globales a los registros.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-233">Global variables are assigned to registers automatically by the compiler.</span></span> <span data-ttu-id="1d1c6-234">Las variables globales también se denominan parámetros uniformes porque el contenido de la variable es el mismo para todos los píxeles procesados cada vez que se llama al sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-234">Global variables are also called uniform parameters because the contents of the variable is the same for all pixels processed each time the shader is called.</span></span> <span data-ttu-id="1d1c6-235">Los registros se encuentran en la tabla de constantes, que se puede leer mediante la interfaz [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) .</span><span class="sxs-lookup"><span data-stu-id="1d1c6-235">The registers are contained in the constant table, which can be read using the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span>

<span data-ttu-id="1d1c6-236">La semántica de entrada para los sombreadores de píxeles asigna valores en registros de hardware específicos para el transporte entre los sombreadores de vértices y los sombreadores de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-236">Input semantics for pixel shaders map values into specific hardware registers for transport between vertex shaders and pixel shaders.</span></span> <span data-ttu-id="1d1c6-237">Cada tipo de registro tiene propiedades específicas.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-237">Each register type has specific properties.</span></span> <span data-ttu-id="1d1c6-238">Dado que actualmente solo hay dos semánticas para las coordenadas de color y de textura, es habitual que la mayoría de los datos se marquen como una coordenada de textura aunque no lo sea.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-238">Because there are currently only two semantics for color and texture coordinates, it is common for most data to be marked as a texture coordinate even when it is not.</span></span>

<span data-ttu-id="1d1c6-239">Tenga en cuenta que la estructura de salida del sombreador de vértices usó una entrada con datos de posición, que no se usa en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-239">Notice that the vertex shader output structure used an input with position data, which is not used by the pixel shader.</span></span> <span data-ttu-id="1d1c6-240">HLSL permite datos de salida válidos de un sombreador de vértices que no son datos de entrada válidos para un sombreador de píxeles, siempre que no se haga referencia a ellos en el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-240">HLSL allows valid output data of a vertex shader that is not valid input data for a pixel shader, provided that it is not referenced in the pixel shader.</span></span>

<span data-ttu-id="1d1c6-241">Los argumentos de entrada también pueden ser matrices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-241">Input arguments can also be arrays.</span></span> <span data-ttu-id="1d1c6-242">El compilador incrementa automáticamente la semántica para cada elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-242">Semantics are automatically incremented by the compiler for each element of the array.</span></span> <span data-ttu-id="1d1c6-243">Por ejemplo, considere la siguiente declaración explícita:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-243">For instance, consider the following explicit declaration:</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



<span data-ttu-id="1d1c6-244">La declaración explícita que se indicó anteriormente es equivalente a la declaración siguiente que tendrá la semántica automáticamente incrementada por el compilador:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-244">The explicit declaration given above is equivalent to the following declaration that will have semantics automatically incremented by the compiler:</span></span>


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



<span data-ttu-id="1d1c6-245">Al igual que la semántica de entrada, la semántica de salida identifica el uso de datos para los datos de salida del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-245">Just like input semantics, output semantics identify data usage for pixel shader output data.</span></span> <span data-ttu-id="1d1c6-246">Muchos sombreadores de píxeles escriben en un solo color de salida.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-246">Many pixel shaders write to only one output color.</span></span> <span data-ttu-id="1d1c6-247">Los sombreadores de píxeles también pueden escribir un valor de profundidad en uno o varios destinos de representación al mismo tiempo (hasta cuatro).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-247">Pixel shaders can also write out a depth value into one or more multiple render targets at the same time (up to four).</span></span> <span data-ttu-id="1d1c6-248">Al igual que los sombreadores de vértices, los sombreadores de píxeles usan una estructura para devolver más de una salida.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-248">Like vertex shaders, pixel shaders use a structure to return more than one output.</span></span> <span data-ttu-id="1d1c6-249">Este sombreador escribe 0 en los componentes de color, así como en el componente de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-249">This shader writes 0 to the color components, as well as to the depth component.</span></span>


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



<span data-ttu-id="1d1c6-250">Los colores de salida del sombreador de píxeles deben ser del tipo FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-250">Pixel shader output colors must be of type float4.</span></span> <span data-ttu-id="1d1c6-251">Al escribir varios colores, todos los colores de salida deben usarse de forma contigua.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-251">When writing multiple colors, all output colors must be used contiguously.</span></span> <span data-ttu-id="1d1c6-252">En otras palabras, [COLOR1](dx-graphics-hlsl-semantics.md) no puede ser una salida a menos que ya se haya escrito [COLOR0](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="1d1c6-252">In other words, [COLOR1](dx-graphics-hlsl-semantics.md) cannot be an output unless [COLOR0](dx-graphics-hlsl-semantics.md) has already been written.</span></span> <span data-ttu-id="1d1c6-253">La salida de profundidad del sombreador de píxeles debe ser de tipo float1.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-253">Pixel shader depth output must be of type float1.</span></span>

### <a name="samplers-and-texture-objects"></a><span data-ttu-id="1d1c6-254">Muestras y objetos de textura</span><span class="sxs-lookup"><span data-stu-id="1d1c6-254">Samplers and Texture Objects</span></span>

<span data-ttu-id="1d1c6-255">Una muestra contiene el estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-255">A sampler contains sampler state.</span></span> <span data-ttu-id="1d1c6-256">Estado de muestra especifica la textura que se va a muestrear y controla el filtrado que se realiza durante el muestreo.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-256">Sampler state specifies the texture to be sampled, and controls the filtering that is done during sampling.</span></span> <span data-ttu-id="1d1c6-257">Se requieren tres cosas para muestrear una textura:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-257">Three things are required to sample a texture:</span></span>

-   <span data-ttu-id="1d1c6-258">Una textura</span><span class="sxs-lookup"><span data-stu-id="1d1c6-258">A texture</span></span>
-   <span data-ttu-id="1d1c6-259">Una muestra (con el estado de muestra)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-259">A sampler (with sampler state)</span></span>
-   <span data-ttu-id="1d1c6-260">Una instrucción de muestreo</span><span class="sxs-lookup"><span data-stu-id="1d1c6-260">A sampling instruction</span></span>

<span data-ttu-id="1d1c6-261">Los muestreadores se pueden inicializar con las texturas y el estado de muestra como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-261">Samplers can be initialized with textures and sampler state as shown here:</span></span>


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



<span data-ttu-id="1d1c6-262">Este es un ejemplo del código para muestrear una textura 2D:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-262">Here's an example of the code to sample a 2D texture:</span></span>


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



<span data-ttu-id="1d1c6-263">La textura se declara con una variable de textura tex0.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-263">The texture is declared with a texture variable tex0.</span></span>

<span data-ttu-id="1d1c6-264">En este ejemplo, se declara una variable de muestra denominada s \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-264">In this example, a sampler variable named s\_2D is declared.</span></span> <span data-ttu-id="1d1c6-265">El muestreador contiene el estado de muestra dentro de las llaves.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-265">The sampler contains the sampler state inside of curly braces.</span></span> <span data-ttu-id="1d1c6-266">Esto incluye la textura que se muestreará y, opcionalmente, el estado del filtro (es decir, modos de ajuste, modos de filtro, etc.).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-266">This includes the texture that will be sampled and, optionally, the filter state (that is, wrap modes, filter modes, etc.).</span></span> <span data-ttu-id="1d1c6-267">Si se omite el estado de muestra, se aplica un estado de muestra predeterminado que especifica el filtrado lineal y un modo de ajuste para las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-267">If the sampler state is omitted, a default sampler state is applied specifying linear filtering and a wrap mode for the texture coordinates.</span></span> <span data-ttu-id="1d1c6-268">La función de muestra toma una coordenada de textura de punto flotante de dos componentes y devuelve un color de dos componentes.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-268">The sampler function takes a two-component floating-point texture coordinate, and returns a two-component color.</span></span> <span data-ttu-id="1d1c6-269">Esto se representa con el tipo de valor devuelto float2 y representa los datos en los componentes rojo y verde.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-269">This is represented with the float2 return type and represents data in the red and green components.</span></span>

<span data-ttu-id="1d1c6-270">Se definen cuatro tipos de muestreadores (vea [palabras clave](dx-graphics-hlsl-appendix.md)) y las búsquedas de textura las realizan las funciones intrínsecas: [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**Tex3D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-270">Four types of samplers are defined (see [Keywords](dx-graphics-hlsl-appendix.md)) and texture lookups are performed by the intrinsic functions: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span></span> <span data-ttu-id="1d1c6-271">Este es un ejemplo de muestreo 3D:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-271">Here is an example of 3D sampling:</span></span>


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



<span data-ttu-id="1d1c6-272">Esta declaración de muestra usa el estado de muestra predeterminado para la configuración de filtro y el modo de dirección.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-272">This sampler declaration uses default sampler state for the filter settings and address mode.</span></span>

<span data-ttu-id="1d1c6-273">Este es el ejemplo de muestreo del cubo correspondiente:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-273">Here is the corresponding cube sampling example:</span></span>


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



<span data-ttu-id="1d1c6-274">Y, por último, este es el ejemplo de muestreo 1D:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-274">And finally, here is the 1D sampling example:</span></span>


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



<span data-ttu-id="1d1c6-275">Dado que el tiempo de ejecución no admite las texturas 1D, el compilador usará una textura 2D con el conocimiento de que la coordenada y no es importante.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-275">Because the runtime does not support 1D textures, the compiler will use a 2D texture with the knowledge that the y-coordinate is unimportant.</span></span> <span data-ttu-id="1d1c6-276">Dado que [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) se implementa como una búsqueda de textura 2D, el compilador es libre de elegir el componente y de una manera eficaz.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-276">Since [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) is implemented as a 2D texture lookup, the compiler is free to choose the y-component in an efficient manner.</span></span> <span data-ttu-id="1d1c6-277">En algunos escenarios poco frecuentes, el compilador no puede elegir un componente y eficaz, en cuyo caso emitirá una advertencia.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-277">In some rare scenarios, the compiler cannot choose an efficient y-component, in which case it will issue a warning.</span></span>


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



<span data-ttu-id="1d1c6-278">Este ejemplo concreto es ineficaz porque el compilador debe trasladar la coordenada de entrada a otro registro (porque una búsqueda 1D se implementa como una búsqueda en 2D y la coordenada de textura se declara como float1).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-278">This particular example is inefficient because the compiler must move the input coordinate into another register (because a 1D lookup is implemented as a 2D lookup and the texture coordinate is declared as a float1).</span></span> <span data-ttu-id="1d1c6-279">Si el código se reescribe con una entrada float2 en lugar de un float1, el compilador puede usar la coordenada de textura de entrada porque sabe que y se inicializa en algo.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-279">If the code is rewritten using a float2 input instead of a float1, the compiler can use the input texture coordinate because it knows that y is initialized to something.</span></span>


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



<span data-ttu-id="1d1c6-280">Todas las búsquedas de textura se pueden anexar con "bias" o "proj" (es decir, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**TEXCUBEPROJ (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-280">All texture lookups can be appended with "bias" or "proj" (that is, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span></span> <span data-ttu-id="1d1c6-281">Con el sufijo "proj", la coordenada de textura se divide por el componente w.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-281">With the "proj" suffix, the texture coordinate is divided by the w-component.</span></span> <span data-ttu-id="1d1c6-282">Con "bias", el nivel de MIP se desplaza por el componente w-.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-282">With "bias," the mip level is shifted by the w-component.</span></span> <span data-ttu-id="1d1c6-283">Por lo tanto, todas las búsquedas de textura con un sufijo siempre toman una entrada FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-283">Thus, all texture lookups with a suffix always take a float4 input.</span></span> <span data-ttu-id="1d1c6-284">[**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) y [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) omiten los componentes YZ y z, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) and [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignore the yz- and z-components respectively.</span></span>

<span data-ttu-id="1d1c6-285">Los muestreadores también se pueden usar en una matriz, aunque ningún back-end admite actualmente el acceso a matrices dinámicas de los muestreadores.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-285">Samplers may also be used in array, although no back end currently supports dynamic array access of samplers.</span></span> <span data-ttu-id="1d1c6-286">Por lo tanto, el siguiente código es válido porque puede resolverse en tiempo de compilación:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-286">Therefore, the following is valid because it can be resolved at compile time:</span></span>


```
tex2D(s[0],tex)
```



<span data-ttu-id="1d1c6-287">Sin embargo, este ejemplo no es válido.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-287">However, this example is not valid.</span></span>


```
tex2D(s[a],tex)
```



<span data-ttu-id="1d1c6-288">El acceso dinámico de los muestreadores es principalmente útil para escribir programas con bucles literales.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-288">Dynamic access of samplers is primarily useful for writing programs with literal loops.</span></span> <span data-ttu-id="1d1c6-289">El código siguiente muestra el acceso a la matriz de muestra:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-289">The following code illustrates sampler array accessing:</span></span>


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> <span data-ttu-id="1d1c6-290">El uso del tiempo de ejecución de depuración de Microsoft Direct3D puede ayudarle a detectar discrepancias entre el número de componentes de una textura y una muestra.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-290">Using the Microsoft Direct3D debug runtime can help you catch mismatches between the number of components in a texture and a sampler.</span></span>

 

## <a name="writing-functions"></a><span data-ttu-id="1d1c6-291">Escribir funciones</span><span class="sxs-lookup"><span data-stu-id="1d1c6-291">Writing Functions</span></span>

<span data-ttu-id="1d1c6-292">Las funciones dividen las tareas grandes en otras más pequeñas.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-292">Functions break large tasks into smaller ones.</span></span> <span data-ttu-id="1d1c6-293">Las tareas pequeñas son más fáciles de depurar y se pueden volver a usar, una vez probadas.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-293">Small tasks are easier to debug and can be reused, once proven.</span></span> <span data-ttu-id="1d1c6-294">Las funciones se pueden usar para ocultar detalles de otras funciones, lo que hace que un programa compuesto por funciones sea más fácil de seguir.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-294">Functions can be used to hide details of other functions, which makes a program composed of functions easier to follow.</span></span>

<span data-ttu-id="1d1c6-295">Las funciones de HLSL son similares a las funciones de C de varias maneras: ambas contienen una definición y un cuerpo de función y ambos declaran tipos de valor devuelto y listas de argumentos.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-295">HLSL functions are similar to C functions in several ways: They both contain a definition and a function body and they both declare return types and argument lists.</span></span> <span data-ttu-id="1d1c6-296">Al igual que las funciones de C, la validación de HLSL realiza la comprobación de tipos en los argumentos, los tipos de argumento y el valor devuelto durante la compilación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-296">Like C functions, HLSL validation does type checking on the arguments, argument types, and the return value during shader compilation.</span></span>

<span data-ttu-id="1d1c6-297">A diferencia de las funciones de C, las funciones de punto de entrada de HLSL usan la semántica para enlazar argumentos de función a entradas y salidas del sombreador (las funciones de HLSL llaman internamente omitir semántica).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-297">Unlike C functions, HLSL entry point functions use semantics to bind function arguments to shader inputs and outputs (HLSL functions called internally ignore semantics).</span></span> <span data-ttu-id="1d1c6-298">Esto hace que sea más fácil enlazar los datos del búfer a un sombreador y enlazar las salidas del sombreador a las entradas del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-298">This makes it easier to bind buffer data to a shader, and bind shader outputs to shader inputs.</span></span>

<span data-ttu-id="1d1c6-299">Una función contiene una declaración y un cuerpo, y la declaración debe preceder al cuerpo.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-299">A function contains a declaration and a body, and the declaration must precede the body.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="1d1c6-300">La declaración de función incluye todo lo delante de las llaves:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-300">The function declaration includes everything in front of the curly braces:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="1d1c6-301">Una declaración de función contiene:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-301">A function declaration contains:</span></span>

-   <span data-ttu-id="1d1c6-302">Un tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d1c6-302">A return type</span></span>
-   <span data-ttu-id="1d1c6-303">Un nombre de función</span><span class="sxs-lookup"><span data-stu-id="1d1c6-303">A function name</span></span>
-   <span data-ttu-id="1d1c6-304">Una lista de argumentos (opcional)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-304">An argument list (optional)</span></span>
-   <span data-ttu-id="1d1c6-305">Una semántica de salida (opcional)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-305">An output semantic (optional)</span></span>
-   <span data-ttu-id="1d1c6-306">Una anotación (opcional)</span><span class="sxs-lookup"><span data-stu-id="1d1c6-306">An annotation (optional)</span></span>

<span data-ttu-id="1d1c6-307">El tipo de valor devuelto puede ser cualquiera de los tipos de datos básicos de HLSL, como FLOAT4:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-307">The return type can be any of the HLSL basic data types such as a float4:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



<span data-ttu-id="1d1c6-308">El tipo de valor devuelto puede ser una estructura que ya se ha definido:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-308">The return type can be a structure that has already been defined:</span></span>


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="1d1c6-309">Si la función no devuelve un valor, se puede usar void como tipo de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-309">If the function does not return a value, void can be used as the return type.</span></span>


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="1d1c6-310">El tipo de valor devuelto siempre aparece primero en una declaración de función.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-310">The return type always appears first in a function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="1d1c6-311">Una lista de argumentos declara los argumentos de entrada de una función.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-311">An argument list declares the input arguments to a function.</span></span> <span data-ttu-id="1d1c6-312">También puede declarar valores que se devolverán.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-312">It may also declare values that will be returned.</span></span> <span data-ttu-id="1d1c6-313">Algunos argumentos son los argumentos de entrada y de salida.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-313">Some arguments are both input and output arguments.</span></span> <span data-ttu-id="1d1c6-314">Este es un ejemplo de un sombreador que toma cuatro argumentos de entrada.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-314">Here is an example of a shader that takes four input arguments.</span></span>


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



<span data-ttu-id="1d1c6-315">Esta función devuelve un color final, que es una combinación de una muestra de textura y el color claro.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-315">This function returns a final color, that is a blend of a texture sample and the light color.</span></span> <span data-ttu-id="1d1c6-316">La función toma cuatro entradas.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-316">The function takes four inputs.</span></span> <span data-ttu-id="1d1c6-317">Dos entradas tienen semántica: LightDir tiene la semántica [TEXCOORD1](dx-graphics-hlsl-semantics.md) y texcrd tiene la semántica [TEXCOORD0](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="1d1c6-317">Two inputs have semantics: LightDir has the [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, and texcrd has the [TEXCOORD0](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="1d1c6-318">La semántica significa que los datos de estas variables procederán del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-318">The semantics mean that the data for these variables will come from the vertex buffer.</span></span> <span data-ttu-id="1d1c6-319">Aunque la variable LightDir tiene una semántica [TEXCOORD1](dx-graphics-hlsl-semantics.md) , es probable que el parámetro no sea una coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-319">Even though the LightDir variable has a [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, the parameter is probably not a texture coordinate.</span></span> <span data-ttu-id="1d1c6-320">El tipo semántico TEXCOORDn se usa a menudo para proporcionar una semántica para un tipo que no está predefinido (no hay ninguna semántica de entrada del sombreador de vértices para una dirección clara).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-320">The TEXCOORDn semantic type is often used to supply a semantic for a type that is not predefined (there is no vertex shader input semantic for a light direction).</span></span>

<span data-ttu-id="1d1c6-321">Las otras dos entradas LightColor y samp se etiquetan con la palabra clave [Uniform](dx-graphics-hlsl-appendix.md) .</span><span class="sxs-lookup"><span data-stu-id="1d1c6-321">The other two inputs LightColor and samp are labeled with the [uniform](dx-graphics-hlsl-appendix.md) keyword.</span></span> <span data-ttu-id="1d1c6-322">Son constantes uniformes que no cambiarán entre las llamadas a Draw.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-322">These are uniform constants that will not change between draw calls.</span></span> <span data-ttu-id="1d1c6-323">Los valores de estos parámetros proceden de variables globales de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-323">The values for these parameters come from shader global variables.</span></span>

<span data-ttu-id="1d1c6-324">Los argumentos se pueden etiquetar como entradas con la palabra clave in y argumentos output con la palabra clave out.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-324">Arguments can be labeled as inputs with the in keyword, and output arguments with the out keyword.</span></span> <span data-ttu-id="1d1c6-325">Los argumentos no se pueden pasar por referencia; sin embargo, un argumento puede ser una entrada y una salida si se declara con la palabra clave INOUT.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-325">Arguments cannot be passed by reference; however, an argument can be both an input and an output if it is declared with the inout keyword.</span></span> <span data-ttu-id="1d1c6-326">Los argumentos pasados a una función que están marcados con la palabra clave INOUT se consideran copias del original hasta que la función devuelve y se copian de nuevo.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-326">Arguments passed to a function that are marked with the inout keyword are considered copies of the original until the function returns, and they are copied back.</span></span> <span data-ttu-id="1d1c6-327">A continuación se muestra un ejemplo del uso de INOUT:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-327">Here's an example using inout:</span></span>


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



<span data-ttu-id="1d1c6-328">Esta función incrementa los valores en A y B, y los devuelve.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-328">This function increments the values in A and B and returns them.</span></span>

<span data-ttu-id="1d1c6-329">El cuerpo de la función es todo el código después de la declaración de función.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-329">The function body is all of the code after the function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="1d1c6-330">El cuerpo consta de instrucciones que están entre llaves.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-330">The body consists of statements which are surrounded by curly braces.</span></span> <span data-ttu-id="1d1c6-331">El cuerpo de la función implementa toda la funcionalidad mediante variables, literales, expresiones e instrucciones.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-331">The function body implements all of the functionality using variables, literals, expressions, and statements.</span></span>

<span data-ttu-id="1d1c6-332">El cuerpo del sombreador hace dos cosas: realiza una multiplicación de la matriz y devuelve un resultado de FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-332">The shader body does two things: it performs a matrix multiply and returns a float4 result.</span></span> <span data-ttu-id="1d1c6-333">La multiplicación de la matriz se realiza con la función [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , que realiza multiplicaciones de matriz 4x4.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-333">The matrix multiply is accomplished with the [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) function, which performs a 4x4 matrix multiply.</span></span> <span data-ttu-id="1d1c6-334">**mul (DirectX HLSL)** se denomina función intrínseca porque ya está integrada en la biblioteca HLSL de funciones.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-334">**mul (DirectX HLSL)** is called an intrinsic function because it is already built into the HLSL library of functions.</span></span> <span data-ttu-id="1d1c6-335">Las funciones intrínsecas se tratarán con más detalle en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-335">Intrinsic functions will be covered in more detail in the next section.</span></span>

<span data-ttu-id="1d1c6-336">La matriz multiplica una combinación de vectores de entrada y una WorldViewProj de matriz compuesta.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-336">The matrix multiply combines an input vector Pos and a composite matrix WorldViewProj.</span></span> <span data-ttu-id="1d1c6-337">El resultado es colocar los datos transformados en el espacio de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-337">The result is position data transformed into screen space.</span></span> <span data-ttu-id="1d1c6-338">Este es el procesamiento del sombreador de vértices mínimo que se puede hacer.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-338">This is the minimum vertex shader processing we can do.</span></span> <span data-ttu-id="1d1c6-339">Si usamos la canalización de función fija en lugar de un sombreador de vértices, los datos de vértices podrían dibujarse después de realizar esta transformación.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-339">If we were using the fixed function pipeline instead of a vertex shader, the vertex data could be drawn after doing this transform.</span></span>

<span data-ttu-id="1d1c6-340">La última instrucción de un cuerpo de función es una instrucción return.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-340">The last statement in a function body is a return statement.</span></span> <span data-ttu-id="1d1c6-341">Al igual que C, esta instrucción devuelve el control de la función a la instrucción que llamó a la función.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-341">Just like C, this statement returns control from the function to the statement that called the function.</span></span>

<span data-ttu-id="1d1c6-342">Los tipos de valor devueltos de función pueden ser cualquiera de los tipos de datos simples definidos en HLSL, incluidos bool, int Half, float y Double.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-342">Function return types can be any of the simple data types defined in HLSL, including bool, int half, float, and double.</span></span> <span data-ttu-id="1d1c6-343">Los tipos devueltos pueden ser uno de los tipos de datos complejos como vectores y matrices.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-343">Return types can be one of the complex data types such as vectors and matrices.</span></span> <span data-ttu-id="1d1c6-344">Los tipos HLSL que hacen referencia a objetos no se pueden usar como tipos de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-344">HLSL types that refer to objects cannot be used as return types.</span></span> <span data-ttu-id="1d1c6-345">Esto incluye u, Vertexshader, Texture y muestreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-345">This includes pixelshader, vertexshader, texture, and sampler.</span></span>

<span data-ttu-id="1d1c6-346">Este es un ejemplo de una función que usa una estructura para un tipo de valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-346">Here is an example of a function that uses a structure for a return type.</span></span>


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



<span data-ttu-id="1d1c6-347">El tipo de valor devuelto FLOAT4 se ha reemplazado por la estructura VS \_ Output, que ahora contiene un solo miembro FLOAT4.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-347">The float4 return type has been replaced with the structure VS\_OUTPUT, which now contains a single float4 member.</span></span>

<span data-ttu-id="1d1c6-348">Una instrucción return indica el final de una función.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-348">A return statement signals the end of a function.</span></span> <span data-ttu-id="1d1c6-349">Esta es la instrucción return más sencilla.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-349">This is the simplest return statement.</span></span> <span data-ttu-id="1d1c6-350">Devuelve el control de la función al programa que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-350">It returns control from the function to the calling program.</span></span> <span data-ttu-id="1d1c6-351">No devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-351">It returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="1d1c6-352">Una instrucción return puede devolver uno o más valores.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-352">A return statement can return one or more values.</span></span> <span data-ttu-id="1d1c6-353">Este ejemplo devuelve un valor literal:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-353">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="1d1c6-354">En este ejemplo se devuelve el resultado escalar de una expresión:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-354">This example returns the scalar result of an expression:</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="1d1c6-355">Este ejemplo devuelve un FLOAT4 construido a partir de una variable local y un literal:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-355">This example returns a float4 constructed from a local variable and a literal:</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="1d1c6-356">Este ejemplo devuelve un FLOAT4 que se construye a partir del resultado devuelto de una función intrínseca y algunos valores literales:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-356">This example returns a float4 that is constructed from the result returned from an intrinsic function, and a few literal values:</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="1d1c6-357">En este ejemplo se devuelve una estructura que contiene uno o más miembros:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-357">This example returns a structure that contains one or more members:</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a><span data-ttu-id="1d1c6-358">Control de flujo</span><span class="sxs-lookup"><span data-stu-id="1d1c6-358">Flow Control</span></span>

<span data-ttu-id="1d1c6-359">El hardware del sombreador de píxeles y vértices más actual está diseñado para ejecutar un sombreador línea a línea y ejecutar cada instrucción una vez.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-359">Most current vertex and pixel shader hardware is designed to run a shader line by line, executing each instruction once.</span></span> <span data-ttu-id="1d1c6-360">HLSL admite el control de flujo, que incluye bifurcaciones estáticas, instrucciones de predicado, bucles estáticos, bifurcación dinámica y bucle dinámico.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-360">HLSL supports flow control, which includes static branching, predicated instructions, static looping, dynamic branching, and dynamic looping.</span></span>

<span data-ttu-id="1d1c6-361">Anteriormente, el uso de una instrucción If producía el código del sombreador de lenguaje de ensamblado que implementa tanto el lado if como el lado else del flujo de código.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-361">Previously, using an if statement resulted in assembly-language shader code that implements both the if side and the else side of the code flow.</span></span> <span data-ttu-id="1d1c6-362">Este es un ejemplo de en el código HLSL que se compiló para vs \_ 1 \_ 1:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-362">Here is an example of the in HLSL code that was compiled for vs\_1\_1:</span></span>


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



<span data-ttu-id="1d1c6-363">Y este es el código de ensamblado resultante:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-363">And here is the resulting assembly code:</span></span>


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



<span data-ttu-id="1d1c6-364">Cierto hardware permite bucles estáticos o dinámicos, pero la mayoría de ellas requieren ejecución lineal.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-364">Some hardware allows for either static or dynamic looping, but most require linear execution.</span></span> <span data-ttu-id="1d1c6-365">En los modelos que no admiten bucles, todos los bucles deben estar inscritos.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-365">On the models that do not support looping, all loops must be unrolled.</span></span> <span data-ttu-id="1d1c6-366">Un ejemplo es el ejemplo de ejemplo [DepthOfField](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) que usa bucles no rescritos incluso para los \_ sombreadores de PS 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-366">An example is the [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) sample that uses unrolled loops even for ps\_1\_1 shaders.</span></span>

<span data-ttu-id="1d1c6-367">HLSL ahora incluye compatibilidad con cada uno de estos tipos de control de flujo:</span><span class="sxs-lookup"><span data-stu-id="1d1c6-367">HLSL now includes support for each of these types of flow control:</span></span>

-   <span data-ttu-id="1d1c6-368">bifurcación estática</span><span class="sxs-lookup"><span data-stu-id="1d1c6-368">static branching</span></span>
-   <span data-ttu-id="1d1c6-369">instrucciones de predicado</span><span class="sxs-lookup"><span data-stu-id="1d1c6-369">predicated instructions</span></span>
-   <span data-ttu-id="1d1c6-370">bucle estático</span><span class="sxs-lookup"><span data-stu-id="1d1c6-370">static looping</span></span>
-   <span data-ttu-id="1d1c6-371">bifurcación dinámica</span><span class="sxs-lookup"><span data-stu-id="1d1c6-371">dynamic branching</span></span>
-   <span data-ttu-id="1d1c6-372">bucle dinámico</span><span class="sxs-lookup"><span data-stu-id="1d1c6-372">dynamic looping</span></span>

<span data-ttu-id="1d1c6-373">La bifurcación estática permite activar o desactivar bloques de código de sombreador en función de una constante de sombreador booleano.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-373">Static branching allows blocks of shader code to be switched on or off based on a Boolean shader constant.</span></span> <span data-ttu-id="1d1c6-374">Este es un método práctico para habilitar o deshabilitar las rutas de acceso de código según el tipo de objeto que se está representando actualmente.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-374">This is a convenient method for enabling or disabling code paths based on the type of object currently being rendered.</span></span> <span data-ttu-id="1d1c6-375">Entre las llamadas a Draw, puede decidir qué características desea admitir con el sombreador actual y, a continuación, establecer las marcas booleanas necesarias para obtener ese comportamiento.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-375">Between draw calls, you can decide which features you want to support with the current shader and then set the Boolean flags required to get that behavior.</span></span> <span data-ttu-id="1d1c6-376">Las instrucciones que están deshabilitadas por una constante booleana se omiten durante la ejecución del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-376">Any statements that are disabled by a Boolean constant are skipped during shader execution.</span></span>

<span data-ttu-id="1d1c6-377">La compatibilidad con bifurcación más conocida es la bifurcación dinámica.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-377">The most familiar branching support is dynamic branching.</span></span> <span data-ttu-id="1d1c6-378">Con las bifurcaciones dinámicas, la condición de comparación reside en una variable, lo que significa que la comparación se realiza para cada vértice o cada píxel en tiempo de ejecución (en lugar de la comparación que se produce en tiempo de compilación, o entre dos llamadas a Draw).</span><span class="sxs-lookup"><span data-stu-id="1d1c6-378">With dynamic branching, the comparison condition resides in a variable, which means that the comparison is done for each vertex or each pixel at run time (as opposed to the comparison occurring at compile time, or between two draw calls).</span></span> <span data-ttu-id="1d1c6-379">El impacto en el rendimiento es el costo de la bifurcación más el costo de las instrucciones en el lateral de la bifurcación tomada.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-379">The performance hit is the cost of the branch plus the cost of the instructions on the side of the branch taken.</span></span> <span data-ttu-id="1d1c6-380">La bifurcación dinámica se implementa en el modelo de sombreador 3 o superior.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-380">Dynamic branching is implemented in shader model 3 or higher.</span></span> <span data-ttu-id="1d1c6-381">La optimización de los sombreadores que funcionan con estos modelos es similar a la optimización del código que se ejecuta en una CPU.</span><span class="sxs-lookup"><span data-stu-id="1d1c6-381">Optimizing shaders that work with these models is similar to optimizing code that runs on a CPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d1c6-382">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1d1c6-382">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d1c6-383">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="1d1c6-383">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 