---
description: Define información de posición, textura y color sobre un sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: D3DX10_SPRITE estructura (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ec8b220d55d3ac55d2a8b68fa3b95398a395611da150235d03314114055214e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753515"
---
# <a name="d3dx10_sprite-structure"></a>Estructura sprite D3DX10 \_

Define información de posición, textura y color sobre un sprite.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**matWorld**
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**

</dd> <dd>

Transformación del mundo del modelo del sprite. Esto define la posición y la orientación del sprite en el espacio mundial.

</dd> <dt>

**TexCoord**
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Desplazamiento desde la esquina superior izquierda de la textura que indica dónde debe comenzar la imagen de sprite en la textura. **TexCoord está** en coordenadas de textura.

</dd> <dt>

**TexSize**
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Vector que contiene el ancho y alto del sprite en coordenadas de textura.

</dd> <dt>

**ColorModulate**
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

</dd> <dd>

Color que se multiplicará por el color de píxel antes de la representación.

</dd> <dt>

**pTexture**
</dt> <dd>

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***

</dd> <dd>

Puntero a una vista de sombreador y recurso que representa la textura del sprite. Vea [**ID3D10ShaderResourceView (Interfaz).**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)

</dd> <dt>

**TextureIndex**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Índice de la textura. Si pTexture no representa una matriz de texturas, debe ser 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
