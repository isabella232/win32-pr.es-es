---
title: Cómo obtener el nivel de características del dispositivo
description: En este tema se muestra cómo obtener el nivel de características más alto compatible con un dispositivo.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903752"
---
# <a name="how-to-get-the-device-feature-level"></a>Cómo: obtener el nivel de características del dispositivo

En este tema se muestra cómo obtener el [nivel de características](overviews-direct3d-11-devices-downlevel-intro.md) más alto compatible con un [dispositivo](overviews-direct3d-11-devices-intro.md). Los dispositivos de Direct3D 11 admiten un conjunto fijo de niveles de características que se definen en la enumeración de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Cuando conozca el nivel de [característica](overviews-direct3d-11-devices-downlevel-intro.md) más alto compatible con un dispositivo, puede ejecutar rutas de acceso de código apropiadas para ese dispositivo.

**Para obtener el nivel de características del dispositivo**

1.  Llame a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o a las funciones [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) al especificar **null** para el parámetro *ppDevice* . Puede hacerlo antes de crear el dispositivo.

    \- o -

    Llame a [**ID3D11Device:: GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) después de la creación del dispositivo.

2.  Examine el valor de la enumeración de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) devuelta desde el último paso para determinar el nivel de característica admitido.

En el ejemplo de código siguiente se muestra cómo determinar el nivel de característica compatible más alto mediante una llamada a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) . **D3D11CreateDevice** almacena el nivel de características admitido más alto en la variable FeatureLevel. Puede usar este código para examinar el valor del tipo enumerado del [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) que devuelve **D3D11CreateDevice** . Tenga en cuenta que en este código se enumeran todos los niveles de características explícitamente (para Direct3D 11,1 y Direct3D 11,2).

> [!Note]  
> Si el tiempo de ejecución de Direct3D 11,1 está presente en el equipo y *pFeatureLevels* está establecido en **null**, esta función no creará un dispositivo de [**nivel de característica de D3D \_ \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Para crear un dispositivo de **nivel de característica de D3D \_ \_ \_ 11 \_ 1** , debe proporcionar explícitamente una matriz de **\_ \_ nivel de característica D3D** que incluya el **nivel de característica de D3D \_ \_ \_ 11 \_ 1**. Si proporciona una matriz **de \_ \_ nivel de característica D3D** que contiene el **nivel de característica de D3D \_ \_ \_ 11 \_ 1** en un equipo que no tiene instalado el tiempo de ejecución de Direct3D 11,1, esta función genera un error inmediatamente con E \_ INVALIDARG.

 


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



En la sección de [referencia de 10Level9 se](d3d11-graphics-reference-10level9.md) enumeran las diferencias entre el comportamiento de varios métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en distintos niveles de características de 10Level9.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




