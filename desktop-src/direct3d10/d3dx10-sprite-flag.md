---
description: Marcas de sprite que le dicen a la API de dibujo de sprite cómo comportarse. Se pasan a ID3DX10Sprite::Begin.
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: D3DX10_SPRITE_FLAG enumeración (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 53b2c7965beaeb2976e88d38f5af90d546f644b6d4879964c23b2166cd51b19b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634945"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>Enumeración SPRITE \_ FLAG de D3DX10 \_

Marcas de sprite que le dicen a la API de dibujo de sprite cómo comportarse. Se pasan a [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**TEXTURA DE ORDENACIÓN DE SPRITE D3DX10 \_ \_ \_**
</dt> <dd>

Ordene los sprites por textura antes de la representación para que, cuando haya muchos sprites con la misma textura, todos esos sprites se represente al mismo tiempo, lo que mejora el rendimiento.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**PROFUNDIDAD DE ORDENACIÓN DEL SPRITE D3DX10 \_ \_ HACIA \_ \_ \_ \_ DELANTE**
</dt> <dd>

Ordene los sprites de atrás a delante para que los que están más lejos de la cámara se dibujarán primero.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**PROFUNDIDAD DE ORDENACIÓN DEL SPRITE D3DX10 \_ \_ HACIA \_ \_ \_ \_ ATRÁS**
</dt> <dd>

Ordene los sprites de delante hacia atrás para que los más cercanos a la cámara se dibujarán primero.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**ESTADO DE GUARDADO DE SPRITE D3DX10 \_ \_ \_**
</dt> <dd>

Guarda el estado para que, cuando se llame a [**ID3DX10Sprite::End,**](id3dx10sprite-end.md) restaure el estado como estaba antes de llamar a [**ID3DX10Sprite::Begin.**](id3dx10sprite-begin.md)

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**TEXTURAS \_ ADDREF DE SPRITE D3DX10 \_ \_**
</dt> <dd>

Llama a AddRef en todas las texturas cuando se pasan a [**ID3DX10Sprite::D rawSpritesBuffered.**](id3dx10sprite-drawspritesbuffered.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una vez realizada una ordenación front-to-back o back-to-front, realizará automáticamente una ordenación secundaria por textura. Esto resulta útil cuando hay muchos sprites con la misma textura en el mismo plano, como al dibujar la interfaz de usuario en un juego.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




