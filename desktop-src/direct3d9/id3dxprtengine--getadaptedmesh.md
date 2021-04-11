---
description: Devuelve una malla con modificaciones resultantes del muestreo espacial adaptable. La malla devuelta solo contiene posiciones, normales y coordenadas de textura (si se definen).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'ID3DXPRTEngine:: GetAdaptedMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362738"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a><span data-ttu-id="7b753-104">ID3DXPRTEngine:: GetAdaptedMesh (método)</span><span class="sxs-lookup"><span data-stu-id="7b753-104">ID3DXPRTEngine::GetAdaptedMesh method</span></span>

<span data-ttu-id="7b753-105">Devuelve una malla con modificaciones resultantes del muestreo espacial adaptable.</span><span class="sxs-lookup"><span data-stu-id="7b753-105">Returns a mesh with modifications resulting from adaptive spatial sampling.</span></span> <span data-ttu-id="7b753-106">La malla devuelta solo contiene posiciones, normales y coordenadas de textura (si se definen).</span><span class="sxs-lookup"><span data-stu-id="7b753-106">The returned mesh contains only positions, normals, and texture coordinates (if defined).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b753-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b753-107">Syntax</span></span>


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="7b753-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b753-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b753-109">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7b753-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b753-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7b753-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7b753-111">Puntero a un dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para crear la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="7b753-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="7b753-112">*pFaceRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7b753-112">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b753-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b753-113">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7b753-114">Puntero a la superficie de la malla original que se ha dividido para generar la superficie actual.</span><span class="sxs-lookup"><span data-stu-id="7b753-114">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> <dt>

<span data-ttu-id="7b753-115">*pVertRemap* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7b753-115">*pVertRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b753-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b753-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7b753-117">Puntero a una matriz de destino que contiene los tres vértices de malla originales que son los elementos primarios del vértice actual.</span><span class="sxs-lookup"><span data-stu-id="7b753-117">Pointer to a destination array containing the three original mesh vertices that are the parents of the current vertex.</span></span>

</dd> <dt>

<span data-ttu-id="7b753-118">*pfVertWeights* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7b753-118">*pfVertWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b753-119">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b753-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7b753-120">Puntero a una matriz de destino que contiene factores de mezcla para los vértices de pVertRemap.</span><span class="sxs-lookup"><span data-stu-id="7b753-120">Pointer to a destination array containing blending factors for the pVertRemap vertices.</span></span>

</dd> <dt>

<span data-ttu-id="7b753-121">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7b753-121">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b753-122">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b753-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="7b753-123">Puntero al objeto de malla [**ID3DXMesh**](id3dxmesh.md) de salida.</span><span class="sxs-lookup"><span data-stu-id="7b753-123">Pointer to the output [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b753-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7b753-124">Return value</span></span>

<span data-ttu-id="7b753-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b753-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b753-126">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b753-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7b753-127">Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="7b753-127">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="7b753-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b753-128">Remarks</span></span>

<span data-ttu-id="7b753-129">pVertRemap y pfVertWeights se pueden usar para interpolar cualquier valor por vértice en la malla.</span><span class="sxs-lookup"><span data-stu-id="7b753-129">pVertRemap and pfVertWeights can be used to interpolate any per-vertex value over the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b753-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b753-130">Requirements</span></span>



| <span data-ttu-id="7b753-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b753-131">Requirement</span></span> | <span data-ttu-id="7b753-132">Value</span><span class="sxs-lookup"><span data-stu-id="7b753-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b753-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b753-133">Header</span></span><br/>  | <dl> <span data-ttu-id="7b753-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b753-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7b753-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b753-135">Library</span></span><br/> | <dl> <span data-ttu-id="7b753-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b753-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7b753-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b753-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b753-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="7b753-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
