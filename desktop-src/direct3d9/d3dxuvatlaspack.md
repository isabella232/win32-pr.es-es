---
description: Empaquetar los datos de la partición de malla en un Atlas.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Función D3DXUVAtlasPack (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717725"
---
# <a name="d3dxuvatlaspack-function"></a><span data-ttu-id="a9f91-103">D3DXUVAtlasPack función)</span><span class="sxs-lookup"><span data-stu-id="a9f91-103">D3DXUVAtlasPack function</span></span>

<span data-ttu-id="a9f91-104">Empaquetar los datos de la partición de malla en un Atlas.</span><span class="sxs-lookup"><span data-stu-id="a9f91-104">Pack mesh partitioning data into an atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f91-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a9f91-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a><span data-ttu-id="a9f91-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a9f91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9f91-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="a9f91-109">Puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el Atlas.</span><span class="sxs-lookup"><span data-stu-id="a9f91-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="a9f91-110">Como mínimo, la malla debe contener datos de posición y coordenadas de textura 2D.</span><span class="sxs-lookup"><span data-stu-id="a9f91-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-111">*dwWidth* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-111">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9f91-113">Ancho de la textura.</span><span class="sxs-lookup"><span data-stu-id="a9f91-113">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-114">*dwHeight* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-114">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9f91-116">Alto de textura.</span><span class="sxs-lookup"><span data-stu-id="a9f91-116">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-117">*fGutter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-117">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9f91-119">Distancia mínima, en textura, entre dos gráficos en el Atlas.</span><span class="sxs-lookup"><span data-stu-id="a9f91-119">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="a9f91-120">El margen se escala siempre por el ancho; por lo tanto, si se usa un medianil de 2,5 en una textura 512 x 512, la distancia mínima entre dos gráficos es 2,5/512,0 textura.</span><span class="sxs-lookup"><span data-stu-id="a9f91-120">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-121">*dwTextureIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-121">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9f91-123">Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="a9f91-123">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-124">*pdwPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="a9f91-124">*pdwPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="a9f91-125">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="a9f91-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a9f91-126">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="a9f91-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="a9f91-127">Debe derivarse del ppPartitionResultAdjacency devuelto desde [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span><span class="sxs-lookup"><span data-stu-id="a9f91-127">It should be derived from the ppPartitionResultAdjacency returned from [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span></span> <span data-ttu-id="a9f91-128">Este valor no puede ser **null** porque Pack debe saber dónde se han cortado los gráficos en el paso de partición para encontrar los bordes de cada gráfico.</span><span class="sxs-lookup"><span data-stu-id="a9f91-128">This value cannot be **NULL**, because Pack needs to know where charts were cut in the partition step in order to find the edges of each chart.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-129">*pCallback* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-129">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-130">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-130">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="a9f91-131">Un puntero a una función de devolución de llamada (vea [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) que es útil para supervisar el progreso.</span><span class="sxs-lookup"><span data-stu-id="a9f91-131">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-132">*fCallbackFrequency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-132">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-133">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9f91-134">Especificar la frecuencia con la que D3DX llamará a la devolución de llamada; un valor predeterminado razonable es 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="a9f91-134">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-135">*pUserContent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-135">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-136">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-136">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9f91-137">Puntero void que se va a devolver a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="a9f91-137">A void pointer to be passed back to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-138">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-138">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a9f91-140">Este parámetro de opciones está actualmente reservado.</span><span class="sxs-lookup"><span data-stu-id="a9f91-140">This options parameter is currently reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a9f91-141">*pFacePartitioning* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a9f91-141">*pFacePartitioning* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f91-142">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-142">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="a9f91-143">Un puntero a un [**ID3DXBuffer**](id3dxbuffer.md) que contiene la matriz de la creación de particiones de caras final.</span><span class="sxs-lookup"><span data-stu-id="a9f91-143">A pointer to an [**ID3DXBuffer**](id3dxbuffer.md) containing the array of the final face-partitioning.</span></span> <span data-ttu-id="a9f91-144">Cada elemento contiene un valor DWORD por cada tipo.</span><span class="sxs-lookup"><span data-stu-id="a9f91-144">Each element contains one DWORD per face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9f91-145">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9f91-145">Return value</span></span>

<span data-ttu-id="a9f91-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a9f91-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a9f91-147">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a9f91-147">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9f91-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9f91-148">Requirements</span></span>



| <span data-ttu-id="a9f91-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9f91-149">Requirement</span></span> | <span data-ttu-id="a9f91-150">Value</span><span class="sxs-lookup"><span data-stu-id="a9f91-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f91-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9f91-151">Header</span></span><br/>  | <dl> <span data-ttu-id="a9f91-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f91-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a9f91-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a9f91-153">Library</span></span><br/> | <dl> <span data-ttu-id="a9f91-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9f91-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a9f91-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9f91-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f91-156">Funciones de UVAtlas</span><span class="sxs-lookup"><span data-stu-id="a9f91-156">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
