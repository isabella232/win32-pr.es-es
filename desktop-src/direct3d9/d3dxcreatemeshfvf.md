---
description: Crea un objeto de malla con un código de formato de vértice flexible (FVF).
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: Función D3DXCreateMeshFVF (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9d5589b0f02bfcb85f9c0f0dc4dc5de69e2fb23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698403"
---
# <a name="d3dxcreatemeshfvf-function"></a><span data-ttu-id="d366d-103">D3DXCreateMeshFVF función)</span><span class="sxs-lookup"><span data-stu-id="d366d-103">D3DXCreateMeshFVF function</span></span>

<span data-ttu-id="d366d-104">Crea un objeto de malla con un código de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="d366d-104">Creates a mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d366d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d366d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="d366d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d366d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d366d-107">*NumFaces* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d366d-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d366d-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d366d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d366d-109">Número de caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="d366d-109">Number of faces for the mesh.</span></span> <span data-ttu-id="d366d-110">El intervalo válido para este número es mayor que 0 y uno menos que el valor DWORD máximo, normalmente 2 ³ ²-1, porque el último índice está reservado.</span><span class="sxs-lookup"><span data-stu-id="d366d-110">The valid range for this number is greater than 0, and one less than the max DWORD value, typically 2³² - 1, because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="d366d-111">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d366d-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d366d-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d366d-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d366d-113">Número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="d366d-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="d366d-114">Este parámetro debe ser mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="d366d-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="d366d-115">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d366d-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d366d-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d366d-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d366d-117">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) , especificando las opciones de creación para la malla.</span><span class="sxs-lookup"><span data-stu-id="d366d-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d366d-118">*FVF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d366d-118">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d366d-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d366d-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d366d-120">Combinación de [D3DFVF](d3dfvf.md) que describe el formato de vértice de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="d366d-120">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned mesh.</span></span> <span data-ttu-id="d366d-121">Esta función no es compatible con D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="d366d-121">This function does not support D3DFVF\_XYZRHW.</span></span>

</dd> <dt>

<span data-ttu-id="d366d-122">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d366d-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d366d-123">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d366d-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d366d-124">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo que se va a asociar a la malla.</span><span class="sxs-lookup"><span data-stu-id="d366d-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="d366d-125">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d366d-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d366d-126">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="d366d-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="d366d-127">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa el objeto de malla creado.</span><span class="sxs-lookup"><span data-stu-id="d366d-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d366d-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d366d-128">Return value</span></span>

<span data-ttu-id="d366d-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d366d-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d366d-130">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d366d-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d366d-131">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d366d-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d366d-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d366d-132">Requirements</span></span>



| <span data-ttu-id="d366d-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d366d-133">Requirement</span></span> | <span data-ttu-id="d366d-134">Value</span><span class="sxs-lookup"><span data-stu-id="d366d-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d366d-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d366d-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d366d-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d366d-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d366d-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d366d-137">Library</span></span><br/> | <dl> <span data-ttu-id="d366d-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d366d-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d366d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="d366d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d366d-140">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="d366d-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="d366d-141">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="d366d-141">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
