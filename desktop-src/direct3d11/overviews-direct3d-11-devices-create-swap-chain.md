---
title: Cómo crear una cadena de intercambio
description: En este tema se muestra cómo crear una cadena de intercambio que encapsule dos o más búferes que se usan para la representación y presentación.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421047"
---
# <a name="how-to-create-a-swap-chain"></a><span data-ttu-id="cdaf9-103">Cómo: crear una cadena de intercambio</span><span class="sxs-lookup"><span data-stu-id="cdaf9-103">How To: Create a Swap Chain</span></span>

<span data-ttu-id="cdaf9-104">En este tema se muestra cómo crear una cadena de intercambio que encapsule dos o más búferes que se usan para la representación y presentación.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-104">This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display.</span></span> <span data-ttu-id="cdaf9-105">Normalmente contienen un búfer frontal que se presenta al dispositivo de pantalla y un búfer de reserva que actúa como destino de representación.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-105">They usually contain a front buffer that is presented to the display device and a back buffer that serves as the render target.</span></span> <span data-ttu-id="cdaf9-106">Una vez que el contexto inmediato finaliza la representación en el búfer de reserva, la cadena de intercambio presenta el búfer de reserva intercambiando los dos búferes.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-106">After the immediate context is done rendering to the back buffer, the swap chain presents the back buffer by swapping the two buffers.</span></span>

<span data-ttu-id="cdaf9-107">La cadena de intercambio define varias características de representación, entre las que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="cdaf9-107">The swap chain defines several rendering characteristics including:</span></span>

-   <span data-ttu-id="cdaf9-108">Tamaño del área de representación.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-108">The size of the render area.</span></span>
-   <span data-ttu-id="cdaf9-109">La frecuencia de actualización de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-109">The display refresh rate.</span></span>
-   <span data-ttu-id="cdaf9-110">Modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-110">The display mode.</span></span>
-   <span data-ttu-id="cdaf9-111">El formato de la superficie.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-111">The surface format.</span></span>

<span data-ttu-id="cdaf9-112">Defina las características de la cadena de intercambio rellenando una estructura de DESC de cadena de intercambio de DXGI e inicializando una interfaz [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) . [**\_ \_ \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)</span><span class="sxs-lookup"><span data-stu-id="cdaf9-112">Define the characteristics of the swap chain by filling in a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure and initializing an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) interface.</span></span> <span data-ttu-id="cdaf9-113">Inicialice una cadena de intercambio mediante una llamada a [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="cdaf9-113">Initialize a swap chain by calling [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="create-a-device-and-a-swap-chain"></a><span data-ttu-id="cdaf9-114">Crear un dispositivo y una cadena de intercambio</span><span class="sxs-lookup"><span data-stu-id="cdaf9-114">Create a device and a swap chain</span></span>

<span data-ttu-id="cdaf9-115">Para inicializar un dispositivo y una cadena de intercambio, utilice una de las dos funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="cdaf9-115">To initialize a device and swap chain, use one of the following two functions:</span></span>

-   <span data-ttu-id="cdaf9-116">Utilice la función [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) cuando desee inicializar la cadena de intercambio al mismo tiempo que la inicialización del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-116">Use the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function when you want to initialize the swap chain at the same time as device initialization.</span></span> <span data-ttu-id="cdaf9-117">Normalmente, esta es la opción más sencilla.</span><span class="sxs-lookup"><span data-stu-id="cdaf9-117">This usually is the easiest option.</span></span>

-   <span data-ttu-id="cdaf9-118">Use la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) cuando ya haya creado una cadena de intercambio mediante [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span><span class="sxs-lookup"><span data-stu-id="cdaf9-118">Use the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function when you have already created a swap chain using [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdaf9-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cdaf9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdaf9-120">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="cdaf9-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="cdaf9-121">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="cdaf9-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 