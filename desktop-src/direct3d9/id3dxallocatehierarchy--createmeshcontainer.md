---
description: Solicita la asignación de un objeto de contenedor de malla.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'ID3DXAllocateHierarchy:: CreateMeshContainer (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698180"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a><span data-ttu-id="e3a55-103">ID3DXAllocateHierarchy:: CreateMeshContainer (método)</span><span class="sxs-lookup"><span data-stu-id="e3a55-103">ID3DXAllocateHierarchy::CreateMeshContainer method</span></span>

<span data-ttu-id="e3a55-104">Solicita la asignación de un objeto de contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="e3a55-104">Requests allocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3a55-105">Syntax</span></span>


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a><span data-ttu-id="e3a55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3a55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a55-107">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="e3a55-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a55-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3a55-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3a55-109">Nombre de la malla.</span><span class="sxs-lookup"><span data-stu-id="e3a55-109">Name of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e3a55-110">*pMeshData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3a55-110">*pMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a55-111">Tipo: **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3a55-111">Type: **const [**D3DXMESHDATA**](d3dxmeshdata.md)\***</span></span>

<span data-ttu-id="e3a55-112">Puntero a la estructura de datos de malla.</span><span class="sxs-lookup"><span data-stu-id="e3a55-112">Pointer to the mesh data structure.</span></span> <span data-ttu-id="e3a55-113">Vea [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="e3a55-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3a55-114">*pMaterials* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3a55-114">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a55-115">Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3a55-115">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="e3a55-116">Matriz de materiales utilizados en la malla.</span><span class="sxs-lookup"><span data-stu-id="e3a55-116">Array of materials used in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e3a55-117">*pEffectInstances* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3a55-117">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a55-118">Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3a55-118">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="e3a55-119">Matriz de instancias de efecto usadas en la malla.</span><span class="sxs-lookup"><span data-stu-id="e3a55-119">Array of effect instances used in the mesh.</span></span> <span data-ttu-id="e3a55-120">Vea [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="e3a55-120">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3a55-121">*NumMaterials* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3a55-121">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a55-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3a55-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e3a55-123">Número de materiales en la matriz de materiales.</span><span class="sxs-lookup"><span data-stu-id="e3a55-123">Number of materials in the materials array.</span></span>

</dd> <dt>

<span data-ttu-id="e3a55-124">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3a55-124">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a55-125">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3a55-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e3a55-126">Matriz de adyacencias para la malla.</span><span class="sxs-lookup"><span data-stu-id="e3a55-126">Adjacency array for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e3a55-127">*pSkinInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e3a55-127">*pSkinInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a55-128">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="e3a55-128">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

<span data-ttu-id="e3a55-129">Puntero al objeto de malla de máscara si se encuentran datos de máscara.</span><span class="sxs-lookup"><span data-stu-id="e3a55-129">Pointer to the skin mesh object if skin data is found.</span></span> <span data-ttu-id="e3a55-130">Vea [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="e3a55-130">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3a55-131">*ppNewMeshContainer* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e3a55-131">*ppNewMeshContainer* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e3a55-132">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3a55-132">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="e3a55-133">Devuelve el contenedor de malla creado.</span><span class="sxs-lookup"><span data-stu-id="e3a55-133">Returns the created mesh container.</span></span> <span data-ttu-id="e3a55-134">Vea [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="e3a55-134">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a55-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3a55-135">Return value</span></span>

<span data-ttu-id="e3a55-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e3a55-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e3a55-137">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="e3a55-137">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="e3a55-138">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e3a55-138">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="e3a55-139">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="e3a55-139">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a55-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3a55-140">Requirements</span></span>



| <span data-ttu-id="e3a55-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a55-141">Requirement</span></span> | <span data-ttu-id="e3a55-142">Value</span><span class="sxs-lookup"><span data-stu-id="e3a55-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a55-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3a55-143">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a55-144"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3a55-144"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e3a55-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3a55-145">Library</span></span><br/> | <dl> <span data-ttu-id="e3a55-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3a55-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3a55-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3a55-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a55-148">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="e3a55-148">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
