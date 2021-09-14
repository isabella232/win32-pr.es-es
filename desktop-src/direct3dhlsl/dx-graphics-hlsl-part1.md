---
title: Compilación de sombreadores
description: Ahora se verán varias maneras de compilar el código del sombreador y las convenciones de las extensiones de archivo para el código del sombreador.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258455"
---
# <a name="compiling-shaders"></a>Compilación de sombreadores

> [!NOTE]
> En este tema se trata `FXC.EXE` el compilador usado para los modelos de sombreador 2 a 5.1. Para El modelo de sombreador 6, se usa en su lugar, que se documenta en Uso de dxc.exe `DXC.EXE` [y dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).

Microsoft Visual Studio 2012 ahora puede compilar código de sombreador a partir de archivos \* .hlsl que incluya en el proyecto de C++.

Como parte del proceso de compilación, Visual Studio 2012 usa el compilador de código HLSL de [fxc.exe](/windows/desktop/direct3dtools/fxc) para compilar los archivos .hlsl en archivos de objeto de sombreador binario o en matrices de bytes definidas en archivos de encabezado. La forma en que el compilador de código HLSL compila cada archivo .hlsl del proyecto depende de cómo especifique la propiedad **Ouput Files** para ese archivo. Para obtener más información sobre las páginas de propiedades HLSL, vea [HLSL Property Pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).

El método de compilación que se usa normalmente depende del tamaño del \* archivo .hlsl. Si incluye una gran cantidad de código de bytes en un encabezado, aumenta el tamaño y el tiempo de carga inicial de la aplicación. También se fuerza que todo el código de bytes resida en memoria incluso después de crear el sombreador, lo que desperdicia recursos. Pero al incluir código de bytes en un encabezado, puede reducir la complejidad del código y simplificar la creación del sombreador.

Ahora se verán varias maneras de compilar el código del sombreador y las convenciones de las extensiones de archivo para el código del sombreador.

-   [Uso de extensiones de archivo de código de sombreador](#using-shader-code-file-extensions)
-   [Compilación en tiempo de compilación en archivos objeto](#compiling-at-build-time-to-object-files)
-   [Compilación en tiempo de compilación en archivos de encabezado](#compiling-at-build-time-to-header-files)
-   [Compilación con D3DCompileFromFile](#compiling-with-d3dcompilefromfile)
-   [Temas relacionados](#related-topics)
-   [Temas relacionados](#related-topics)

## <a name="using-shader-code-file-extensions"></a>Uso de extensiones de archivo de código de sombreador

Para cumplir con la convención de Microsoft, use estas extensiones de archivo para el código del sombreador:

-   Un archivo con la extensión .hlsl contiene código fuente de lenguaje de sombreado de alto nivel[(HLSL).](dx-graphics-hlsl-reference.md)
-   Un archivo con la extensión .cso contiene un objeto de sombreador compilado.
-   Un archivo con la extensión .h es un archivo de encabezado, pero en un contexto de código de sombreador, este archivo de encabezado define una matriz de bytes que contiene los datos del sombreador.

## <a name="compiling-at-build-time-to-object-files"></a>Compilación en tiempo de compilación en archivos objeto

Si compila los archivos .hlsl en archivos de objeto de sombreador binario, la aplicación debe leer los datos de esos archivos objeto (.cso es la extensión predeterminada para estos archivos de objeto), asignar los datos a matrices de bytes y crear objetos de sombreador a partir de esas matrices de bytes. Por ejemplo, para crear un sombreador de vértices [**(ID3D11VertexShader),**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)llame al método \* \* [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) con una matriz de bytes que contiene código de bytes compilado del sombreador de vértices. En [el ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) se muestra cómo crear objetos de sombreador a partir de matrices de bytes que obtuvo de los archivos de objeto de sombreador binario .cso. En este código de ejemplo del ejemplo de [tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), la propiedad **Ouput Files** del archivo SimpleVertexShader.hlsl especifica que se compile en el archivo de objeto SimpleVertexShader.cso.

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

## <a name="compiling-at-build-time-to-header-files"></a>Compilación en tiempo de compilación en archivos de encabezado

Si compila los archivos .hlsl en matrices de bytes definidas en archivos de encabezado, debe incluir esos archivos de encabezado en el código. El [ejemplo de extensiones multimedia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) muestra cómo crear objetos de sombreador a partir de matrices de bytes que se definen en archivos de encabezado y que se incluyen en el proyecto en tiempo de compilación. En este código de ejemplo del ejemplo extensiones multimedia [,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample)la propiedad **Ouput Files** del archivo PixelShader.hlsl especifica que se compile en la matriz de bytes g *\_ psshader* que se define en el archivo de encabezado PixelShader.h.


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a>Compilación con D3DCompileFromFile

También puede usar la función [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) en tiempo de ejecución para compilar el código del sombreador. Para obtener más información sobre cómo hacerlo, vea [Cómo: Compilar un sombreador.](/windows/desktop/direct3d11/how-to--compile-a-shader)

> [!Note]  
> Windows Las aplicaciones de la tienda [**admiten el uso de D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) para el desarrollo, pero no para la implementación.

 

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de programación para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 