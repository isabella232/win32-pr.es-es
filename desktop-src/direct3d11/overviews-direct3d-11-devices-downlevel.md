---
title: Direct3D 11 en hardware de nivel inferior
description: En esta sección se describe cómo Direct3D 11 está diseñado para admitir hardware nuevo y existente, de DirectX 9 a DirectX 11.
ms.assetid: 9a1ca4ff-df3d-46e5-8895-37199523343e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f730a43db803e1e5198794167d0078a5b2896f6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063767"
---
# <a name="direct3d-11-on-downlevel-hardware"></a>Direct3D 11 en hardware de nivel inferior

En esta sección se describe cómo Direct3D 11 está diseñado para admitir hardware nuevo y existente, de DirectX 9 a DirectX 11.

En este diagrama se muestra cómo Direct3D 11 admite hardware nuevo y existente.

![diagrama del hardware compatible con Direct3d 11](images/d3d11-on-downlevel-hardware.png)

Con Direct3D 11, se introduce un nuevo paradigma denominado niveles de características. Un nivel de característica es un conjunto bien definido de funcionalidad de GPU. Con un nivel de característica, puede dirigirse a una aplicación de Direct3D para que se ejecute en una versión de nivel inferior del hardware de Direct3D.

En la sección 10Level9 Reference (Referencia de [10Level9)](d3d11-graphics-reference-10level9.md) se enumeran las diferencias entre el comportamiento de los distintos métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en varios niveles de características de 10Level9.


## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                  | Descripción                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Niveles de característica de Direct3D](overviews-direct3d-11-devices-downlevel-intro.md)<br/>                                | En este tema se deba a los niveles de características de Direct3D.<br/>                                                                                                                       |
| [Excepciones](overviews-direct3d-11-devices-downlevel-exceptions.md)<br/>                                        | En este tema se describen las excepciones al usar Direct3D 11 en hardware de nivel inferior. <br/>                                                                                      |
| [Sombreadores de proceso en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel-compute-shaders.md)<br/>        | En este tema se describe [](direct3d-11-advanced-stages-compute-shader.md) cómo usar sombreadores de proceso en una aplicación Direct3D 11 en hardware direct3D 10.<br/>             |
| [Evitar los SRV del sombreador de píxeles NULL no deseados](overviews-direct3d-11-devices-downlevel-prevent-null-srvs.md)<br/> | En este tema se describe cómo  evitar que el controlador que recibe vistas de recursos de sombreador NULL (SRV) incluso cuando los SRV que no son **NULL** estén enlazados a la fase del sombreador de píxeles.<br/> |



 

## <a name="how-to-topics-about-feature-levels"></a>Temas sobre los niveles de características



| Tema                                                                                                                                                                                                                                                                   | Descripción                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="How_To__Get_the_Device_Feature_Level"></span><span id="how_to__get_the_device_feature_level"></span><span id="HOW_TO__GET_THE_DEVICE_FEATURE_LEVEL"></span>[Cómo: Obtener el nivel de característica de dispositivo](overviews-direct3d-11-devices-downlevel-get.md)<br/> | Cómo obtener un nivel de característica.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





