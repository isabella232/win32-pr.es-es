---
description: 'Función D3DXFillVolumeTextureTX: usa una función compilada de lenguaje de sombreador de alto nivel (HLSL) para rellenar cada textura de cada nivel de mapa mipmap de una textura.'
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: Función D3DXFillVolumeTextureTX (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30aac53aa6451885bbd4ae2cac63050b01157974
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107633"
---
# <a name="d3dxfillvolumetexturetx-function"></a><span data-ttu-id="c2e79-103">Función D3DXFillVolumeTextureTX</span><span class="sxs-lookup"><span data-stu-id="c2e79-103">D3DXFillVolumeTextureTX function</span></span>

<span data-ttu-id="c2e79-104">Usa una función de lenguaje de sombreador de alto nivel (HLSL) compilada para rellenar cada texel de cada nivel de mapa mip de una textura.</span><span class="sxs-lookup"><span data-stu-id="c2e79-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e79-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2e79-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="c2e79-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2e79-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e79-107">*pTexture* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c2e79-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e79-108">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="c2e79-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="c2e79-109">Puntero a un [**objeto IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa la textura que se va a rellenar.</span><span class="sxs-lookup"><span data-stu-id="c2e79-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="c2e79-110">*pTextureShader* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c2e79-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2e79-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="c2e79-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="c2e79-112">Puntero a un [**objeto de sombreador de textura ID3DXTextureShader.**](id3dxtextureshader.md)</span><span class="sxs-lookup"><span data-stu-id="c2e79-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e79-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2e79-113">Return value</span></span>

<span data-ttu-id="c2e79-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2e79-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2e79-115">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2e79-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c2e79-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c2e79-116">If the function fails, the return value can be one of the following:D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e79-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c2e79-117">Remarks</span></span>

<span data-ttu-id="c2e79-118">El destino de textura debe ser una función HLSL que tome la semántica siguiente:</span><span class="sxs-lookup"><span data-stu-id="c2e79-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="c2e79-119">Un parámetro de entrada debe usar una semántica POSITION.</span><span class="sxs-lookup"><span data-stu-id="c2e79-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="c2e79-120">Un parámetro de entrada debe usar una semántica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="c2e79-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="c2e79-121">La función debe devolver un parámetro que use la semántica COLOR.</span><span class="sxs-lookup"><span data-stu-id="c2e79-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="c2e79-122">Los parámetros de entrada pueden estar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="c2e79-122">The input parameters can be in any order.</span></span> <span data-ttu-id="c2e79-123">Para obtener un ejemplo, [ **vea D3DXFillTextureTX.**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="c2e79-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e79-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e79-124">Requirements</span></span>



| <span data-ttu-id="c2e79-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e79-125">Requirement</span></span> | <span data-ttu-id="c2e79-126">Value</span><span class="sxs-lookup"><span data-stu-id="c2e79-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e79-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2e79-127">Header</span></span><br/>  | <dl> <span data-ttu-id="c2e79-128"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e79-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c2e79-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2e79-129">Library</span></span><br/> | <dl> <span data-ttu-id="c2e79-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2e79-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c2e79-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c2e79-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e79-132">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c2e79-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="c2e79-133">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="c2e79-133">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="c2e79-134">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="c2e79-134">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
