---
title: Creación de un dispositivo WARP
description: En este tema se muestra cómo crear un dispositivo de ALABEo que implementa un rasterizador de software de alta velocidad.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997109"
---
# <a name="how-to-create-a-warp-device"></a>Cómo: crear un dispositivo WARP

En este tema se muestra cómo crear un dispositivo de ALABEo que implementa un rasterizador de software de alta velocidad. Para crear un dispositivo de deformación, simplemente especifique que el dispositivo que está creando usará un controlador WARP. En este ejemplo se crea un dispositivo y una cadena de intercambio al mismo tiempo.

**Para crear un dispositivo WARP**

1.  Defina los parámetros iniciales de una cadena de intercambio.
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  Solicite un nivel de características que implemente las características que necesitará la aplicación. Se puede crear correctamente un dispositivo de deformación para niveles de características D3D de nivel de característica del **\_ \_ \_ \_ 1** al **nivel de características de D3d \_ \_ \_ 10 \_ 1** y a partir de Windows 8 para todos los niveles de características.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    Vea más información sobre los niveles de características en la enumeración de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .

3.  Cree el dispositivo mediante una llamada a [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



Tendrá que proporcionar la llamada de API con el tipo de controlador WARP desde la enumeración de [**\_ \_ tipo de controlador D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Una vez que el método se ejecuta correctamente, devolverá una interfaz de la cadena de intercambio, una interfaz de dispositivo, un puntero al nivel de característica que ha concedido el controlador y una interfaz de contexto inmediata.

Para obtener información sobre las limitaciones de la creación de un dispositivo de deformación en determinados niveles de características, vea [limitaciones para crear dispositivos de Hipersalto y de referencia](overviews-direct3d-11-devices-limitations.md).

## <a name="new-for-windows-8"></a>Novedades de Windows 8

Cuando el adaptador de pantalla principal de un equipo es el "adaptador de pantalla básico de Microsoft" (adaptador de deformación), ese equipo también tiene un segundo adaptador. Este segundo adaptador es el dispositivo de solo representación que no tiene salidas de presentación. Para obtener más información sobre el dispositivo de solo representación, consulte [nueva información en Windows 8 acerca de la enumeración de adaptadores](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 