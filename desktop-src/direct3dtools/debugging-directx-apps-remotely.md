---
title: Depuración remota de aplicaciones DirectX
description: Puede usar Visual Studio y el SDK Windows 8 para depurar aplicaciones directX de forma remota.
ms.assetid: CA471465-47C2-4706-B391-C9E6C2CD69D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f9fd97519bb88a0a89206e5a8c3aa43cf990948cb9aa8c9dd40379c53ed1a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505680"
---
# <a name="debugging-directx-apps-remotely"></a>Depuración remota de aplicaciones DirectX

Puede usar Visual Studio y el SDK Windows 8 para depurar aplicaciones directX de forma remota. El SDK Windows 8 proporciona un conjunto de componentes que admiten el desarrollo de DirectX y proporcionan comprobación de errores y validación de parámetros, además de la depuración que Visual Studio proporciona. Estos componentes son D3D11 \_1SDKLayers.dll, D2D1Debug1.dll y Dxgidebug.dll.

Si desea depurar de forma remota en un equipo sin el SDK de Windows 8 instalado y desea esta funcionalidad de depuración adicional, debe instalar el paquete de depuración remota adecuado para la arquitectura en la que desea depurar. Los Windows instalador de instalación de `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` instalan la compatibilidad adecuada.

Para habilitar las funcionalidades de depuración adicionales para las aplicaciones de Direct2D, use este código:

```cpp
    D2D1_FACTORY_OPTIONS options;
    ZeroMemory(&options, sizeof(D2D1_FACTORY_OPTIONS));

#if defined(_DEBUG)
     // If the project is in a debug build, enable Direct2D debugging via SDK Layers.
    options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
#endif

    DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );         
```

Para habilitar las funcionalidades de depuración adicionales para las aplicaciones de Direct3D, use este código:

```cpp
    // This flag supports surfaces with a different color channel ordering than the API default.
    // It is recommended usage, and is required for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    ComPtr<IDXGIDevice> dxgiDevice;

#if defined(_DEBUG)
    // If the project is in a debug build, enable debugging via SDK Layers with this flag.
    creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          // leave as 0 unless software device
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of entries in above list
            D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION for modern
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );
```

Para obtener más información sobre la depuración de aplicaciones de Direct2D, vea [Capa de depuración de Direct2D.](/windows/desktop/Direct2D/direct2ddebuglayer-portal)

Para obtener más información sobre la depuración de aplicaciones de Direct3D, vea [Capa de depuración de Direct3D.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers)