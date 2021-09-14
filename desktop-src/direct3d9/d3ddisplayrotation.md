---
description: Especifica cómo se gira el monitor que se usa para mostrar una aplicación de pantalla completa.
ms.assetid: 190aa10e-4bf0-45ec-9c07-2582c5536074
title: Enumeración D3DDISPLAYROTATION (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDISPLAYROTATION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 28f4d38dca78f0f34daf931a6bf651b40c1b0a78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126971000"
---
# <a name="d3ddisplayrotation-enumeration"></a>Enumeración D3DDISPLAYROTATION

Especifica cómo se gira el monitor que se usa para mostrar una aplicación de pantalla completa.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DDISPLAYROTATION { 
  D3DDISPLAYROTATION_IDENTITY  = 1,
  D3DDISPLAYROTATION_90        = 2,
  D3DDISPLAYROTATION_180       = 3,
  D3DDISPLAYROTATION_270       = 4
} D3DDISPLAYROTATION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDISPLAYROTATION_IDENTITY"></span><span id="d3ddisplayrotation_identity"></span>**D3DDISPLAYROTATION \_ IDENTITY**
</dt> <dd>

La pantalla no gira.

</dd> <dt>

<span id="D3DDISPLAYROTATION_90"></span><span id="d3ddisplayrotation_90"></span>**D3DDISPLAYROTATION \_ 90**
</dt> <dd>

La pantalla gira 90 grados.

</dd> <dt>

<span id="D3DDISPLAYROTATION_180"></span><span id="d3ddisplayrotation_180"></span>**D3DDISPLAYROTATION \_ 180**
</dt> <dd>

La pantalla gira 180 grados.

</dd> <dt>

<span id="D3DDISPLAYROTATION_270"></span><span id="d3ddisplayrotation_270"></span>**D3DDISPLAYROTATION \_ 270**
</dt> <dd>

La pantalla gira 270 grados.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se usa en [**IDirect3D9Ex::GetAdapterDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex), [**IDirect3DDevice9Ex::GetDisplayModeEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-getdisplaymodeex)e [**IDirect3DSwapChain9Ex::GetDisplayModeEx**](/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex).

Las aplicaciones pueden optar por controlar la rotación de supervisión por sí mismas mediante [D3DPRESENTFLAG \_ NOAUTOROTATE,](d3dpresentflag.md)en cuyo caso, la aplicación deberá saber cómo se gira el monitor para que pueda ajustar su representación en consecuencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




