---
description: Cree un Sprite para dibujar una textura 2D. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar Direct2D y la biblioteca DirectXTK, SpriteBatch Class.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Función D3DX10CreateSprite (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707807"
---
# <a name="d3dx10createsprite-function"></a><span data-ttu-id="52f20-103">D3DX10CreateSprite función)</span><span class="sxs-lookup"><span data-stu-id="52f20-103">D3DX10CreateSprite function</span></span>

<span data-ttu-id="52f20-104">Cree un Sprite para dibujar una textura 2D.</span><span class="sxs-lookup"><span data-stu-id="52f20-104">Create a sprite for drawing a 2D texture.</span></span>

> [!Note]  
> <span data-ttu-id="52f20-105">En lugar de usar esta función, se recomienda usar [Direct2D](../direct2d/direct2d-portal.md) y la biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteBatch** Class.</span><span class="sxs-lookup"><span data-stu-id="52f20-105">Instead of using this function, we recommend that you use [Direct2D](../direct2d/direct2d-portal.md) and the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SpriteBatch** class.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="52f20-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52f20-106">Syntax</span></span>


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="52f20-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52f20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52f20-108">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52f20-108">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52f20-109">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="52f20-109">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="52f20-110">Un puntero al dispositivo (vea la [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que va a dibujar el sprite.</span><span class="sxs-lookup"><span data-stu-id="52f20-110">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will draw the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="52f20-111">*cDeviceBufferSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="52f20-111">*cDeviceBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52f20-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="52f20-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="52f20-113">Tamaño del búfer de vértices, en número de sprites, que se enviará al dispositivo cuando se llame a [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) o [**ID3DX10Sprite::D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) .</span><span class="sxs-lookup"><span data-stu-id="52f20-113">The size of the vertex buffer, in number of sprites, that will be sent to the device when [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) or [**ID3DX10Sprite::DrawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) is called.</span></span> <span data-ttu-id="52f20-114">Debe ser un número pequeño si sabe que va a representar un pequeño número de sprites a la vez (para ahorrar memoria) y un número grande si sabe que va a representar un gran número de objetos Sprite a la vez.</span><span class="sxs-lookup"><span data-stu-id="52f20-114">This should be a small number if you know you will be rendering a small number of sprites at a time (to save memory) and a large number if you know you will be rendering a large number of sprites at a time.</span></span> <span data-ttu-id="52f20-115">El valor máximo es 4096.</span><span class="sxs-lookup"><span data-stu-id="52f20-115">The maximum value is 4096.</span></span> <span data-ttu-id="52f20-116">Si se especifica 0, el tamaño del búfer de vértices se establecerá automáticamente en 4096.</span><span class="sxs-lookup"><span data-stu-id="52f20-116">If 0 is specified, the vertex buffer size will automatically be set to 4096.</span></span>

</dd> <dt>

<span data-ttu-id="52f20-117">*ppSprite* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="52f20-117">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52f20-118">Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="52f20-118">Type: **[**LPD3DX10SPRITE**](id3dx10sprite.md)\***</span></span>

<span data-ttu-id="52f20-119">La dirección de un puntero a una interfaz de Sprite (vea la [**interfaz ID3DX10Sprite**](id3dx10sprite.md)).</span><span class="sxs-lookup"><span data-stu-id="52f20-119">The address of a pointer to a sprite interface (see [**ID3DX10Sprite Interface**](id3dx10sprite.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52f20-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52f20-120">Return value</span></span>

<span data-ttu-id="52f20-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52f20-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52f20-122">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52f20-122">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="52f20-123">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="52f20-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="52f20-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52f20-124">Requirements</span></span>



| <span data-ttu-id="52f20-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="52f20-125">Requirement</span></span> | <span data-ttu-id="52f20-126">Value</span><span class="sxs-lookup"><span data-stu-id="52f20-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52f20-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52f20-127">Header</span></span><br/>  | <dl> <span data-ttu-id="52f20-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="52f20-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="52f20-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52f20-129">Library</span></span><br/> | <dl> <span data-ttu-id="52f20-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52f20-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52f20-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="52f20-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52f20-132">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="52f20-132">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
