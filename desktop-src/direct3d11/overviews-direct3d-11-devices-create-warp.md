---
title: Cómo crear un dispositivo WARP
description: En este tema se muestra cómo crear un dispositivo WARP que implementa un rasterizador de software de alta velocidad.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465666"
---
# <a name="how-to-create-a-warp-device"></a>Cómo: Crear un dispositivo WARP

En este tema se muestra cómo crear un dispositivo WARP que implementa un rasterizador de software de alta velocidad. Para crear un dispositivo WARP, simplemente especifique que el dispositivo que está creando usará un controlador WARP. En este ejemplo se crea un dispositivo y una cadena de intercambio al mismo tiempo.

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

    

2.  Solicite un nivel de característica que implemente las características que necesitará la aplicación. Se puede crear correctamente un dispositivo WARP para los niveles de características **D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1** a **D3D \_ FEATURE LEVEL \_ \_ 10 \_ 1** y a partir de Windows 8 para todos los niveles de características.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    Consulte más información sobre los niveles de características en la [**enumeración D3D \_ FEATURE \_ LEVEL.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)

3.  Cree el dispositivo mediante una llamada [**a D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


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



Deberá proporcionar la llamada API con el tipo de controlador WARP de la [**enumeración D3D \_ DRIVER \_ TYPE.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) Una vez que el método se realiza correctamente, devolverá una interfaz de cadena de intercambio, una interfaz de dispositivo, un puntero al nivel de característica concedido por el controlador y una interfaz de contexto inmediata.

Para obtener información sobre las limitaciones de creación de un dispositivo WARP en determinados niveles de características, vea [Limitaciones de creación de DISPOSITIVOs de referencia y WARP.](overviews-direct3d-11-devices-limitations.md)

## <a name="new-for-windows-8"></a>Novedades de Windows 8

Cuando el adaptador de pantalla principal de un equipo es el "Adaptador de pantalla básico de Microsoft" (adaptador WARP), ese equipo también tiene un segundo adaptador. Este segundo adaptador es el dispositivo de solo representación que no tiene salidas de pantalla. Para obtener más información sobre el dispositivo de solo representación, vea nueva información [en Windows 8 sobre la enumeración de adaptadores](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 