---
description: Para crear un dispositivo Direct3D, primero debe crear un objeto de Direct3D (vea Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Crear un dispositivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714783"
---
# <a name="creating-a-device-direct3d-9"></a><span data-ttu-id="e1926-103">Crear un dispositivo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e1926-103">Creating a Device (Direct3D 9)</span></span>

<span data-ttu-id="e1926-104">Para crear un dispositivo Direct3D, primero debe crear un objeto de Direct3D (vea [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span><span class="sxs-lookup"><span data-stu-id="e1926-104">To create a Direct3D device, first create a Direct3D object (see [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span></span> <span data-ttu-id="e1926-105">Todos los dispositivos de representación creados por un objeto de Direct3D comparten los mismos recursos físicos.</span><span class="sxs-lookup"><span data-stu-id="e1926-105">All rendering devices created by a Direct3D object share the same physical resources.</span></span> <span data-ttu-id="e1926-106">Si crea varios dispositivos de representación a partir de un único objeto de Direct3D, se aplicarán penalizaciones extremas al rendimiento porque comparten el mismo hardware.</span><span class="sxs-lookup"><span data-stu-id="e1926-106">If you create multiple rendering devices from a single Direct3D object, extreme performance penalties will be incurred because they share the same hardware.</span></span>

<span data-ttu-id="e1926-107">En primer lugar, inicialice los valores de la estructura de [**\_ parámetros D3DPRESENT**](d3dpresent-parameters.md) que se usa para crear el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1926-107">First, initialize values for the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure that is used to create the Direct3D device.</span></span> <span data-ttu-id="e1926-108">En el ejemplo de código siguiente se especifica una aplicación de ventana en la que el búfer de reserva se copia en el búfer frontal durante una operación de sincronización vertical.</span><span class="sxs-lookup"><span data-stu-id="e1926-108">The following code example specifies a windowed application where the back buffer is copied to the front buffer during a vertical sync operation only.</span></span>


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



<span data-ttu-id="e1926-109">A continuación, cree el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e1926-109">Next, create the Direct3D device.</span></span> <span data-ttu-id="e1926-110">La siguiente llamada a [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) especifica el adaptador predeterminado, un dispositivo de capa de abstracción de hardware (HAL) y el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="e1926-110">The following [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call specifies the default adapter, a hardware abstraction layer (HAL) device, and software vertex processing.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



<span data-ttu-id="e1926-111">Tenga en cuenta que una llamada para crear, liberar o restablecer el dispositivo solo debe ocurrir en el mismo subproceso que el procedimiento de ventana de la ventana de enfoque.</span><span class="sxs-lookup"><span data-stu-id="e1926-111">Note that a call to create, release, or reset the device should happen only on the same thread as the window procedure of the focus window.</span></span>

<span data-ttu-id="e1926-112">Después de crear el dispositivo, establezca su estado.</span><span class="sxs-lookup"><span data-stu-id="e1926-112">After creating the device, set its state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1926-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1926-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1926-114">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="e1926-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
