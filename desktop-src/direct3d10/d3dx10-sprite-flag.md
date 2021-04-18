---
description: 'Marcadores de Sprite que indican a la API de dibujo de Sprite cómo comportarse. Se pasan a ID3DX10Sprite:: Begin.'
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: Enumeración D3DX10_SPRITE_FLAG (D3DX10Core. h)
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
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721513"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>D3DX10 \_ \_ (enumeración de marcador de Sprite)

Marcadores de Sprite que indican a la API de dibujo de Sprite cómo comportarse. Se pasan a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md).

## <a name="syntax"></a>Sintaxis


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

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_ \_ Textura de ordenación de Sprite D3DX10 \_**
</dt> <dd>

Ordene los sprites por textura antes de la representación, de modo que cuando haya muchos sprites con la misma textura que afecten a todos esos sprites al mismo tiempo, con lo que se mejora el rendimiento.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**\_ \_ Profundidad de ordenación \_ \_ de Sprite \_ de D3DX10 hacia \_ delante**
</dt> <dd>

Ordene en primer lugar los sprites de atrás a los que se van alejando de la cámara.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**\_ \_ Profundidad de orden ascendente \_ \_ \_ de \_ D3DX10 Sprite**
</dt> <dd>

Ordene los sprites de delante hacia atrás para que se dibujen en primer lugar los que se acerquen a la cámara.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**Estado de guardado de Sprite de D3DX10 \_ \_ \_**
</dt> <dd>

Guarda el estado de modo que, cuando se llama a [**ID3DX10Sprite:: end**](id3dx10sprite-end.md) , restaure el estado de la manera que tenía antes de que se llamara a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) .

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**\_ \_ Texturas ADDREF de D3DX10 Sprite \_**
</dt> <dd>

Llama a AddRef en todas las texturas cuando se pasan a [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Una vez que se realiza una ordenación anterior o posterior, se realizará automáticamente una ordenación secundaria por textura. Esto resulta útil cuando hay muchos sprites con la misma textura en el mismo plano, por ejemplo, al dibujar la interfaz de usuario en un juego.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




