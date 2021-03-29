---
title: Funciones de D3DX (gráficos de Direct3D 11)
description: Esta sección contiene información sobre las funciones de D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- funciones, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421751"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a>Funciones de D3DX (gráficos de Direct3D 11)

Esta sección contiene información sobre las funciones de D3DX 11.

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 


## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> .
</blockquote>
<br/> Compilar un sombreador o un efecto desde un archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .
</blockquote>
<br/> Compilar un sombreador o un efecto que se carga en la memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar funciones de <a href="/windows/desktop/menurc/resources-functions">recursos</a>y, a continuación, compilar sin conexión mediante el compilador de línea de comandos de Fxc.exe o usar una de las API de compilación de HLSL, como la API de <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .
</blockquote>
<br/> Compilar un sombreador o un efecto desde un recurso.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ComputeNormalMap</strong>.
</blockquote>
<br/> Convierte un mapa de alto en un mapa normal. Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un procesador de datos asincrónico para un sombreador.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un cargador de archivos asincrónicos.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un cargador de memoria asincrónica.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un cargador de recursos asíncronos.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un procesador de datos para un sombreador de forma asincrónica.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un procesador de datos para usarlo con un <a href="id3dx11threadpump.md"><strong>bombeo de subprocesos</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un procesador de datos para usarlo con un <a href="id3dx11threadpump.md"><strong>bombeo de subprocesos</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un procesador de datos que cargue un recurso y, a continuación, cree una vista de recursos del sombreador para él. Los procesadores de datos son un componente de la característica de carga asincrónica de datos de D3DX11 que usa los <a href="id3dx11threadpump.md"><strong>bombeos de subprocesos</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
En lugar de usar esta función, se recomienda usar estas:</p>
<ul>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (donde xxx es DDS o WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (herramientas), <strong>LOADFROMXXXFILE</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Cree una vista de recursos del sombreador a partir de un archivo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
En lugar de usar esta función, se recomienda usar estas:</p>
<ul>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (donde xxx es DDS o WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (herramientas), <strong>LOADFROMXXXMEMORY</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Cree una vista de recursos del sombreador desde un archivo en la memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
En lugar de usar esta función, se recomienda usar funciones de <a href="/windows/desktop/menurc/resources-functions">recursos</a>y, a continuación:</p>
<ul>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (donde xxx es DDS o WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (herramientas), <strong>LOADFROMXXXMEMORY</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego <strong>CreateShaderResourceView</strong></li>
</ul>
</blockquote>
<br/> Cree una vista de recursos del sombreador desde un recurso.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
En lugar de usar esta función, se recomienda usar estas:</p>
<ul>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (donde xxx es DDS o WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (herramientas), <strong>LOADFROMXXXFILE</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Cree un recurso de textura a partir de un archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
En lugar de usar esta función, se recomienda usar estas:</p>
<ul>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (donde xxx es DDS o WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (herramientas), <strong>LOADFROMXXXMEMORY</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Cree un recurso de textura a partir de un archivo que reside en la memoria del sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
En lugar de usar esta función, se recomienda usar funciones de <a href="/windows/desktop/menurc/resources-functions">recursos</a>y, a continuación:</p>
<ul>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (donde xxx es DDS o WIC)</li>
<li>Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (herramientas), <strong>LOADFROMXXXMEMORY</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos) y luego <strong>CreateTexture</strong></li>
</ul>
</blockquote>
<br/> Cree una textura a partir de otro recurso.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows. Vea la sección Comentarios.
</blockquote>
<br/> Cree un bombeo de subprocesos.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GenerateMipMaps</strong> y <strong>GenerateMipMaps3D</strong>.
</blockquote>
<br/> Genera una cadena de mipmap mediante un filtro de textura determinado.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXFILE</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.
</blockquote>
<br/> Recupera información sobre un archivo de imagen determinado.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXMEMORY</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.
</blockquote>
<br/> Obtiene información acerca de una imagen ya cargada en la memoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar funciones de <a href="/windows/desktop/menurc/resources-functions">recursos</a>y, a continuación, usar la biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (herramientas), <strong>LOADFROMXXXMEMORY</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.
</blockquote>
<br/> Recupera información acerca de una imagen determinada en un recurso.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , cambiar el <strong>tamaño</strong>, <strong>convertir</strong>, <strong>comprimir</strong>, <strong>descomprimir</strong>o <strong>CopyRectangle</strong>.
</blockquote>
<br/> Cargar una textura de una textura.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la API de <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Cree un sombreador a partir de un archivo sin compilarlo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la API de <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Cree un sombreador a partir de la memoria sin compilarlo.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la API de <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .
</blockquote>
<br/> Cree un sombreador a partir de un recurso sin compilarlo.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> then <strong>SAVETOXXXFILE</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos. Para el escenario simplificado de creación de una captura de pantalla a partir de una textura de destino de representación, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> , <strong>SaveDDSTextureToFile</strong> o <strong>SaveWICTextureToFile</strong>.
</blockquote>
<br/> Guardar una textura en un archivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> then <strong>SAVETOXXXMEMORY</strong> (donde xxx es WIC, DDS o TGA; WIC no admite DDS ni TGA; D3DX 9 admitía TGA como formato de fuente de arte común para juegos.
</blockquote>
<br/> Guardar una textura en la memoria.<br/></td>
</tr>
<tr class="even">
<td><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar la biblioteca <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">matemática de armónicos esféricos</a> , <strong>SHProjectCubeMap</strong>.
</blockquote>
<br/> Proyecta una función representada en un mapa de cubo en armónicos esféricos.<br/></td>
</tr>
<tr class="odd">
<td><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
En lugar de usar esta función, se recomienda usar el método <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext:: ClearState</strong></a> .
</blockquote>
<br/> Quita todos los recursos del dispositivo estableciendo sus punteros en <strong>null</strong>. Se debe llamar a este método durante el cierre de la aplicación. Ayuda a garantizar que cuando se liberan todos los recursos que no están enlazados al dispositivo.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

