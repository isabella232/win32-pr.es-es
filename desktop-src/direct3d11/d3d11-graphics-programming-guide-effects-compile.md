---
title: Compilar un efecto (Direct3D 11)
description: Una vez creado un efecto, el paso siguiente consiste en compilar el código para comprobar si hay problemas de sintaxis.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995372"
---
# <a name="compile-an-effect-direct3d-11"></a><span data-ttu-id="d74fc-103">Compilar un efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d74fc-103">Compile an Effect (Direct3D 11)</span></span>

<span data-ttu-id="d74fc-104">Una vez creado un efecto, el paso siguiente consiste en compilar el código para comprobar si hay problemas de sintaxis.</span><span class="sxs-lookup"><span data-stu-id="d74fc-104">After an effect has been authored, the next step is to compile the code to check for syntax problems.</span></span>

<span data-ttu-id="d74fc-105">Para ello, llame a una de las API de compilación ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)o [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span><span class="sxs-lookup"><span data-stu-id="d74fc-105">You do so by calling one of the compile APIs ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md), or [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span></span> <span data-ttu-id="d74fc-106">Estas API invocan el efecto compilador fxc.exe, que compila el código HLSL.</span><span class="sxs-lookup"><span data-stu-id="d74fc-106">These APIs invoke the effect compiler fxc.exe, which compiles HLSL code.</span></span> <span data-ttu-id="d74fc-107">Este es el motivo por el que la sintaxis del código de un efecto es muy parecida a la del código HLSL.</span><span class="sxs-lookup"><span data-stu-id="d74fc-107">This is why the syntax for code in an effect looks very much like HLSL code.</span></span> <span data-ttu-id="d74fc-108">(Hay algunas excepciones que se tratarán más adelante).</span><span class="sxs-lookup"><span data-stu-id="d74fc-108">(There are a few exceptions that will be handled later).</span></span> <span data-ttu-id="d74fc-109">El compilador de efecto compilador o HLSL, fxc.exe, está disponible en el SDK en la carpeta Utilities para que los sombreadores (o efectos) se puedan compilar sin conexión si así lo desea.</span><span class="sxs-lookup"><span data-stu-id="d74fc-109">The effect compiler/hlsl compiler, fxc.exe, is available in the SDK in the utilities folder so that shaders (or effects) can be compiled offline if you choose.</span></span> <span data-ttu-id="d74fc-110">Consulte la documentación para ejecutar el compilador desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="d74fc-110">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="d74fc-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d74fc-111">Example</span></span>](#example)
-   [<span data-ttu-id="d74fc-112">Presenta</span><span class="sxs-lookup"><span data-stu-id="d74fc-112">Includes</span></span>](#includes)
-   [<span data-ttu-id="d74fc-113">Buscar archivos de inclusión</span><span class="sxs-lookup"><span data-stu-id="d74fc-113">Searching for Include Files</span></span>](#searching-for-include-files)
-   [<span data-ttu-id="d74fc-114">Macros</span><span class="sxs-lookup"><span data-stu-id="d74fc-114">Macros</span></span>](#macros)
-   [<span data-ttu-id="d74fc-115">Marcas de sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="d74fc-115">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="d74fc-116">Marcas FX</span><span class="sxs-lookup"><span data-stu-id="d74fc-116">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="d74fc-117">Comprobar errores</span><span class="sxs-lookup"><span data-stu-id="d74fc-117">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="d74fc-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d74fc-118">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="d74fc-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d74fc-119">Example</span></span>

<span data-ttu-id="d74fc-120">A continuación se muestra un ejemplo de cómo compilar un archivo de efectos.</span><span class="sxs-lookup"><span data-stu-id="d74fc-120">Here's an example of compiling an effect file.</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a><span data-ttu-id="d74fc-121">Includes</span><span class="sxs-lookup"><span data-stu-id="d74fc-121">Includes</span></span>

<span data-ttu-id="d74fc-122">Un parámetro de las API de compilación es una interfaz de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d74fc-122">One parameter of the compile APIs is an include interface.</span></span> <span data-ttu-id="d74fc-123">Genere uno de estos si desea incluir un comportamiento personalizado cuando el compilador lea un archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="d74fc-123">Generate one of these if you want to include a customized behavior when the compiler reads an include file.</span></span> <span data-ttu-id="d74fc-124">El compilador ejecuta este comportamiento personalizado cada vez que crea o compila un efecto (que usa el puntero include).</span><span class="sxs-lookup"><span data-stu-id="d74fc-124">The compiler executes this custom behavior each time it creates or compiles an effect (that uses the include pointer).</span></span> <span data-ttu-id="d74fc-125">Para implementar el comportamiento de inclusión personalizado, derive una clase de la interfaz [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) .</span><span class="sxs-lookup"><span data-stu-id="d74fc-125">To implement customized include behavior, derive a class from the [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) interface.</span></span> <span data-ttu-id="d74fc-126">Esto proporciona a la clase dos métodos: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) y [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span><span class="sxs-lookup"><span data-stu-id="d74fc-126">This provides your class with two methods: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) and [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span></span> <span data-ttu-id="d74fc-127">Implemente el comportamiento personalizado en estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d74fc-127">Implement the custom behavior in these methods.</span></span>

## <a name="searching-for-include-files"></a><span data-ttu-id="d74fc-128">Buscar archivos de inclusión</span><span class="sxs-lookup"><span data-stu-id="d74fc-128">Searching for Include Files</span></span>

<span data-ttu-id="d74fc-129">El puntero que el compilador pasa en el parámetro *pParentData* al método [**abierto**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del controlador de inclusión podría no señalar al contenedor que incluye el \# archivo de inclusión que el compilador necesita para compilar el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d74fc-129">The pointer that the compiler passes in the *pParentData* parameter to your include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method might not point to the container that includes the \#include file that the compiler needs to compile your shader code.</span></span> <span data-ttu-id="d74fc-130">Es decir, el compilador podría pasar **null** en *pParentData*.</span><span class="sxs-lookup"><span data-stu-id="d74fc-130">That is, the compiler might pass **NULL** in *pParentData*.</span></span> <span data-ttu-id="d74fc-131">Por lo tanto, se recomienda que el controlador de inclusión busque en su propia lista de ubicaciones de inclusión para el contenido.</span><span class="sxs-lookup"><span data-stu-id="d74fc-131">Therefore, we recommend that your include handler search its own list of include locations for content.</span></span> <span data-ttu-id="d74fc-132">El controlador de inclusión puede agregar dinámicamente nuevas ubicaciones de inclusión al recibir esas ubicaciones en llamadas a su método **abierto** .</span><span class="sxs-lookup"><span data-stu-id="d74fc-132">Your include handler can dynamically add new include locations as it receives those locations in calls to its **Open** method.</span></span>

<span data-ttu-id="d74fc-133">En el ejemplo siguiente, suponga que los archivos de inclusión del código del sombreador se almacenan en el directorio *somewhereelse* .</span><span class="sxs-lookup"><span data-stu-id="d74fc-133">In the following example, suppose that the shader code's include files are both stored in the *somewhereelse* directory.</span></span> <span data-ttu-id="d74fc-134">Cuando el compilador llama al método [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) del controlador de inclusión para abrir y leer el contenido de *somewhereelse \\ foo. h*, el controlador de inclusión puede guardar la ubicación del directorio **somewhereelse** .</span><span class="sxs-lookup"><span data-stu-id="d74fc-134">When the compiler calls the include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method to open and read the contents of *somewhereelse\\foo.h*, the include handler can save the location of the **somewhereelse** directory.</span></span> <span data-ttu-id="d74fc-135">Más adelante, cuando el compilador llama al método **Open** del controlador de inclusión para abrir y leer el contenido de *bar. h*, el controlador de inclusión puede buscar automáticamente en el directorio *somewhereelse* de *bar. h*.</span><span class="sxs-lookup"><span data-stu-id="d74fc-135">Later, when the compiler calls the include handler's **Open** method to open and read the contents of *bar.h*, the include handler can automatically search in the *somewhereelse* directory for *bar.h*.</span></span>


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a><span data-ttu-id="d74fc-136">Macros</span><span class="sxs-lookup"><span data-stu-id="d74fc-136">Macros</span></span>

<span data-ttu-id="d74fc-137">La compilación del efecto también puede tomar un puntero a las macros que se definen en otro lugar.</span><span class="sxs-lookup"><span data-stu-id="d74fc-137">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="d74fc-138">Por ejemplo, supongamos que desea modificar el efecto en BasicHLSL10 para usar dos macros: cero y uno.</span><span class="sxs-lookup"><span data-stu-id="d74fc-138">For example, suppose you want to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="d74fc-139">Aquí se muestra el código de efecto que usa las dos macros.</span><span class="sxs-lookup"><span data-stu-id="d74fc-139">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="d74fc-140">Esta es la declaración de las dos macros.</span><span class="sxs-lookup"><span data-stu-id="d74fc-140">Here is the declaration for the two macros.</span></span>


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="d74fc-141">Las macros son una matriz terminada en NULL de macros; donde cada macro se define mediante un struct [**de \_ \_ macros de sombreador D3D10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="d74fc-141">The macros are a NULL-terminated array of macros; where each macro is defined by using a [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="d74fc-142">Modifique la llamada al efecto compilar para que tome un puntero a las macros.</span><span class="sxs-lookup"><span data-stu-id="d74fc-142">Modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="d74fc-143">Marcas de sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="d74fc-143">HLSL Shader Flags</span></span>

<span data-ttu-id="d74fc-144">Las marcas del sombreador especifican las restricciones del sombreador en el compilador de HLSL.</span><span class="sxs-lookup"><span data-stu-id="d74fc-144">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="d74fc-145">Estas marcas afectan al código generado por el compilador del sombreador de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="d74fc-145">These flags affect the code generated by the shader compiler in the following ways:</span></span>

-   <span data-ttu-id="d74fc-146">Optimizar el tamaño del código.</span><span class="sxs-lookup"><span data-stu-id="d74fc-146">Optimize the code size.</span></span>
-   <span data-ttu-id="d74fc-147">Incluye información de depuración, que impide el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="d74fc-147">Including debug information, which prevents flow control.</span></span>
-   <span data-ttu-id="d74fc-148">Afecta al destino de compilación y si un sombreador puede ejecutarse en hardware heredado.</span><span class="sxs-lookup"><span data-stu-id="d74fc-148">Affects the compile target and whether a shader can run on legacy hardware.</span></span>

<span data-ttu-id="d74fc-149">Estas marcas se pueden combinar lógicamente si no se han especificado dos características conflictivas.</span><span class="sxs-lookup"><span data-stu-id="d74fc-149">These flags can be logically combined if you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="d74fc-150">Para obtener una lista de las marcas, vea [D3D10 ( \_ constantes del sombreador](/windows/desktop/direct3d10/d3d10-shader)).</span><span class="sxs-lookup"><span data-stu-id="d74fc-150">For a listing of the flags see [D3D10\_SHADER Constants](/windows/desktop/direct3d10/d3d10-shader).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="d74fc-151">Marcas FX</span><span class="sxs-lookup"><span data-stu-id="d74fc-151">FX Flags</span></span>

<span data-ttu-id="d74fc-152">Use estas marcas cuando cree un efecto para definir el comportamiento de la compilación o del efecto en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="d74fc-152">Use these flags when you create an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="d74fc-153">Para obtener una lista de las marcas, consulte [ \_ constantes Effect D3D10](/windows/desktop/direct3d10/d3d10-effect).</span><span class="sxs-lookup"><span data-stu-id="d74fc-153">For a listing of the flags see [D3D10\_EFFECT Constants](/windows/desktop/direct3d10/d3d10-effect).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="d74fc-154">Comprobar errores</span><span class="sxs-lookup"><span data-stu-id="d74fc-154">Checking Errors</span></span>

<span data-ttu-id="d74fc-155">Si durante la compilación se produce un error, la API devuelve una interfaz que contiene los errores del compilador de efectos.</span><span class="sxs-lookup"><span data-stu-id="d74fc-155">If during compilation an error occurs, the API returns an interface that contains the errors from the effect compiler.</span></span> <span data-ttu-id="d74fc-156">Esta interfaz se denomina [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d74fc-156">This interface is called [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span></span> <span data-ttu-id="d74fc-157">No se puede leer directamente; sin embargo, al devolver un puntero al búfer que contiene los datos (que es una cadena), puede ver los errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="d74fc-157">It is not directly readable; however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="d74fc-158">Este ejemplo contiene un error en BasicHLSL. FX, la primera declaración de variable aparece dos veces.</span><span class="sxs-lookup"><span data-stu-id="d74fc-158">This example contains an error in the BasicHLSL.fx, the first variable declaration occurs twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="d74fc-159">Este error hace que el compilador devuelva el siguiente error, como se muestra en la siguiente captura de pantalla del ventana Inspección en Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d74fc-159">This error causes the compiler to return the following error, as shown in the following screen shot of the Watch window in Microsoft Visual Studio.</span></span>

![captura de pantalla de la ventana Inspección de Visual Studio con un error 0x01997fb8](images/effect-compile-errors-2.jpg)

<span data-ttu-id="d74fc-161">Dado que el compilador devuelve el error en un puntero LPVOID, conviértalo en una cadena de caracteres en el ventana Inspección.</span><span class="sxs-lookup"><span data-stu-id="d74fc-161">Because the compiler returns the error in a LPVOID pointer, cast it to a character string in the Watch window.</span></span>

<span data-ttu-id="d74fc-162">Este es el código que devuelve el error de la compilación con errores.</span><span class="sxs-lookup"><span data-stu-id="d74fc-162">Here is the code that returns the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="d74fc-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d74fc-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d74fc-164">Representar un efecto (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="d74fc-164">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 