---
description: 'Función D3DXComputeNormalMap: convierte un mapa de altura en un mapa normal. Los componentes (x, y,z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.'
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Función D3DXComputeNormalMap (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 920ad763f478a2e6bcb9fbe98cc7e2a677ebe783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105233"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="145a1-104">Función D3DXComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="145a1-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="145a1-105">Convierte un mapa de alto en un mapa normal.</span><span class="sxs-lookup"><span data-stu-id="145a1-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="145a1-106">Los componentes (x, y,z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.</span><span class="sxs-lookup"><span data-stu-id="145a1-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="145a1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="145a1-107">Syntax</span></span>


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a><span data-ttu-id="145a1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="145a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="145a1-109">*pTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="145a1-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="145a1-110">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="145a1-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="145a1-111">Puntero a una [**interfaz IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="145a1-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="145a1-112">*pSrcTexture* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="145a1-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145a1-113">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="145a1-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="145a1-114">Puntero a una [**interfaz IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura del mapa de alto de origen.</span><span class="sxs-lookup"><span data-stu-id="145a1-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="145a1-115">*pSrcPalette* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="145a1-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145a1-116">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="145a1-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="145a1-117">Puntero a un [**tipo PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene la paleta de origen de 256 colores o **NULL.**</span><span class="sxs-lookup"><span data-stu-id="145a1-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="145a1-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="145a1-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145a1-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="145a1-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="145a1-120">Una o varias [marcas D3DX \_ NORMALMAP](d3dx-normalmap.md) que controlan la generación de mapas normales.</span><span class="sxs-lookup"><span data-stu-id="145a1-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="145a1-121">*Canal* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="145a1-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145a1-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="145a1-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="145a1-123">Una [marca D3DX \_ CHANNEL](d3dx-channel.md) que especifica el origen de la información de alto.</span><span class="sxs-lookup"><span data-stu-id="145a1-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="145a1-124">*Amplitude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="145a1-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145a1-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="145a1-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="145a1-126">Multiplicador de valor constante que aumenta (o disminuye) los valores del mapa normal.</span><span class="sxs-lookup"><span data-stu-id="145a1-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="145a1-127">Los valores más altos suelen hacer que los aumentos sean más visibles, y los valores más bajos suelen hacer que los aumentos sean menos visibles.</span><span class="sxs-lookup"><span data-stu-id="145a1-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="145a1-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="145a1-128">Return value</span></span>

<span data-ttu-id="145a1-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="145a1-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="145a1-130">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="145a1-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="145a1-131">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="145a1-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="145a1-132">Comentarios</span><span class="sxs-lookup"><span data-stu-id="145a1-132">Remarks</span></span>

<span data-ttu-id="145a1-133">Este método calcula lo normal mediante la diferencia central con un tamaño de kernel de 3x3.</span><span class="sxs-lookup"><span data-stu-id="145a1-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="145a1-134">El denominador de diferenciación central utilizado es 2.0.</span><span class="sxs-lookup"><span data-stu-id="145a1-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="145a1-135">Los canales RGB del destino contienen componentes sesgados (x,y,z) de lo normal.</span><span class="sxs-lookup"><span data-stu-id="145a1-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="145a1-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="145a1-136">Requirements</span></span>



| <span data-ttu-id="145a1-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="145a1-137">Requirement</span></span> | <span data-ttu-id="145a1-138">Value</span><span class="sxs-lookup"><span data-stu-id="145a1-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="145a1-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="145a1-139">Header</span></span><br/>  | <dl> <span data-ttu-id="145a1-140"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="145a1-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="145a1-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="145a1-141">Library</span></span><br/> | <dl> <span data-ttu-id="145a1-142"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="145a1-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="145a1-143">Consulte también</span><span class="sxs-lookup"><span data-stu-id="145a1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145a1-144">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="145a1-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
