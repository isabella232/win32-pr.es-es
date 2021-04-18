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
# <a name="d3dx10_sprite_flag-enumeration"></a><span data-ttu-id="8a1f2-104">D3DX10 \_ \_ (enumeración de marcador de Sprite)</span><span class="sxs-lookup"><span data-stu-id="8a1f2-104">D3DX10\_SPRITE\_FLAG enumeration</span></span>

<span data-ttu-id="8a1f2-105">Marcadores de Sprite que indican a la API de dibujo de Sprite cómo comportarse.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-105">Sprite flags that tell the sprite drawing API how to behave.</span></span> <span data-ttu-id="8a1f2-106">Se pasan a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md).</span><span class="sxs-lookup"><span data-stu-id="8a1f2-106">These are passed into [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a1f2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a1f2-107">Syntax</span></span>


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a><span data-ttu-id="8a1f2-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8a1f2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8a1f2-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_ \_ Textura de ordenación de Sprite D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="8a1f2-109"><span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**D3DX10\_SPRITE\_SORT\_TEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="8a1f2-110">Ordene los sprites por textura antes de la representación, de modo que cuando haya muchos sprites con la misma textura que afecten a todos esos sprites al mismo tiempo, con lo que se mejora el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-110">Sort the sprites by texture before rendering so that when there are many sprites with the same texture that texture all of those sprites will be rendered at the same time, thereby improving performance.</span></span>

</dd> <dt>

<span data-ttu-id="8a1f2-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**\_ \_ Profundidad de ordenación \_ \_ de Sprite \_ de D3DX10 hacia \_ delante**</span><span class="sxs-lookup"><span data-stu-id="8a1f2-111"><span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_BACK\_TO\_FRONT**</span></span>
</dt> <dd>

<span data-ttu-id="8a1f2-112">Ordene en primer lugar los sprites de atrás a los que se van alejando de la cámara.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-112">Sort the sprites from back to front to that those farther away from the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="8a1f2-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**\_ \_ Profundidad de orden ascendente \_ \_ \_ de \_ D3DX10 Sprite**</span><span class="sxs-lookup"><span data-stu-id="8a1f2-113"><span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10\_SPRITE\_SORT\_DEPTH\_FRONT\_TO\_BACK**</span></span>
</dt> <dd>

<span data-ttu-id="8a1f2-114">Ordene los sprites de delante hacia atrás para que se dibujen en primer lugar los que se acerquen a la cámara.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-114">Sort the sprites from front to back so that those closer to the camera will be drawn first.</span></span>

</dd> <dt>

<span data-ttu-id="8a1f2-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**Estado de guardado de Sprite de D3DX10 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8a1f2-115"><span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10\_SPRITE\_SAVE\_STATE**</span></span>
</dt> <dd>

<span data-ttu-id="8a1f2-116">Guarda el estado de modo que, cuando se llama a [**ID3DX10Sprite:: end**](id3dx10sprite-end.md) , restaure el estado de la manera que tenía antes de que se llamara a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) .</span><span class="sxs-lookup"><span data-stu-id="8a1f2-116">Saves the state so that when [**ID3DX10Sprite::End**](id3dx10sprite-end.md) is called, it will restore the state to the way it was before [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) was called.</span></span>

</dd> <dt>

<span data-ttu-id="8a1f2-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**\_ \_ Texturas ADDREF de D3DX10 Sprite \_**</span><span class="sxs-lookup"><span data-stu-id="8a1f2-117"><span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**D3DX10\_SPRITE\_ADDREF\_TEXTURES**</span></span>
</dt> <dd>

<span data-ttu-id="8a1f2-118">Llama a AddRef en todas las texturas cuando se pasan a [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md).</span><span class="sxs-lookup"><span data-stu-id="8a1f2-118">Calls AddRef on all of the textures when they are passed into [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a1f2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a1f2-119">Remarks</span></span>

<span data-ttu-id="8a1f2-120">Una vez que se realiza una ordenación anterior o posterior, se realizará automáticamente una ordenación secundaria por textura.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-120">After a front-to-back or back-to-front sort is done, it will automatically do a secondary sort by texture.</span></span> <span data-ttu-id="8a1f2-121">Esto resulta útil cuando hay muchos sprites con la misma textura en el mismo plano, por ejemplo, al dibujar la interfaz de usuario en un juego.</span><span class="sxs-lookup"><span data-stu-id="8a1f2-121">This is helpful for when there are many sprites with the same texture all on the same plane, such as when drawing the user interface in a game.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a1f2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a1f2-122">Requirements</span></span>



| <span data-ttu-id="8a1f2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a1f2-123">Requirement</span></span> | <span data-ttu-id="8a1f2-124">Value</span><span class="sxs-lookup"><span data-stu-id="8a1f2-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a1f2-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a1f2-125">Header</span></span><br/> | <dl> <span data-ttu-id="8a1f2-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a1f2-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a1f2-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a1f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a1f2-128">Enumeraciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="8a1f2-128">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




