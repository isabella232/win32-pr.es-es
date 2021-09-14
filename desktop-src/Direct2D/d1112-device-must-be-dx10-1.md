---
title: El dispositivo D1112 debe ser DX11
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: El dispositivo asociado a la superficie DXGI debe ser un dispositivo D3D11.
keywords:
- El dispositivo D1112 debe ser DX11 Direct2D
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 68408c56710589def033c34d20d9bac81e8d4947
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164109"
---
# <a name="d1112-device-must-be-dx11"></a>D1112: El dispositivo debe ser DX11

El dispositivo asociado a la superficie DXGI debe ser un dispositivo D3D11.



| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="possible-causes"></a>Causas posibles

Se intentó usar [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) con una superficie DXGI creada por un dispositivo que no es Direct3D11.

 

 




