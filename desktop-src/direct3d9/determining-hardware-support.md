---
description: Direct3D proporciona las siguientes funciones para determinar la compatibilidad de hardware.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Determinar la compatibilidad de hardware (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714701"
---
# <a name="determining-hardware-support-direct3d-9"></a><span data-ttu-id="3645c-103">Determinar la compatibilidad de hardware (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3645c-103">Determining Hardware Support (Direct3D 9)</span></span>

<span data-ttu-id="3645c-104">Direct3D proporciona las siguientes funciones para determinar la compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="3645c-104">Direct3D provides the following functions to determine hardware support.</span></span>

-   [<span data-ttu-id="3645c-105">**IDirect3D9::CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="3645c-105">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    <span data-ttu-id="3645c-106">Se usa para comprobar si un formato de superficie se puede usar como textura, si se puede usar un formato de superficie como una textura y un destino de representación, o si se puede usar un formato de superficie como búfer de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="3645c-106">Used to verify whether a surface format can be used as a texture, whether a surface format can be used as a texture and a render target, or whether a surface format can be used as a depth-stencil buffer.</span></span> <span data-ttu-id="3645c-107">Además, este método se usa para comprobar la compatibilidad con el formato de búfer de profundidad y la compatibilidad con el formato de búfer de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="3645c-107">In addition, this method is used to verify depth buffer format support and depth-stencil buffer format support.</span></span>

-   [<span data-ttu-id="3645c-108">**IDirect3D9::CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="3645c-108">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    <span data-ttu-id="3645c-109">Se usa para comprobar la capacidad de un dispositivo para realizar la aceleración de hardware, la capacidad de un dispositivo para crear una cadena de intercambio para la presentación o la capacidad de un dispositivo para representarse en el formato de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="3645c-109">Used to verify a device's ability to perform hardware acceleration, a device's ability to build a swap chain for presentation, or a device's ability to render to the current display format.</span></span>

-   [<span data-ttu-id="3645c-110">**IDirect3D9::CheckDepthStencilMatch**</span><span class="sxs-lookup"><span data-stu-id="3645c-110">**IDirect3D9::CheckDepthStencilMatch**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    <span data-ttu-id="3645c-111">Se usa para comprobar si un formato de búfer de estarcido de profundidad es compatible con un formato de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="3645c-111">Used to verify whether a depth-stencil buffer format is compatible with a render-target format.</span></span> <span data-ttu-id="3645c-112">Tenga en cuenta que, antes de llamar a este método, la aplicación debe llamar a [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) en los formatos de la galería de símbolos de profundidad y de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="3645c-112">Note that before calling this method, the application should call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) on both the depth-stencil and render-target formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3645c-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3645c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3645c-114">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="3645c-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
