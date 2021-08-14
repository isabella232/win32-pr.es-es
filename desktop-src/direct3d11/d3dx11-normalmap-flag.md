---
title: D3DX11_NORMALMAP_FLAG enumeración (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Opciones de mapa normales. Puede combinar cualquier número de estas marcas mediante una operación OR bit a bit.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- D3DX11_NORMALMAP_FLAG enumeración Direct3D 11
- LPD3DX11_NORMALMAP_FLAG puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbea7c787ac2e2aa7d988e052e2ca548a49a338c9b9f981ce73d51c40e0b4edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300654"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>Enumeración D3DX11 \_ NORMALMAP \_ FLAG

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Opciones de mapa normales. Puede combinar cualquier número de estas marcas mediante una operación OR bit a bit.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NORMALMAP \_ MIRROR \_ U**
</dt> <dd>

Indica que los píxeles del borde de la textura del eje U deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NORMALMAP \_ MIRROR \_ V**
</dt> <dd>

Indica que los píxeles del borde de la textura del eje V deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11 \_ NORMALMAP \_ MIRROR**
</dt> <dd>

Igual que D3DX11 \_ NORMALMAP \_ MIRROR U \_ \| D3DX11 \_ NORMALMAP MIRROR \_ \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

Invierte la dirección de cada normal.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**OCLUSIÓN DE PROCESO \_ DE NORMALMAP \_ D3DX11 \_**
</dt> <dd>

Calcula el término de oclusión por píxel y lo codifica en el alfa. Un alfa de 1 significa que el píxel no se oculta de ninguna manera, y un alfa de 0 significaría que el píxel está completamente oculto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

[**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md)usa estas marcas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





