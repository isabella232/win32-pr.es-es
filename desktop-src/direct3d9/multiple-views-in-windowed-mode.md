---
description: 'Además de la cadena de intercambio propiedad y manipulada a través del objeto Direct3DDevice, una aplicación puede usar el método IDirect3DDevice9:: CreateAdditionalSwapChain para crear cadenas de intercambio adicionales para presentar varias vistas del mismo dispositivo.'
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Varias vistas en modo de ventana (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714699"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="f7a10-103">Varias vistas en modo de ventana (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f7a10-103">Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="f7a10-104">Además de la cadena de intercambio propiedad y manipulada a través del objeto Direct3DDevice, una aplicación puede usar el método [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) para crear cadenas de intercambio adicionales para presentar varias vistas del mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f7a10-104">In addition to the swap chain that is owned and manipulated through the Direct3DDevice object, an application can use the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method to create additional swap chains to present multiple views from the same device.</span></span>

<span data-ttu-id="f7a10-105">Normalmente, la aplicación crea una cadena de intercambio por cada vista y asocia cada cadena de intercambio a una vista determinada.</span><span class="sxs-lookup"><span data-stu-id="f7a10-105">Typically, the application creates one swap chain per view, and it associates each swap chain with a particular view.</span></span> <span data-ttu-id="f7a10-106">La aplicación representa las imágenes en los búferes de reserva de cada cadena de intercambio y, a continuación, usa el método [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para presentarlas individualmente.</span><span class="sxs-lookup"><span data-stu-id="f7a10-106">The application renders images in the back buffers of each swap chain, and then uses the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method to present them individually.</span></span> <span data-ttu-id="f7a10-107">Tenga en cuenta que solo puede haber una cadena de intercambio a la vez en pantalla completa en cada adaptador.</span><span class="sxs-lookup"><span data-stu-id="f7a10-107">Note that only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7a10-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7a10-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7a10-109">Presentación de una escena</span><span class="sxs-lookup"><span data-stu-id="f7a10-109">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 
