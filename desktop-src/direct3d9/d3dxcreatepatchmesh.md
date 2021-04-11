---
description: Crea una malla a partir de una malla de revisión de control.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: Función D3DXCreatePatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362771"
---
# <a name="d3dxcreatepatchmesh-function"></a><span data-ttu-id="a3674-103">D3DXCreatePatchMesh función)</span><span class="sxs-lookup"><span data-stu-id="a3674-103">D3DXCreatePatchMesh function</span></span>

<span data-ttu-id="a3674-104">Crea una malla a partir de una malla de revisión de control.</span><span class="sxs-lookup"><span data-stu-id="a3674-104">Creates a mesh from a control-patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3674-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3674-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="a3674-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3674-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3674-107">*Pinfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3674-107">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3674-108">Tipo: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3674-108">Type: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md)\***</span></span>

<span data-ttu-id="a3674-109">Estructura de información de revisión.</span><span class="sxs-lookup"><span data-stu-id="a3674-109">Patch information structure.</span></span> <span data-ttu-id="a3674-110">Para obtener más información, vea [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="a3674-110">For more information, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3674-111">*dwNumPatches* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3674-111">*dwNumPatches* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3674-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3674-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3674-113">Número de revisiones.</span><span class="sxs-lookup"><span data-stu-id="a3674-113">Number of patches.</span></span>

</dd> <dt>

<span data-ttu-id="a3674-114">*dwNumVertices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3674-114">*dwNumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3674-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3674-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3674-116">Número de vértices de control de la revisión.</span><span class="sxs-lookup"><span data-stu-id="a3674-116">Number of control vertices in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="a3674-117">*dwOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3674-117">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3674-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3674-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3674-119">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="a3674-119">Unused.</span></span> <span data-ttu-id="a3674-120">Reservado para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="a3674-120">Reserved for later use.</span></span>

</dd> <dt>

<span data-ttu-id="a3674-121">*pDecl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3674-121">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3674-122">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3674-122">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="a3674-123">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que describe el formato de vértice de la malla devuelta.</span><span class="sxs-lookup"><span data-stu-id="a3674-123">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a3674-124">*pD3DDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a3674-124">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3674-125">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a3674-125">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a3674-126">Puntero el dispositivo que crea la malla de revisión.</span><span class="sxs-lookup"><span data-stu-id="a3674-126">Pointer the device that creates the patch mesh.</span></span> <span data-ttu-id="a3674-127">Vea [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="a3674-127">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="a3674-128">*pPatchMesh* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a3674-128">*pPatchMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3674-129">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3674-129">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="a3674-130">Puntero al objeto [**ID3DXPatchMesh**](id3dxpatchmesh.md) que se crea.</span><span class="sxs-lookup"><span data-stu-id="a3674-130">Pointer to the [**ID3DXPatchMesh**](id3dxpatchmesh.md) object that is created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3674-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3674-131">Return value</span></span>

<span data-ttu-id="a3674-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3674-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3674-133">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3674-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3674-134">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a3674-134">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3674-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3674-135">Remarks</span></span>

<span data-ttu-id="a3674-136">Este método toma una malla de revisión de entrada y la convierte en una malla teselada.</span><span class="sxs-lookup"><span data-stu-id="a3674-136">This method takes an input patch mesh and converts it to a tessellated mesh.</span></span> <span data-ttu-id="a3674-137">Las mallas de revisión utilizan búferes de índice de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a3674-137">Patch meshes use 16-bit index buffers.</span></span> <span data-ttu-id="a3674-138">Por lo tanto, los índices de [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) son de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a3674-138">Therefore, indices to [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) are 16 bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3674-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3674-139">Requirements</span></span>



| <span data-ttu-id="a3674-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3674-140">Requirement</span></span> | <span data-ttu-id="a3674-141">Value</span><span class="sxs-lookup"><span data-stu-id="a3674-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3674-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3674-142">Header</span></span><br/>  | <dl> <span data-ttu-id="a3674-143"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3674-143"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a3674-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3674-144">Library</span></span><br/> | <dl> <span data-ttu-id="a3674-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3674-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3674-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3674-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3674-147">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="a3674-147">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="a3674-148">**D3DXPATCHINFO**</span><span class="sxs-lookup"><span data-stu-id="a3674-148">**D3DXPATCHINFO**</span></span>](d3dxpatchinfo.md)
</dt> </dl>

 

 
