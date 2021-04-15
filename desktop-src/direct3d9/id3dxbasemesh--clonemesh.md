---
description: Clona una malla mediante un declarador.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'ID3DXBaseMesh:: CloneMesh (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 421b72a080564886a10c187594223fb58a0b69fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707854"
---
# <a name="id3dxbasemeshclonemesh-method"></a><span data-ttu-id="83347-103">ID3DXBaseMesh:: CloneMesh (método)</span><span class="sxs-lookup"><span data-stu-id="83347-103">ID3DXBaseMesh::CloneMesh method</span></span>

<span data-ttu-id="83347-104">Clona una malla mediante un declarador.</span><span class="sxs-lookup"><span data-stu-id="83347-104">Clones a mesh using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="83347-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="83347-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="83347-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="83347-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83347-107">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="83347-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83347-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="83347-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="83347-109">Combinación de una o varias marcas [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.</span><span class="sxs-lookup"><span data-stu-id="83347-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="83347-110">*pDeclaration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83347-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83347-111">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="83347-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="83347-112">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que especifican el formato de vértice de los vértices de la malla de salida.</span><span class="sxs-lookup"><span data-stu-id="83347-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, which specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="83347-113">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="83347-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83347-114">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="83347-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="83347-115">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="83347-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="83347-116">*ppCloneMesh* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="83347-116">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="83347-117">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="83347-117">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="83347-118">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla clonada.</span><span class="sxs-lookup"><span data-stu-id="83347-118">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83347-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="83347-119">Return value</span></span>

<span data-ttu-id="83347-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="83347-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="83347-121">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="83347-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="83347-122">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="83347-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="83347-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="83347-123">Remarks</span></span>

<span data-ttu-id="83347-124">**ID3DXBaseMesh:: CloneMesh** se usa para volver a formatear y cambiar el diseño de los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="83347-124">**ID3DXBaseMesh::CloneMesh** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="83347-125">Esto se hace creando un nuevo objeto de malla.</span><span class="sxs-lookup"><span data-stu-id="83347-125">This is done by creating a new mesh object.</span></span> <span data-ttu-id="83347-126">Por ejemplo, úselo para agregar espacio para las normales, coordenadas de textura, colores, pesos, etc., que no estaban presentes antes.</span><span class="sxs-lookup"><span data-stu-id="83347-126">For example, use it to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="83347-127">[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) actualiza la declaración de vértices con información semántica diferente sin cambiar el diseño del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="83347-127">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="83347-128">Este método no modifica el contenido del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="83347-128">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="83347-129">Por ejemplo, úselo para cambiar la etiqueta de una coordenada de textura 3D como binormal o tangente, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="83347-129">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="83347-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83347-130">Requirements</span></span>



| <span data-ttu-id="83347-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="83347-131">Requirement</span></span> | <span data-ttu-id="83347-132">Value</span><span class="sxs-lookup"><span data-stu-id="83347-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83347-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="83347-133">Header</span></span><br/>  | <dl> <span data-ttu-id="83347-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="83347-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="83347-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83347-135">Library</span></span><br/> | <dl> <span data-ttu-id="83347-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83347-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="83347-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="83347-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83347-138">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="83347-138">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="83347-139">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="83347-139">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="83347-140">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="83347-140">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
