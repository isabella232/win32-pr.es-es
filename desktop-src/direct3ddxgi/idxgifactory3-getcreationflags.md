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
# <a name="idxgifactory3getcreationflags-method"></a>IDXGIFactory3:: GetCreationFlags (método)

Obtiene las marcas que se usaron cuando se creó un objeto de infraestructura de gráficos de Microsoft DirectX (DXGI).

## <a name="syntax"></a>Sintaxis


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Marcas de creación.

## <a name="remarks"></a>Observaciones

El método **GetCreationFlags** devuelve las marcas que se pasaron a la función [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) o que se construyeron implícitamente mediante [**CreateDXGIFactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory), [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1), [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)o [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDXGIFactory3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
