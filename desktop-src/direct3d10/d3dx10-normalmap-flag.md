---
description: Estas marcas se usan para controlar cómo D3DX10ComputeNormalMap genera asignaciones normales. Cualquier número de estas marcas puede ser OR juntos en cualquier combinación.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: D3DX10_NORMALMAP_FLAG enumeración (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566725"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a>Enumeración D3DX10 \_ NORMALMAP \_ FLAG

Estas marcas se usan para controlar cómo [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) genera asignaciones normales. Cualquier número de estas marcas puede ser OR juntos en cualquier combinación.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ NORMALMAP \_ MIRROR \_ U**
</dt> <dd>

Indica que los píxeles del borde de la textura en el eje U deben reflejarse, no ajustarse.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ NORMALMAP \_ MIRROR \_ V**
</dt> <dd>

Indica que los píxeles fuera del borde de la textura en el eje V deben estar reflejados, no encapsulados.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10 \_ NORMALMAP \_ MIRROR**
</dt> <dd>

Igual que D3DX10 \_ NORMALMAP \_ MIRROR U \_ \| D3DX10 \_ NORMALMAP MIRROR \_ \_ V.

</dd> <dt>

<span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

Invierte la dirección de cada normal.

</dd> <dt>

<span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**OCLUSIÓN DE PROCESO \_ DE ASIGNACIÓN NORMAL DE D3DX10 \_ \_**
</dt> <dd>

Calcula el término de oclusión por píxel y lo codifica en alfa. Un alfa de 1 significa que el píxel no se oculta de ninguna manera, y un alfa de 0 significaría que el píxel está completamente oculto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




