---
description: Una vez creado un efecto, el primer paso consiste en compilar el código para comprobar si hay problemas de sintaxis.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compilación de un efecto (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274890"
---
# <a name="compile-an-effect-direct3d-10"></a><span data-ttu-id="0cdce-103">Compilación de un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0cdce-103">Compile an Effect (Direct3D 10)</span></span>

<span data-ttu-id="0cdce-104">Una vez creado un efecto, el primer paso consiste en compilar el código para comprobar si hay problemas de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="0cdce-104">Once an effect has been authored, the first step is to compile the code to check for syntax problems.</span></span> <span data-ttu-id="0cdce-105">Esto se hace mediante una llamada a una de las API de compilación (como D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span><span class="sxs-lookup"><span data-stu-id="0cdce-105">This is done by calling one of the compile APIs (like D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span></span> <span data-ttu-id="0cdce-106">Estas API invocan el compilador de efecto fxc.exe que es el compilador que se usa para compilar código HLSL.</span><span class="sxs-lookup"><span data-stu-id="0cdce-106">These API's invoke the effect compiler fxc.exe which is the compiler used to compile HLSL code.</span></span> <span data-ttu-id="0cdce-107">Este es el motivo por el que la sintaxis del código de un efecto es muy similar a la del código HLSL (hay algunas excepciones que se tratarán más adelante).</span><span class="sxs-lookup"><span data-stu-id="0cdce-107">This is why the syntax for code in an effect looks very much like HLSL code (there are a few exceptions that will be handled later).</span></span> <span data-ttu-id="0cdce-108">Por la forma, el compilador de efectos compilador/HLSL (fxc.exe) está en el SDK de la carpeta Utilities para que pueda compilar los sombreadores (o efectos) sin conexión si lo desea.</span><span class="sxs-lookup"><span data-stu-id="0cdce-108">By the way, the effect compiler/hlsl compiler (fxc.exe) is in the SDK in the utilities folder so that you can compile your shaders (or effects) offline if you choose.</span></span> <span data-ttu-id="0cdce-109">Consulte la documentación para ejecutar el compilador desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="0cdce-109">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="0cdce-110">Presenta</span><span class="sxs-lookup"><span data-stu-id="0cdce-110">Includes</span></span>](#includes)
-   [<span data-ttu-id="0cdce-111">Macros</span><span class="sxs-lookup"><span data-stu-id="0cdce-111">Macros</span></span>](#macros)
-   [<span data-ttu-id="0cdce-112">Marcas de sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="0cdce-112">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="0cdce-113">Marcas FX</span><span class="sxs-lookup"><span data-stu-id="0cdce-113">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="0cdce-114">Comprobar errores</span><span class="sxs-lookup"><span data-stu-id="0cdce-114">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="0cdce-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0cdce-115">Related topics</span></span>](#related-topics)

<span data-ttu-id="0cdce-116">A continuación se muestra un ejemplo de cómo compilar un archivo de efectos (desde el ejemplo BasicHLSL10).</span><span class="sxs-lookup"><span data-stu-id="0cdce-116">Here's an example of compiling an effect file (from the BasicHLSL10 sample).</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a><span data-ttu-id="0cdce-117">Includes</span><span class="sxs-lookup"><span data-stu-id="0cdce-117">Includes</span></span>

<span data-ttu-id="0cdce-118">Un parámetro es una interfaz include.</span><span class="sxs-lookup"><span data-stu-id="0cdce-118">One parameter is an include interface.</span></span> <span data-ttu-id="0cdce-119">Genere uno de estos si desea incluir un comportamiento personalizado al leer un archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="0cdce-119">Generate one of these if you want to include a customized behavior when reading an include file.</span></span> <span data-ttu-id="0cdce-120">Este comportamiento personalizado se ejecuta cada vez que se crea un efecto (que usa el puntero include) o cuando se compila un efecto (que usa el puntero include).</span><span class="sxs-lookup"><span data-stu-id="0cdce-120">This custom behavior is executed each time an effect (that uses the include pointer) is created or when an effect (that uses the include pointer) is compiled.</span></span> <span data-ttu-id="0cdce-121">Para implementar el comportamiento de inclusión personalizado, derive una clase de la interfaz include.</span><span class="sxs-lookup"><span data-stu-id="0cdce-121">To implement customized include behavior, derive a class from the Include interface.</span></span> <span data-ttu-id="0cdce-122">Esto proporciona a los dos métodos de la clase: abrir y cerrar.</span><span class="sxs-lookup"><span data-stu-id="0cdce-122">This provides your class two methods: Open and Close.</span></span> <span data-ttu-id="0cdce-123">Implemente el comportamiento personalizado en los métodos de apertura y cierre.</span><span class="sxs-lookup"><span data-stu-id="0cdce-123">Implement the custom behavior in the Open and Close methods.</span></span>

## <a name="macros"></a><span data-ttu-id="0cdce-124">Macros</span><span class="sxs-lookup"><span data-stu-id="0cdce-124">Macros</span></span>

<span data-ttu-id="0cdce-125">La compilación del efecto también puede tomar un puntero a las macros que se definen en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="0cdce-125">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="0cdce-126">Por ejemplo, supongamos que va a modificar el efecto en BasicHLSL10 para usar dos macros: cero y uno.</span><span class="sxs-lookup"><span data-stu-id="0cdce-126">For example, suppose you were to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="0cdce-127">Aquí se muestra el código de efecto que usa las dos macros.</span><span class="sxs-lookup"><span data-stu-id="0cdce-127">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="0cdce-128">Esta es la declaración de las dos macros.</span><span class="sxs-lookup"><span data-stu-id="0cdce-128">Here is the declaration for the two macros.</span></span>


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="0cdce-129">Las macros son una matriz terminada en NULL de macros; donde cada macro se define con un struct de [**\_ \_ macros de sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="0cdce-129">The macros are a NULL terminated array of macros; where each macro is defined with a [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="0cdce-130">Por último, modifique la llamada al efecto compilar para que tome un puntero a las macros.</span><span class="sxs-lookup"><span data-stu-id="0cdce-130">Lastly, modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="0cdce-131">Marcas de sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="0cdce-131">HLSL Shader Flags</span></span>

<span data-ttu-id="0cdce-132">Las marcas del sombreador especifican las restricciones del sombreador en el compilador de HLSL.</span><span class="sxs-lookup"><span data-stu-id="0cdce-132">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="0cdce-133">Estas marcas afectan al código generado por el compilador del sombreador, incluidos:</span><span class="sxs-lookup"><span data-stu-id="0cdce-133">These flags impact the code generated by the shader compiler including:</span></span>

-   <span data-ttu-id="0cdce-134">Consideraciones de tamaño: optimice el código.</span><span class="sxs-lookup"><span data-stu-id="0cdce-134">Size considerations: optimize the code.</span></span>
-   <span data-ttu-id="0cdce-135">Consideraciones sobre depuración: incluir información de depuración, evitar el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="0cdce-135">Debug considerations: including debug information, preventing flow control.</span></span>
-   <span data-ttu-id="0cdce-136">Consideraciones de hardware: el destino de compilación y si un sombreador puede ejecutarse en hardware heredado.</span><span class="sxs-lookup"><span data-stu-id="0cdce-136">Hardware considerations: the compile target and whether or not a shader can run on legacy hardware.</span></span>

<span data-ttu-id="0cdce-137">En general, estas marcas se pueden combinar lógicamente, suponiendo que no se han especificado dos características conflictivas.</span><span class="sxs-lookup"><span data-stu-id="0cdce-137">In general, these flags can be logically combined, assuming you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="0cdce-138">Para obtener una lista de las marcas [, vea constantes de efecto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0cdce-138">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="0cdce-139">Marcas FX</span><span class="sxs-lookup"><span data-stu-id="0cdce-139">FX Flags</span></span>

<span data-ttu-id="0cdce-140">Estas marcas se usan al crear un efecto para definir el comportamiento de la compilación o del efecto en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="0cdce-140">These flags used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="0cdce-141">Para obtener una lista de las marcas [, vea constantes de efecto (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="0cdce-141">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="0cdce-142">Comprobar errores</span><span class="sxs-lookup"><span data-stu-id="0cdce-142">Checking Errors</span></span>

<span data-ttu-id="0cdce-143">Si durante la compilación se produce un error, la API devuelve una interfaz que contiene los errores devueltos por el compilador de efectos.</span><span class="sxs-lookup"><span data-stu-id="0cdce-143">If during compilation, an error occurs, the API returns an interface which contains the errors returned from the effect compiler.</span></span> <span data-ttu-id="0cdce-144">Esta interfaz se denomina ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="0cdce-144">This interface is called ID3D10Blob.</span></span> <span data-ttu-id="0cdce-145">Sin embargo, no se puede leer directamente; si se devuelve un puntero al búfer que contiene los datos (que es una cadena), se pueden ver los errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="0cdce-145">It is not directly readable, however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="0cdce-146">En este ejemplo, se ha introducido un error en el efecto BasicHLSL. FX mediante la copia de la primera declaración de variable dos veces.</span><span class="sxs-lookup"><span data-stu-id="0cdce-146">In this example, an error was introduced into the BasicHLSL.fx effect by copying the first variable declaration twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="0cdce-147">Este error hizo que el compilador devolvera el siguiente error, como se muestra en la siguiente captura de pantalla de la ventana Inspección en Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0cdce-147">This error caused the compiler to return the following error, as shown in the following screen shot of the watch window in Microsoft Visual Studio.</span></span>

![captura de pantalla de la ventana Inspección de Visual Studio](images/effect-compile-errors-2.jpg)

<span data-ttu-id="0cdce-149&quot;>Dado que el error se devuelve en un puntero LPVOID, conviértalo en una cadena de caracteres en la ventana Inspección.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;0cdce-149&quot;>Since the error is returned in a LPVOID pointer, cast it to a character string in the watch window.</span></span>

<span data-ttu-id=&quot;0cdce-150&quot;>Este es el código que se usa para devolver el error de la compilación con errores.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;0cdce-150&quot;>Here is the code used to return the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L&quot;BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="0cdce-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0cdce-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cdce-152">Representar un efecto (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0cdce-152">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



