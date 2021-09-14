---
title: Características de Direct3D 11.2
description: Se ha agregado la siguiente funcionalidad en Direct3D 11.2, que se incluye con Windows 8.1, Windows RT 8.1 y Windows Server 2012 R2.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299b720bfb91297043c8e7d76beb50067eb64e17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884601"
---
# <a name="direct3d-112-features"></a>Características de Direct3D 11.2

Se ha agregado la siguiente funcionalidad en Direct3D 11.2, que se incluye con Windows 8.1, Windows RT 8.1 y Windows Server 2012 R2.

-   [Recursos en mosaico](#tiled-resources)
    -   [Comprobación de la compatibilidad con recursos en mosaico](#check-tiled-resources-support)
-   [Compatibilidad ampliada con dispositivos WARP](#extended-support-for-warp-devices)
-   [Anotación de comandos de gráficos](#annotate-graphics-commands)
-   [Vinculación del sombreador HLSL](#hlsl-shader-linking)
    -   [Gráfico de vinculación de funciones (FLG)](#function-linking-graph-flg)
-   [Compilador HLSL de bandeja de entrada](#inbox-hlsl-compiler)
-   [Temas relacionados](#related-topics)

## <a name="tiled-resources"></a>Recursos en mosaico

Direct3D 11.2 permite crear recursos en mosaico que se pueden pensar como recursos lógicos grandes que usan pequeñas cantidades de memoria física. Los recursos en mosaico son útiles (por ejemplo) con el terreno en juegos y la interfaz de usuario de la aplicación.

Los recursos en mosaico se crean especificando la [**marca \_ \_ MISC \_ TILED DE RECURSOS D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) Para trabajar con recursos en mosaico, use estas API:

-   [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2::TiledResourceBarresourceBarresource**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3D11 \_ DEBUG \_ FEATURE DISABLE TILED RESOURCE MAPPING TRACKING AND VALIDATION \_ \_ \_ \_ \_ \_ \_ flag** with [ **ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Para obtener más información sobre los recursos en mosaico, consulte [Recursos en mosaico.](tiled-resources.md)

### <a name="check-tiled-resources-support"></a>Comprobación de la compatibilidad con recursos en mosaico

Antes de usar los recursos en mosaico, debe averiguar si el dispositivo admite recursos en mosaico. A continuación se muestra cómo comprobar la compatibilidad con los recursos en mosaico:


```C++
HRESULT hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    creationFlags,              // Set debug and Direct2D compatibility flags.
    featureLevels,              // List of feature levels this app can support.
    ARRAYSIZE(featureLevels),   // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_d3dFeatureLevel,         // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (SUCCEEDED(hr))
{
    D3D11_FEATURE_DATA_D3D11_OPTIONS1 featureData;
    DX::ThrowIfFailed(
        device->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS1, &featureData, sizeof(featureData))
        );

    m_tiledResourcesTier = featureData.TiledResourcesTier;
}
```



## <a name="extended-support-for-warp-devices"></a>Compatibilidad ampliada con dispositivos WARP

Direct3D 11.2 amplía la compatibilidad con dispositivos [WARP,](overviews-direct3d-11-devices-create-warp.md) que se crean pasando [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) en el parámetro *DriverType* [**de D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice). El representador de software WARP en Direct3D 11.2 agrega compatibilidad completa con el nivel [de](overviews-direct3d-11-devices-downlevel-intro.md) característica 11 1 de Direct3D, incluidos los recursos en mosaico \_ , [**IDXGIDevice3::Trim,**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim)las superficies BCn compartidas, minblend y el valor predeterminado del mapa. [](#tiled-resources) [También](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) se ha habilitado la compatibilidad doble en sombreadores HLSL junto con la compatibilidad con MSAA 16x.

## <a name="annotate-graphics-commands"></a>Anotación de comandos de gráficos

Direct3D 11.2 permite anotar comandos de gráficos con estas API:

-   [**ID3D11DeviceContext2::IsAnnotationEnabled**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2::BeginEventInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2::SetMarkerInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2::EndEvent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>Vinculación del sombreador HLSL

Windows 8.1 agrega compilación y vinculación independientes de sombreadores HLSL, lo que permite a los programadores de gráficos crear funciones HLSL precompiladas, empaquetarlos en bibliotecas y vincularlos a sombreadores completos en tiempo de ejecución. Esto es básicamente un equivalente de compilación, bibliotecas y vinculación independientes de C/C++, y permite a los programadores crear código HLSL precompilado cuando haya más información disponible para finalizar el cálculo. Para obtener más información sobre cómo usar la vinculación de sombreador, vea [Usar la vinculación de sombreador.](/windows/desktop/direct3dhlsl/using-shader-linking)

Complete estos pasos para crear un sombreador final mediante la vinculación dinámica en tiempo de ejecución.

**Para crear y usar la vinculación de sombreador**

1.  Cree un [**objeto de vinculador ID3D11Linker,**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) que representa un contexto de vinculación. No se puede usar un único contexto para generar varios sombreadores; Un contexto de vinculación se usa para generar un solo sombreador y, a continuación, se descarta el contexto de vinculación.
2.  Use [**D3DLoadModule para**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) cargar y establecer bibliotecas desde sus blobs de biblioteca.
3.  Use [**D3DLoadModule para**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) cargar y establecer un blob de sombreador de entrada, o cree un [sombreador FLG](#function-linking-graph-flg).
4.  Use [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) para crear objetos [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) y, a continuación, llame a funciones en estos objetos para volver a enlabinar los recursos a sus ranuras finales.
5.  Agregue las bibliotecas al enlazador y, a continuación, llame a [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) para generar el código de bytes del sombreador final que se puede cargar y usar en el tiempo de ejecución como un sombreador totalmente precompilado y vinculado.

### <a name="function-linking-graph-flg"></a>Gráfico de vinculación de funciones (FLG)

Windows 8.1 agrega también la función de Graph (FLG). Puede usar FLG para construir sombreadores que constan de una secuencia de invocaciones de función precompiladas que pasan valores entre sí. Cuando se usa FLG, no es necesario escribir HLSL e invocar el compilador HLSL. En su lugar, la estructura del sombreador se especifica mediante programación mediante llamadas API de C++. Los nodos FLG representan firmas de entrada y salida e invocaciones de funciones de biblioteca precompiladas. El orden de registro de los nodos de llamada de función define la secuencia de invocaciones. El nodo de firma de entrada debe especificarse primero, mientras que el nodo de firma de salida debe especificarse en último lugar. Los bordes flg definen cómo se pasan los valores de un nodo a otro. Los tipos de datos de los valores pasados deben ser los mismos; no hay ninguna conversión implícita de tipos. Las reglas de forma y desdoba siguen el comportamiento hlsl y los valores solo se pueden pasar hacia delante en esta secuencia. Para obtener información sobre la API de FLG, [**vea ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).

## <a name="inbox-hlsl-compiler"></a>Compilador HLSL de bandeja de entrada

El compilador HLSL ahora está en bandeja de Windows 8.1 y versiones posteriores. Ahora, la mayoría de las API para la programación de sombreadores se pueden usar en Windows Store que se compilan para Windows 8.1 y versiones posteriores. Muchas API para la programación de sombreadores no se podían usar en Windows Store que se compilaban para Windows 8; las páginas de referencia de estas API se marcaron con una nota. Sin embargo, algunas API de sombreador (por ejemplo, [**D3DCompileFromFile)**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)solo se pueden usar para desarrollar aplicaciones de la Tienda Windows y no en aplicaciones que envíe a Windows Store. las páginas de referencia de estas API siguen marcadas con una nota.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 