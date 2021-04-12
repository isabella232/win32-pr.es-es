---
description: Dibuja una matriz de objetos Sprite.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: ID3DX10Sprite::D método rawSpritesImmediate (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362823"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a><span data-ttu-id="352a6-103">ID3DX10Sprite::D método rawSpritesImmediate</span><span class="sxs-lookup"><span data-stu-id="352a6-103">ID3DX10Sprite::DrawSpritesImmediate method</span></span>

<span data-ttu-id="352a6-104">Dibuja una matriz de objetos Sprite.</span><span class="sxs-lookup"><span data-stu-id="352a6-104">Draw an array of sprites.</span></span> <span data-ttu-id="352a6-105">Esto enviará inmediatamente los sprites al dispositivo para su representación, que es diferente de [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , que solo agrega una matriz de sprites a un lote de sprites que se representará cuando se llame a [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) .</span><span class="sxs-lookup"><span data-stu-id="352a6-105">This will immediately send the sprites to the device for rendering, which is different from [**ID3DX10Sprite::DrawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md) which only adds an array of sprites to a batch of sprites to be rendered when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) is called.</span></span> <span data-ttu-id="352a6-106">Este método draw es muy útil cuando se dibuja un gran número de sprites que ya se han ordenado en la CPU (o no es necesario ordenarlos), como en un sistema de partículas.</span><span class="sxs-lookup"><span data-stu-id="352a6-106">This draw method is most useful when drawing a large number of sprites that have already been sorted on the CPU (or do not need to be sorted), such as in a particle system.</span></span> <span data-ttu-id="352a6-107">Se debe llamar a este método entre las llamadas a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) y [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).</span><span class="sxs-lookup"><span data-stu-id="352a6-107">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="352a6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="352a6-108">Syntax</span></span>


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a><span data-ttu-id="352a6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="352a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="352a6-110">*pSprites* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="352a6-110">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352a6-111">Tipo: **[ **D3DX10 \_ Sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="352a6-111">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="352a6-112">Matriz de sprites que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="352a6-112">The array of sprites to draw.</span></span> <span data-ttu-id="352a6-113">Vea [**D3DX10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="352a6-113">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="352a6-114">*cSprites* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="352a6-114">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352a6-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="352a6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="352a6-116">El número de sprites en pSprites.</span><span class="sxs-lookup"><span data-stu-id="352a6-116">The number of sprites in pSprites.</span></span>

</dd> <dt>

<span data-ttu-id="352a6-117">*cbSprite* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="352a6-117">*cbSprite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352a6-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="352a6-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="352a6-119">Tamaño de la estructura de Sprite que se pasa a pSprites.</span><span class="sxs-lookup"><span data-stu-id="352a6-119">The size of the sprite structure you are passing into pSprites.</span></span> <span data-ttu-id="352a6-120">Pasar 0 es el equivalente de pasar sizeof (D3DX10 \_ Sprite).</span><span class="sxs-lookup"><span data-stu-id="352a6-120">Passing in 0 is the equivalent of passing in sizeof(D3DX10\_SPRITE).</span></span>

</dd> <dt>

<span data-ttu-id="352a6-121">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="352a6-121">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="352a6-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="352a6-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="352a6-123">Reservado.</span><span class="sxs-lookup"><span data-stu-id="352a6-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="352a6-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="352a6-124">Return value</span></span>

<span data-ttu-id="352a6-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="352a6-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="352a6-126">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="352a6-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="352a6-127">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="352a6-127">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="352a6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="352a6-128">Requirements</span></span>



| <span data-ttu-id="352a6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="352a6-129">Requirement</span></span> | <span data-ttu-id="352a6-130">Value</span><span class="sxs-lookup"><span data-stu-id="352a6-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="352a6-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="352a6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="352a6-132"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="352a6-132"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="352a6-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="352a6-133">Library</span></span><br/> | <dl> <span data-ttu-id="352a6-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="352a6-134"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="352a6-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="352a6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="352a6-136">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="352a6-136">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="352a6-137">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="352a6-137">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
