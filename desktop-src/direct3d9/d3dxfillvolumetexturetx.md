---
description: Usa una función de lenguaje de sombreado de alto nivel (HLSL) compilada para rellenar cada textura de cada nivel de mipmap de una textura.
ms.assetid: f082e1d2-c433-482c-9288-58e5c558cdc5
title: Función D3DXFillVolumeTextureTX (D3dx9tex. h)
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
ms.openlocfilehash: de310ee6171924a5d2b61071d47c421739f15833
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678791"
---
# <a name="d3dxfillvolumetexturetx-function"></a><span data-ttu-id="4c5c9-103">D3DXFillVolumeTextureTX función)</span><span class="sxs-lookup"><span data-stu-id="4c5c9-103">D3DXFillVolumeTextureTX function</span></span>

<span data-ttu-id="4c5c9-104">Usa una función de lenguaje de sombreado de alto nivel (HLSL) compilada para rellenar cada textura de cada nivel de mipmap de una textura.</span><span class="sxs-lookup"><span data-stu-id="4c5c9-104">Uses a compiled high-level shader language (HLSL) function to fill each texel of each mipmap level of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c5c9-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTextureTX(
  _In_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_ LPD3DXTEXTURESHADER      pTextureShader
);
```



## <a name="parameters"></a><span data-ttu-id="4c5c9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c5c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c5c9-107">*pTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c5c9-107">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5c9-108">Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="4c5c9-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="4c5c9-109">Puntero a un objeto [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa la textura que se va a rellenar.</span><span class="sxs-lookup"><span data-stu-id="4c5c9-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) object, representing the texture to be filled.</span></span>

</dd> <dt>

<span data-ttu-id="4c5c9-110">*pTextureShader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4c5c9-110">*pTextureShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5c9-111">Tipo: **[ **LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span><span class="sxs-lookup"><span data-stu-id="4c5c9-111">Type: **[**LPD3DXTEXTURESHADER**](id3dxtextureshader.md)**</span></span>

<span data-ttu-id="4c5c9-112">Puntero a un objeto de sombreador de textura de [**ID3DXTextureShader**](id3dxtextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="4c5c9-112">Pointer to a [**ID3DXTextureShader**](id3dxtextureshader.md) texture shader object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c5c9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c5c9-113">Return value</span></span>

<span data-ttu-id="4c5c9-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c5c9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c5c9-115">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c5c9-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4c5c9-116">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4c5c9-116">If the function fails, the return value can be one of the following:D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c5c9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c5c9-117">Remarks</span></span>

<span data-ttu-id="4c5c9-118">El destino de la textura debe ser una función HLSL que tenga la semántica siguiente:</span><span class="sxs-lookup"><span data-stu-id="4c5c9-118">The texture target must be an HLSL function that takes contains the following semantics:</span></span>

-   <span data-ttu-id="4c5c9-119">Un parámetro de entrada debe utilizar una semántica de posición.</span><span class="sxs-lookup"><span data-stu-id="4c5c9-119">One input parameter must use a POSITION semantic.</span></span>
-   <span data-ttu-id="4c5c9-120">Un parámetro de entrada debe utilizar una semántica PSIZE.</span><span class="sxs-lookup"><span data-stu-id="4c5c9-120">One input parameter must use a PSIZE semantic.</span></span>
-   <span data-ttu-id="4c5c9-121">La función debe devolver un parámetro que use la semántica de COLOR.</span><span class="sxs-lookup"><span data-stu-id="4c5c9-121">The function must return a parameter that uses the COLOR semantic.</span></span>

<span data-ttu-id="4c5c9-122">Los parámetros de entrada pueden estar en cualquier orden.</span><span class="sxs-lookup"><span data-stu-id="4c5c9-122">The input parameters can be in any order.</span></span> <span data-ttu-id="4c5c9-123">Para obtener un ejemplo, consulte [ **D3DXFillTextureTX**](d3dxfilltexturetx.md)</span><span class="sxs-lookup"><span data-stu-id="4c5c9-123">For an example, see [**D3DXFillTextureTX**](d3dxfilltexturetx.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="4c5c9-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c5c9-124">Requirements</span></span>



| <span data-ttu-id="4c5c9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c5c9-125">Requirement</span></span> | <span data-ttu-id="4c5c9-126">Value</span><span class="sxs-lookup"><span data-stu-id="4c5c9-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5c9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c5c9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4c5c9-128"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c5c9-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4c5c9-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c5c9-129">Library</span></span><br/> | <dl> <span data-ttu-id="4c5c9-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c5c9-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4c5c9-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c5c9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5c9-132">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="4c5c9-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="4c5c9-133">**D3DXFillTextureTX**</span><span class="sxs-lookup"><span data-stu-id="4c5c9-133">**D3DXFillTextureTX**</span></span>](d3dxfilltexturetx.md)
</dt> <dt>

[<span data-ttu-id="4c5c9-134">**D3DXFillCubeTextureTX**</span><span class="sxs-lookup"><span data-stu-id="4c5c9-134">**D3DXFillCubeTextureTX**</span></span>](d3dxfillcubetexturetx.md)
</dt> </dl>

 

 
