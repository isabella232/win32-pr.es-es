---
title: Interfaces de vídeo de Direct3D
description: En este tema se enumeran las interfaces de vídeo de Direct3D que están disponibles en Direct3D 9Ex y que se admiten en Windows 7 y versiones posteriores de los sistemas operativos de cliente Windows y en Windows Server 2008 R2 y versiones posteriores de los sistemas operativos Windows Server.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487830"
---
# <a name="direct3d-video-interfaces"></a><span data-ttu-id="55d25-103">Interfaces de vídeo de Direct3D</span><span class="sxs-lookup"><span data-stu-id="55d25-103">Direct3D Video Interfaces</span></span>

<span data-ttu-id="55d25-104">En este tema se enumeran las interfaces de vídeo de Direct3D que están disponibles en Direct3D 9Ex y que se admiten en Windows 7 y versiones posteriores de los sistemas operativos de cliente Windows y en Windows Server 2008 R2 y versiones posteriores de los sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="55d25-104">This topic lists the Direct3D video interfaces that are available in Direct3D 9Ex and that are supported on Windows 7 and later versions of Windows client operating systems and on Windows Server 2008 R2 and later versions of Windows server operating systems.</span></span> <span data-ttu-id="55d25-105">Puede utilizar estas interfaces y sus métodos para obtener las capacidades de protección del contenido de vídeo del controlador de gráficos y las capacidades de hardware de superposición de un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="55d25-105">You can use these interfaces and their methods to obtain the video content protection capabilities of the graphics driver and the overlay hardware capabilities of a Direct3D device.</span></span> <span data-ttu-id="55d25-106">También puede utilizar estas interfaces y sus métodos para proteger el contenido de vídeo.</span><span class="sxs-lookup"><span data-stu-id="55d25-106">You can also use these interfaces and their methods to protect video content.</span></span> <span data-ttu-id="55d25-107">Estas interfaces y sus métodos se definen en d3d9. h y se describen en la sección [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .</span><span class="sxs-lookup"><span data-stu-id="55d25-107">These interfaces and their methods are defined in D3d9.h and described in the [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) section.</span></span>



| <span data-ttu-id="55d25-108">Interfaz</span><span class="sxs-lookup"><span data-stu-id="55d25-108">Interface</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="55d25-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="55d25-109">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55d25-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span><span class="sxs-lookup"><span data-stu-id="55d25-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span></span><br/>           | <span data-ttu-id="55d25-111">Consulta las capacidades de hardware de superposición de un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="55d25-111">Queries the overlay hardware capabilities of a Direct3D device.</span></span><br/>                                                     |
| <span data-ttu-id="55d25-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span><span class="sxs-lookup"><span data-stu-id="55d25-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span></span><br/> | <span data-ttu-id="55d25-113">Proporciona un canal de comunicación con el controlador de gráficos o el tiempo de ejecución de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="55d25-113">Provides a communication channel with the graphics driver or the Direct3D runtime.</span></span><br/>                                  |
| <span data-ttu-id="55d25-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span><span class="sxs-lookup"><span data-stu-id="55d25-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span></span><br/>                                    | <span data-ttu-id="55d25-115">Representa una sesión de cifrado que se usa para tener acceso a una superficie protegida.</span><span class="sxs-lookup"><span data-stu-id="55d25-115">Represents a cryptographic session that is used to access a protected surface.</span></span><br/>                                      |
| <span data-ttu-id="55d25-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span><span class="sxs-lookup"><span data-stu-id="55d25-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span></span><br/>                                              | <span data-ttu-id="55d25-117">Permite que una aplicación use los servicios de cifrado y protección de contenido que se implementan mediante un controlador de gráficos.</span><span class="sxs-lookup"><span data-stu-id="55d25-117">Enables an application to use content protection and encryption services that are implemented by a graphics driver.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="55d25-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="55d25-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55d25-119">Efectos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="55d25-119">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="55d25-120">Programming Guide for Direct3D 11 (Guía de programación para Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="55d25-120">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

