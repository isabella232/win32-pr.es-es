---
description: Obtiene las marcas que se usaron cuando se creó Infraestructura de gráficos de DirectX de microsoft (DXGI).
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
title: IDXGIFactory3::GetCreationFlags (método)
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
ms.openlocfilehash: eaa668235ca5893e74b3019d02f2cc8cd899e8661669252e14c458aababfda82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984095"
---
# <a name="idxgifactory3getcreationflags-method"></a>IDXGIFactory3::GetCreationFlags (método)

Obtiene las marcas que se usaron cuando se creó Infraestructura de gráficos de DirectX de microsoft (DXGI).

## <a name="syntax"></a>Sintaxis


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Marcas de creación.

## <a name="remarks"></a>Comentarios

El método **GetCreationFlags** devuelve marcas que se pasaron a la función [**CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) o que crearon implícitamente [**CreateDXGIFactory,**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory) [**CreateDXGIFactory1,**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1) [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)o [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDXGIFactory3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
