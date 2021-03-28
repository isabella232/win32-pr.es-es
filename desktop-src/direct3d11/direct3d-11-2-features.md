---
title: Características de Direct3D 11,2
description: La siguiente funcionalidad se ha agregado en Direct3D 11,2, que se incluye con Windows 8.1, Windows RT 8,1 y Windows Server 2012 R2.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299b720bfb91297043c8e7d76beb50067eb64e17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984026"
---
# <a name="direct3d-112-features"></a>Características de Direct3D 11,2

La siguiente funcionalidad se ha agregado en Direct3D 11,2, que se incluye con Windows 8.1, Windows RT 8,1 y Windows Server 2012 R2.

-   [Recursos en mosaico](#tiled-resources)
    -   [Comprobar la compatibilidad con los recursos en mosaico](#check-tiled-resources-support)
-   [Compatibilidad ampliada con dispositivos dewarps](#extended-support-for-warp-devices)
-   [Anotar comandos de gráficos](#annotate-graphics-commands)
-   [Vinculación de sombreador HLSL](#hlsl-shader-linking)
    -   [Gráfico de vinculación de funciones (FLG)](#function-linking-graph-flg)
-   [Compilador HLSL de bandeja de entrada](#inbox-hlsl-compiler)
-   [Temas relacionados](#related-topics)

## <a name="tiled-resources"></a>Recursos en mosaico

Direct3D 11,2 le permite crear recursos en mosaico que se pueden considerar como recursos lógicos de gran tamaño que utilizan pequeñas cantidades de memoria física. Los recursos en mosaico son útiles (por ejemplo) con el terreno en los juegos y la interfaz de usuario de la aplicación.

Los recursos en mosaico se crean especificando la marca de [**\_ \_ \_ mosaico varios de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . Para trabajar con un recurso en mosaico, use estas API:

-   [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3D11 \_ Característica de depuración \_ \_ deshabilitar el \_ \_ \_ \_ seguimiento \_ de asignación de \_ recursos en mosaico y** la marca de validación con [ **ID3D11Debug:: SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Para obtener más información sobre los recursos en mosaico, vea [recursos en mosaico](tiled-resources.md).

### <a name="check-tiled-resources-support"></a>Comprobar la compatibilidad con los recursos en mosaico

Antes de usar recursos en mosaico, debe averiguar si el dispositivo admite recursos en mosaico. Aquí se muestra cómo comprobar la compatibilidad con los recursos en mosaico:


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



## <a name="extended-support-for-warp-devices"></a>Compatibilidad ampliada con dispositivos dewarps

Direct3D 11,2 extiende la compatibilidad con los dispositivos [Dewarps](overviews-direct3d-11-devices-create-warp.md) , que se crean pasando el [**\_ tipo de controlador D3D \_ \_ Warp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) en el parámetro *DriverType* de [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice). El representador de dewarp software en Direct3D 11,2 agrega compatibilidad completa con el [nivel de característica](overviews-direct3d-11-devices-downlevel-intro.md) 11 1 de Direct3D \_ , incluidos [los recursos en mosaico](#tiled-resources), [**IDXGIDevice3:: Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim), superficies compartidas de BCn, minblend y mapa predeterminado. También se ha habilitado la compatibilidad con [Double](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) en sombreadores HLSL junto con la compatibilidad con 16X MSAA.

## <a name="annotate-graphics-commands"></a>Anotar comandos de gráficos

Direct3D 11,2 le permite anotar comandos de gráficos con estas API:

-   [**ID3D11DeviceContext2::IsAnnotationEnabled**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2::BeginEventInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2::SetMarkerInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2::EndEvent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>Vinculación de sombreador HLSL

Windows 8.1 agrega una compilación independiente y una vinculación de sombreadores HLSL, que permite a los programadores de gráficos crear funciones HLSL precompiladas, empaquetarlas en bibliotecas y vincularlas a los sombreadores completos en tiempo de ejecución. Esto es esencialmente un equivalente de compilación, bibliotecas y vinculación independiente de C/C++, y permite a los programadores crear código HLSL precompilado cuando hay más información disponible para finalizar el cálculo. Para obtener más información sobre cómo usar la vinculación del sombreador, vea uso de la [vinculación del sombreador](/windows/desktop/direct3dhlsl/using-shader-linking).

Siga estos pasos para crear un sombreador final mediante la vinculación dinámica en tiempo de ejecución.

**Para crear y usar la vinculación del sombreador**

1.  Cree un objeto del enlazador [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) , que representa un contexto de vinculación. No se puede usar un solo contexto para generar varios sombreadores; un contexto de vinculación se usa para generar un sombreador único y, a continuación, se produce el contexto de vinculación.
2.  Use [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) para cargar y establecer bibliotecas desde sus blobs de biblioteca.
3.  Use [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) para cargar y establecer un BLOB de sombreador de entrada o crear un [sombreador de FLG](#function-linking-graph-flg).
4.  Use [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) para crear objetos [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) y, a continuación, llame a las funciones de estos objetos para volver a enlazar los recursos a sus ranuras finales.
5.  Agregue las bibliotecas al vinculador y, a continuación, llame a [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) para generar el código de byte del sombreador final que se puede cargar y usar en el tiempo de ejecución de la misma manera que un sombreador vinculado y precompilado completamente.

### <a name="function-linking-graph-flg"></a>Gráfico de vinculación de funciones (FLG)

Windows 8.1 también agrega el gráfico de vinculación de funciones (FLG). Puede usar FLG para construir sombreadores que consten de una secuencia de llamadas a funciones precompiladas que pasan valores entre sí. Cuando se usa FLG, no es necesario escribir HLSL e invocar el compilador de HLSL. En su lugar, la estructura del sombreador se especifica mediante programación con las llamadas a la API de C++. Los nodos FLG representan las firmas de entrada y salida y las invocaciones de las funciones de biblioteca precompiladas. El orden de registro de los nodos de llamada de función define la secuencia de invocaciones. El nodo de firma de entrada debe especificarse primero, mientras que el nodo de firma de salida debe especificarse en último lugar. Los bordes de FLG definen cómo se pasan los valores de un nodo a otro. Los tipos de datos de los valores pasados deben ser iguales; no hay ninguna conversión de tipo implícita. Las reglas de forma y permutación siguen el comportamiento de HLSL y los valores solo se pueden pasar hacia delante en esta secuencia. Para obtener información sobre la API de FLG, consulte [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).

## <a name="inbox-hlsl-compiler"></a>Compilador HLSL de bandeja de entrada

El compilador de HLSL ahora está en la bandeja de entrada en Windows 8.1 y versiones posteriores. Ahora, la mayoría de las API para la programación del sombreador se pueden usar en aplicaciones de la tienda Windows compiladas para Windows 8.1 y versiones posteriores. Muchas API para la programación del sombreador no se pueden usar en aplicaciones de la tienda Windows compiladas para Windows 8; las páginas de referencia de estas API se marcaron con una nota. Pero algunas API de sombreador (por ejemplo, [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) se pueden seguir usando solo para desarrollar aplicaciones de la tienda Windows y no en las aplicaciones que se envían a la tienda Windows. las páginas de referencia de estas API se siguen marcando con una nota.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Novedades de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 