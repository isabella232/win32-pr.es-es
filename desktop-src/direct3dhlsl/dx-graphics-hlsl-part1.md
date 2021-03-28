---
title: Compilación de sombreadores
description: Echemos un vistazo a las distintas formas de compilar el código del sombreador y las convenciones para las extensiones de archivo para el código del sombreador.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359104"
---
# <a name="compiling-shaders"></a><span data-ttu-id="4821e-103">Compilar sombreadores</span><span class="sxs-lookup"><span data-stu-id="4821e-103">Compiling shaders</span></span>

> [!NOTE]
> <span data-ttu-id="4821e-104">En este tema se trata el `FXC.EXE` compilador que se usa para los modelos de sombreador del 2 al 5,1.</span><span class="sxs-lookup"><span data-stu-id="4821e-104">This topic covers the `FXC.EXE` compiler used for Shader Models 2 through 5.1.</span></span> <span data-ttu-id="4821e-105">En el modelo de sombreador 6, se usa en `DXC.EXE` su lugar, que se documenta en [uso de dxc.exe y dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span><span class="sxs-lookup"><span data-stu-id="4821e-105">For Shader Model 6, you use `DXC.EXE` instead, which is documented in [Using dxc.exe and dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span></span>

<span data-ttu-id="4821e-106">Microsoft Visual Studio 2012 ahora puede compilar código de sombreador a partir de \* archivos. HLSL que se incluyen en el proyecto de C++.</span><span class="sxs-lookup"><span data-stu-id="4821e-106">Microsoft Visual Studio 2012 can now compile shader code from \*.hlsl files that you include in your C++ project.</span></span>

<span data-ttu-id="4821e-107">Como parte del proceso de compilación, Visual Studio 2012 usa el compilador de código [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL para compilar los archivos. HLSL en archivos de objeto de sombreador binario o en matrices de bytes que se definen en archivos de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4821e-107">As part of the build process, Visual Studio 2012 uses the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler to compile the .hlsl files into binary shader object files or into byte arrays that are defined in header files.</span></span> <span data-ttu-id="4821e-108">La forma en que el compilador de código HLSL compila cada archivo. HLSL en el proyecto depende de cómo se especifique la propiedad **archivos** de resultados para ese archivo.</span><span class="sxs-lookup"><span data-stu-id="4821e-108">How the HLSL code compiler compiles each .hlsl file in your project depends on how you specify the **Ouput Files** property for that file.</span></span> <span data-ttu-id="4821e-109">Para obtener más información sobre las páginas de propiedades de HLSL, consulte [páginas de propiedades de HLSL](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span><span class="sxs-lookup"><span data-stu-id="4821e-109">For more info about HLSL property pages, see [HLSL Property Pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span></span>

<span data-ttu-id="4821e-110">El método de compilación que usa normalmente depende del tamaño del \* archivo. HLSL.</span><span class="sxs-lookup"><span data-stu-id="4821e-110">The compile method that you use typically depends on the size of your \*.hlsl file.</span></span> <span data-ttu-id="4821e-111">Si incluye una gran cantidad de código de bytes en un encabezado, aumentará el tamaño y el tiempo de carga inicial de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4821e-111">If you include a large amount of byte code in a header, you increase the size and the initial load time of your app.</span></span> <span data-ttu-id="4821e-112">También puede forzar que todo el código de byte resida en la memoria incluso después de crear el sombreador, lo que desperdicia recursos.</span><span class="sxs-lookup"><span data-stu-id="4821e-112">You also force all byte code to reside in memory even after the shader is created, which wastes resources.</span></span> <span data-ttu-id="4821e-113">Pero al incluir código de bytes en un encabezado, puede reducir la complejidad del código y simplificar la creación del sombreador.</span><span class="sxs-lookup"><span data-stu-id="4821e-113">But when you include byte code in a header, you can reduce code complexity and simplify shader creation.</span></span>

<span data-ttu-id="4821e-114">Echemos un vistazo a las distintas formas de compilar el código del sombreador y las convenciones para las extensiones de archivo para el código del sombreador.</span><span class="sxs-lookup"><span data-stu-id="4821e-114">Let's now look at various ways to compile your shader code and conventions for file extensions for shader code.</span></span>

-   [<span data-ttu-id="4821e-115">Usar extensiones de archivo de código de sombreador</span><span class="sxs-lookup"><span data-stu-id="4821e-115">Using shader code file extensions</span></span>](#using-shader-code-file-extensions)
-   [<span data-ttu-id="4821e-116">Compilar en archivos de objeto en tiempo de compilación</span><span class="sxs-lookup"><span data-stu-id="4821e-116">Compiling at build time to object files</span></span>](#compiling-at-build-time-to-object-files)
-   [<span data-ttu-id="4821e-117">Compilar en los archivos de encabezado en tiempo de compilación</span><span class="sxs-lookup"><span data-stu-id="4821e-117">Compiling at build time to header files</span></span>](#compiling-at-build-time-to-header-files)
-   [<span data-ttu-id="4821e-118">Compilar con D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="4821e-118">Compiling with D3DCompileFromFile</span></span>](#compiling-with-d3dcompilefromfile)
-   [<span data-ttu-id="4821e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4821e-119">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="4821e-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4821e-120">Related topics</span></span>](#related-topics)

## <a name="using-shader-code-file-extensions"></a><span data-ttu-id="4821e-121">Usar extensiones de archivo de código de sombreador</span><span class="sxs-lookup"><span data-stu-id="4821e-121">Using shader code file extensions</span></span>

<span data-ttu-id="4821e-122">Para cumplir la Convención de Microsoft, use estas extensiones de archivo para el código del sombreador:</span><span class="sxs-lookup"><span data-stu-id="4821e-122">To conform to Microsoft convention, use these file extensions for your shader code:</span></span>

-   <span data-ttu-id="4821e-123">Un archivo con la extensión. HLSL contiene código fuente de lenguaje de sombreado de alto nivel ([HLSL](dx-graphics-hlsl-reference.md)).</span><span class="sxs-lookup"><span data-stu-id="4821e-123">A file with the .hlsl extension holds High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)) source code.</span></span>
-   <span data-ttu-id="4821e-124">Un archivo con la extensión. CSO contiene un objeto de sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="4821e-124">A file with the .cso extension holds a compiled shader object.</span></span>
-   <span data-ttu-id="4821e-125">Un archivo con la extensión. h es un archivo de encabezado, pero en un contexto de código del sombreador, este archivo de encabezado define una matriz de bytes que contiene los datos del sombreador.</span><span class="sxs-lookup"><span data-stu-id="4821e-125">A file with the .h extension is a header file, but in a shader code context, this header file defines a byte array that holds shader data.</span></span>

## <a name="compiling-at-build-time-to-object-files"></a><span data-ttu-id="4821e-126">Compilar en archivos de objeto en tiempo de compilación</span><span class="sxs-lookup"><span data-stu-id="4821e-126">Compiling at build time to object files</span></span>

<span data-ttu-id="4821e-127">Si compila los archivos. HLSL en archivos de objeto de sombreador binario, la aplicación debe leer los datos de esos archivos objeto (. CSO es la extensión predeterminada para estos archivos objeto), asignar los datos a las matrices de bytes y crear objetos de sombreador a partir de esas matrices de bytes.</span><span class="sxs-lookup"><span data-stu-id="4821e-127">If you compile your .hlsl files into binary shader object files, your app needs to read the data from those object files (.cso is the default extension for these object files), assign the data to byte arrays, and create shader objects from those byte arrays.</span></span> <span data-ttu-id="4821e-128">Por ejemplo, para crear un sombreador de vértices ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), llame al método [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) con una matriz de bytes que contenga el código de byte del sombreador de vértices compilados.</span><span class="sxs-lookup"><span data-stu-id="4821e-128">For example, to create a vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)\*\*), call the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method with a byte array that contains compiled vertex shader byte code.</span></span> <span data-ttu-id="4821e-129">En el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) se muestra cómo crear objetos de sombreador a partir de matrices de bytes obtenidas de archivos de objeto de sombreador binario. CSO.</span><span class="sxs-lookup"><span data-stu-id="4821e-129">The [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) shows how to create shader objects from byte arrays that it obtained from .cso binary shader object files.</span></span> <span data-ttu-id="4821e-130">En este código de ejemplo del [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), la propiedad **archivos de salida** del archivo SimpleVertexShader. HLSL especifica que se compile en el archivo de objeto SimpleVertexShader. CSO.</span><span class="sxs-lookup"><span data-stu-id="4821e-130">In this example code from the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), the **Ouput Files** property for the SimpleVertexShader.hlsl file specifies to compile into the SimpleVertexShader.cso object file.</span></span>

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a><span data-ttu-id="4821e-131">Compilar en los archivos de encabezado en tiempo de compilación</span><span class="sxs-lookup"><span data-stu-id="4821e-131">Compiling at build time to header files</span></span>

<span data-ttu-id="4821e-132">Si compila los archivos. HLSL en matrices de bytes que se definen en archivos de encabezado, debe incluir esos archivos de encabezado en el código.</span><span class="sxs-lookup"><span data-stu-id="4821e-132">If you compile your .hlsl files into byte arrays that are defined in header files, you need to include those header files in your code.</span></span> <span data-ttu-id="4821e-133">El [ejemplo de extensiones multimedia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) muestra cómo crear objetos de sombreador a partir de matrices de bytes que se definen en archivos de encabezado y que se incluyen en el proyecto en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="4821e-133">The [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) shows how to create shader objects from byte arrays that are defined in header files and that you include in your project at compile time.</span></span> <span data-ttu-id="4821e-134">En este código de ejemplo del [ejemplo de las extensiones multimedia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), la propiedad **archivos** de resultados del archivo u. HLSL especifica que se compile en la matriz de bytes de *g \_ psshader* que se define en el archivo de encabezado u. h.</span><span class="sxs-lookup"><span data-stu-id="4821e-134">In this example code from the [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), the **Ouput Files** property for the PixelShader.hlsl file specifies to compile into the *g\_psshader* byte array that is defined in the PixelShader.h header file.</span></span>


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a><span data-ttu-id="4821e-135">Compilar con D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="4821e-135">Compiling with D3DCompileFromFile</span></span>

<span data-ttu-id="4821e-136">También puede usar la función [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) en tiempo de ejecución para compilar código de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4821e-136">You can also use the [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function at run time to compile shader code.</span></span> <span data-ttu-id="4821e-137">Para obtener más información sobre cómo hacerlo, vea [Cómo: compilar un sombreador](/windows/desktop/direct3d11/how-to--compile-a-shader).</span><span class="sxs-lookup"><span data-stu-id="4821e-137">For more info about how to do this, see [How To: Compile a Shader](/windows/desktop/direct3d11/how-to--compile-a-shader).</span></span>

> [!Note]  
> <span data-ttu-id="4821e-138">Las aplicaciones de la tienda Windows admiten el uso de [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) para el desarrollo, pero no para la implementación.</span><span class="sxs-lookup"><span data-stu-id="4821e-138">Windows Store apps support using [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) for development but not for deployment.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4821e-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4821e-139">Related Topics</span></span>

[<span data-ttu-id="4821e-140">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="4821e-140">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="4821e-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4821e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4821e-142">Guía de programación para HLSL</span><span class="sxs-lookup"><span data-stu-id="4821e-142">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 