---
description: Agrega un objeto Sprite a la lista de objetos Sprite por lotes.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: ID3DXSprite::D método RAW (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718477"
---
# <a name="id3dxspritedraw-method"></a><span data-ttu-id="bcfe8-103">ID3DXSprite::D método sin formato</span><span class="sxs-lookup"><span data-stu-id="bcfe8-103">ID3DXSprite::Draw method</span></span>

<span data-ttu-id="bcfe8-104">Agrega un objeto Sprite a la lista de objetos Sprite por lotes.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-104">Adds a sprite to the list of batched sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcfe8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcfe8-105">Syntax</span></span>


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a><span data-ttu-id="bcfe8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcfe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcfe8-107">*pTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcfe8-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfe8-108">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="bcfe8-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="bcfe8-109">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de Sprite.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface that represents the sprite texture.</span></span>

</dd> <dt>

<span data-ttu-id="bcfe8-110">*pSrcRect* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcfe8-110">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfe8-111">Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="bcfe8-111">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="bcfe8-112">Puntero a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que indica la parte de la textura de origen que se va a usar para el sprite.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-112">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that indicates the portion of the source texture to use for the sprite.</span></span> <span data-ttu-id="bcfe8-113">Si este parámetro es **null**, se usa la imagen de origen completa para el sprite.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-113">If this parameter is **NULL**, then the entire source image is used for the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="bcfe8-114">*pCenter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcfe8-114">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfe8-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcfe8-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bcfe8-116">Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que identifica el centro del objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-116">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the center of the sprite.</span></span> <span data-ttu-id="bcfe8-117">Si este argumento es **null**, se usa el punto (0,0), que es la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-117">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="bcfe8-118">*pPosition* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bcfe8-118">*pPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfe8-119">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="bcfe8-119">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="bcfe8-120">Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que identifica la posición del objeto Sprite.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-120">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) vector that identifies the position of the sprite.</span></span> <span data-ttu-id="bcfe8-121">Si este argumento es **null**, se usa el punto (0,0), que es la esquina superior izquierda.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-121">If this argument is **NULL**, the point (0,0,0) is used, which is the upper-left corner.</span></span>

</dd> <dt>

<span data-ttu-id="bcfe8-122">*Color* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bcfe8-122">*Color* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfe8-123">Tipo: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="bcfe8-123">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="bcfe8-124">Tipo [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="bcfe8-124">[**D3DCOLOR**](d3dcolor.md) type.</span></span> <span data-ttu-id="bcfe8-125">El color y los canales alfa se modulan con este valor.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-125">The color and alpha channels are modulated by this value.</span></span> <span data-ttu-id="bcfe8-126">Un valor de 0xFFFFFFFF mantiene el color de origen y los datos alfa originales.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-126">A value of 0xFFFFFFFF maintains the original source color and alpha data.</span></span> <span data-ttu-id="bcfe8-127">Use la macro [**D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) para ayudar a generar este color.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-127">Use the [**D3DCOLOR\_RGBA**](d3dcolor-rgba.md) macro to help generate this color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcfe8-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcfe8-128">Return value</span></span>

<span data-ttu-id="bcfe8-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bcfe8-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bcfe8-130">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bcfe8-131">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcfe8-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcfe8-132">Remarks</span></span>

<span data-ttu-id="bcfe8-133">Para escalar, girar o traducir un Sprite, llame a [**ID3DXSprite:: SetTransform**](id3dxsprite--settransform.md) con una matriz que contenga los valores Scale, Rotate y translate (SRT) antes de llamar a ID3DXSprite::D RAW.</span><span class="sxs-lookup"><span data-stu-id="bcfe8-133">To scale, rotate, or translate a sprite, call [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) with a matrix that contains the scale, rotate, and translate (SRT) values, before calling ID3DXSprite::Draw.</span></span> <span data-ttu-id="bcfe8-134">Para obtener información sobre cómo establecer los valores de SRT en una matriz, vea [transformaciones de matriz](transforms.md).</span><span class="sxs-lookup"><span data-stu-id="bcfe8-134">For information about setting SRT values in a matrix, see [Matrix Transforms](transforms.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcfe8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcfe8-135">Requirements</span></span>



| <span data-ttu-id="bcfe8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcfe8-136">Requirement</span></span> | <span data-ttu-id="bcfe8-137">Value</span><span class="sxs-lookup"><span data-stu-id="bcfe8-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcfe8-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcfe8-138">Header</span></span><br/>  | <dl> <span data-ttu-id="bcfe8-139"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcfe8-139"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="bcfe8-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bcfe8-140">Library</span></span><br/> | <dl> <span data-ttu-id="bcfe8-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bcfe8-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bcfe8-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcfe8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcfe8-143">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="bcfe8-143">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="bcfe8-144">**ID3DXSprite::GetTransform**</span><span class="sxs-lookup"><span data-stu-id="bcfe8-144">**ID3DXSprite::GetTransform**</span></span>](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
