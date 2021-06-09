---
title: Uso de sombreadores en Direct3D 10
description: Uso de sombreadores en Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0d6212851e4603aac4db7ec85dd20714dc87774
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826293"
---
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="07b37-103">Uso de sombreadores en Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="07b37-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="07b37-104">La canalización tiene tres fases de sombreador y cada una se programa con un sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="07b37-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="07b37-105">Todos los sombreadores de Direct3D 10 se escriben en HLSL y tienen como destino el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="07b37-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>


<span data-ttu-id="07b37-106">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="07b37-106">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="07b37-107">A diferencia de los modelos de sombreador de Direct3D 9 que podrían crearse en un lenguaje de ensamblado intermedio, los sombreadores del modelo de sombreador 4.0 solo se han creado en HLSL.</span><span class="sxs-lookup"><span data-stu-id="07b37-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="07b37-108">Todavía se admite la compilación sin conexión de sombreadores en código de bytes que se puede consumir en el dispositivo y se recomienda para la mayoría de los escenarios.</span><span class="sxs-lookup"><span data-stu-id="07b37-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span>



 

<span data-ttu-id="07b37-109">En este ejemplo solo se usa un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="07b37-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="07b37-110">Dado que todos los sombreadores se compilan a partir del núcleo común del sombreador, aprender a usar un sombreador de vértices es muy similar al uso de un sombreador de geometría o píxeles.</span><span class="sxs-lookup"><span data-stu-id="07b37-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="07b37-111">Una vez que haya creado un sombreador HLSL (en este ejemplo se usa el sombreador de vértices HLSLWithoutFX.vsh), deberá prepararlo para la fase de canalización concreta que lo usará.</span><span class="sxs-lookup"><span data-stu-id="07b37-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="07b37-112">Para ello, debe:</span><span class="sxs-lookup"><span data-stu-id="07b37-112">To do this you need to:</span></span>

-   [<span data-ttu-id="07b37-113">Compilación de un sombreador</span><span class="sxs-lookup"><span data-stu-id="07b37-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="07b37-114">Crear un objeto shader</span><span class="sxs-lookup"><span data-stu-id="07b37-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="07b37-115">Establecer el objeto Shader</span><span class="sxs-lookup"><span data-stu-id="07b37-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="07b37-116">Repetir para las tres fases del sombreador</span><span class="sxs-lookup"><span data-stu-id="07b37-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="07b37-117">Estos pasos deben repetirse para cada sombreador de la canalización.</span><span class="sxs-lookup"><span data-stu-id="07b37-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="07b37-118">Compilación de un sombreador</span><span class="sxs-lookup"><span data-stu-id="07b37-118">Compile a Shader</span></span>

<span data-ttu-id="07b37-119">El primer paso consiste en compilar el sombreador para comprobar que ha codificado correctamente las instrucciones HLSL.</span><span class="sxs-lookup"><span data-stu-id="07b37-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="07b37-120">Para ello, llame a D3D10CompileShader y proporcione varios parámetros, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="07b37-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="07b37-121">Esta función toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="07b37-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="07b37-122">Nombre del archivo ( y longitud de la cadena de nombre en bytes ) que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="07b37-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="07b37-123">En este ejemplo solo se usa un sombreador de vértices (en el archivo HLSLWithoutFX.vsh, donde la extensión de archivo .vsh es una abreviatura del sombreador de vértices).</span><span class="sxs-lookup"><span data-stu-id="07b37-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="07b37-124">Nombre de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="07b37-124">The shader function name.</span></span> <span data-ttu-id="07b37-125">En este ejemplo se compila un sombreador de vértices a partir de la función Waterfall que toma una única entrada y devuelve una estructura de salida (la función es del ejemplo HLSLWithoutFX):</span><span class="sxs-lookup"><span data-stu-id="07b37-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="07b37-126">Puntero a todas las macros usadas por el sombreador.</span><span class="sxs-lookup"><span data-stu-id="07b37-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="07b37-127">Use D3D10 SHADER MACRO para ayudar a definir las macros; simplemente cree una cadena de nombre que contenga todos los nombres de macro (con cada nombre separado por un espacio) y una cadena de definición (con cada cuerpo de macro separado por \_ \_ un espacio).</span><span class="sxs-lookup"><span data-stu-id="07b37-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="07b37-128">Ambas cadenas deben terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="07b37-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="07b37-129">Puntero a cualquier otro archivo que necesite incluir para que los sombreadores se compilen.</span><span class="sxs-lookup"><span data-stu-id="07b37-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="07b37-130">Esto usa la interfaz ID3D10Include, que tiene dos métodos implementados por el usuario: Open y Close.</span><span class="sxs-lookup"><span data-stu-id="07b37-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="07b37-131">Para que esto funcione, deberá implementar el cuerpo de los métodos Open y Close. en el método Open, agregue el código que usaría para abrir los archivos de incluyeción que desee, en la función Close agregue el código para cerrar los archivos cuando haya terminado con ellos.</span><span class="sxs-lookup"><span data-stu-id="07b37-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="07b37-132">Nombre de la función de sombreador que se compilará.</span><span class="sxs-lookup"><span data-stu-id="07b37-132">The name of the shader function to compile.</span></span> <span data-ttu-id="07b37-133">Este sombreador compila la función Waterfall.</span><span class="sxs-lookup"><span data-stu-id="07b37-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="07b37-134">El perfil de sombreador que se debe tener como destino al compilar.</span><span class="sxs-lookup"><span data-stu-id="07b37-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="07b37-135">Puesto que puede compilar una función en un sombreador de vértices, geometría o píxeles, el perfil indica al compilador qué tipo de sombreador y con qué modelo de sombreador comparar el código.</span><span class="sxs-lookup"><span data-stu-id="07b37-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="07b37-136">Marcas del compilador del sombreador.</span><span class="sxs-lookup"><span data-stu-id="07b37-136">Shader compiler flags.</span></span> <span data-ttu-id="07b37-137">Estas marcas le informan al compilador qué información se debe colocar en la salida compilada y cómo desea optimizar el código de salida: para la velocidad, para la depuración, etc. Consulte [Constantes de efecto (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) para obtener una lista de las marcas disponibles.</span><span class="sxs-lookup"><span data-stu-id="07b37-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="07b37-138">El ejemplo contiene código que puede usar para establecer los valores de la marca del compilador para el proyecto; se trata principalmente de una pregunta sobre si desea generar o no información de depuración.</span><span class="sxs-lookup"><span data-stu-id="07b37-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="07b37-139">Puntero al búfer que contiene el código del sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="07b37-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="07b37-140">El búfer también contiene cualquier información de tabla de símbolos y depuración incrustada solicitada por las marcas del compilador.</span><span class="sxs-lookup"><span data-stu-id="07b37-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="07b37-141">Puntero a un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación, que son los mismos mensajes que vería en la salida de depuración si estuviera ejecutando el depurador mientras compilaba el sombreador.</span><span class="sxs-lookup"><span data-stu-id="07b37-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="07b37-142">**NULL** es un valor aceptable cuando no desea que se devuelvan los errores a un búfer.</span><span class="sxs-lookup"><span data-stu-id="07b37-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="07b37-143">Si el sombreador se compila correctamente, se devuelve un puntero al código del sombreador como una interfaz ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="07b37-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="07b37-144">Se denomina interfaz blob porque el puntero es a una ubicación en memoria que está integrada por una matriz de DWORD.</span><span class="sxs-lookup"><span data-stu-id="07b37-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="07b37-145">La interfaz se proporciona para que pueda obtener un puntero al sombreador compilado que necesitará en el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="07b37-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="07b37-146">A partir del SDK de diciembre de 2006, el compilador HLSL de DirectX 10 es ahora el compilador predeterminado en DirectX 9 y DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="07b37-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="07b37-147">Vea [Effect-Compiler Tool para](/windows/desktop/direct3dtools/fxc) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="07b37-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="07b37-148">Obtener un puntero a un sombreador compilado</span><span class="sxs-lookup"><span data-stu-id="07b37-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="07b37-149">Varios métodos de API requieren un puntero a un sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="07b37-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="07b37-150">Este argumento se suele *denominar pShaderBytecode porque* apunta a un sombreador compilado representado como una secuencia de códigos de bytes.</span><span class="sxs-lookup"><span data-stu-id="07b37-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="07b37-151">Para obtener un puntero a un sombreador compilado, compile primero el sombreador llamando a [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) o a una función similar.</span><span class="sxs-lookup"><span data-stu-id="07b37-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="07b37-152">Si la compilación se realiza correctamente, el sombreador compilado se devuelve en una [**interfaz ID3D10Blob.**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)</span><span class="sxs-lookup"><span data-stu-id="07b37-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="07b37-153">Por último, use [**el método GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) para devolver el puntero.</span><span class="sxs-lookup"><span data-stu-id="07b37-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="07b37-154">Crear un objeto shader</span><span class="sxs-lookup"><span data-stu-id="07b37-154">Create a Shader Object</span></span>

<span data-ttu-id="07b37-155">Una vez compilado el sombreador, llame a CreateVertexShader para crear el objeto de sombreador:</span><span class="sxs-lookup"><span data-stu-id="07b37-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="07b37-156">Para crear el objeto de sombreador, pase el puntero al sombreador compilado en CreateVertexShader.</span><span class="sxs-lookup"><span data-stu-id="07b37-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="07b37-157">Dado que antes tenía que compilar correctamente el sombreador, esta llamada casi seguro pasará, a menos que tenga un problema de memoria en la máquina.</span><span class="sxs-lookup"><span data-stu-id="07b37-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="07b37-158">Puede crear tantos objetos de sombreador como quiera y simplemente mantener punteros a ellos.</span><span class="sxs-lookup"><span data-stu-id="07b37-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="07b37-159">Este mismo mecanismo funciona para sombreadores de geometría y píxeles suponiendo que coincida con los perfiles de sombreador (cuando se llama al método de compilación) con los nombres de interfaz (cuando se llama al método create).</span><span class="sxs-lookup"><span data-stu-id="07b37-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="07b37-160">Establecer el objeto Shader</span><span class="sxs-lookup"><span data-stu-id="07b37-160">Set the Shader Object</span></span>

<span data-ttu-id="07b37-161">El último paso es establecer el sombreador en la fase de canalización.</span><span class="sxs-lookup"><span data-stu-id="07b37-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="07b37-162">Dado que hay tres fases de sombreador en la canalización, deberá realizar tres llamadas API, una para cada fase.</span><span class="sxs-lookup"><span data-stu-id="07b37-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="07b37-163">La llamada a VSSetShader toma el puntero al sombreador de vértices creado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="07b37-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="07b37-164">Esto establece el sombreador en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07b37-164">This sets the shader in the device.</span></span> <span data-ttu-id="07b37-165">La fase del sombreador de vértices ahora se inicializa con su código de sombreador de vértices, lo único que queda es inicializar cualquier variable de sombreador.</span><span class="sxs-lookup"><span data-stu-id="07b37-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="07b37-166">Repetir para las tres fases del sombreador</span><span class="sxs-lookup"><span data-stu-id="07b37-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="07b37-167">Repita este mismo conjunto de pasos para crear cualquier sombreador de vértices o píxeles o incluso un sombreador de geometría que genere el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="07b37-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07b37-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07b37-168">Related Topics</span></span>

[<span data-ttu-id="07b37-169">Compilación de sombreadores</span><span class="sxs-lookup"><span data-stu-id="07b37-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="07b37-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07b37-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07b37-171">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="07b37-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

