---
description: Genera una malla simplificada usando los pesos proporcionados lo más cerca posible del MinValue dado.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Función D3DXSimplifyMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717735"
---
# <a name="d3dxsimplifymesh-function"></a><span data-ttu-id="5e487-103">D3DXSimplifyMesh función)</span><span class="sxs-lookup"><span data-stu-id="5e487-103">D3DXSimplifyMesh function</span></span>

<span data-ttu-id="5e487-104">Genera una malla simplificada usando los pesos proporcionados lo más cerca posible del MinValue dado.</span><span class="sxs-lookup"><span data-stu-id="5e487-104">Generates a simplified mesh using the provided weights that come as close as possible to the given MinValue.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e487-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e487-105">Syntax</span></span>


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="5e487-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e487-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e487-107">*pmesh* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e487-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e487-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="5e487-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="5e487-109">Puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla de origen.</span><span class="sxs-lookup"><span data-stu-id="5e487-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5e487-110">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e487-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e487-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e487-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5e487-112">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla que se van a simplificar.</span><span class="sxs-lookup"><span data-stu-id="5e487-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="5e487-113">*pVertexAttributeWeights* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e487-113">*pVertexAttributeWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e487-114">Tipo: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e487-114">Type: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)\***</span></span>

<span data-ttu-id="5e487-115">Puntero a una estructura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) , que contiene el peso de cada componente de vértice.</span><span class="sxs-lookup"><span data-stu-id="5e487-115">Pointer to a [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure, containing the weight for each vertex component.</span></span> <span data-ttu-id="5e487-116">Si este parámetro se establece en **null**, se usa una estructura predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5e487-116">If this parameter is set to **NULL**, a default structure is used.</span></span> <span data-ttu-id="5e487-117">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="5e487-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5e487-118">*pVertexWeights* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e487-118">*pVertexWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e487-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e487-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5e487-120">Puntero a una matriz de pesos de vértice.</span><span class="sxs-lookup"><span data-stu-id="5e487-120">Pointer to an array of vertex weights.</span></span> <span data-ttu-id="5e487-121">Si este parámetro se establece en **null**, todos los pesos de vértice se establecen en 1,0.</span><span class="sxs-lookup"><span data-stu-id="5e487-121">If this parameter is set to **NULL**, all vertex weights are set to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="5e487-122">*MinValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e487-122">*MinValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e487-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e487-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e487-124">Número de vértices o caras, dependiendo del marcador establecido en el parámetro *Options* , por el que se va a simplificar la malla de origen.</span><span class="sxs-lookup"><span data-stu-id="5e487-124">Number of vertices or faces, depending on the flag set in the *Options* parameter, by which to simplify the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="5e487-125">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5e487-125">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e487-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e487-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e487-127">Especifica las opciones de simplificación para la malla.</span><span class="sxs-lookup"><span data-stu-id="5e487-127">Specifies simplification options for the mesh.</span></span> <span data-ttu-id="5e487-128">Se puede establecer una de las marcas de [**D3DXMESHSIMP**](./d3dxmeshsimp.md) .</span><span class="sxs-lookup"><span data-stu-id="5e487-128">One of the flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) can be set.</span></span>

</dd> <dt>

<span data-ttu-id="5e487-129">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5e487-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e487-130">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e487-130">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="5e487-131">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla de simplificación devuelta.</span><span class="sxs-lookup"><span data-stu-id="5e487-131">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned simplification mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e487-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e487-132">Return value</span></span>

<span data-ttu-id="5e487-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e487-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e487-134">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5e487-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5e487-135">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="5e487-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e487-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e487-136">Remarks</span></span>

<span data-ttu-id="5e487-137">Esta función genera una malla que tiene vértices o caras *MinValue* .</span><span class="sxs-lookup"><span data-stu-id="5e487-137">This function generates a mesh that has *MinValue* vertices or faces.</span></span>

<span data-ttu-id="5e487-138">Si el proceso de simplificación no puede reducir la malla a *MinValue*, la llamada todavía se realiza correctamente porque *MinValue* es un mínimo deseado, no un mínimo absoluto.</span><span class="sxs-lookup"><span data-stu-id="5e487-138">If the simplification process cannot reduce the mesh to *MinValue*, the call still succeeds because *MinValue* is a desired minimum, not an absolute minimum.</span></span>

<span data-ttu-id="5e487-139">Si *pVertexAttributeWeights* se establece en **null**, los valores siguientes se asignan a la estructura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5e487-139">If *pVertexAttributeWeights* is set to **NULL**, the following values are assigned to the default [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure.</span></span>


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



<span data-ttu-id="5e487-140">Esta estructura predeterminada es lo que la mayoría de las aplicaciones deben usar porque solo tiene en cuenta el ajuste geométrico y normal.</span><span class="sxs-lookup"><span data-stu-id="5e487-140">This default structure is what most applications should use because it considers only geometric and normal adjustment.</span></span> <span data-ttu-id="5e487-141">Solo en casos especiales, los demás campos de miembro deben modificarse.</span><span class="sxs-lookup"><span data-stu-id="5e487-141">Only in special cases will the other member fields need to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e487-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e487-142">Requirements</span></span>



| <span data-ttu-id="5e487-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e487-143">Requirement</span></span> | <span data-ttu-id="5e487-144">Value</span><span class="sxs-lookup"><span data-stu-id="5e487-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e487-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e487-145">Header</span></span><br/>  | <dl> <span data-ttu-id="5e487-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e487-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5e487-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e487-147">Library</span></span><br/> | <dl> <span data-ttu-id="5e487-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e487-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e487-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e487-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e487-150">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="5e487-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
