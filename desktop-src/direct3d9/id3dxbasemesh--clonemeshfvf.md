---
description: Clona una malla con un código de formato de vértice flexible (FVF).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'ID3DXBaseMesh:: CloneMeshFVF (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707853"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a><span data-ttu-id="0a267-103">ID3DXBaseMesh:: CloneMeshFVF (método)</span><span class="sxs-lookup"><span data-stu-id="0a267-103">ID3DXBaseMesh::CloneMeshFVF method</span></span>

<span data-ttu-id="0a267-104">Clona una malla con un código de formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="0a267-104">Clones a mesh using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a267-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a267-105">Syntax</span></span>


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="0a267-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a267-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a267-107">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0a267-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a267-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a267-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a267-109">Combinación de una o varias marcas [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.</span><span class="sxs-lookup"><span data-stu-id="0a267-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0a267-110">*FVF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a267-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a267-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a267-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a267-112">Combinación de códigos de FVF, que especifica el formato de vértice de los vértices de la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="0a267-112">Combination of FVF codes, which specifies the vertex format for the vertices in the output mesh.</span></span> <span data-ttu-id="0a267-113">Para obtener los valores de los códigos, vea [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="0a267-113">For the values of the codes, see [D3DFVF](d3dfvf.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a267-114">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a267-114">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a267-115">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0a267-115">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0a267-116">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="0a267-116">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0a267-117">*ppCloneMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0a267-117">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0a267-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a267-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0a267-119">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla clonada.</span><span class="sxs-lookup"><span data-stu-id="0a267-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a267-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a267-120">Return value</span></span>

<span data-ttu-id="0a267-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a267-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a267-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a267-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0a267-123">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0a267-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a267-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a267-124">Remarks</span></span>

<span data-ttu-id="0a267-125">**ID3DXBaseMesh:: CloneMeshFVF** se usa para volver a formatear y cambiar el diseño de los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="0a267-125">**ID3DXBaseMesh::CloneMeshFVF** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="0a267-126">Esto se hace creando un nuevo objeto de malla.</span><span class="sxs-lookup"><span data-stu-id="0a267-126">This is done by creating a new mesh object.</span></span> <span data-ttu-id="0a267-127">Por ejemplo, úselo para agregar espacio para las normales, coordenadas de textura, colores, pesos, etc., que no estaban presentes antes.</span><span class="sxs-lookup"><span data-stu-id="0a267-127">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="0a267-128">[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) actualiza la declaración de vértices con información semántica diferente sin cambiar el diseño del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="0a267-128">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="0a267-129">Este método no modifica el contenido del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="0a267-129">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="0a267-130">Por ejemplo, úselo para cambiar la etiqueta de una coordenada de textura 3D como binormal o tangente, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="0a267-130">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a267-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a267-131">Requirements</span></span>



| <span data-ttu-id="0a267-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a267-132">Requirement</span></span> | <span data-ttu-id="0a267-133">Value</span><span class="sxs-lookup"><span data-stu-id="0a267-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a267-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a267-134">Header</span></span><br/>  | <dl> <span data-ttu-id="0a267-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a267-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="0a267-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a267-136">Library</span></span><br/> | <dl> <span data-ttu-id="0a267-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a267-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0a267-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a267-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a267-139">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="0a267-139">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="0a267-140">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="0a267-140">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
