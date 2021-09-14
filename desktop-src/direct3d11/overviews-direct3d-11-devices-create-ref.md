---
title: Cómo crear un dispositivo de referencia
description: En este tema se muestra cómo crear un dispositivo de referencia que implementa una implementación de software altamente precisa del tiempo de ejecución.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160463"
---
# <a name="how-to-create-a-reference-device"></a>Cómo: Crear un dispositivo de referencia

En este tema se muestra cómo crear un dispositivo de referencia que implementa una implementación de software altamente precisa del tiempo de ejecución. Para crear un dispositivo de referencia, simplemente especifique que el dispositivo que está creando usará un controlador de referencia. En este ejemplo se crea un dispositivo y una cadena de intercambio al mismo tiempo.

**Para crear un dispositivo de referencia**

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

    

2.  Solicite un nivel de característica que implemente las características que necesitará la aplicación. Se puede crear correctamente un dispositivo de referencia para el entorno de ejecución de Direct3D 11.

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    Consulte más información sobre los niveles de características en la [**enumeración D3D \_ FEATURE \_ LEVEL.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)

3.  Cree el dispositivo mediante una llamada [**a D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
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



Deberá proporcionar la llamada API con el tipo de controlador de referencia de la [**enumeración D3D \_ DRIVER \_ TYPE.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) Una vez que el método se realiza correctamente, devolverá una interfaz de cadena de intercambio, una interfaz de dispositivo, un puntero al nivel de característica concedido por el controlador y una interfaz de contexto inmediata.

Para obtener información sobre las limitaciones de creación de un dispositivo de referencia en determinados niveles de características, vea [Limitaciones de creación de WARP y dispositivos de referencia.](overviews-direct3d-11-devices-limitations.md) [Uso de Direct3D 11](how-to-use-direct3d-11.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




