---
description: Agregue una matriz de sprites al lote de sprites que se va a representar.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: ID3DX10Sprite::D método rawSpritesBuffered (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718562"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a><span data-ttu-id="d2227-103">ID3DX10Sprite::D método rawSpritesBuffered</span><span class="sxs-lookup"><span data-stu-id="d2227-103">ID3DX10Sprite::DrawSpritesBuffered method</span></span>

<span data-ttu-id="d2227-104">Agregue una matriz de sprites al lote de sprites que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="d2227-104">Add an array of sprites to the batch of sprites to be rendered.</span></span> <span data-ttu-id="d2227-105">Se debe llamar a este método entre las llamadas a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) y [**ID3DX10Sprite:: end**](id3dx10sprite-end.md), y se debe llamar a [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) antes de que finalice el envío de todos los sprites por lotes al dispositivo para su representación.</span><span class="sxs-lookup"><span data-stu-id="d2227-105">This must be called in between calls to [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) and [**ID3DX10Sprite::End**](id3dx10sprite-end.md), and [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) must be called before End to send all of the batched sprites to the device for rendering.</span></span> <span data-ttu-id="d2227-106">Este método draw es muy útil cuando se dibuja un número pequeño de sprites que se desea almacenar en el búfer en un lote grande, como las fuentes.</span><span class="sxs-lookup"><span data-stu-id="d2227-106">This draw method is most useful when drawing a small number of sprites that you want buffered into a large batch, such as fonts.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2227-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2227-107">Syntax</span></span>


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
);
```



## <a name="parameters"></a><span data-ttu-id="d2227-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2227-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2227-109">*pSprites* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2227-109">*pSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2227-110">Tipo: **[ **D3DX10 \_ Sprite**](d3dx10-sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="d2227-110">Type: **[**D3DX10\_SPRITE**](d3dx10-sprite.md)\***</span></span>

<span data-ttu-id="d2227-111">Matriz de sprites que se va a dibujar.</span><span class="sxs-lookup"><span data-stu-id="d2227-111">The array of sprites to draw.</span></span> <span data-ttu-id="d2227-112">Vea [**D3DX10 \_ Sprite**](d3dx10-sprite.md).</span><span class="sxs-lookup"><span data-stu-id="d2227-112">See [**D3DX10\_SPRITE**](d3dx10-sprite.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2227-113">*cSprites* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d2227-113">*cSprites* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2227-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d2227-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d2227-115">El número de sprites en pSprites.</span><span class="sxs-lookup"><span data-stu-id="d2227-115">The number of sprites in pSprites.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2227-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2227-116">Return value</span></span>

<span data-ttu-id="d2227-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d2227-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d2227-118">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d2227-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d2227-119">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="d2227-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2227-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2227-120">Requirements</span></span>



| <span data-ttu-id="d2227-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2227-121">Requirement</span></span> | <span data-ttu-id="d2227-122">Value</span><span class="sxs-lookup"><span data-stu-id="d2227-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2227-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d2227-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d2227-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2227-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2227-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2227-125">Library</span></span><br/> | <dl> <span data-ttu-id="d2227-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2227-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2227-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2227-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2227-128">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="d2227-128">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="d2227-129">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="d2227-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
