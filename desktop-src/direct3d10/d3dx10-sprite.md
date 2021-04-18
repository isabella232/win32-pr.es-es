---
description: Define la información de posición, textura y color sobre un objeto Sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: D3DX10_SPRITE estructura (D3DX10. h)
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
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721512"
---
# <a name="d3dx10_sprite-structure"></a><span data-ttu-id="fe459-103">D3DX10 ( \_ estructura de Sprite)</span><span class="sxs-lookup"><span data-stu-id="fe459-103">D3DX10\_SPRITE structure</span></span>

<span data-ttu-id="fe459-104">Define la información de posición, textura y color sobre un objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="fe459-104">Defines position, texture, and color information about a sprite.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe459-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe459-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="fe459-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe459-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fe459-107">**matWorld**</span><span class="sxs-lookup"><span data-stu-id="fe459-107">**matWorld**</span></span>
</dt> <dd>

<span data-ttu-id="fe459-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="fe459-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fe459-109">La transformación modelo-mundo del objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="fe459-109">The sprite's model-world transformation.</span></span> <span data-ttu-id="fe459-110">Esto define la posición y la orientación del Sprite en el espacio universal.</span><span class="sxs-lookup"><span data-stu-id="fe459-110">This defines the position and orientation of the sprite in world space.</span></span>

</dd> <dt>

<span data-ttu-id="fe459-111">**TexCoord**</span><span class="sxs-lookup"><span data-stu-id="fe459-111">**TexCoord**</span></span>
</dt> <dd>

<span data-ttu-id="fe459-112">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="fe459-112">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fe459-113">Desplazamiento desde la esquina superior izquierda de la textura que indica dónde debe comenzar la imagen de Sprite en la textura.</span><span class="sxs-lookup"><span data-stu-id="fe459-113">Offset from the upper-left corner of the texture indicating where the sprite image should start in the texture.</span></span> <span data-ttu-id="fe459-114">**TexCoord** está en coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fe459-114">**TexCoord** is in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="fe459-115">**TexSize**</span><span class="sxs-lookup"><span data-stu-id="fe459-115">**TexSize**</span></span>
</dt> <dd>

<span data-ttu-id="fe459-116">Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="fe459-116">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fe459-117">Vector que contiene el ancho y el alto del Sprite en coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fe459-117">A vector containing the width and height of the sprite in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="fe459-118">**ColorModulate**</span><span class="sxs-lookup"><span data-stu-id="fe459-118">**ColorModulate**</span></span>
</dt> <dd>

<span data-ttu-id="fe459-119">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="fe459-119">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fe459-120">Color que se multiplicará por el color de píxel antes de la representación.</span><span class="sxs-lookup"><span data-stu-id="fe459-120">A color that will be multiplied with the pixel color before rendering.</span></span>

</dd> <dt>

<span data-ttu-id="fe459-121">**pTexture**</span><span class="sxs-lookup"><span data-stu-id="fe459-121">**pTexture**</span></span>
</dt> <dd>

<span data-ttu-id="fe459-122">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="fe459-122">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span></span>

</dd> <dd>

<span data-ttu-id="fe459-123">Puntero a una vista de recursos del sombreador que representa la textura del Sprite.</span><span class="sxs-lookup"><span data-stu-id="fe459-123">Pointer to a shader-resource view representing the sprite's texture.</span></span> <span data-ttu-id="fe459-124">Consulte la [**interfaz ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="fe459-124">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="fe459-125">**TextureIndex**</span><span class="sxs-lookup"><span data-stu-id="fe459-125">**TextureIndex**</span></span>
</dt> <dd>

<span data-ttu-id="fe459-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe459-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fe459-127">Índice de la textura.</span><span class="sxs-lookup"><span data-stu-id="fe459-127">The index of the texture.</span></span> <span data-ttu-id="fe459-128">Si pTexture no representa una matriz de texturas, debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="fe459-128">If pTexture does not represent a texture array, then this should be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe459-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe459-129">Requirements</span></span>



| <span data-ttu-id="fe459-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe459-130">Requirement</span></span> | <span data-ttu-id="fe459-131">Value</span><span class="sxs-lookup"><span data-stu-id="fe459-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fe459-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe459-132">Header</span></span><br/> | <dl> <span data-ttu-id="fe459-133"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe459-133"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe459-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe459-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe459-135">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="fe459-135">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
