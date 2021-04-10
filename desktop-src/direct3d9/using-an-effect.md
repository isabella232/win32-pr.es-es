---
description: En esta página se muestra cómo generar y usar un efecto.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Usar un efecto (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152687"
---
# <a name="using-an-effect-direct3d-9"></a><span data-ttu-id="40109-103">Usar un efecto (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="40109-103">Using an Effect (Direct3D 9)</span></span>

<span data-ttu-id="40109-104">En esta página se muestra cómo generar y usar un efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-104">This page will show you how to generate and use an effect.</span></span> <span data-ttu-id="40109-105">Los temas tratados incluyen cómo:</span><span class="sxs-lookup"><span data-stu-id="40109-105">The topics covered include how to:</span></span>

-   [<span data-ttu-id="40109-106">Crear un efecto</span><span class="sxs-lookup"><span data-stu-id="40109-106">Create an Effect</span></span>](#create-an-effect)
-   [<span data-ttu-id="40109-107">Representar un efecto</span><span class="sxs-lookup"><span data-stu-id="40109-107">Render an Effect</span></span>](#render-an-effect)
-   [<span data-ttu-id="40109-108">Usar la semántica para buscar parámetros de efectos</span><span class="sxs-lookup"><span data-stu-id="40109-108">Use Semantics to Find Effect Parameters</span></span>](#use-semantics-to-find-effect-parameters)
-   [<span data-ttu-id="40109-109">Usar los controladores para obtener y establecer los parámetros de forma eficaz</span><span class="sxs-lookup"><span data-stu-id="40109-109">Use Handles to Get and Set Parameters Efficiently</span></span>](#use-handles-to-get-and-set-parameters-efficiently)
-   [<span data-ttu-id="40109-110">Agregar información de parámetros con anotaciones</span><span class="sxs-lookup"><span data-stu-id="40109-110">Add Parameter Information with Annotations</span></span>](#add-parameter-information-with-annotations)
-   [<span data-ttu-id="40109-111">Parámetros de efectos compartidos</span><span class="sxs-lookup"><span data-stu-id="40109-111">Share Effect Parameters</span></span>](#share-effect-parameters)
-   [<span data-ttu-id="40109-112">Compilar un efecto sin conexión</span><span class="sxs-lookup"><span data-stu-id="40109-112">Compile an Effect Offline</span></span>](#compile-an-effect-offline)
-   [<span data-ttu-id="40109-113">Mejorar el rendimiento con los sombreadores</span><span class="sxs-lookup"><span data-stu-id="40109-113">Improve Performance with Preshaders</span></span>](#improve-performance-with-preshaders)
-   [<span data-ttu-id="40109-114">Usar bloques de parámetros para administrar parámetros de efectos</span><span class="sxs-lookup"><span data-stu-id="40109-114">Use Parameter Blocks to Manage Effect Parameters</span></span>](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a><span data-ttu-id="40109-115">Crear un efecto</span><span class="sxs-lookup"><span data-stu-id="40109-115">Create an Effect</span></span>

<span data-ttu-id="40109-116">Este es un ejemplo de la creación de un efecto tomado del [ejemplo BasicHLSL](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="40109-116">Here is an example of creating an effect taken from the [BasicHLSL Sample](../directx-sdk--august-2009-.md).</span></span> <span data-ttu-id="40109-117">El código de creación del efecto para crear un sombreador de depuración es desde **OnCreateDevice**:</span><span class="sxs-lookup"><span data-stu-id="40109-117">The effect creation code for creating a debug shader is from **OnCreateDevice**:</span></span>


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



<span data-ttu-id="40109-118">Esta función toma estos argumentos:</span><span class="sxs-lookup"><span data-stu-id="40109-118">This function takes these arguments:</span></span>

-   <span data-ttu-id="40109-119">Dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40109-119">The device.</span></span>
-   <span data-ttu-id="40109-120">Nombre del archivo de efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-120">The file name of the effect file.</span></span>
-   <span data-ttu-id="40109-121">Un puntero a una lista de definiciones terminada en NULL \# que se va a utilizar al analizar el sombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-121">A pointer to a NULL-terminated list of \#defines, to be used while parsing the shader.</span></span>
-   <span data-ttu-id="40109-122">Un puntero opcional a un controlador de inclusión escrito por el usuario.</span><span class="sxs-lookup"><span data-stu-id="40109-122">An optional pointer to a user-written include handler.</span></span> <span data-ttu-id="40109-123">El procesador llama al controlador cada vez que necesita resolver un \# include.</span><span class="sxs-lookup"><span data-stu-id="40109-123">The handler is called by the processor whenever it needs to resolve a \#include.</span></span>
-   <span data-ttu-id="40109-124">Una marca de compilación del sombreador que proporciona sugerencias del compilador sobre cómo se utilizará el sombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-124">A shader compile flag that gives the compiler hints about how the shader will be used.</span></span> <span data-ttu-id="40109-125">Entre estas opciones se incluyen:</span><span class="sxs-lookup"><span data-stu-id="40109-125">The options include:</span></span>
    -   <span data-ttu-id="40109-126">Omitiendo la validación, si se están compilando sombreadores buenos conocidos.</span><span class="sxs-lookup"><span data-stu-id="40109-126">Skipping validation, if known good shaders are being compiled.</span></span>
    -   <span data-ttu-id="40109-127">Omitiendo la optimización (a veces se usa cuando las optimizaciones dificultan la depuración).</span><span class="sxs-lookup"><span data-stu-id="40109-127">Skipping optimization (sometimes used when optimizations make debugging harder).</span></span>
    -   <span data-ttu-id="40109-128">Solicitar la información de depuración que se va a incluir en el sombreador para que se pueda depurar.</span><span class="sxs-lookup"><span data-stu-id="40109-128">Requesting debug information to be included in the shader so it can be debugged.</span></span>
-   <span data-ttu-id="40109-129">Grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="40109-129">The effect pool.</span></span> <span data-ttu-id="40109-130">Si más de un efecto utiliza el mismo puntero de bloque de memoria, las variables globales de los efectos se comparten entre sí.</span><span class="sxs-lookup"><span data-stu-id="40109-130">If more than one effect uses the same memory pool pointer, the global variables in the effects are shared with each other.</span></span> <span data-ttu-id="40109-131">Si no es necesario compartir las variables de efecto, el bloque de memoria se puede establecer en **null**.</span><span class="sxs-lookup"><span data-stu-id="40109-131">If there is no need to share effect variables, the memory pool can be set to **NULL**.</span></span>
-   <span data-ttu-id="40109-132">Puntero al nuevo efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-132">A pointer to the new effect.</span></span>
-   <span data-ttu-id="40109-133">Un puntero a un búfer al que se pueden enviar los errores de validación.</span><span class="sxs-lookup"><span data-stu-id="40109-133">A pointer to a buffer to which validation errors can be sent.</span></span> <span data-ttu-id="40109-134">En este ejemplo, el parámetro se ha establecido en **null** y no se ha usado.</span><span class="sxs-lookup"><span data-stu-id="40109-134">In this example, the parameter was set to **NULL** and not used.</span></span>

> [!Note]  
> <span data-ttu-id="40109-135">A partir del SDK de diciembre de 2006, el compilador de HLSL de DirectX 10 es ahora el compilador predeterminado en DirectX 9 y DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="40109-135">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="40109-136">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="40109-136">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

 

## <a name="render-an-effect"></a><span data-ttu-id="40109-137">Representar un efecto</span><span class="sxs-lookup"><span data-stu-id="40109-137">Render an Effect</span></span>

<span data-ttu-id="40109-138">La secuencia de llamadas para aplicar el estado de efectos a un dispositivo es:</span><span class="sxs-lookup"><span data-stu-id="40109-138">The sequence of calls for applying effect state to a device is:</span></span>

-   <span data-ttu-id="40109-139">[**ID3DXEffect:: Begin**](id3dxeffect--begin.md) establece la técnica activa.</span><span class="sxs-lookup"><span data-stu-id="40109-139">[**ID3DXEffect::Begin**](id3dxeffect--begin.md) sets the active technique.</span></span>
-   <span data-ttu-id="40109-140">[**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) establece el paso activo.</span><span class="sxs-lookup"><span data-stu-id="40109-140">[**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) sets the active pass.</span></span>
-   <span data-ttu-id="40109-141">[**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md) actualiza los cambios en cualquier llamada establecida en el paso.</span><span class="sxs-lookup"><span data-stu-id="40109-141">[**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) updates changes to any set calls in the pass.</span></span> <span data-ttu-id="40109-142">Se debe llamar a este método antes de cualquier llamada a Draw.</span><span class="sxs-lookup"><span data-stu-id="40109-142">This should be called before any draw call.</span></span>
-   <span data-ttu-id="40109-143">[**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) finaliza un paso.</span><span class="sxs-lookup"><span data-stu-id="40109-143">[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) ends a pass.</span></span>
-   <span data-ttu-id="40109-144">[**ID3DXEffect:: end**](id3dxeffect--end.md) finaliza la técnica activa.</span><span class="sxs-lookup"><span data-stu-id="40109-144">[**ID3DXEffect::End**](id3dxeffect--end.md) ends the active technique.</span></span>

<span data-ttu-id="40109-145">El código de representación del efecto también es más sencillo que el código de representación correspondiente sin ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-145">Effect render code is also simpler than the corresponding render code without an effect.</span></span> <span data-ttu-id="40109-146">Este es el código de representación con un efecto:</span><span class="sxs-lookup"><span data-stu-id="40109-146">Here's the render code with an effect:</span></span>


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



<span data-ttu-id="40109-147">El bucle de representación consiste en consultar el efecto para ver cuántas pasadas contiene y, a continuación, llamar a todas las pasadas para una técnica.</span><span class="sxs-lookup"><span data-stu-id="40109-147">The render loop consists of querying the effect to see how many passes it contains, and then calling all the passes for a technique.</span></span> <span data-ttu-id="40109-148">El bucle de representación se puede expandir para llamar a varias técnicas, cada una con varias fases.</span><span class="sxs-lookup"><span data-stu-id="40109-148">The render loop could be expanded to call multiple techniques, each with multiple passes.</span></span>

## <a name="use-semantics-to-find-effect-parameters"></a><span data-ttu-id="40109-149">Usar la semántica para buscar parámetros de efectos</span><span class="sxs-lookup"><span data-stu-id="40109-149">Use Semantics to Find Effect Parameters</span></span>

<span data-ttu-id="40109-150">Una semántica es un identificador que se adjunta a un parámetro de efecto para permitir que una aplicación busque el parámetro.</span><span class="sxs-lookup"><span data-stu-id="40109-150">A semantic is an identifier that is attached to an effect parameter to allow an application to search for the parameter.</span></span> <span data-ttu-id="40109-151">Un parámetro puede tener como máximo una semántica.</span><span class="sxs-lookup"><span data-stu-id="40109-151">A parameter can have at most one semantic.</span></span> <span data-ttu-id="40109-152">La semántica se encuentra después de dos puntos (:) después del nombre del parámetro.</span><span class="sxs-lookup"><span data-stu-id="40109-152">The semantic is located following a colon (:) after the parameter name.</span></span> <span data-ttu-id="40109-153">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="40109-153">For instance:</span></span>


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



<span data-ttu-id="40109-154">Si ha declarado la variable global de efecto sin usar una semántica, tendría un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="40109-154">If you declared the effect global variable without using a semantic, it would look like this instead:</span></span>


```
float4x4 matWorldViewProj;
```



<span data-ttu-id="40109-155">La interfaz de efecto puede usar una semántica para obtener un identificador de un parámetro de efecto determinado.</span><span class="sxs-lookup"><span data-stu-id="40109-155">The effect interface can use a semantic to get a handle to a particular effect parameter.</span></span> <span data-ttu-id="40109-156">Por ejemplo, lo siguiente devuelve el identificador de la matriz:</span><span class="sxs-lookup"><span data-stu-id="40109-156">For instance, the following returns the handle of the matrix:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



<span data-ttu-id="40109-157">Además de buscar por nombre semántico, la interfaz de efecto tiene muchos otros métodos para buscar parámetros.</span><span class="sxs-lookup"><span data-stu-id="40109-157">In addition to searching by semantic name, the effect interface has many other methods to search for parameters.</span></span>

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a><span data-ttu-id="40109-158">Usar los controladores para obtener y establecer los parámetros de forma eficaz</span><span class="sxs-lookup"><span data-stu-id="40109-158">Use Handles to Get and Set Parameters Efficiently</span></span>

<span data-ttu-id="40109-159">Los identificadores proporcionan un medio eficaz para hacer referencia a parámetros de efectos, técnicas, pasadas y anotaciones con un efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-159">Handles provide an efficient means for referencing effect parameters, techniques, passes, and annotations with an effect.</span></span> <span data-ttu-id="40109-160">Los identificadores (que son de tipo D3DXHANDLE) son punteros de cadena.</span><span class="sxs-lookup"><span data-stu-id="40109-160">Handles (which are of type D3DXHANDLE) are string pointers.</span></span> <span data-ttu-id="40109-161">Los identificadores que se pasan a funciones como GetParameterxxx o GetAnnotationxxx pueden tener una de las tres formas siguientes:</span><span class="sxs-lookup"><span data-stu-id="40109-161">The handles that are passed into functions such as GetParameterxxx or GetAnnotationxxx can be in one of three forms:</span></span>

-   <span data-ttu-id="40109-162">Identificador devuelto por una función como GetParameterxxx.</span><span class="sxs-lookup"><span data-stu-id="40109-162">A handle returned by a function such as GetParameterxxx.</span></span>
-   <span data-ttu-id="40109-163">Cadena que contiene el nombre del parámetro, la técnica, la fase o la anotación.</span><span class="sxs-lookup"><span data-stu-id="40109-163">A string containing the name of the parameter, technique, pass, or annotation.</span></span>
-   <span data-ttu-id="40109-164">Identificador establecido en **null**.</span><span class="sxs-lookup"><span data-stu-id="40109-164">A handle set to **NULL**.</span></span>

<span data-ttu-id="40109-165">Este ejemplo devuelve un identificador al parámetro que tiene la semántica WORLDVIEWPROJ asociada:</span><span class="sxs-lookup"><span data-stu-id="40109-165">This example returns a handle to the parameter that has the WORLDVIEWPROJ semantic attached to it:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a><span data-ttu-id="40109-166">Agregar información de parámetros con anotaciones</span><span class="sxs-lookup"><span data-stu-id="40109-166">Add Parameter Information with Annotations</span></span>

<span data-ttu-id="40109-167">Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro.</span><span class="sxs-lookup"><span data-stu-id="40109-167">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="40109-168">Una anotación es una forma flexible de agregar información a parámetros individuales.</span><span class="sxs-lookup"><span data-stu-id="40109-168">An annotation is a flexible way to add information to individual parameters.</span></span> <span data-ttu-id="40109-169">La información se puede volver a leer y usar de cualquier manera que la aplicación elija.</span><span class="sxs-lookup"><span data-stu-id="40109-169">The information can be read back and used any way the application chooses.</span></span> <span data-ttu-id="40109-170">Una anotación puede ser de cualquier tipo de datos y se puede agregar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="40109-170">An annotation can be of any data type and can be added dynamically.</span></span> <span data-ttu-id="40109-171">Las declaraciones de anotación se delimitan mediante corchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="40109-171">Annotation declarations are delimited by angle brackets.</span></span> <span data-ttu-id="40109-172">Una anotación contiene:</span><span class="sxs-lookup"><span data-stu-id="40109-172">An annotation contains:</span></span>

-   <span data-ttu-id="40109-173">Un tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="40109-173">A data type.</span></span>
-   <span data-ttu-id="40109-174">Un nombre de variable.</span><span class="sxs-lookup"><span data-stu-id="40109-174">A variable name.</span></span>
-   <span data-ttu-id="40109-175">Un signo igual (=).</span><span class="sxs-lookup"><span data-stu-id="40109-175">An equals sign (=).</span></span>
-   <span data-ttu-id="40109-176">Valor de datos.</span><span class="sxs-lookup"><span data-stu-id="40109-176">The data value.</span></span>
-   <span data-ttu-id="40109-177">Punto y coma final (;).</span><span class="sxs-lookup"><span data-stu-id="40109-177">A ending semicolon (;).</span></span>

<span data-ttu-id="40109-178">Por ejemplo, los dos ejemplos anteriores de este documento contienen esta anotación:</span><span class="sxs-lookup"><span data-stu-id="40109-178">For instance, both of the previous examples in this paper contain this annotation:</span></span>


```
texture Tex0 < string name = "tiger.bmp"; >;
```



<span data-ttu-id="40109-179">La anotación se adjunta al objeto Texture y especifica el archivo de textura que se debe usar para inicializar el objeto Texture.</span><span class="sxs-lookup"><span data-stu-id="40109-179">The annotation is attached to the texture object and specifies the texture file that should be used to initialize the texture object.</span></span> <span data-ttu-id="40109-180">La anotación no inicializa el objeto Texture, sino simplemente una parte de la información del usuario que se adjunta a la variable.</span><span class="sxs-lookup"><span data-stu-id="40109-180">The annotation does not initialize the texture object, it is simply a piece of user information that is attached to the variable.</span></span> <span data-ttu-id="40109-181">Una aplicación puede leer la anotación con [**ID3DXBaseEffect:: GetAnnotation**](id3dxbaseeffect--getannotation.md) o [**ID3DXBaseEffect:: GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) para devolver la cadena.</span><span class="sxs-lookup"><span data-stu-id="40109-181">An application can read the annotation with either [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) or [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) to return the string.</span></span> <span data-ttu-id="40109-182">La aplicación también puede agregar anotaciones.</span><span class="sxs-lookup"><span data-stu-id="40109-182">Annotations can also be added by the application.</span></span>

<span data-ttu-id="40109-183">Cada anotación:</span><span class="sxs-lookup"><span data-stu-id="40109-183">Each annotation:</span></span>

-   <span data-ttu-id="40109-184">Debe ser un valor numérico o cadenas.</span><span class="sxs-lookup"><span data-stu-id="40109-184">Must be either numeric or strings.</span></span>
-   <span data-ttu-id="40109-185">Siempre se debe inicializar con un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="40109-185">Must always be initialized with a default value.</span></span>
-   <span data-ttu-id="40109-186">Se puede asociar a [técnicas y pases (Direct3D 9)](techniques-and-passes.md) y [parámetros de efecto](/previous-versions/windows/desktop/ee417539(v=vs.85))de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="40109-186">Can be associated with [Techniques and Passes (Direct3D 9)](techniques-and-passes.md) and top-level [Effect Parameters](/previous-versions/windows/desktop/ee417539(v=vs.85)).</span></span>
-   <span data-ttu-id="40109-187">Se puede escribir y leer desde con [**ID3DXEffect**](id3dxeffect.md) o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="40109-187">Can be written to and read from with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>
-   <span data-ttu-id="40109-188">Se puede Agregar con [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="40109-188">Can be added with [**ID3DXEffect**](id3dxeffect.md).</span></span>
-   <span data-ttu-id="40109-189">No se puede hacer referencia dentro del efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-189">Cannot be referenced inside the effect.</span></span>
-   <span data-ttu-id="40109-190">No puede tener subexpresiones o subestados.</span><span class="sxs-lookup"><span data-stu-id="40109-190">Cannot have sub-semantics or sub-annotations.</span></span>

## <a name="share-effect-parameters"></a><span data-ttu-id="40109-191">Parámetros de efectos compartidos</span><span class="sxs-lookup"><span data-stu-id="40109-191">Share Effect Parameters</span></span>

<span data-ttu-id="40109-192">Los parámetros de efecto son todas las variables no estáticas declaradas en un efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-192">Effect parameters are all the non-static variables declared in an effect.</span></span> <span data-ttu-id="40109-193">Esto puede incluir variables globales y anotaciones.</span><span class="sxs-lookup"><span data-stu-id="40109-193">This can include global variables and annotations.</span></span> <span data-ttu-id="40109-194">Los parámetros de efecto se pueden compartir entre distintos efectos declarando parámetros con la palabra clave "Shared" y creando después el efecto con un grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="40109-194">Effect parameters can be shared between different effects by declaring parameters with the "shared" keyword and then creating the effect with an effect pool.</span></span>

<span data-ttu-id="40109-195">Un grupo de efectos contiene parámetros de efectos compartidos.</span><span class="sxs-lookup"><span data-stu-id="40109-195">An effect pool contains shared effect parameters.</span></span> <span data-ttu-id="40109-196">El grupo se crea llamando a [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), que devuelve una interfaz [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="40109-196">The pool is created by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), which returns an [**ID3DXEffectPool**](id3dxeffectpool.md) interface.</span></span> <span data-ttu-id="40109-197">La interfaz se puede proporcionar como entrada a cualquiera de las funciones de D3DXCreateEffectxxx cuando se crea un efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-197">The interface can be supplied as an input to any of the D3DXCreateEffectxxx functions when an effect is created.</span></span> <span data-ttu-id="40109-198">Para que un parámetro se comparta entre varios efectos, el parámetro debe tener el mismo nombre, tipo y semántica en cada uno de los efectos compartidos.</span><span class="sxs-lookup"><span data-stu-id="40109-198">For a parameter to be shared across multiple effects, the parameter must have the same name, type, and semantic in each of the shared effects.</span></span>


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



<span data-ttu-id="40109-199">Los efectos que comparten parámetros deben usar el mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40109-199">Effects that share parameters must use the same device.</span></span> <span data-ttu-id="40109-200">Esto se aplica para impedir el uso compartido de parámetros dependientes del dispositivo (como sombreadores o texturas) en distintos dispositivos.</span><span class="sxs-lookup"><span data-stu-id="40109-200">This is enforced to prevent the sharing of device-dependent parameters (such as shaders or textures) across different devices.</span></span> <span data-ttu-id="40109-201">Los parámetros se eliminan del grupo cada vez que se liberan los efectos que contienen los parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="40109-201">Parameters are deleted from the pool whenever the effects that contain the shared parameters are released.</span></span> <span data-ttu-id="40109-202">Si los parámetros de uso compartido no son necesarios, proporcione **null** para el grupo de efectos cuando se cree un efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-202">If sharing parameters is not necessary, supply **NULL** for the effect pool when an effect is created.</span></span>

<span data-ttu-id="40109-203">Los efectos clonados usan el mismo grupo de efectos que el efecto desde el que se clonan.</span><span class="sxs-lookup"><span data-stu-id="40109-203">Cloned effects use the same effect pool as the effect from which they are cloned.</span></span> <span data-ttu-id="40109-204">La clonación de un efecto realiza una copia exacta de un efecto, incluidas las variables globales, las técnicas, las pasadas y las anotaciones.</span><span class="sxs-lookup"><span data-stu-id="40109-204">Cloning an effect makes an exact copy of an effect, including global variables, techniques, passes, and annotations.</span></span>

## <a name="compile-an-effect-offline"></a><span data-ttu-id="40109-205">Compilar un efecto sin conexión</span><span class="sxs-lookup"><span data-stu-id="40109-205">Compile an Effect Offline</span></span>

<span data-ttu-id="40109-206">Puede compilar un efecto en tiempo de ejecución con [**D3DXCreateEffect**](d3dxcreateeffect.md)o puede compilar un efecto sin conexión mediante la herramienta de compilador de línea de comandos fxc.exe.</span><span class="sxs-lookup"><span data-stu-id="40109-206">You can compile an effect at run time with [**D3DXCreateEffect**](d3dxcreateeffect.md), or you can compile an effect offline using the command-line compiler tool fxc.exe.</span></span> <span data-ttu-id="40109-207">El efecto en el [ejemplo CompiledEffect](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contiene un sombreador de vértices, un sombreador de píxeles y una técnica:</span><span class="sxs-lookup"><span data-stu-id="40109-207">The effect in the [CompiledEffect Sample](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contains a vertex shader, a pixel shader, and one technique:</span></span>


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



<span data-ttu-id="40109-208">El uso de la [herramienta de compilador de efectos](../direct3dtools/fxc.md) para compilar el sombreador de vs \_ 1 \_ 1 generó las siguientes instrucciones del sombreador de ensamblado:</span><span class="sxs-lookup"><span data-stu-id="40109-208">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generated the following assembly shader instructions:</span></span>


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a><span data-ttu-id="40109-209">Mejorar el rendimiento con los sombreadores</span><span class="sxs-lookup"><span data-stu-id="40109-209">Improve Performance with Preshaders</span></span>

<span data-ttu-id="40109-210">Un presombreador es una técnica para aumentar la eficacia del sombreador mediante el cálculo previo de expresiones de sombreador constantes.</span><span class="sxs-lookup"><span data-stu-id="40109-210">A preshader is a technique for increasing shader efficiency by pre-calculating constant shader expressions.</span></span> <span data-ttu-id="40109-211">El compilador de efectos extrae automáticamente los cálculos del sombreador del cuerpo de un sombreador y los ejecuta en la CPU antes de que se ejecute el sombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-211">The effect compiler automatically pulls out shader computations from the body of a shader and executes them on the CPU prior to the shader running.</span></span> <span data-ttu-id="40109-212">Por consiguiente, los presombreadores solo funcionan con efectos.</span><span class="sxs-lookup"><span data-stu-id="40109-212">Consequently, preshaders only work with effects.</span></span> <span data-ttu-id="40109-213">Por ejemplo, estas dos expresiones se pueden evaluar fuera del sombreador antes de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="40109-213">For instance, these two expressions can be evaluated outside of the shader before it runs.</span></span>


```
mul(World,mul(View, Projection));
sin(time)
```



<span data-ttu-id="40109-214">Los cálculos del sombreador que se pueden desplace son los asociados a los parámetros uniformes; es decir, los cálculos no cambian para cada vértice o píxel.</span><span class="sxs-lookup"><span data-stu-id="40109-214">Shader computations that can be moved are those associated with uniform parameters; that is, the computations do not change for each vertex or pixel.</span></span> <span data-ttu-id="40109-215">Si usa efectos, el compilador de efectos genera y ejecuta automáticamente un sombreador. no hay marcas para habilitar.</span><span class="sxs-lookup"><span data-stu-id="40109-215">If you are using effects, the effect compiler automatically generates and runs a preshader for you; there are no flags to enable.</span></span> <span data-ttu-id="40109-216">Los presombreadores pueden reducir el número de instrucciones por sombreador y también pueden reducir el número de registros constantes que utiliza un sombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-216">Preshaders can reduce the number of instructions per shader and can also reduce the number of constant registers a shader consumes.</span></span>

<span data-ttu-id="40109-217">Piense en el compilador de efectos como una especie de compilador de varios procesadores porque compila código de sombreador para dos tipos de procesadores: una CPU y una GPU.</span><span class="sxs-lookup"><span data-stu-id="40109-217">Think of the effect compiler as a sort of multi-processor compiler because it compiles shader code for two types of processors: a CPU and a GPU.</span></span> <span data-ttu-id="40109-218">Además, el compilador de efectos está diseñado para trasladar el código de la GPU a la CPU y, por tanto, mejorar el rendimiento del sombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-218">In addition, the effect compiler is designed to move code from the GPU to the CPU and therefore improve shader performance.</span></span> <span data-ttu-id="40109-219">Esto es muy similar a la extracción de una expresión estática fuera de un bucle.</span><span class="sxs-lookup"><span data-stu-id="40109-219">This is very similar to pulling a static expression out of a loop.</span></span> <span data-ttu-id="40109-220">Sombreador que transforma la posición del espacio universal en el espacio de proyección y copia las coordenadas de textura con el siguiente aspecto en HLSL:</span><span class="sxs-lookup"><span data-stu-id="40109-220">A shader that transforms position from world space to projection space, and copies texture coordinates would look like this in HLSL:</span></span>


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



<span data-ttu-id="40109-221">El uso de la [herramienta de compilador de efectos](../direct3dtools/fxc.md) para compilar el sombreador de vs \_ 1 \_ 1 genera las siguientes instrucciones de ensamblado:</span><span class="sxs-lookup"><span data-stu-id="40109-221">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generates the following assembly instructions:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="40109-222">Esto usa 14 ranuras aproximadamente y consume 9 registros constantes.</span><span class="sxs-lookup"><span data-stu-id="40109-222">This uses up approximately 14 slots and consumes 9 constant registers.</span></span> <span data-ttu-id="40109-223">Con un presombreador, el compilador mueve las expresiones estáticas fuera del sombreador y al sombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-223">With a preshader, the compiler moves the static expressions out of the shader and into the preshader.</span></span> <span data-ttu-id="40109-224">El mismo sombreador tendría un aspecto similar al siguiente con un sombreador:</span><span class="sxs-lookup"><span data-stu-id="40109-224">The same shader would look like this with a preshader:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="40109-225">Un efecto ejecuta un sombreador inmediatamente antes de ejecutar un sombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-225">An effect executes a preshader just before executing a shader.</span></span> <span data-ttu-id="40109-226">El resultado es la misma funcionalidad con mayor rendimiento del sombreador, ya que se ha reducido el número de instrucciones que es necesario ejecutar (para cada vértice o píxel según el tipo de sombreador).</span><span class="sxs-lookup"><span data-stu-id="40109-226">The result is the same functionality with increased shader performance because the number of instructions that need to be executed (for each vertex or pixel depending on the type of shader) has been reduced.</span></span> <span data-ttu-id="40109-227">Además, el sombreador consume menos registros constantes como resultado de las expresiones estáticas que se mueven al presombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-227">In addition, fewer constant registers are consumed by the shader as a result of the static expressions being moved to the preshader.</span></span> <span data-ttu-id="40109-228">Esto significa que los sombreadores previamente limitados por el número de registros constantes que requieren ahora pueden compilarse porque requieren menos registros constantes.</span><span class="sxs-lookup"><span data-stu-id="40109-228">This means that shaders previously limited by the number of constant registers they required may now compile because they require fewer constant registers.</span></span> <span data-ttu-id="40109-229">Es razonable esperar una mejora del rendimiento del 5 por ciento y del 20 por ciento de los sombreadores.</span><span class="sxs-lookup"><span data-stu-id="40109-229">It is reasonable to expect a 5 percent and a 20 percent performance improvement from preshaders.</span></span>

<span data-ttu-id="40109-230">Tenga en cuenta que las constantes de entrada son diferentes de las constantes de salida en un sombreador.</span><span class="sxs-lookup"><span data-stu-id="40109-230">Keep in mind that the input constants are different from the output constants in a preshader.</span></span> <span data-ttu-id="40109-231">El resultado C1 no es el mismo que el registro C1 de entrada.</span><span class="sxs-lookup"><span data-stu-id="40109-231">The output c1 is not the same as the input c1 register.</span></span> <span data-ttu-id="40109-232">La escritura en un registro constante en un sombreador escribe realmente en la ranura de entrada (constante) del sombreador correspondiente.</span><span class="sxs-lookup"><span data-stu-id="40109-232">Writing to a constant register in a preshader actually writes into the corresponding shader's input (constant) slot.</span></span>


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



<span data-ttu-id="40109-233">La instrucción de CMP anterior leerá el valor C1 del presombreador, mientras que la instrucción mul escribirá en los registros del sombreador de hardware para que los use el sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="40109-233">The cmp instruction above will read the preshader c1 value, while the mul instruction will write to the hardware shader registers to be used by the vertex shader.</span></span>

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a><span data-ttu-id="40109-234">Usar bloques de parámetros para administrar parámetros de efectos</span><span class="sxs-lookup"><span data-stu-id="40109-234">Use Parameter Blocks to Manage Effect Parameters</span></span>

<span data-ttu-id="40109-235">Los bloques de parámetros son bloques de cambios de estado de efecto.</span><span class="sxs-lookup"><span data-stu-id="40109-235">Parameter blocks are blocks of effect state changes.</span></span> <span data-ttu-id="40109-236">Un bloque de parámetros puede registrar cambios de estado, de modo que se puedan aplicar más adelante con una sola llamada.</span><span class="sxs-lookup"><span data-stu-id="40109-236">A parameter block can record state changes, so that they can be applied later on with a single call.</span></span> <span data-ttu-id="40109-237">Cree un bloque de parámetros mediante una llamada a [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span><span class="sxs-lookup"><span data-stu-id="40109-237">Create a parameter block by calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span></span>


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



<span data-ttu-id="40109-238">El bloque de parámetros guarda cuatro cambios aplicados por las llamadas a la API.</span><span class="sxs-lookup"><span data-stu-id="40109-238">The parameter block saves four changes applied by the API calls.</span></span> <span data-ttu-id="40109-239">La llamada a [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md) inicia la grabación de los cambios de estado.</span><span class="sxs-lookup"><span data-stu-id="40109-239">Calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) starts recording the state changes.</span></span> <span data-ttu-id="40109-240">[**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md) deja de agregar los cambios al bloque de parámetros y devuelve un identificador.</span><span class="sxs-lookup"><span data-stu-id="40109-240">[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md) stops adding the changes to the parameter block and returns a handle.</span></span> <span data-ttu-id="40109-241">El identificador se usará al llamar a [**ID3DXEffect:: ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="40109-241">The handle will be used when calling [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span></span>

<span data-ttu-id="40109-242">En el [ejemplo EffectParam](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), el bloque de parámetros se aplica en la secuencia de representación:</span><span class="sxs-lookup"><span data-stu-id="40109-242">In the [EffectParam Sample](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), the parameter block is applied in the render sequence:</span></span>


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



<span data-ttu-id="40109-243">El bloque de parámetros establece el valor de los cuatro cambios de Estado justo antes de que se llame a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) .</span><span class="sxs-lookup"><span data-stu-id="40109-243">The parameter block sets the value of all four of the state changes just before [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called.</span></span> <span data-ttu-id="40109-244">Los bloques de parámetros son una forma cómoda de establecer varios cambios de estado con una única llamada API.</span><span class="sxs-lookup"><span data-stu-id="40109-244">Parameter blocks are a handy way to set multiple state changes with a single API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40109-245">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="40109-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40109-246">Efectos</span><span class="sxs-lookup"><span data-stu-id="40109-246">Effects</span></span>](effects.md)
</dt> </dl>

 

 
