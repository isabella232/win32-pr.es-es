---
description: Crea un objeto Mesh mediante un declarador.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: Función D3DXCreateMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cfb56fe5c52d2726dff0877522b6f72f70437552
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698346"
---
# <a name="d3dxcreatemesh-function"></a><span data-ttu-id="4e171-103">D3DXCreateMesh función)</span><span class="sxs-lookup"><span data-stu-id="4e171-103">D3DXCreateMesh function</span></span>

<span data-ttu-id="4e171-104">Crea un objeto Mesh mediante un declarador.</span><span class="sxs-lookup"><span data-stu-id="4e171-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e171-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e171-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="4e171-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e171-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e171-107">*NumFaces* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e171-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e171-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e171-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e171-109">Número de caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="4e171-109">Number of faces for the mesh.</span></span> <span data-ttu-id="4e171-110">El intervalo válido para este número es mayor que 0 y uno menos que el valor DWORD máximo (normalmente 65534), ya que el último índice está reservado.</span><span class="sxs-lookup"><span data-stu-id="4e171-110">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4e171-111">*NumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e171-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e171-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e171-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e171-113">Número de vértices de la malla.</span><span class="sxs-lookup"><span data-stu-id="4e171-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="4e171-114">Este parámetro debe ser mayor que 0.</span><span class="sxs-lookup"><span data-stu-id="4e171-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="4e171-115">*Opciones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4e171-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e171-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e171-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e171-117">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) , especificando las opciones de la malla.</span><span class="sxs-lookup"><span data-stu-id="4e171-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4e171-118">*pDeclaration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e171-118">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e171-119">Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e171-119">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="4e171-120">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que describe el formato de vértice de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="4e171-120">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="4e171-121">Este parámetro debe asignarse directamente a un formato de vértice flexible (FVF).</span><span class="sxs-lookup"><span data-stu-id="4e171-121">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="4e171-122">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4e171-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e171-123">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4e171-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4e171-124">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo que se va a asociar a la malla.</span><span class="sxs-lookup"><span data-stu-id="4e171-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="4e171-125">*ppMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4e171-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e171-126">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e171-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="4e171-127">Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa el objeto de malla creado.</span><span class="sxs-lookup"><span data-stu-id="4e171-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e171-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e171-128">Return value</span></span>

<span data-ttu-id="4e171-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e171-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e171-130">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e171-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e171-131">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4e171-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e171-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e171-132">Requirements</span></span>



| <span data-ttu-id="4e171-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e171-133">Requirement</span></span> | <span data-ttu-id="4e171-134">Value</span><span class="sxs-lookup"><span data-stu-id="4e171-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e171-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e171-135">Header</span></span><br/>  | <dl> <span data-ttu-id="4e171-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e171-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4e171-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e171-137">Library</span></span><br/> | <dl> <span data-ttu-id="4e171-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e171-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4e171-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e171-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e171-140">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="4e171-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="4e171-141">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="4e171-141">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
