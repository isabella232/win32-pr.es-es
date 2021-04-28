---
description: 'Función D3DXFillCubeTextureTX: usa una función compilada de lenguaje de sombreador de alto nivel (HLSL) para rellenar cada texel de cada nivel de mapa mip de una textura.'
ms.assetid: a0c36967-57e6-4771-8e9f-f32949c12001
title: Función D3DXFillCubeTextureTX (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillCubeTextureTX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c6d054900f3f4c4710e22c54759161800137c2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107673"
---
# <a name="d3dxfillcubetexturetx-function"></a><span data-ttu-id="f1320-103">Función D3DXFillCubeTextureTX</span><span class="sxs-lookup"><span data-stu-id="f1320-103">D3DXFillCubeTextureTX function</span></span>

<span data-ttu-id="f1320-104">Usa una función de lenguaje de sombreador de alto nivel (HLSL) compilada para rellenar cada texel de cada nivel de mapa mip de una textura.</span><span class="sxs-lookup"><span data-stu-id="f1320-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1320-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1320-105">Syntax</span></span>


```C++
HRESULT D3DXFillCubeTextureTX(
  _In_ LPDIRECT3DCUBETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER    pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="f1320-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1320-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1320-107">*pTexture* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f1320-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1320-108">Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="f1320-108">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="f1320-109">Puntero a un [**objeto IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa la textura que se va a rellenar.</span><span class="sxs-lookup"><span data-stu-id="f1320-109">Pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="f1320-110">*pTextureShader* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="f1320-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1320-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="f1320-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="f1320-112">Puntero a un [**objeto de sombreador de textura ID3DXTextureShader.**](id3dxtextureshader.md)</span><span class="sxs-lookup"><span data-stu-id="f1320-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1320-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1320-113">Return value</span></span>

<span data-ttu-id="f1320-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1320-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1320-115">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f1320-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f1320-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f1320-116">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1320-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1320-117">Remarks</span></span>

<span data-ttu-id="f1320-118">El destino de textura debe ser una función HLSL que tome la semántica siguiente:</span><span class="sxs-lookup"><span data-stu-id="f1320-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="f1320-119">Un parámetro de entrada debe usar una semántica POSITION.</span><span class="sxs-lookup"><span data-stu-id="f1320-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="f1320-120">Un parámetro de entrada debe usar una semántica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="f1320-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="f1320-121">La función debe devolver un parámetro que use la semántica COLOR.</span><span class="sxs-lookup"><span data-stu-id="f1320-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="f1320-122">Los parámetros de entrada pueden estar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="f1320-122">The input parameters can be in any order.</span></span> <span data-ttu-id="f1320-123">Para obtener un ejemplo, [ **vea D3DXFillTextureTX.**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="f1320-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="f1320-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1320-124">Requirements</span></span>



| <span data-ttu-id="f1320-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1320-125">Requirement</span></span> | <span data-ttu-id="f1320-126">Value</span><span class="sxs-lookup"><span data-stu-id="f1320-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1320-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1320-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f1320-128"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="f1320-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f1320-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1320-129">Library</span></span><br/> | <dl> <span data-ttu-id="f1320-130"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1320-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f1320-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f1320-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1320-132">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f1320-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="f1320-133">**D3DXFillVolumeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="f1320-133">**D3DXFillVolumeTextureTX**</span></span>](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 
