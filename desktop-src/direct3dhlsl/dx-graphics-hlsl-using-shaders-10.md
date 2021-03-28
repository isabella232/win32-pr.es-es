---
title: Usar sombreadores en Direct3D 10
description: Usar sombreadores en Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e19275532ce8fd034813d8574f6bdc04d72f966
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358989"
---
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="4f3c5-103">Usar sombreadores en Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="4f3c5-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="4f3c5-104">La canalización tiene tres fases del sombreador y cada una se programa con un sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="4f3c5-105">Todos los sombreadores de Direct3D 10 están escritos en HLSL y tienen como destino el modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>



|                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3c5-106">Diferencias entre Direct3D 9 y Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="4f3c5-106">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="4f3c5-107">A diferencia de los modelos de sombreador de Direct3D 9 que podrían crearse en un lenguaje de ensamblado intermedio, los sombreadores de modelo de sombreador 4,0 solo se crean en HLSL.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="4f3c5-108">Todavía se admite la compilación sin conexión de los sombreadores en código de bytes consumible por dispositivo y se recomienda para la mayoría de los escenarios.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span><br/> |



 

<span data-ttu-id="4f3c5-109">En este ejemplo se usa solo un sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="4f3c5-110">Dado que todos los sombreadores se crean a partir de la base de sombreador común, aprender a usar un sombreador de vértices es muy similar al uso de una geometría o un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="4f3c5-111">Una vez que haya creado un sombreador HLSL (en este ejemplo se usa el sombreador de vértices HLSLWithoutFX. VSH), deberá prepararlo para la fase de canalización concreta que lo usará.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="4f3c5-112">Para ello, debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f3c5-112">To do this you need to:</span></span>

-   [<span data-ttu-id="4f3c5-113">Compilar un sombreador</span><span class="sxs-lookup"><span data-stu-id="4f3c5-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="4f3c5-114">Crear un objeto de sombreador</span><span class="sxs-lookup"><span data-stu-id="4f3c5-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="4f3c5-115">Establecimiento del objeto de sombreador</span><span class="sxs-lookup"><span data-stu-id="4f3c5-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="4f3c5-116">Repetir para las tres fases del sombreador</span><span class="sxs-lookup"><span data-stu-id="4f3c5-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="4f3c5-117">Estos pasos deben repetirse para cada sombreador de la canalización.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="4f3c5-118">Compilar un sombreador</span><span class="sxs-lookup"><span data-stu-id="4f3c5-118">Compile a Shader</span></span>

<span data-ttu-id="4f3c5-119">El primer paso consiste en compilar el sombreador para comprobar que ha codificado las instrucciones de HLSL correctamente.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="4f3c5-120">Esto se hace llamando a D3D10CompileShader y proporcionando varios parámetros, como se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="4f3c5-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="4f3c5-121">Esta función toma los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="4f3c5-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="4f3c5-122">El nombre del archivo (y la longitud de la cadena de nombre en bytes) que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="4f3c5-123">En este ejemplo solo se usa un sombreador de vértices (en el archivo HLSLWithoutFX. VSH de archivo donde la extensión de archivo. VSH es una abreviatura del sombreador de vértices).</span><span class="sxs-lookup"><span data-stu-id="4f3c5-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="4f3c5-124">Nombre de la función de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-124">The shader function name.</span></span> <span data-ttu-id="4f3c5-125">En este ejemplo se compila un sombreador de vértices de la función rizo que toma una sola entrada y devuelve un struct de salida (la función es del ejemplo HLSLWithoutFX):</span><span class="sxs-lookup"><span data-stu-id="4f3c5-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="4f3c5-126">Puntero a todas las macros utilizadas por el sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="4f3c5-127">Use \_ \_ la macro D3D10 Shader para ayudar a definir las macros; simplemente cree una cadena de nombre que contenga todos los nombres de macro (con cada nombre separado por un espacio) y una cadena de definición (con cada cuerpo de macro separado por un espacio).</span><span class="sxs-lookup"><span data-stu-id="4f3c5-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="4f3c5-128">Ambas cadenas deben terminar en NULL.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="4f3c5-129">Un puntero a cualquier otro archivo que se necesite para obtener los sombreadores que se van a compilar.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="4f3c5-130">Usa la interfaz ID3D10Include, que tiene dos métodos implementados por el usuario: abrir y cerrar.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="4f3c5-131">Para realizar este trabajo, debe implementar el cuerpo de los métodos Open y Close; en el método Open, agregue el código que desea utilizar para abrir los archivos de inclusión que desee, en la función Close agregue el código para cerrar los archivos cuando haya terminado con ellos.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="4f3c5-132">Nombre de la función de sombreador que se va a compilar.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-132">The name of the shader function to compile.</span></span> <span data-ttu-id="4f3c5-133">Este sombreador compila la función Ripple.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="4f3c5-134">Perfil del sombreador al que se va a compilar.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="4f3c5-135">Dado que puede compilar una función en un sombreador de píxeles, geometría o vértice, el perfil indica al compilador qué tipo de sombreador y en qué modelo de sombreador comparar el código.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="4f3c5-136">Marcas de compilador de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-136">Shader compiler flags.</span></span> <span data-ttu-id="4f3c5-137">Estas marcas indican al compilador qué información debe incluir en la salida compilada y cómo desea optimizar el código de salida: para la velocidad, para la depuración, etc. Vea [constantes de efecto (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) para obtener una lista de las marcas disponibles.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="4f3c5-138">El ejemplo contiene código que se puede usar para establecer los valores de la marca del compilador para el proyecto; esto es principalmente una pregunta sobre si se desea o no generar información de depuración.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="4f3c5-139">Puntero al búfer que contiene el código del sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="4f3c5-140">El búfer también contiene cualquier información de la tabla de símbolos y depuración insertada solicitada por las marcas del compilador.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="4f3c5-141">Un puntero a un búfer que contiene una lista de errores y advertencias encontrados durante la compilación, que son los mismos mensajes que se verán en la salida de depuración si se estaba ejecutando el depurador mientras se compilaba el sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="4f3c5-142">**Null** es un valor aceptable cuando no se desea que los errores se devuelvan a un búfer.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="4f3c5-143">Si el sombreador se compila correctamente, se devuelve un puntero al código del sombreador como una interfaz ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="4f3c5-144">Se denomina interfaz de blobs porque el puntero está en una ubicación de memoria que se compone de una matriz de DWORD.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="4f3c5-145">La interfaz se proporciona para que pueda obtener un puntero al sombreador compilado que necesitará en el paso siguiente.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="4f3c5-146">A partir del SDK de diciembre de 2006, el compilador de HLSL de DirectX 10 es ahora el compilador predeterminado en DirectX 9 y DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="4f3c5-147">Consulte [herramienta de compilador de efectos](/windows/desktop/direct3dtools/fxc) para más información.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="4f3c5-148">Obtener un puntero a un sombreador compilado</span><span class="sxs-lookup"><span data-stu-id="4f3c5-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="4f3c5-149">Varios métodos de API requieren un puntero a un sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="4f3c5-150">Este argumento se denomina normalmente *pShaderBytecode* porque apunta a un sombreador compilado representado como una secuencia de códigos de bytes.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="4f3c5-151">Para obtener un puntero a un sombreador compilado, primero compile el sombreador llamando a [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) o a una función similar.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="4f3c5-152">Si la compilación se realiza correctamente, el sombreador compilado se devuelve en una interfaz [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) .</span><span class="sxs-lookup"><span data-stu-id="4f3c5-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="4f3c5-153">Por último, use el método [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) para devolver el puntero.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="4f3c5-154">Crear un objeto de sombreador</span><span class="sxs-lookup"><span data-stu-id="4f3c5-154">Create a Shader Object</span></span>

<span data-ttu-id="4f3c5-155">Una vez compilado el sombreador, llame a CreateVertexShader para crear el objeto de sombreador:</span><span class="sxs-lookup"><span data-stu-id="4f3c5-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="4f3c5-156">Para crear el objeto de sombreador, pase el puntero al sombreador compilado en CreateVertexShader.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="4f3c5-157">Como antes tenía que compilar el sombreador correctamente, esta llamada se realizará casi con toda certeza, a menos que tenga un problema de memoria en el equipo.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="4f3c5-158">Puede crear tantos objetos de sombreador como desee y simplemente mantener punteros a ellos.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="4f3c5-159">Este mismo mecanismo funciona para los sombreadores de píxeles y de geometría, siempre que se haga coincidir los perfiles del sombreador (cuando se llama al método compile) con los nombres de interfaz (cuando se llama al método Create).</span><span class="sxs-lookup"><span data-stu-id="4f3c5-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="4f3c5-160">Establecimiento del objeto de sombreador</span><span class="sxs-lookup"><span data-stu-id="4f3c5-160">Set the Shader Object</span></span>

<span data-ttu-id="4f3c5-161">El último paso es establecer el sombreador en la fase de canalización.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="4f3c5-162">Dado que hay tres fases del sombreador en la canalización, tendrá que realizar tres llamadas API, una para cada fase.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="4f3c5-163">La llamada a VSSetShader toma el puntero al sombreador de vértices creado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="4f3c5-164">Esto establece el sombreador en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-164">This sets the shader in the device.</span></span> <span data-ttu-id="4f3c5-165">La fase del sombreador de vértices se inicializa ahora con el código del sombreador de vértices; todo lo que queda es inicializar las variables de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="4f3c5-166">Repetir para las tres fases del sombreador</span><span class="sxs-lookup"><span data-stu-id="4f3c5-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="4f3c5-167">Repita este mismo conjunto de pasos para compilar cualquier sombreador de vértices o píxeles, o incluso un sombreador de geometría que genere el sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="4f3c5-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f3c5-168">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f3c5-168">Related Topics</span></span>

[<span data-ttu-id="4f3c5-169">Compilación de sombreadores</span><span class="sxs-lookup"><span data-stu-id="4f3c5-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="4f3c5-170">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4f3c5-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f3c5-171">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="4f3c5-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

