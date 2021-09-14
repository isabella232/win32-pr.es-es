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
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060874"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>Enumeración D3DX11 \_ NORMALMAP \_ FLAG

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Opciones de mapa normales. Puede combinar cualquier número de estas marcas mediante una operación OR bit a bit.

## <a name="syntax"></a>Sintaxis


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

## <a name="remarks"></a>Observaciones

[**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md)usa estas marcas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





