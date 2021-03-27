---
title: Características de Direct3D 11,4
description: En Direct3D 11,4 se ha agregado la siguiente funcionalidad.
ms.assetid: 689A0460-5725-4C48-B960-41FE20499082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b0d2814aa1f9a7ac7b5f2c87ff9d918b36116f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995413"
---
# <a name="direct3d-114-features"></a><span data-ttu-id="b9276-103">Características de Direct3D 11,4</span><span class="sxs-lookup"><span data-stu-id="b9276-103">Direct3D 11.4 Features</span></span>

<span data-ttu-id="b9276-104">En Direct3D 11,4 se ha agregado la siguiente funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="b9276-104">The following functionality has been added in Direct3D 11.4.</span></span>

<span data-ttu-id="b9276-105">Vea también [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="b9276-105">Also see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="direct3d-device-removal"></a><span data-ttu-id="b9276-106">Eliminación de dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="b9276-106">Direct3D device removal</span></span>

<span data-ttu-id="b9276-107">Los métodos [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent)y [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) se admiten en una nueva interfaz, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), para admitir la recepción de una notificación de eventos asincrónicos cuando se ha quitado un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b9276-107">The [**RegisterDeviceRemovedEvent**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-registerdeviceremovedevent), and [**UnregisterDeviceRemoved**](/windows/desktop/api/d3d11_4/nf-d3d11_4-id3d11device4-unregisterdeviceremoved) methods are supported by a new interface, [**ID3D11Device4**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device4), to support receiving an asynchronous event notification when a Direct3D device has been removed.</span></span>

## <a name="multithreaded-protection"></a><span data-ttu-id="b9276-108">Protección multiproceso</span><span class="sxs-lookup"><span data-stu-id="b9276-108">Multithreaded protection</span></span>

<span data-ttu-id="b9276-109">Para asegurarse de que los comandos de gráficos en particular se ejecutan en un orden específico, la interfaz [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) tiene métodos para activar y desactivar la protección de multiproceso, y métodos para escribir y dejar código crítico que requiera esta protección.</span><span class="sxs-lookup"><span data-stu-id="b9276-109">To ensure that graphics commands in particular are executed in a specific order, the [**ID3D11Multithread**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11multithread) interface has methods to turn multithread protection on and off, and methods to enter and leave critical code requiring this protection.</span></span>

## <a name="fences-for-multi-device-synchronization-and-interop-with-direct3d-12"></a><span data-ttu-id="b9276-110">Barreras para la interoperabilidad y la sincronización de varios dispositivos con Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="b9276-110">Fences for multi-device synchronization and interop with Direct3D 12</span></span>

<span data-ttu-id="b9276-111">[**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) y [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) proporcionan la misma funcionalidad de barrera que Direct3D 12 para Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="b9276-111">The [**ID3D11Fence**](/windows/desktop/api/D3D11_3/nn-d3d11_3-id3d11fence), [**ID3D11Device5**](/windows/desktop/api/d3d11_4/nn-d3d11_4-id3d11device5) and [**ID3D11DeviceContext4**](/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext4) provide the same fence functionality as Direct3D 12 for Direct3D 11.</span></span> <span data-ttu-id="b9276-112">Las barreras se usan para sincronizar varios dispositivos Direct3D 11 y para la interoperabilidad entre Direct3D 11 y Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="b9276-112">Fences are used to synchronize multiple Direct3D11 devices, and for interop between Direct3D 11 and Direct3D 12.</span></span> <span data-ttu-id="b9276-113">Se admiten las barreras en Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="b9276-113">Fences are supported in the Windows 10 Creators Update.</span></span>

## <a name="extended-nv12-texture-support"></a><span data-ttu-id="b9276-114">Compatibilidad con textura NV12 extendida</span><span class="sxs-lookup"><span data-stu-id="b9276-114">Extended NV12 texture support</span></span>

<span data-ttu-id="b9276-115">Las texturas de NV12 con capacidades de captura y de vídeo admiten ahora el uso compartido.</span><span class="sxs-lookup"><span data-stu-id="b9276-115">NV12 textures with capture and video encode capabilities now support sharing.</span></span> <span data-ttu-id="b9276-116">Las marcas de textura D3D11 anteriores para la captura y la codificación de vídeo están desusadas para NV12, ya que se establecerán todo el tiempo para los nuevos controladores.</span><span class="sxs-lookup"><span data-stu-id="b9276-116">Older D3D11 texture flags for video encode and capture are deprecated for NV12, as it will be set all the time for new drivers.</span></span> <span data-ttu-id="b9276-117">Estas texturas se pueden compartir no solo con D3D11, sino también con D3D12.</span><span class="sxs-lookup"><span data-stu-id="b9276-117">Such textures can be shared not only with D3D11, but also with D3D12.</span></span> <span data-ttu-id="b9276-118">En D3D12, ninguna marca nueva representa estas funciones de textura.</span><span class="sxs-lookup"><span data-stu-id="b9276-118">In D3D12, no new flags represent these texture capabilities.</span></span>

<span data-ttu-id="b9276-119">Consulte el valor booleano en [**D3D11 \_ \_ Data \_ D3D11 \_ OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span><span class="sxs-lookup"><span data-stu-id="b9276-119">Refer to the boolean setting in [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS4**](/windows/desktop/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4).</span></span>

## <a name="shader-caching"></a><span data-ttu-id="b9276-120">Almacenamiento en caché del sombreador</span><span class="sxs-lookup"><span data-stu-id="b9276-120">Shader Caching</span></span>

<span data-ttu-id="b9276-121">Los controladores pueden admitir el almacenamiento en caché del sombreador administrado por el sistema operativo de las aplicaciones de Direct3D 11 en Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="b9276-121">Drivers may support OS-managed shader caching of Direct3D11 applications in the Windows 10 Creators update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9276-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b9276-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9276-123">Novedades de Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="b9276-123">What's new in Direct3D 11</span></span>](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 