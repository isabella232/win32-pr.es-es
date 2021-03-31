---
title: El dispositivo D1112 debe ser DX11
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: El dispositivo asociado a la superficie de DXGI debe ser un dispositivo D3D11.
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
ms.openlocfilehash: b4204e04332876db9145baba9888dbb2d339eff9
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104077462"
---
# <a name="d1112-device-must-be-dx11"></a>D1112: el dispositivo debe ser DX11

El dispositivo asociado a la superficie de DXGI debe ser un dispositivo D3D11.



|             |         |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="possible-causes"></a>Causas posibles

Se intentó usar [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) con una superficie de DXGI creada por un dispositivo que no es de Direct3D 11.

 

 




