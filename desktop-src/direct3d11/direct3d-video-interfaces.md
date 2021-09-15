---
title: Interfaces de vídeo de Direct3D
description: En este tema se enumeran las interfaces de vídeo de Direct3D que están disponibles en Direct3D 9Ex y que se admiten en Windows 7 y versiones posteriores de sistemas operativos cliente de Windows y en Windows Server 2008 R2 y versiones posteriores de sistemas operativos Windows Server.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465404"
---
# <a name="direct3d-video-interfaces"></a>Interfaces de vídeo de Direct3D

En este tema se enumeran las interfaces de vídeo de Direct3D que están disponibles en Direct3D 9Ex y que se admiten en Windows 7 y versiones posteriores de sistemas operativos cliente de Windows y en Windows Server 2008 R2 y versiones posteriores de sistemas operativos Windows Server. Puede usar estas interfaces y sus métodos para obtener las funcionalidades de protección de contenido de vídeo del controlador de gráficos y las funcionalidades de hardware de superposición de un dispositivo Direct3D. También puede usar estas interfaces y sus métodos para proteger el contenido de vídeo. Estas interfaces y sus métodos se definen en D3d9.h y se describen [en Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) sección.



| Interfaz                                                                                                                                                                                                                             | Descripción                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)<br/>           | Consulta las funcionalidades de hardware de superposición de un dispositivo Direct3D.<br/>                                                     |
| <span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)<br/> | Proporciona un canal de comunicación con el controlador de gráficos o el entorno de ejecución de Direct3D.<br/>                                  |
| <span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)<br/>                                    | Representa una sesión criptográfica que se usa para acceder a una superficie protegida.<br/>                                      |
| <span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)<br/>                                              | Permite que una aplicación use servicios de cifrado y protección de contenido implementados por un controlador de gráficos.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Efectos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)](dx-graphics-overviews.md)
</dt> </dl>

 

