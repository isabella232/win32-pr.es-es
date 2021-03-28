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
# <a name="compiling-shaders"></a>Compilar sombreadores

> [!NOTE]
> En este tema se trata el `FXC.EXE` compilador que se usa para los modelos de sombreador del 2 al 5,1. En el modelo de sombreador 6, se usa en `DXC.EXE` su lugar, que se documenta en [uso de dxc.exe y dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).

Microsoft Visual Studio 2012 ahora puede compilar código de sombreador a partir de \* archivos. HLSL que se incluyen en el proyecto de C++.

Como parte del proceso de compilación, Visual Studio 2012 usa el compilador de código [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL para compilar los archivos. HLSL en archivos de objeto de sombreador binario o en matrices de bytes que se definen en archivos de encabezado. La forma en que el compilador de código HLSL compila cada archivo. HLSL en el proyecto depende de cómo se especifique la propiedad **archivos** de resultados para ese archivo. Para obtener más información sobre las páginas de propiedades de HLSL, consulte [páginas de propiedades de HLSL](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).

El método de compilación que usa normalmente depende del tamaño del \* archivo. HLSL. Si incluye una gran cantidad de código de bytes en un encabezado, aumentará el tamaño y el tiempo de carga inicial de la aplicación. También puede forzar que todo el código de byte resida en la memoria incluso después de crear el sombreador, lo que desperdicia recursos. Pero al incluir código de bytes en un encabezado, puede reducir la complejidad del código y simplificar la creación del sombreador.

Echemos un vistazo a las distintas formas de compilar el código del sombreador y las convenciones para las extensiones de archivo para el código del sombreador.

-   [Usar extensiones de archivo de código de sombreador](#using-shader-code-file-extensions)
-   [Compilar en archivos de objeto en tiempo de compilación](#compiling-at-build-time-to-object-files)
-   [Compilar en los archivos de encabezado en tiempo de compilación](#compiling-at-build-time-to-header-files)
-   [Compilar con D3DCompileFromFile](#compiling-with-d3dcompilefromfile)
-   [Temas relacionados](#related-topics)
-   [Temas relacionados](#related-topics)

## <a name="using-shader-code-file-extensions"></a>Usar extensiones de archivo de código de sombreador

Para cumplir la Convención de Microsoft, use estas extensiones de archivo para el código del sombreador:

-   Un archivo con la extensión. HLSL contiene código fuente de lenguaje de sombreado de alto nivel ([HLSL](dx-graphics-hlsl-reference.md)).
-   Un archivo con la extensión. CSO contiene un objeto de sombreador compilado.
-   Un archivo con la extensión. h es un archivo de encabezado, pero en un contexto de código del sombreador, este archivo de encabezado define una matriz de bytes que contiene los datos del sombreador.

## <a name="compiling-at-build-time-to-object-files"></a>Compilar en archivos de objeto en tiempo de compilación

Si compila los archivos. HLSL en archivos de objeto de sombreador binario, la aplicación debe leer los datos de esos archivos objeto (. CSO es la extensión predeterminada para estos archivos objeto), asignar los datos a las matrices de bytes y crear objetos de sombreador a partir de esas matrices de bytes. Por ejemplo, para crear un sombreador de vértices ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), llame al método [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) con una matriz de bytes que contenga el código de byte del sombreador de vértices compilados. En el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) se muestra cómo crear objetos de sombreador a partir de matrices de bytes obtenidas de archivos de objeto de sombreador binario. CSO. En este código de ejemplo del [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), la propiedad **archivos de salida** del archivo SimpleVertexShader. HLSL especifica que se compile en el archivo de objeto SimpleVertexShader. CSO.

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

## <a name="compiling-at-build-time-to-header-files"></a>Compilar en los archivos de encabezado en tiempo de compilación

Si compila los archivos. HLSL en matrices de bytes que se definen en archivos de encabezado, debe incluir esos archivos de encabezado en el código. El [ejemplo de extensiones multimedia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) muestra cómo crear objetos de sombreador a partir de matrices de bytes que se definen en archivos de encabezado y que se incluyen en el proyecto en tiempo de compilación. En este código de ejemplo del [ejemplo de las extensiones multimedia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), la propiedad **archivos** de resultados del archivo u. HLSL especifica que se compile en la matriz de bytes de *g \_ psshader* que se define en el archivo de encabezado u. h.


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a>Compilar con D3DCompileFromFile

También puede usar la función [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) en tiempo de ejecución para compilar código de sombreador. Para obtener más información sobre cómo hacerlo, vea [Cómo: compilar un sombreador](/windows/desktop/direct3d11/how-to--compile-a-shader).

> [!Note]  
> Las aplicaciones de la tienda Windows admiten el uso de [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) para el desarrollo, pero no para la implementación.

 

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 