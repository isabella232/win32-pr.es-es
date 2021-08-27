---
title: Cómo obtener el nivel de característica de dispositivo
description: En estos temas se muestra cómo obtener el nivel de características más alto admitido por un dispositivo.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac21d00aeef8ae6c82ffd9f55a40415b6af1d0a780cc6878d8c30bf453457eb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119605"
---
# <a name="how-to-get-the-device-feature-level"></a>Cómo: Obtener el nivel de característica de dispositivo

En estos temas se muestra cómo obtener el nivel [de característica más alto](overviews-direct3d-11-devices-downlevel-intro.md) compatible con un [dispositivo](overviews-direct3d-11-devices-intro.md). Los dispositivos Direct3D 11 admiten un conjunto fijo de niveles de características que se definen en la [**enumeración D3D \_ FEATURE \_ LEVEL.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) Cuando conozca el nivel de [características más alto](overviews-direct3d-11-devices-downlevel-intro.md) admitido por un dispositivo, puede ejecutar rutas de acceso de código adecuadas para ese dispositivo.

**Para obtener el nivel de características del dispositivo**

1.  Llame a la [**función D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o a las funciones [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) y especifique **NULL** para el *parámetro ppDevice.* Puede hacerlo antes de crear el dispositivo.

    \- O bien

    Llame [**a ID3D11Device::GetFeatureLevel después**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) de la creación del dispositivo.

2.  Examine el valor de la enumeración [**D3D \_ FEATURE \_ LEVEL devuelta**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) del último paso para determinar el nivel de característica admitido.

En el ejemplo de código siguiente se muestra cómo determinar el nivel de característica más alto admitido mediante una llamada a la [**función D3D11CreateDevice.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) **D3D11CreateDevice almacena** el nivel de característica más alto admitido en la variable FeatureLevel. Puede usar este código para examinar el valor del tipo enumerado [**D3D \_ FEATURE \_ LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) que **devuelve D3D11CreateDevice.** Tenga en cuenta que este código enumera todos los niveles de características explícitamente (para Direct3D 11.1 y Direct3D 11.2).

> [!Note]  
> Si el tiempo de ejecución de Direct3D 11.1 está presente en el equipo y *pFeatureLevels* está establecido en **NULL,** esta función no creará un dispositivo [**D3D \_ FEATURE LEVEL \_ \_ \_ 11 1.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) Para crear un dispositivo **D3D \_ FEATURE \_ LEVEL \_ \_ 11 1,** debe proporcionar explícitamente una matriz **D3D \_ FEATURE \_ LEVEL** que incluya **D3D \_ FEATURE LEVEL \_ \_ 11 \_ 1**. Si proporciona una matriz D3D FEATURE LEVEL que contiene **D3D \_ FEATURE \_ LEVEL \_ 11 \_ 1** en un equipo que no tiene instalado el entorno de ejecución de Direct3D 11.1, esta función produce un error inmediatamente con E **\_ \_** \_ INVALIDARG.

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



En la sección 10Level9 Reference (Referencia de [10Level9)](d3d11-graphics-reference-10level9.md) se enumeran las diferencias entre el comportamiento de los distintos métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en varios niveles de características de 10Level9.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




