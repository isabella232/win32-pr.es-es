---
description: Vectores de la tangente de proceso, binormalización y normal para una malla.
ms.assetid: 54edb9a5-440d-4191-a58f-296e5b804e0c
title: Función D3DXComputeTangentFrame (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrame
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b95d8f046499716a2c7972593093dfb409b11f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718445"
---
# <a name="d3dxcomputetangentframe-function"></a><span data-ttu-id="a82f0-103">D3DXComputeTangentFrame función)</span><span class="sxs-lookup"><span data-stu-id="a82f0-103">D3DXComputeTangentFrame function</span></span>

<span data-ttu-id="a82f0-104">Vectores de la tangente de proceso, binormalización y normal para una malla.</span><span class="sxs-lookup"><span data-stu-id="a82f0-104">Compute tangent, binormal, and normal vectors for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82f0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a82f0-105">Syntax</span></span>


```C++
HRESULT D3DXComputeTangentFrame(
  _In_ ID3DXMesh *pMesh,
  _In_ DWORD     dwOptions
);
```



## <a name="parameters"></a><span data-ttu-id="a82f0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a82f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a82f0-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a82f0-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82f0-108">Tipo: **[ **ID3DXMesh**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a82f0-108">Type: **[**ID3DXMesh**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a82f0-109">Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de entrada.</span><span class="sxs-lookup"><span data-stu-id="a82f0-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="a82f0-110">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a82f0-110">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82f0-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a82f0-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a82f0-112">Combinación de una o varias marcas de [**D3DXTANGENT**](./d3dxtangent.md) .</span><span class="sxs-lookup"><span data-stu-id="a82f0-112">Combination of one or more [**D3DXTANGENT**](./d3dxtangent.md) flags.</span></span>

<span data-ttu-id="a82f0-113">Use **null** para especificar las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="a82f0-113">Use **NULL** to specify the following options:</span></span>

-   <span data-ttu-id="a82f0-114">Pondera la longitud del vector normal por el ángulo, en radianes, que se repite en los dos bordes que abandonan el vértice.</span><span class="sxs-lookup"><span data-stu-id="a82f0-114">Weight the normal vector length by the angle, in radians, subtended by the two edges leaving the vertex.</span></span>
-   <span data-ttu-id="a82f0-115">Calcula las coordenadas cartesianas ortogonales a partir de las coordenadas de textura UV.</span><span class="sxs-lookup"><span data-stu-id="a82f0-115">Compute orthogonal Cartesian coordinates from the UV texture coordinates.</span></span>
-   <span data-ttu-id="a82f0-116">Las texturas no se ajustan en las direcciones U o V</span><span class="sxs-lookup"><span data-stu-id="a82f0-116">Textures are not wrapped in either U or V directions</span></span>
-   <span data-ttu-id="a82f0-117">Se normalizan las derivadas parciales con respecto a las coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a82f0-117">Partial derivatives with respect to texture coordinates are normalized.</span></span>
-   <span data-ttu-id="a82f0-118">Los vértices se ordenan en sentido contrario a las agujas del reloj alrededor de cada triángulo.</span><span class="sxs-lookup"><span data-stu-id="a82f0-118">Vertices are ordered in a counterclockwise direction around each triangle.</span></span>
-   <span data-ttu-id="a82f0-119">Use vectores normales por vértice ya presentes en la malla de entrada.</span><span class="sxs-lookup"><span data-stu-id="a82f0-119">Use per-vertex normal vectors already present in the input mesh.</span></span>
-   <span data-ttu-id="a82f0-120">Los resultados se almacenarán en la malla de entrada original.</span><span class="sxs-lookup"><span data-stu-id="a82f0-120">The results will be stored in the original input mesh.</span></span> <span data-ttu-id="a82f0-121">Se producirá un error en la función si es necesario crear nuevos vértices.</span><span class="sxs-lookup"><span data-stu-id="a82f0-121">The function will fail if new vertices need to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a82f0-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a82f0-122">Return value</span></span>

<span data-ttu-id="a82f0-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a82f0-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a82f0-124">Si la función se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a82f0-124">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a82f0-125">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a82f0-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a82f0-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a82f0-126">Remarks</span></span>

<span data-ttu-id="a82f0-127">Esta función simplemente llama a [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) con los siguientes parámetros de entrada:</span><span class="sxs-lookup"><span data-stu-id="a82f0-127">This function simply calls [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) with the following input parameters:</span></span>


```
D3DXComputeTangentFrameEx(pMesh, D3DDECLUSAGE_TEXCOORD, 0,   
      D3DDECLUSAGE_BINORMAL, 0, D3DDECLUSAGE_TANGENT, 0, 
      D3DDECLUSAGE_NORMAL, 0, 
      dwOptions | D3DXTANGENT_GENERATE_IN_PLACE,
      NULL, 0.01f, 0.25f, 0.01f, NULL, NULL);
```



<span data-ttu-id="a82f0-128">Las singularidades se controlan según sea necesario mediante la agrupación de los bordes y la división de los vértices.</span><span class="sxs-lookup"><span data-stu-id="a82f0-128">Singularities are handled as required by grouping edges and splitting vertices.</span></span> <span data-ttu-id="a82f0-129">Si es necesario dividir los vértices, se producirá un error en la función.</span><span class="sxs-lookup"><span data-stu-id="a82f0-129">If any vertices need to be split, the function will fail.</span></span> <span data-ttu-id="a82f0-130">El vector normal calculado en cada vértice siempre se normaliza para tener una longitud de unidad.</span><span class="sxs-lookup"><span data-stu-id="a82f0-130">The computed normal vector at each vertex is always normalized to have unit length.</span></span>

<span data-ttu-id="a82f0-131">La solución más sólida para calcular coordenadas cartesianas ortogonales consiste en no establecer marcas D3DXTANGENT \_ ortogonales \_ desde el \_ usuario y D3DXTANGENT \_ ortogonal \_ desde \_ V, de modo que las coordenadas ortogonales se calculan a partir de las coordenadas de textura UV.</span><span class="sxs-lookup"><span data-stu-id="a82f0-131">The most robust solution for computing orthogonal Cartesian coordinates is to not set flags D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V, so that orthogonal coordinates are computed from both UV texture coordinates.</span></span> <span data-ttu-id="a82f0-132">Sin embargo, en este caso, si U o V es cero, la función calculará las coordenadas ortogonales mediante D3DXTANGENT \_ ortogonal \_ desde \_ V o D3DXTANGENT se \_ ortogonala \_ desde \_ U, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a82f0-132">However, in this case, if either U or V is zero, then the function will compute orthogonal coordinates using D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V or D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="a82f0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a82f0-133">Requirements</span></span>



| <span data-ttu-id="a82f0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a82f0-134">Requirement</span></span> | <span data-ttu-id="a82f0-135">Value</span><span class="sxs-lookup"><span data-stu-id="a82f0-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a82f0-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a82f0-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a82f0-137"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a82f0-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a82f0-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a82f0-138">Library</span></span><br/> | <dl> <span data-ttu-id="a82f0-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a82f0-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a82f0-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="a82f0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82f0-141">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="a82f0-141">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="a82f0-142">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="a82f0-142">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> <dt>

[<span data-ttu-id="a82f0-143">**D3DXTANGENT**</span><span class="sxs-lookup"><span data-stu-id="a82f0-143">**D3DXTANGENT**</span></span>](./d3dxtangent.md)
</dt> </dl>

 

 
