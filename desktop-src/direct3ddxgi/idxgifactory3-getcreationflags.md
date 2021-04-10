---
description: Obtiene las marcas que se usaron cuando se creó un objeto de infraestructura de gráficos de Microsoft DirectX (DXGI).
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
title: 'IDXGIFactory3:: GetCreationFlags (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDXGIFactory3.GetCreationFlags
api_type:
- COM
api_location:
- dxgi1_3.h
ms.openlocfilehash: 56d1f35ea5a4ce26a0d9ccb5ee0d79035f74a0ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151937"
---
# <a name="idxgifactory3getcreationflags-method"></a><span data-ttu-id="983b6-103">IDXGIFactory3:: GetCreationFlags (método)</span><span class="sxs-lookup"><span data-stu-id="983b6-103">IDXGIFactory3::GetCreationFlags method</span></span>

<span data-ttu-id="983b6-104">Obtiene las marcas que se usaron cuando se creó un objeto de infraestructura de gráficos de Microsoft DirectX (DXGI).</span><span class="sxs-lookup"><span data-stu-id="983b6-104">Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.</span></span>

## <a name="syntax"></a><span data-ttu-id="983b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="983b6-105">Syntax</span></span>


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a><span data-ttu-id="983b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="983b6-106">Parameters</span></span>

<span data-ttu-id="983b6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="983b6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="983b6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="983b6-108">Return value</span></span>

<span data-ttu-id="983b6-109">Marcas de creación.</span><span class="sxs-lookup"><span data-stu-id="983b6-109">The creation flags.</span></span>

## <a name="remarks"></a><span data-ttu-id="983b6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="983b6-110">Remarks</span></span>

<span data-ttu-id="983b6-111">El método **GetCreationFlags** devuelve las marcas que se pasaron a la función [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) o que se construyeron implícitamente mediante [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)o [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="983b6-111">The **GetCreationFlags** method returns flags that were passed to the [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) function, or were implicitly constructed by [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice), or [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="see-also"></a><span data-ttu-id="983b6-112">Vea también</span><span class="sxs-lookup"><span data-stu-id="983b6-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="983b6-113">**IDXGIFactory3**</span><span class="sxs-lookup"><span data-stu-id="983b6-113">**IDXGIFactory3**</span></span>](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
