---
description: A partir de Windows 8, el SDK de DirectX se incluye como parte de la Windows SDK.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: ¿Dónde está el SDK de DirectX?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c070313c5c7f6105afaf7b629ff1ca2618a469fb
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314628"
---
# <a name="where-is-the-directx-sdk"></a>¿Dónde está el SDK de DirectX?

A partir de Windows 8, el SDK de DirectX se incluye como parte de la Windows SDK.

Originalmente, el SDK de DirectX se creó como una plataforma de alto rendimiento para el desarrollo de juegos sobre Windows. A medida que las tecnologías de DirectX evolucionaron, se hicieron relevantes para una amplia gama de aplicaciones. En la actualidad, la disponibilidad del hardware de Direct3D en los equipos impulsa incluso las aplicaciones de escritorio tradicionales para usar la aceleración de hardware gráfico. En paralelo, las tecnologías de DirectX están más integradas con Windows. DirectX es ahora una parte fundamental de Windows.

Dado que Windows SDK es el SDK que principalmente se usa para el desarrollo en Windows, ahora DirectX está incluido en él. Ahora puedes usar Windows SDK para crear juegos espectaculares para Windows. Para descargar el SDK de Windows 8. x o el SDK de Windows 10, consulte [Windows SDK y el archivo de emulador](https://developer.microsoft.com/windows/downloads/sdk-archive).

Las siguientes tecnologías y herramientas, que antes formaban parte del SDK de DirectX, ahora forman parte de la Windows SDK.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tecnología o herramienta</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Componentes gráficos de Windows<br/></td>
<td>Los encabezados y las bibliotecas de <a href="/windows/desktop/direct3d">Direct3D</a> y otras API de gráficos de Windows, como <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>, están disponibles en la Windows SDK. <br/>
<blockquote>
[!Note]<br />
Las bibliotecas de la utilidad D3DX9/D3DX10/D3DX11 desusadas están disponibles a través de <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, pero también hay una serie de <a href="https://walbourn.github.io/living-without-d3dx/">alternativas de código abierto</a>. La biblioteca de la utilidad D3DCSX DirectCompute y el archivo DLL redistribuible están disponibles en el Windows SDK. D3DX12 está disponible en <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Compilador de HLSL (FXC.EXE)<br/></td>
<td>El compilador de <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> es una herramienta que se encuentra en el subdirectorio Architecture adecuado en la carpeta bin en el Windows SDK.<br/>
<blockquote>
[!Note]<br />
La API de D3DCompiler y el archivo DLL redistribuible están disponibles en la Windows SDK.
</blockquote>
<br/><br/>Para el desarrollo de DirectX 12, use DXCompiler en el Windows SDK y hospedado en [GitHub](https://github.com/Microsoft/DirectXShaderCompiler).
<br/></td>
</tr>
<tr class="odd">
<td><span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>PIX para Windows<br/></td>
<td>Un reemplazo de la herramienta PIX para Windows ahora es una característica de Microsoft Visual Studio, denominada depurador de gráficos de Visual Studio. Esta característica ha mejorado considerablemente el uso, la compatibilidad con Windows 8 y Direct3D 11,1, y la integración con características de Microsoft Visual Studio tradicionales, como pilas de llamadas y ventanas de depuración para la depuración de <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL</a> . Para obtener más información sobre esta nueva característica, consulte <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">depuración de gráficos de DirectX</a>.<br/><br/>Para el desarrollo de DirectX 12, consulte la última generación de <a href="https://devblogs.microsoft.com/pix/">PIX en Windows</a><br/></td>
</tr>
<tr class="even">
<td><span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> para Windows<br/></td>
<td>La API de <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> es ahora un componente del sistema en Windows 8. x y Windows 10. Los encabezados y las bibliotecas de XAudio2 están disponibles en el Windows SDK. Para obtener soporte técnico de Windows 7, vea <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> para Windows<br/></td>
<td>La API de <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> 1,4 es ahora un componente del sistema en Windows 8. x y Windows 10. Los encabezados y las bibliotecas de XInput están disponibles en el Windows SDK.<br/>
<blockquote>
[!Note]<br />
La 9.1.0 de XInput heredada también está disponible como parte de Windows 7 o posterior.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br/></td>
<td>La versión más reciente de XNAMATH, que se actualiza para los nuevos conjuntos de instrucciones, así como ARM/ARM64, es ahora <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a>. Los encabezados de DirectXMath están disponibles en el Windows SDK y en <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>Panel de control de DirectX y visor de funciones de DirectX<br/></td>
<td>Las utilidades del panel de control de DirectX y del visor de funciones de DirectX se incluyen en el subdirectorio de la arquitectura correspondiente en la carpeta bin en el Windows SDK. El visor de funcionalidades de DirectX también está disponible en <a href="https://github.com/microsoft/DxCapsViewer">GitHub</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="XACT"></span><span id="xact"></span>XACT<br/></td>
<td>La herramienta multiplataforma de audio de Xbox (XACT) ya no se admite para su uso en Windows.<br/></td>
</tr>
<tr class="odd">
<td><span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Explorador de juegos</a> y GDFMAKER<br/></td>
<td>La API del <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Explorador de juegos</a> presenta juegos a los usuarios de Windows. La API del explorador de juegos solo se admite en Windows Vista y Windows 7. Use la herramienta Game Definition File Maker (GDFMAKER.EXE) para declarar clasificaciones de juego para aplicaciones de la tienda Windows. <br/> La herramienta Game Definition File Maker (GDFMaker.exe) se incluye en el subdirectorio x86 de la carpeta bin del Windows SDK y admite aplicaciones de la tienda Windows y aplicaciones de escritorio Win32.<br/>
<br/></td>
</tr>
<tr class="even">
<td><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Ejemplos<br/></td>
<td>Puede encontrar aplicaciones de ejemplo que resaltan las tecnologías de DirectX 12 en Windows en el repositorio de <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">ejemplos de DirectX</a> . La mayoría de los ejemplos de las versiones anteriores de Direct3D también están disponibles en línea. Para obtener más información sobre estos ejemplos, consulte el <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">Catálogo de ejemplos del SDK de DirectX</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>DirectX 1,1 administrado<br/></td>
<td>Los ensamblados de .NET DirectX están desusados y no se recomiendan para su uso por parte de aplicaciones nuevas. Hay una serie de alternativas disponibles. Consulte <a href="https://walbourn.github.io/directx-and-net/">DirectX y .net</a>. <br/></td>
</tr>
</tbody>
</table>



 

El SDK de DirectX heredado está disponible para su descarga desde el [centro de descarga de Microsoft](https://go.microsoft.com/fwlink/?LinkId=226640) , si es necesario, pero no se recomienda usar para proyectos nuevos.

> [!Note]  
> No se puede instalar el SDK de DirectX si tiene una versión determinada del paquete redistribuible Visual C++ 2010 ya instalado. Para obtener más información acerca de y una solución para solucionar este problema, vea [el error "S1023" al instalar el SDK de DirectX (2010 de junio)](https://support.microsoft.com/kb/2728613).

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Uso de proyectos de DirectX SDK con Visual Studio

Los ejemplos del SDK de DirectX de junio de 2010 son compatibles con las SKU Premium de Visual Studio (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 o Microsoft Visual Studio Ultimate 2013) en Windows 7 y Windows 8 y versiones posteriores. Debido a la transición de las bibliotecas y los encabezados de DirectX en el Windows SDK, es necesario realizar cambios en la configuración del proyecto para compilar estos ejemplos correctamente con el modo en que el SDK de Windows 8 y versiones posteriores se empaquetan con las SKU Premium de Visual Studio.

Estos pasos también se aplican a sus propios proyectos que dependen del SDK de DirectX.

1.  Asegúrese de que la versión del SDK de DirectX de junio de 2010 está instalada en el equipo de desarrollo. Si instala en un equipo que ejecuta Windows 8 y versiones posteriores, se le pedirá que habilite .NET 3,5 como una instalación de requisitos previos para el SDK de DirectX.

    > [!Note]  
    > No se puede instalar el SDK de DirectX si tiene una versión determinada del paquete redistribuible Visual C++ 2010 ya instalado. Para obtener más información acerca de y una solución para solucionar este problema, vea [el error "S1023" al instalar el SDK de DirectX (2010 de junio)](https://support.microsoft.com/kb/2728613).

     

2.  Asegúrese de que usa una de las SKU Premium de Visual Studio. Microsoft Visual Studio Express 2012 para Windows 8 o Microsoft Visual Studio Express 2013 para Windows no creará aplicaciones de escritorio de Windows 8 y versiones posteriores, como los ejemplos del SDK de DirectX. Para instalar una de las SKU Premium de Visual Studio, vaya a: [descargas de Visual Studio](https://www.microsoft.com/visualstudio/11/downloads) y siga las instrucciones.

3.  Use el explorador de ejemplo de DirectX SDK para instalar los archivos de proyecto para el ejemplo deseado. Abra el archivo de solución compatible con Microsoft Visual Studio 2010 de ejemplo (con el sufijo **\_ 2010**).

4.  Si está abriendo el ejemplo en un sistema que solo tiene instalado Microsoft Visual Studio 2012 o Microsoft Visual Studio 2013, recibirá el siguiente mensaje: "esta solución contiene uno o varios proyectos que usan una versión anterior del compilador y las bibliotecas de VC + +. Cada proyecto se puede actualizar para usar el compilador y las bibliotecas de VC + + (V110). Elija la opción **Actualizar** de este cuadro de diálogo para actualizar antes de abrir el proyecto.

    De lo contrario, puede actualizar al compilador y las bibliotecas de Visual Studio 2012 o Visual Studio 2013 C++ 11 una vez cargados haciendo clic con el botón derecho en la solución y eligiendo **actualizar proyectos de VC + +**.

5.  D3DX no se considera la API canónica para usar Direct3D en Windows 8 y versiones posteriores, por lo que no se incluye con el Windows SDK correspondiente. Investigue soluciones alternativas para trabajar con la API de Direct3D. En el caso de los proyectos heredados, como los ejemplos de SDK de DirectX de Windows 7 (y versiones anteriores), los siguientes pasos son necesarios para compilar aplicaciones con D3DX mediante el SDK de DirectX:

    1.  Modifique los directorios de **VC + +** del proyecto como se indica a continuación para usar el orden correcto para los encabezados y las bibliotecas del SDK.

        <dl> i. Abra las **propiedades** del proyecto y seleccione la página **directorios de VC + +** .  
        ii. Seleccione **todas las configuraciones y todas las plataformas**.  
        iii. Establezca estos directorios de la manera siguiente:

        -   Directorios ejecutables: **<inherit from parent or project defaults>** (en la lista desplegable del lado derecho)
        -   Directorios de inclusión: **$ (IncludePath); $ (DXSDK \_ dir) include**
        -   Incluir directorios de biblioteca: **$ (LibraryPath); $ (DXSDK \_ dir) lib \\ x86**

          
        iv. Haga clic en **Aplicar**.  
        v. Elija la **plataforma x64**.  
        vi. Establezca el **Directorio de biblioteca** de la siguiente manera:

        -   Directorios de biblioteca: **$ (LibraryPath); $ (DXSDK \_ dir) lib \\ x64**

          
        </dl>

    2.  Siempre que "d3dx9. h", "d3dx10. h" o "d3dx11. h" se incluyan en el proyecto, asegúrese de incluir explícitamente "d3d9. h", "d3d10. h" y "dxgi. h", o "d3d11. h" y "dxgi. h" para asegurarse de que selecciona la versión más reciente. Puede deshabilitar la **ADVERTENCIA C4005** si es necesario. sin embargo, esta advertencia indica que está usando la versión anterior de estos encabezados.
    3.  Quite todas las referencias a DXGIType. h en el proyecto. Este encabezado no existe en el Windows SDK y la versión del SDK de DirectX entra en conflicto con el nuevo Winerror. h.
    4.  Todos los archivos dll de D3DX se instalan en el equipo de desarrollo mediante la instalación del SDK de DirectX. Asegúrese de que las dependencias de D3DX necesarias se redistribuyen con cualquier muestra o con la aplicación si se mueve a otra máquina.
    5.  Tenga en cuenta que las tecnologías de reemplazo para los usos actuales de D3DX11 incluyen [DirectXTex](https://github.com/Microsoft/DirectXTex), [DirectXTK](https://github.com/Microsoft/DirectXTK), [DirectXMesh](https://github.com/Microsoft/DirectXMesh)y [UVAtlas](https://github.com/Microsoft/UVAtlas). D3DXMath se reemplaza por [DirectXMath](./dxmath/directxmath-portal.md).

6.  Asegúrese de que está usando la nueva versión del compilador de sombreador HLSL observando las condiciones siguientes:

    1.  Si cambia el directorio ejecutable como se hace en el paso 5, las compilaciones de proyectos usarán FXC desde la Windows SDK instalar. Tenga en cuenta que Visual Studio reconoce oficialmente los archivos HLSL. Puede agregarlos como archivos de proyecto y establecer opciones del compilador a través del sistema del proyecto.

    2.  Al invocar la compilación en tiempo de ejecución mediante el archivo DLL de D3DX heredado, se usará la versión anterior incorrecta del compilador de HLSL. Reemplace todas las referencias a las \* API D3DXCompile, D3DX10Compile \* y D3DX11Compile del \* código por la función D3DCompile de D3DCOMPILER \_46.DLL o D3DCOMPILER \_47.DLL.

    3.  Cualquier proyecto que use la compilación del sombreador en tiempo de ejecución debe tener D3DCOMPILER \_xx.DLL copiado en la ruta de acceso del archivo ejecutable local para el proyecto. Este archivo dll está disponible en este subdirectorio de la Windows SDK instalación de **% ProgramFiles (x86)% \\ Windows kits \\ 8,0 \\ Redist \\ D3D \\ <arch>** o **% ProgramFiles (x86)% \\ Windows kits \\ 8,1 \\ Redist \\ D3D \\ <arch>** , donde **<arch>** es **x86** y **x64**.

        El \_46.DLL D3DCOMPILER o \_47.DLL D3DCOMPILER de la Windows SDK no es un componente del sistema y no se debe copiar en el directorio del sistema de Windows. Puede redistribuir este archivo DLL a otros equipos con la aplicación como un archivo DLL en paralelo.

7.  Cualquier proyecto que use la API de XInput y está diseñado para ejecutarse en Windows 7 o versiones anteriores de Windows debe usar la versión heredada (9.1.0) o deberá incluir explícitamente los encabezados y las bibliotecas para este componente desde el SDK de DirectX. El encabezado XInput y XINPUT. LIB que se incluye en el Windows SDK tener como destino solo la versión (1,4) que se distribuye como parte de Windows 8 y versiones posteriores. Se puede usar el mismo encabezado con XINPUT9 \_ 1 \_ 0. lib para usar la versión heredada, que se incluye con versiones anteriores de Windows. La versión heredada de XInput no detecta capacidades completas ni audio integrado con el controlador de soporte, por lo que si se requiere compatibilidad con estas características, debe usar la versión del SDK de DirectX (1,3).

    Para usar la API XInput de nivel inferior con todas las características, debe utilizar `#include` directamente los encabezados de XInput específicos del SDK de DirectX:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... y en las opciones del enlazador para las dependencias adicionales, vincule directamente a la biblioteca XInput del SDK de DirectX:

    **% DXSDK \_ dir% incluye \\ <arch> \\ XInput. lib**

    La \_ instalación de DirectX SDK en el equipo de desarrollo instala XINPUT13.DLL binario en los directorios del sistema de Windows. Tendrá que redistribuir este archivo binario con la aplicación mediante la instalación del programa de instalación de DirectX del SDK de DirectX.

8.  Cualquier proyecto que use la API de XAudio2 y está diseñado para ejecutarse en Windows 7 o versiones anteriores de Windows debe usar la versión anterior (9.1.0) o incluir explícitamente los encabezados y las bibliotecas para este componente desde el SDK de DirectX. Los encabezados y las bibliotecas de XAudio2 que se incluyen con el Windows SDK solo tienen como destino la versión (2,8) que se incluye como parte de Windows 8.

    Por ejemplo, con XAudio2, debe tener `#include` directamente los encabezados de xaudio2 específicos del SDK de DirectX:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... y en las opciones del enlazador para las dependencias adicionales, vincule directamente a la biblioteca de XAudio2 del SDK de DirectX:

    **% DXSDK \_ dir% incluye \\ <arch> \\ xaudio2. lib**

    El \_ archivo binario7.DLL de XAUDIO2 se instala en los directorios del sistema de Windows mediante la instalación del SDK de DirectX en el equipo de desarrollo. Debe redistribuir estas bibliotecas con la aplicación mediante la instalación del programa de instalación de DirectX desde el SDK de DirectX.

9.  Si ha usado el SDK de DirectX con versiones anteriores de Visual Studio, la actualización de Visual Studio 2010 podría haber migrado la ruta de acceso del SDK de DirectX a la configuración predeterminada del proyecto. Se recomienda quitar esta configuración para evitar errores de compilación futuros. En el directorio **% userprofile% \\ AppData \\ local \\ Microsoft \\ msbuild \\ v 4.0** , modifique los archivos **Microsoft. cpp. Win32. User** y **Microsoft. cpp. x64. User** para quitar todas las referencias a las rutas de acceso de directorio DXSDK \_ . Como alternativa, puede quitar todo el <PropertyGroup> nodo que contiene las entradas de ruta de acceso como <ExecutablePath> y <IncludePath> para revertir a los valores predeterminados estándar. Si no ve referencias a DXSDK \_ dir en estos archivos, no es necesario ningún cambio.

10. Si la aplicación resultante es compatible con Windows Vista con Service Pack 2 (SP2), así como con Windows 7 y Windows 8 y versiones posteriores, establezca la definición del preprocesador denominada **\_ Win32 \_ WinNT** en 0x600. Si solo es compatible con Windows 7 y Windows 8 y versiones posteriores, establézcalo en 0x601.

    Por ejemplo:

    1.  Abra **las propiedades** del proyecto y seleccione preprocesador de **C/C++**  >  .
    2.  Seleccione **todas las configuraciones** y **todas las plataformas**.
    3.  Vaya a la sección **definiciones del preprocesador** y establezca \_ Win32 \_ WinNT = 0x600.
    4.  Haga clic en **Aplicar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Juegos para Windows y el SDK de DirectX**
</dt> <dt>

[¿Dónde está el SDK de DirectX (edición 2021)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[SDK de DirectX de una edad determinada](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Vida sin D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
