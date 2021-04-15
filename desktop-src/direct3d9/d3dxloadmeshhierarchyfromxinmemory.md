---
description: Carga la primera jerarquía de fotogramas desde un archivo. x.
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: Función D3DXLoadMeshHierarchyFromXInMemory (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91cf119fc8907701f87ebb5bda1bb0bf45294aba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708073"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a><span data-ttu-id="85368-103">D3DXLoadMeshHierarchyFromXInMemory función)</span><span class="sxs-lookup"><span data-stu-id="85368-103">D3DXLoadMeshHierarchyFromXInMemory function</span></span>

<span data-ttu-id="85368-104">Carga la primera jerarquía de fotogramas desde un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="85368-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="85368-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85368-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="85368-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85368-107">*pMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85368-107">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85368-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85368-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85368-109">Puntero a un búfer que contiene la jerarquía de malla.</span><span class="sxs-lookup"><span data-stu-id="85368-109">Pointer to a buffer that contains the mesh hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="85368-110">*SizeOfMemory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85368-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85368-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85368-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85368-112">Tamaño del búfer de pMemory, en bytes.</span><span class="sxs-lookup"><span data-stu-id="85368-112">Size of the pMemory buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="85368-113">*MeshOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85368-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85368-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85368-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85368-115">Combinación de una o varias marcas de la enumeración [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.</span><span class="sxs-lookup"><span data-stu-id="85368-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="85368-116">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85368-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85368-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="85368-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="85368-118">Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="85368-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="85368-119">*pAlloc* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85368-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85368-120">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="85368-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="85368-121">Puntero a una interfaz [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="85368-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="85368-122">*pUserDataLoader* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85368-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85368-123">Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="85368-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="85368-124">Interfaz proporcionada por la aplicación que permite cargar datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="85368-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="85368-125">Vea [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="85368-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="85368-126">*ppFrameHeirarchy* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="85368-126">*ppFrameHeirarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85368-127">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="85368-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="85368-128">Devuelve un puntero a la jerarquía de Marcos cargada.</span><span class="sxs-lookup"><span data-stu-id="85368-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="85368-129">Vea [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="85368-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="85368-130">*ppAnimController* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="85368-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85368-131">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="85368-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="85368-132">Devuelve un puntero al controlador de animación correspondiente a la animación en el archivo. x.</span><span class="sxs-lookup"><span data-stu-id="85368-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="85368-133">Se crea con pistas y eventos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="85368-133">This is created with default tracks and events.</span></span> <span data-ttu-id="85368-134">Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="85368-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85368-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85368-135">Return value</span></span>

<span data-ttu-id="85368-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="85368-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="85368-137">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="85368-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="85368-138">Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="85368-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="85368-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85368-139">Remarks</span></span>

<span data-ttu-id="85368-140">Todas las mallas del archivo se contraen en una malla de salida.</span><span class="sxs-lookup"><span data-stu-id="85368-140">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="85368-141">Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.</span><span class="sxs-lookup"><span data-stu-id="85368-141">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="85368-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85368-142">Requirements</span></span>



| <span data-ttu-id="85368-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="85368-143">Requirement</span></span> | <span data-ttu-id="85368-144">Value</span><span class="sxs-lookup"><span data-stu-id="85368-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85368-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85368-145">Header</span></span><br/>  | <dl> <span data-ttu-id="85368-146"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="85368-146"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="85368-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85368-147">Library</span></span><br/> | <dl> <span data-ttu-id="85368-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85368-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85368-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="85368-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85368-150">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="85368-150">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
