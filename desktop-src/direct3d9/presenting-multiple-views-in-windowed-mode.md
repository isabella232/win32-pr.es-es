---
description: Además de la cadena de intercambio que posee y manipula a través de la interfaz IDirect3DDevice9, una aplicación puede crear cadenas de intercambio adicionales para presentar varias vistas del mismo dispositivo.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Presentar varias vistas en modo de ventana (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104538229"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="7c298-103">Presentar varias vistas en modo de ventana (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7c298-103">Presenting Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="7c298-104">Además de la cadena de intercambio que posee y manipula a través de la interfaz [**IDirect3DDevice9**](/windows/desktop/api) , una aplicación puede crear cadenas de intercambio adicionales para presentar varias vistas del mismo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c298-104">In addition to the swap chain that is owned and manipulated through the [**IDirect3DDevice9**](/windows/desktop/api) interface, an application can create additional swap chains in order to present multiple views from the same device.</span></span> <span data-ttu-id="7c298-105">Normalmente, la aplicación crea una cadena de intercambio por cada vista mediante el método [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) y asocia cada cadena de intercambio a una ventana determinada.</span><span class="sxs-lookup"><span data-stu-id="7c298-105">The application typically creates one swap chain per view by using the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method, and associates each swap chain with a particular window.</span></span> <span data-ttu-id="7c298-106">La aplicación representa las imágenes en los búferes de reserva de cada cadena de intercambio y, a continuación, las presenta individualmente.</span><span class="sxs-lookup"><span data-stu-id="7c298-106">The application renders images into the back buffers of each swap chain, and then presents them individually.</span></span>

<span data-ttu-id="7c298-107">Solo una cadena de intercambio a la vez puede estar en pantalla completa en cada adaptador.</span><span class="sxs-lookup"><span data-stu-id="7c298-107">Only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c298-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c298-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c298-109">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="7c298-109">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
