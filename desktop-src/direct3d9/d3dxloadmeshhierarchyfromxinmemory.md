---
description: 'Función D3DXLoadMeshHierarchyFromXInMemory: carga la primera jerarquía de fotogramas desde un archivo .x.'
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: Función D3DXLoadMeshHierarchyFromXInMemory (D3dx9anim.h)
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
ms.openlocfilehash: 551810c839e619985d9a380197553f5fe4fc9be8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098213"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a><span data-ttu-id="9bd9e-103">Función D3DXLoadMeshHierarchyFromXInMemory</span><span class="sxs-lookup"><span data-stu-id="9bd9e-103">D3DXLoadMeshHierarchyFromXInMemory function</span></span>

<span data-ttu-id="9bd9e-104">Carga la primera jerarquía de fotogramas desde un archivo .x.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd9e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9bd9e-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="9bd9e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9bd9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bd9e-107">*pMemory* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9bd9e-107">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd9e-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bd9e-109">Puntero a un búfer que contiene la jerarquía de malla.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-109">Pointer to a buffer that contains the mesh hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="9bd9e-110">*SizeOfMemory* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9bd9e-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd9e-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bd9e-112">Tamaño del búfer pMemory, en bytes.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-112">Size of the pMemory buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9bd9e-113">*MeshOptions* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9bd9e-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd9e-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9bd9e-115">Combinación de una o varias marcas de la [**enumeración D3DXMESH**](./d3dxmesh.md) que especifican opciones de creación para la malla.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9bd9e-116">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9bd9e-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd9e-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9bd9e-118">Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) el objeto de dispositivo asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9bd9e-119">*pAlloc* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9bd9e-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd9e-120">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="9bd9e-121">Puntero a una [**interfaz ID3DXAllocateHierarchy.**](id3dxallocatehierarchy.md)</span><span class="sxs-lookup"><span data-stu-id="9bd9e-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="9bd9e-122">*pUserDataLoader* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9bd9e-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd9e-123">Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="9bd9e-124">Interfaz proporcionada por la aplicación que permite cargar datos de usuario.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="9bd9e-125">Vea [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="9bd9e-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bd9e-126">*ppFramePlantrarchy* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9bd9e-126">*ppFrameHeirarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd9e-127">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="9bd9e-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="9bd9e-128">Devuelve un puntero a la jerarquía de fotogramas cargada.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="9bd9e-129">Vea [**D3DXFRAME.**](d3dxframe.md)</span><span class="sxs-lookup"><span data-stu-id="9bd9e-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bd9e-130">*ppAnimController* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9bd9e-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bd9e-131">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="9bd9e-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="9bd9e-132">Devuelve un puntero al controlador de animación correspondiente a la animación en el archivo .x.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="9bd9e-133">Esto se crea con pistas y eventos predeterminados.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-133">This is created with default tracks and events.</span></span> <span data-ttu-id="9bd9e-134">Vea [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="9bd9e-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bd9e-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9bd9e-135">Return value</span></span>

<span data-ttu-id="9bd9e-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9bd9e-137">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9bd9e-138">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bd9e-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9bd9e-139">Remarks</span></span>

<span data-ttu-id="9bd9e-140">Todas las mallas del archivo se contraerán en una malla de salida.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-140">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="9bd9e-141">Si el archivo contiene una jerarquía de fotogramas, todas las transformaciones se aplicarán a la malla.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-141">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd9e-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bd9e-142">Requirements</span></span>



| <span data-ttu-id="9bd9e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bd9e-143">Requirement</span></span> | <span data-ttu-id="9bd9e-144">Value</span><span class="sxs-lookup"><span data-stu-id="9bd9e-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd9e-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9bd9e-145">Header</span></span><br/>  | <dl> <span data-ttu-id="9bd9e-146"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="9bd9e-146"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9bd9e-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9bd9e-147">Library</span></span><br/> | <dl> <span data-ttu-id="9bd9e-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bd9e-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9bd9e-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9bd9e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd9e-150">Funciones de animación</span><span class="sxs-lookup"><span data-stu-id="9bd9e-150">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
