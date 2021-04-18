---
description: Convierte un mapa de alto en un mapa normal. Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Función D3DXComputeNormalMap (D3dx9tex. h)
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
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718401"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="4b452-104">D3DXComputeNormalMap función)</span><span class="sxs-lookup"><span data-stu-id="4b452-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="4b452-105">Convierte un mapa de alto en un mapa normal.</span><span class="sxs-lookup"><span data-stu-id="4b452-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="4b452-106">Los componentes (x, y, z) de cada normal se asignan a los canales (r, g, b) de la textura de salida.</span><span class="sxs-lookup"><span data-stu-id="4b452-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b452-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4b452-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4b452-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b452-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b452-109">*pTexture* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4b452-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b452-110">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="4b452-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="4b452-111">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de destino.</span><span class="sxs-lookup"><span data-stu-id="4b452-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="4b452-112">*pSrcTexture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b452-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b452-113">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="4b452-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="4b452-114">Puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa la textura de mapa de alto de origen.</span><span class="sxs-lookup"><span data-stu-id="4b452-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="4b452-115">*pSrcPalette* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b452-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b452-116">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="4b452-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4b452-117">Puntero a un tipo [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que contiene la paleta de origen de 256 colores o **null**.</span><span class="sxs-lookup"><span data-stu-id="4b452-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4b452-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4b452-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b452-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b452-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b452-120">Una o varias marcas de [ \_ NORMALMAP de D3DX](d3dx-normalmap.md) que controlan la generación de asignaciones normales.</span><span class="sxs-lookup"><span data-stu-id="4b452-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="4b452-121">*Canal* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4b452-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b452-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b452-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b452-123">Una marca de [ \_ canal de D3DX](d3dx-channel.md) que especifica el origen de la información de alto.</span><span class="sxs-lookup"><span data-stu-id="4b452-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="4b452-124">*Amplitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4b452-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b452-125">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b452-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4b452-126">Multiplicador de valor constante que aumenta (o reduce) los valores del mapa normal.</span><span class="sxs-lookup"><span data-stu-id="4b452-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="4b452-127">Los valores más altos normalmente hacen que los golpes sean más visibles, los valores más bajos normalmente hacen que los golpes sean menos visibles.</span><span class="sxs-lookup"><span data-stu-id="4b452-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b452-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b452-128">Return value</span></span>

<span data-ttu-id="4b452-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b452-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b452-130">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4b452-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4b452-131">Si se produce un error en la función, el valor devuelto puede ser el siguiente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4b452-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b452-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b452-132">Remarks</span></span>

<span data-ttu-id="4b452-133">Este método calcula el normal mediante el uso de la diferencia central con el tamaño del kernel 3x3.</span><span class="sxs-lookup"><span data-stu-id="4b452-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="4b452-134">El denominador de diferencia central usado es 2,0.</span><span class="sxs-lookup"><span data-stu-id="4b452-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="4b452-135">Los canales RGB del destino contienen componentes sesgados (x, y, z) de la normal.</span><span class="sxs-lookup"><span data-stu-id="4b452-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b452-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b452-136">Requirements</span></span>



| <span data-ttu-id="4b452-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b452-137">Requirement</span></span> | <span data-ttu-id="4b452-138">Value</span><span class="sxs-lookup"><span data-stu-id="4b452-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b452-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b452-139">Header</span></span><br/>  | <dl> <span data-ttu-id="4b452-140"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b452-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4b452-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b452-141">Library</span></span><br/> | <dl> <span data-ttu-id="4b452-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b452-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4b452-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b452-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b452-144">Funciones de textura en D3DX 9</span><span class="sxs-lookup"><span data-stu-id="4b452-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
