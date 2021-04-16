---
description: Las tarjetas de identificación múltiple son aquellas que tienen un acelerador y un búfer de fotogramas comunes, convertidores digitales-analógicos (DAC) independientes y salidas de monitor.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494728"
---
# <a name="multihead-direct3d-9"></a><span data-ttu-id="00001-103">Multihead (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="00001-103">Multihead (Direct3D 9)</span></span>

<span data-ttu-id="00001-104">Las tarjetas de identificación múltiple son aquellas que tienen un acelerador y un búfer de fotogramas comunes, convertidores digitales-analógicos (DAC) independientes y salidas de monitor.</span><span class="sxs-lookup"><span data-stu-id="00001-104">Multihead cards are those that have a common frame buffer and accelerator, independent digital-to-analog converters (DACs), and monitor outputs.</span></span> <span data-ttu-id="00001-105">Estos dispositivos pueden ofrecer compatibilidad con varios monitores más utilizable que un número similar de adaptadores de pantalla heterogéneos.</span><span class="sxs-lookup"><span data-stu-id="00001-105">Such devices can offer much more usable multiple monitor support than a similar number of heterogeneous display adapters.</span></span>

<span data-ttu-id="00001-106">Las tarjetas de múltiples cabezales se exponen en la API como un único dispositivo de nivel de API que puede controlar varias cadenas de intercambio de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="00001-106">Multihead cards are exposed in the API as a single API-level device that can drive several full-screen swap chains.</span></span> <span data-ttu-id="00001-107">Por lo tanto, todos los recursos se comparten con todos los cabezales y cada encabezado tiene exactamente las mismas funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="00001-107">Consequently, all resources are shared with all the heads, and each head has exactly the same capabilities.</span></span> <span data-ttu-id="00001-108">Cada encabezado se puede establecer en modos de presentación independientes.</span><span class="sxs-lookup"><span data-stu-id="00001-108">Each head can be set to independent display modes.</span></span> <span data-ttu-id="00001-109">Puede usar llamadas independientes a [**IDirect3DSwapChain9::P reenviar**](/windows/desktop/api) para actualizar cada cabeza.</span><span class="sxs-lookup"><span data-stu-id="00001-109">You can use separate calls to [**IDirect3DSwapChain9::Present**](/windows/desktop/api) to refresh each head.</span></span> <span data-ttu-id="00001-110">También puede usar una llamada a [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para actualizar cada encabezado secuencialmente.</span><span class="sxs-lookup"><span data-stu-id="00001-110">You can also use one call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) to refresh each head sequentially.</span></span>

> [!Note]  
> <span data-ttu-id="00001-111">La actualización de cada encabezado no se realiza simultáneamente con una única llamada a [**IDirect3DDevice9::P reenviar**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="00001-111">The refresh of each head does not occur simultaneously with a single call to [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="00001-112">Presentar estadísticas en Direct3D 9Ex puede usar la estructura [**D3DPRESENTSTATS**](d3dpresentstats.md) para mantener las actualizaciones en cada una de ellas cerca de otras para limitar los efectos de desgarro en varios cabezales de adaptadores.</span><span class="sxs-lookup"><span data-stu-id="00001-112">Present statistics in Direct3D 9Ex can use the [**D3DPRESENTSTATS**](d3dpresentstats.md) structure to keep the refreshes to each head close to each other to limit tearing effects across multiple heads of adapters.</span></span> <span data-ttu-id="00001-113">Para obtener información sobre cómo sincronizar marcos de aplicaciones de 9Ex Flip Model de Direct3D, consulte [mejoras de 9Ex de Direct3D](../direct3darticles/direct3d-9ex-improvements.md).</span><span class="sxs-lookup"><span data-stu-id="00001-113">For information about synchronizing frames of Direct3D 9Ex flip model applications, see [Direct3D 9Ex Improvements](../direct3darticles/direct3d-9ex-improvements.md).</span></span>

 

<span data-ttu-id="00001-114">Cada cadena de intercambio para un dispositivo con más cabezales debe estar en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="00001-114">Each swap chain for a multihead device must be full screen.</span></span> <span data-ttu-id="00001-115">Cuando un dispositivo ha entrado en modo de Multihead, debe permanecer en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="00001-115">When a device has entered multihead mode, it must remain full screen.</span></span> <span data-ttu-id="00001-116">La transición de vuelta al modo de ventana requiere la destrucción del dispositivo (excepto la operación normal ALT + TAB para minimizar).</span><span class="sxs-lookup"><span data-stu-id="00001-116">The transition back to windowed mode requires the destruction of the device (except for the normal ALT+TAB-to-minimize operation).</span></span>

<span data-ttu-id="00001-117">El método anterior para dividir la memoria de vídeo entre los cabezales y tratar cada cabeza como un acelerador totalmente independiente seguirá siendo un escenario de uso común.</span><span class="sxs-lookup"><span data-stu-id="00001-117">The old method of dividing video memory between the heads and treating each head as a fully independent accelerator will still be a common usage scenario.</span></span> <span data-ttu-id="00001-118">Esta propuesta no sustituye a ese mecanismo a menos que la aplicación se haya codificado específicamente para que funcione en el modo de Multihead de Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="00001-118">This proposal does not replace that mechanism unless the application has been specifically coded to function in the Direct3D 9 multihead mode.</span></span>

<span data-ttu-id="00001-119">A los controladores se les proporciona el conocimiento adecuado para cambiar entre los dos modos de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="00001-119">Drivers are given adequate knowledge to switch between the two modes of operation.</span></span>

<span data-ttu-id="00001-120">Un encabezado se llamará la cabeza maestra y todos los demás cabezales de la misma tarjeta se denominarán cabezas subordinadas.</span><span class="sxs-lookup"><span data-stu-id="00001-120">One head will be called the master head, and all other heads on the same card be called subordinate heads.</span></span> <span data-ttu-id="00001-121">Si hay más de un adaptador de varios cabezales en un sistema, el maestro y sus subordinados de un adaptador de varios cabezales se denominan grupo.</span><span class="sxs-lookup"><span data-stu-id="00001-121">If more than one multihead adapter is present in a system, the master and its subordinates from one multihead adapter are called a group.</span></span> <span data-ttu-id="00001-122">Los grupos se indican mediante el ordinal del adaptador de su cabeza maestra.</span><span class="sxs-lookup"><span data-stu-id="00001-122">Groups are denoted by the adapter ordinal of their master head.</span></span>

<span data-ttu-id="00001-123">La estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) se ha actualizado para exponer los nuevos límites de hardware siguientes.</span><span class="sxs-lookup"><span data-stu-id="00001-123">The [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure has been updated to expose the following new hardware caps.</span></span>


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   <span data-ttu-id="00001-124">NumberOfAdaptersInGroup es 1 para los adaptadores convencionales y mayor que 1 para el adaptador maestro de una tarjeta de varios cabezales.</span><span class="sxs-lookup"><span data-stu-id="00001-124">NumberOfAdaptersInGroup is 1 for conventional adapters, and greater than 1 for the master adapter of a multihead card.</span></span> <span data-ttu-id="00001-125">El valor será 0 para un adaptador subordinado de una tarjeta de varios cabezales.</span><span class="sxs-lookup"><span data-stu-id="00001-125">The value will be 0 for a subordinate adapter of a multihead card.</span></span> <span data-ttu-id="00001-126">Cada tarjeta puede tener como máximo un maestro, pero puede tener muchos subordinados.</span><span class="sxs-lookup"><span data-stu-id="00001-126">Each card can have at most one master, but might have many subordinates.</span></span>
-   <span data-ttu-id="00001-127">MasterAdapterOrdinal indica qué dispositivo es el maestro de este subordinado.</span><span class="sxs-lookup"><span data-stu-id="00001-127">MasterAdapterOrdinal indicates which device is the master for this subordinate.</span></span>
-   <span data-ttu-id="00001-128">AdapterOrdinalInGroup indica el orden en el que la API hace referencia a los encabezados.</span><span class="sxs-lookup"><span data-stu-id="00001-128">AdapterOrdinalInGroup indicates the order in which heads are referenced by the API.</span></span> <span data-ttu-id="00001-129">El adaptador Maestro siempre tiene AdapterOrdinalInGroup 0.</span><span class="sxs-lookup"><span data-stu-id="00001-129">The master adapter always has AdapterOrdinalInGroup 0.</span></span> <span data-ttu-id="00001-130">Estos valores no se corresponden con los ordinales del adaptador que se pasan a los métodos IDirect3D9, pero solo se aplican a los encabezados de un grupo.</span><span class="sxs-lookup"><span data-stu-id="00001-130">These values do not correspond to the adapter ordinals passed to the IDirect3D9 methods, but apply only to heads within a group.</span></span>

<span data-ttu-id="00001-131">Esta definición permite que las tarjetas de múltiples cabezales sigan presentando varios adaptadores como si fueran tarjetas independientes, al igual que en DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="00001-131">This definition allows multihead cards to continue to present multiple adapters as if they were independent cards, just as they did in DirectX 8.</span></span>

<span data-ttu-id="00001-132">Para crear un dispositivo con más cabezal, especifique la marca de comportamiento D3DCREATE \_ ADAPTERGROUP \_ Device in [**IDirect3D9:: CreateDevice**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="00001-132">To create a multihead device, specify the behavior flag D3DCREATE\_ADAPTERGROUP\_DEVICE in [**IDirect3D9::CreateDevice**](/windows/desktop/api).</span></span> <span data-ttu-id="00001-133">Los parámetros de presentación (una matriz [**de \_ parámetros D3DPRESENT**](d3dpresent-parameters.md)) deben contener elementos NumberOfAdaptersInGroup.</span><span class="sxs-lookup"><span data-stu-id="00001-133">The presentation parameters (an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md)) should contain NumberOfAdaptersInGroup elements.</span></span> <span data-ttu-id="00001-134">El tiempo de ejecución asignará cada elemento a cada encabezado en el orden numérico AdapterOrdinalInGroup.</span><span class="sxs-lookup"><span data-stu-id="00001-134">The runtime will assign each element to each head in AdapterOrdinalInGroup numerical order.</span></span> <span data-ttu-id="00001-135">Cuando \_ \_ se establece D3DCREATE ADAPTERGROUP Device, cada parámetro de presentación debe tener:</span><span class="sxs-lookup"><span data-stu-id="00001-135">When D3DCREATE\_ADAPTERGROUP\_DEVICE is set, each presentation parameter must have:</span></span>

-   <span data-ttu-id="00001-136">El miembro de ventana establecido en **false** (es decir, debe ser una pantalla completa).</span><span class="sxs-lookup"><span data-stu-id="00001-136">The Windowed member set to **FALSE** (in other words, be full screen).</span></span>
-   <span data-ttu-id="00001-137">El mismo valor para el miembro EnableAutoDepthStencil de [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="00001-137">The same value for the EnableAutoDepthStencil member of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="00001-138">Además, si EnableAutoDepthStencil es **true**, cada uno de los campos siguientes debe tener el mismo valor para cada uno de los [**\_ parámetros de D3DPRESENT**](d3dpresent-parameters.md):</span><span class="sxs-lookup"><span data-stu-id="00001-138">In addition, if EnableAutoDepthStencil is **TRUE**, then each of the following fields must have the same value for each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md):</span></span>

-   <span data-ttu-id="00001-139">AutoDepthStencilFormat</span><span class="sxs-lookup"><span data-stu-id="00001-139">AutoDepthStencilFormat</span></span>
-   <span data-ttu-id="00001-140">BackBufferWidth</span><span class="sxs-lookup"><span data-stu-id="00001-140">BackBufferWidth</span></span>
-   <span data-ttu-id="00001-141">BackBufferHeight</span><span class="sxs-lookup"><span data-stu-id="00001-141">BackBufferHeight</span></span>
-   <span data-ttu-id="00001-142">BackBufferFormat</span><span class="sxs-lookup"><span data-stu-id="00001-142">BackBufferFormat</span></span>

<span data-ttu-id="00001-143">Si se establece DAC, las llamadas adicionales a [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) no son válidas.</span><span class="sxs-lookup"><span data-stu-id="00001-143">If DAC is set, additional calls to [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) are illegal.</span></span>

<span data-ttu-id="00001-144">Si el dispositivo se creó con la DAC, [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) esperará una matriz de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="00001-144">If the device was created with the DAC, [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) will expect an array of [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

<span data-ttu-id="00001-145">Cada estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) que se pasa a [**IDirect3DDevice9:: RESET**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) debe ser de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="00001-145">Each [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure passed to [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) must be full screen.</span></span> <span data-ttu-id="00001-146">Para volver al modo de ventana, la aplicación debe destruir el dispositivo y volver a crear un dispositivo que no sea de multidirector en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="00001-146">To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.</span></span>

<span data-ttu-id="00001-147">Este es un escenario de uso básico:</span><span class="sxs-lookup"><span data-stu-id="00001-147">Here is a basic usage scenario:</span></span>


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



<span data-ttu-id="00001-148">Para obtener más información, vea [**IDirect3D9:: CreateDevice**](/windows/desktop/api) y [**IDirect3DDevice9:: GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span><span class="sxs-lookup"><span data-stu-id="00001-148">For more information, see [**IDirect3D9::CreateDevice**](/windows/desktop/api) and [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).</span></span>

## <a name="related-topics"></a><span data-ttu-id="00001-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00001-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00001-150">Sugerencias de programación</span><span class="sxs-lookup"><span data-stu-id="00001-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
