---
description: A partir Windows 8, el SDK de DirectX se incluye como parte de Windows SDK.
ms.assetid: d8765da9-e7cf-47e8-8bc3-4b29162da41b
title: ¿Dónde está el SDK de DirectX?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744a48d4db961286123df380dc4718be283363ec
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480101"
---
# <a name="where-is-the-directx-sdk"></a>¿Dónde está el SDK de DirectX?

A partir Windows 8, el SDK de DirectX se incluye como parte de Windows SDK.

Originalmente creamos el SDK de DirectX como una plataforma de alto rendimiento para el desarrollo de juegos sobre Windows. A medida que las tecnologías de DirectX han madurado, se han convertido en relevantes para una gama más amplia de aplicaciones. En la actualidad, la disponibilidad del hardware de Direct3D en equipos impulsa incluso las aplicaciones de escritorio tradicionales para usar la aceleración de hardware gráfico. En paralelo, las tecnologías DirectX están más integradas con Windows. DirectX es ahora una parte fundamental de Windows.

Dado que Windows SDK es el SDK que principalmente se usa para el desarrollo en Windows, ahora DirectX está incluido en él. Ahora puedes usar Windows SDK para crear juegos espectaculares para Windows. Para descargar el SDK Windows 8.x o el SDK de Windows 10, consulte el artículo [Windows SDK y el archivo del emulador.](https://developer.microsoft.com/windows/downloads/sdk-archive)

Las siguientes tecnologías y herramientas, que anteriormente formaban parte del SDK de DirectX, ahora forman parte del SDK Windows sdk.


| Tecnología o herramienta | Descripción | 
|--------------------|-------------|
| <span id="Windows_Graphics_Components"></span><span id="windows_graphics_components"></span><span id="WINDOWS_GRAPHICS_COMPONENTS"></span>Windows Componentes gráficos<br /> | Los encabezados y bibliotecas para <a href="/windows/desktop/direct3d">Direct3D</a> y otras API de gráficos Windows, como <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D,</a>están disponibles en el SDK Windows. <br /><blockquote>[!Note]<br />Las bibliotecas de utilidad D3DX9/D3DX10/D3DX11 en desuso están disponibles a través de <a href="https://www.nuget.org/packages/Microsoft.DXSDK.D3DX">NuGet</a>, pero también hay una serie de <a href="https://walbourn.github.io/living-without-d3dx/">alternativas</a>de código abierto . La biblioteca de utilidades D3DCSX DirectCompute y el archivo DLL redistribuible están disponibles en el SDK Windows. D3DX12 está disponible en <a href="https://github.com/microsoft/DirectX-Headers">GitHub</a>.</blockquote><br /> | 
| <span id="HLSL_compiler__FXC.EXE_"></span><span id="hlsl_compiler__fxc.exe_"></span><span id="HLSL_COMPILER__FXC.EXE_"></span>Compilador HLSL (FXC.EXE)<br /> | El <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">compilador HLSL</a> es una herramienta del subdirectorio de arquitectura adecuado en la carpeta bin del SDK Windows.<br /><blockquote>[!Note]<br />La API D3DCompiler y el archivo DLL redistribuible están disponibles en Windows SDK.</blockquote><br /><br />Para el desarrollo de DirectX 12, use DXCompiler en el SDK de Windows y hospedado [en GitHub](https://github.com/Microsoft/DirectXShaderCompiler).<br /> | 
| <span id="PIX_for_"></span><span id="pix_for_"></span><span id="PIX_FOR_"></span>LAV para Windows<br /> | Ahora, un reemplazo de LA PARA WINDOWS herramienta es una característica de Microsoft Visual Studio, denominada depurador de gráficos Visual Studio gráficos. Esta característica ha mejorado enormemente la facilidad de uso, la compatibilidad con Windows 8 y Direct3D 11.1, y la integración con características tradicionales de Microsoft Visual Studio como pilas de llamadas y ventanas de depuración para la depuración <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl">HLSL.</a> Para obtener más información sobre esta nueva característica, vea <a href="/visualstudio/debugger/visual-studio-graphics-diagnostics?view=vs-2015">Depuración de gráficos directX.</a><br /><br />Para el desarrollo de DirectX 12, consulte la generación más reciente de <a href="https://devblogs.microsoft.com/pix/">LAV en Windows</a><br /> | 
| <span id="XAudio2_for_"></span><span id="xaudio2_for_"></span><span id="XAUDIO2_FOR_"></span><a href="/windows/desktop/xaudio2/xaudio2-apis-portal">XAudio2</a> para Windows<br /> | La <a href="/windows/desktop/xaudio2/xaudio2-apis-portal">API XAudio2</a> es ahora un componente del sistema en Windows 8.x y Windows 10. Los encabezados y bibliotecas de XAudio2 están disponibles en el SDK Windows. Para Windows compatibilidad con 7, vea <a href="/windows/win32/xaudio2/xaudio2-redistributable">XAudio2Redist</a>.<br /> | 
| <span id="XInput_for_"></span><span id="xinput_for_"></span><span id="XINPUT_FOR_"></span><a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">XInput</a> para Windows<br /> | La <a href="/windows/desktop/xinput/xinput-game-controller-apis-portal">API XInput</a> 1.4 es ahora un componente del sistema en Windows 8.x y Windows 10. Los encabezados y bibliotecas de XInput están disponibles en el SDK Windows.<br /><blockquote>[!Note]<br />XInput 9.1.0 heredado también está disponible como parte de Windows 7 o posterior.</blockquote><br /> | 
| <span id="XNAMATH"></span><span id="xnamath"></span>XNAMATH<br /> | La versión más reciente de XNXATH, que se actualiza para nuevos conjuntos de instrucciones, así como para ARM/ARM64, ahora es <a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath.</a> Los encabezados de DirectXMath están disponibles en el SDK de Windows y en <a href="https://github.com/Microsoft/DirectXMath">GitHub</a>.<br /> | 
| <span id="DirectX_Control_Panel_and_DirectX_Capabilities_Viewer"></span><span id="directx_control_panel_and_directx_capabilities_viewer"></span><span id="DIRECTX_CONTROL_PANEL_AND_DIRECTX_CAPABILITIES_VIEWER"></span>Visor de funcionalidades Panel de control DirectX y DirectX<br /> | Las utilidades directX Panel de control y Visor de funcionalidades de DirectX se incluyen en el subdirectorio de arquitectura adecuado en la carpeta bin del SDK Windows. El Visor de funcionalidades de DirectX también está <a href="https://github.com/microsoft/DxCapsViewer">disponible en GitHub</a>.<br /> | 
| <span id="XACT"></span><span id="xact"></span>XACT<br /> | La Herramienta multiplataforma de audio de Xbox (XACT) ya no se admite para su uso en Windows.<br /> | 
| <span id="Games_Explorer_and_GDFMAKER"></span><span id="games_explorer_and_gdfmaker"></span><span id="GAMES_EXPLORER_AND_GDFMAKER"></span><a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">Games Explorer</a> y GDFMAKER<br /> | La API <a href="/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)">de Games Explorer</a> presenta juegos a los usuarios de Windows. La API de Games Explorer solo se admite en Windows Vista y Windows 7. Use la herramienta Creador de archivos de definición de juegos (GDFMAKER.EXE) para declarar clasificaciones de juegos para Windows store. <br /> La herramienta Creador de archivos de definición de juegos (GDFMaker.exe) se incluye en el subdirectorio x86 en la carpeta bin del SDK de Windows y admite aplicaciones de Windows Store y aplicaciones de escritorio Win32.<br /><br /> | 
| <span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span>Ejemplos<br /> | Puede encontrar aplicaciones de ejemplo que resaltan las tecnologías de DirectX 12 Windows en el <a href="https://github.com/Microsoft/DirectX-Graphics-Samples">repositorio de ejemplos de DirectX.</a> La mayoría de los ejemplos de versiones anteriores de Direct3D también están disponibles en línea. Para más información sobre estos ejemplos, consulte <a href="https://walbourn.github.io/directx-sdk-samples-catalog/">Catálogo de ejemplos del SDK de DirectX.</a><br /> | 
| <span id="Managed_DirectX_1.1"></span><span id="managed_directx_1.1"></span><span id="MANAGED_DIRECTX_1.1"></span>DirectX 1.1 administrado<br /> | Los ensamblados directX de .NET están en desuso y no se recomiendan para su uso por las nuevas aplicaciones. Hay varias alternativas disponibles. Consulte <a href="https://walbourn.github.io/directx-and-net/">DirectX y .NET.</a> <br /> | 




 

El SDK de DirectX heredado está disponible para su descarga desde el Centro de descarga de [Microsoft](https://go.microsoft.com/fwlink/?LinkId=226640) si es necesario, pero no se recomienda su uso para nuevos proyectos.

> [!Note]  
> El SDK de DirectX no se puede instalar si tiene una versión determinada del paquete redistribuible de Visual C++ 2010 ya instalado. Para obtener más información sobre y una solución para corregir este problema, vea [el error "S1023" al instalar el SDK de DirectX (junio de 2010).](https://support.microsoft.com/kb/2728613)

 

## <a name="using-directx-sdk-projects-with-visual-studio"></a>Uso de proyectos del SDK de DirectX con Visual Studio

Los ejemplos del SDK de DirectX de junio de 2010 se admiten con SKU premium de Visual Studio (Microsoft Visual Studio Professional 2012, Microsoft Visual Studio Ultimate 2012, Microsoft Visual Studio Professional 2013 o Microsoft Visual Studio Ultimate 2013) en Windows 7 y las versiones Windows 8 y posteriores. Debido a la transición de encabezados y bibliotecas de DirectX al SDK de Windows, se necesitan cambios en la configuración del proyecto para compilar estos ejemplos correctamente con la forma en que el SDK de Windows 8 y versiones posteriores se empaquetan con las SKU de Visual Studio Premium.

Estos pasos también se aplican a sus propios proyectos que dependen del SDK de DirectX.

1.  Asegúrese de que la versión de junio de 2010 del SDK de DirectX esté instalada en el equipo de desarrollo. Si instala en un equipo que ejecuta Windows 8 y versiones posteriores, se le pedirá que habilite .NET 3.5 como instalación de requisitos previos en el SDK de DirectX.

    > [!Note]  
    > El SDK de DirectX no se puede instalar si tiene una versión determinada del paquete redistribuible de Visual C++ 2010 ya instalado. Para obtener más información sobre y una solución para corregir este problema, vea [el error "S1023" al instalar el SDK de DirectX (junio de 2010).](https://support.microsoft.com/kb/2728613)

     

2.  Asegúrese de que usa una de las SKU de Visual Studio premium. Microsoft Visual Studio Express 2012 para Windows 8 o Microsoft Visual Studio Express 2013 para Windows no compila las aplicaciones de escritorio Windows 8 y posteriores, como los ejemplos del SDK de DirectX. Para instalar una de las SKU Visual Studio premium, vaya a: [Visual Studio descargas y](https://www.microsoft.com/visualstudio/11/downloads) siga las instrucciones.

3.  Use el explorador de ejemplo del SDK de DirectX para instalar los archivos de proyecto para el ejemplo deseado. Abra el archivo de solución compatible Microsoft Visual Studio 2010 del ejemplo (con el sufijo **\_ 2010**).

4.  Si abre el ejemplo en un sistema que solo tiene instalado Microsoft Visual Studio 2012 o Microsoft Visual Studio 2013, aparece el mensaje siguiente: "Esta solución contiene uno o varios proyectos que usan una versión anterior del compilador y las bibliotecas de VC++. Cada proyecto se puede actualizar para usar el compilador VC++ bibliotecas (v110)." Elija la **opción** Actualizar de este cuadro de diálogo para actualizar antes de abrir el proyecto.

    De lo contrario, puede actualizar al compilador y las bibliotecas de Visual Studio 2012 o Visual Studio 2013 C++ 11 una vez cargados; para ello, haga clic con el botón derecho en la solución y elija Actualizar **VC++ proyectos**.

5.  D3DX no se considera la API canónica para usar Direct3D en Windows 8 y versiones posteriores y, por tanto, no se incluye con el SDK Windows correspondiente. Investigue soluciones alternativas para trabajar con la API de Direct3D. Para los proyectos heredados, como los ejemplos del SDK de DirectX de Windows 7 (y versiones anteriores), los pasos siguientes son necesarios para compilar aplicaciones con D3DX mediante el SDK de DirectX:

    1.  Modifique los **directorios** de VC++ del proyecto como se muestra a continuación para usar el orden correcto para las bibliotecas y encabezados del SDK.

        <dl> i. Abra **Propiedades** del proyecto y seleccione la **VC++ directorios.**  
        ii. Seleccione **Todas las configuraciones y Todas las plataformas.**  
        iii. Establezca estos directorios de la manera siguiente:

        -   Directorios ejecutables: **<inherit from parent or project defaults>** (en la lista desplegable del lado derecho)
        -   Directorios de include: **$(IncludePath);$(DXSDK \_ DIR)Include**
        -   Incluir directorios de biblioteca: **$(LibraryPath);$(DXSDK \_ DIR)Lib \\ x86**

          
        iv. Haga clic en **Aplicar**.  
        v. Elija la **plataforma x64**.  
        vi. Establezca el **directorio de biblioteca** como se muestra a continuación:

        -   Directorios de biblioteca: **$(LibraryPath);$(DXSDK \_ DIR)Lib \\ x64**

          
        </dl>

    2.  Siempre que se incluyan "d3dx9.h", "d3dx10.h" o "d3dx11.h" en el proyecto, asegúrese de incluir explícitamente "d3d9.h", "d3d10.h" y "dxgi.h", o "d3d11.h" y "dxgi.h" primero para asegurarse de que está seleccionando la versión más reciente. Puede deshabilitar la **advertencia C4005** si es necesario. sin embargo, esta advertencia indica que está usando la versión anterior de estos encabezados.
    3.  Quite todas las referencias a DXGIType.h en el proyecto. Este encabezado no existe en el SDK de Windows y la versión del SDK de DirectX entra en conflicto con el nuevo winerror.h.
    4.  Todos los archivos DLL D3DX se instalan en el equipo de desarrollo mediante la instalación del SDK de DirectX. Asegúrese de que las dependencias D3DX necesarias se redistribuyen con cualquier ejemplo o con la aplicación si se mueve a otra máquina.
    5.  Tenga en cuenta que las tecnologías de reemplazo para los usos actuales de D3DX11 incluyen [DirectXTex,](https://github.com/Microsoft/DirectXTex) [DirectXTK,](https://github.com/Microsoft/DirectXTK) [DirectXMesh](https://github.com/Microsoft/DirectXMesh)y [UVAtlas.](https://github.com/Microsoft/UVAtlas) D3DXMath se reemplaza por [DirectXMath.](./dxmath/directxmath-portal.md)

6.  Asegúrese de que usa la nueva versión del compilador de sombreadores HLSL observando las condiciones siguientes:

    1.  Al cambiar el directorio ejecutable según el paso 5, las compilaciones del proyecto usarán FXC desde Windows SDK. Tenga en cuenta que los archivos HLSL ahora se reconocen oficialmente por Visual Studio. Puede agregarlos como archivos de proyecto y establecer opciones del compilador a través del sistema del proyecto.

    2.  La invocación de la compilación en tiempo de ejecución a través del archivo DLL D3DX heredado usará la versión anterior incorrecta del compilador HLSL. Reemplace todas las referencias a las API D3DXCompile, \* D3DX10Compile y D3DX11Compile del código por la función \* \* D3DCompile de D3DCOMPILER \_46.DLL o D3DCOMPILER \_47.DLL.

    3.  Cualquier proyecto que use la compilación de sombreador en tiempo de ejecución debe tener D3DCOMPILERxx.DLL copia en la ruta de acceso \_ ejecutable local del proyecto. Este archivo DLL está disponible en este subgrupo de la instalación del SDK de Windows en **%ProgramFiles(x86)% \\ Windows Kits \\ 8.0 \\ Redist \\ D3D \\ <arch>** o **%ProgramFiles(x86)% \\ Windows Kits \\ 8.1 \\ Redist \\ D3D, \\ <arch>** donde es **<arch>** **x86** y **x64.**

        D3DCOMPILER46.DLL o \_ D3DCOMPILER47.DLL del SDK de Windows no es un componente del sistema y no debe copiarse en el directorio del Windows del \_ sistema. Puede redistribuir este archivo DLL a otros equipos con la aplicación como un archivo DLL en paralelo.

7.  Cualquier proyecto que use la API XInput y esté pensado para ejecutarse en Windows 7 o versiones anteriores de Windows debe usar la versión heredada (9.1.0) o deberá incluir explícitamente los encabezados y bibliotecas para este componente desde el SDK de DirectX. Encabezado XInput y XINPUT. LIB que se incluyen en el SDK de Windows solo tienen como destino la versión (1.4) que se incluye como parte de Windows 8 y versiones posteriores. El mismo encabezado se puede usar con XINPUT9 \_ 1 0.LIB para usar la versión heredada, que se incluye con versiones anteriores de \_ Windows. La versión heredada de XInput no detecta funcionalidades completas ni admite audio integrado en el controlador, por lo que si se requiere compatibilidad con estas características, debe usar la versión del SDK de DirectX (1.3).

    Para usar la API XInput de nivel inferior completo, debe usar directamente los encabezados XInput específicos `#include` del SDK de DirectX:

    `#include <%DXSDK_DIR%Include\xinput.h>`

    ... y en las opciones del vinculador para dependencias adicionales, vincule directamente a la biblioteca XInput del SDK de DirectX:

    **%DXSDK \_ DIR%Include \\ <arch> \\ xinput.lib**

    El archivo binario3.DLL XINPUT1 se instala en los directorios Windows del sistema mediante la instalación del \_ SDK de DirectX en el equipo de desarrollo. Tendrá que redistribuir este archivo binario con la aplicación mediante la instalación de DirectX Setup desde el SDK de DirectX.

8.  Cualquier proyecto que use la API XAudio2 y esté diseñado para ejecutarse en Windows 7 o versiones anteriores de Windows debe usar la versión anterior (9.1.0) o incluir explícitamente los encabezados y bibliotecas para este componente desde el SDK de DirectX. Los encabezados y bibliotecas XAudio2 que se incluyen con el SDK de Windows tienen como destino solo la versión (2.8) que se incluye como parte de Windows 8.

    Por ejemplo, con XAudio2, debe usar directamente los `#include` encabezados XAudio2 específicos del SDK de DirectX:

    `  #include <%DXSDK_DIR%Include\xaudio2.h> `

    ... y en las opciones del vinculador para dependencias adicionales, vincule directamente a la biblioteca XAudio2 del SDK de DirectX:

    **%DXSDK \_ DIR%Include \\ <arch> \\ xaudio2.lib**

    El archivo binario7.DLL XAUDIO2 se instala en los directorios Windows del sistema mediante la instalación del \_ SDK de DirectX en el equipo de desarrollo. Debe redistribuir estas bibliotecas con la aplicación mediante la instalación del programa de instalación de DirectX desde el SDK de DirectX.

9.  Si ha usado el SDK de DirectX con versiones anteriores de Visual Studio, es posible que la actualización de Visual Studio 2010 haya migrado la ruta de acceso del SDK de DirectX a la configuración predeterminada del proyecto. Se recomienda quitar esta configuración para evitar errores de compilación futuros. En el **directorio %USERPROFILE% \\ AppData \\ Local Microsoft \\ \\ MSBuild \\ v4.0,** modifique los archivos **Microsoft.Cpp.Win32.user** y **Microsoft.Cpp.x64.user** para quitar todas las referencias a las rutas de acceso DE DIR de DXSDK. \_ Como alternativa, puede quitar todo el nodo que contiene las entradas path como y para revertir a <PropertyGroup> <ExecutablePath> los valores predeterminados <IncludePath> estándar. Si no ve referencias a DIR de DXSDK \_ en estos archivos, no es necesario realizar ningún cambio.

10. Si la aplicación resultante admite Windows Vista con Service Pack 2 (SP2), así como Windows 7 y Windows 8 y versiones posteriores, establezca la definición de preprocesador **\_ denominada \_ WINNT win32** en 0x600. Si solo admite Windows 7 y Windows 8 versiones posteriores, esta establezca en 0x601.

    Por ejemplo:

    1.  Abra **Propiedades** del proyecto y seleccione **Preprocesador de C/C++.**  >  
    2.  Seleccione **Todas las configuraciones y** Todas las **plataformas.**
    3.  Vaya a la **sección Definiciones de preprocesador** y establezca \_ WIN32 \_ WINNT=0x600.
    4.  Haga clic en **Aplicar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Juegos para Windows y el SDK de DirectX**
</dt> <dt>

[¿Dónde está el SDK de DirectX (edición 2021)?](https://walbourn.github.io/where-is-the-directx-sdk-2021-edition/)
</dt> <dt>

[SDK de DirectX de una determinada edad](https://walbourn.github.io/directx-sdks-of-a-certain-age/)
</dt> <dt>

[Vida sin D3DX](https://walbourn.github.io/living-without-d3dx/)
</dt> </dl> 
