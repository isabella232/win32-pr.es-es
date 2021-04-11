---
description: La aplicación implementa esta interfaz para asignar o liberar objetos de contenedor de fotogramas y mallas. Se llama a los métodos de este método durante la carga y la destrucción de las jerarquías de Marcos.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interfaz ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083796"
---
# <a name="id3dxallocatehierarchy-interface"></a><span data-ttu-id="aa862-104">Interfaz ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="aa862-104">ID3DXAllocateHierarchy interface</span></span>

<span data-ttu-id="aa862-105">La aplicación implementa esta interfaz para asignar o liberar objetos de contenedor de fotogramas y mallas.</span><span class="sxs-lookup"><span data-stu-id="aa862-105">This interface is implemented by the application to allocate or free frame and mesh container objects.</span></span> <span data-ttu-id="aa862-106">Se llama a los métodos de este método durante la carga y la destrucción de las jerarquías de Marcos.</span><span class="sxs-lookup"><span data-stu-id="aa862-106">Methods on this are called during loading and destroying frame hierarchies.</span></span>

## <a name="members"></a><span data-ttu-id="aa862-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="aa862-107">Members</span></span>

<span data-ttu-id="aa862-108">La interfaz **ID3DXAllocateHierarchy** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aa862-108">The **ID3DXAllocateHierarchy** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aa862-109">**ID3DXAllocateHierarchy** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aa862-109">**ID3DXAllocateHierarchy** also has these types of members:</span></span>

-   [<span data-ttu-id="aa862-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa862-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aa862-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="aa862-111">Methods</span></span>

<span data-ttu-id="aa862-112">La interfaz **ID3DXAllocateHierarchy** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="aa862-112">The **ID3DXAllocateHierarchy** interface has these methods.</span></span>



| <span data-ttu-id="aa862-113">Método</span><span class="sxs-lookup"><span data-stu-id="aa862-113">Method</span></span>                                                                       | <span data-ttu-id="aa862-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa862-114">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="aa862-115">**CreateFrame**</span><span class="sxs-lookup"><span data-stu-id="aa862-115">**CreateFrame**</span></span>](id3dxallocatehierarchy--createframe.md)                   | <span data-ttu-id="aa862-116">Solicita la asignación de un objeto de marco.</span><span class="sxs-lookup"><span data-stu-id="aa862-116">Requests allocation of a frame object.</span></span><br/>            |
| [<span data-ttu-id="aa862-117">**CreateMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="aa862-117">**CreateMeshContainer**</span></span>](id3dxallocatehierarchy--createmeshcontainer.md)   | <span data-ttu-id="aa862-118">Solicita la asignación de un objeto de contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="aa862-118">Requests allocation of a mesh container object.</span></span><br/>   |
| [<span data-ttu-id="aa862-119">**DestroyFrame**</span><span class="sxs-lookup"><span data-stu-id="aa862-119">**DestroyFrame**</span></span>](id3dxallocatehierarchy--destroyframe.md)                 | <span data-ttu-id="aa862-120">Solicita la desasignación de un objeto de marco.</span><span class="sxs-lookup"><span data-stu-id="aa862-120">Requests deallocation of a frame object.</span></span><br/>          |
| [<span data-ttu-id="aa862-121">**DestroyMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="aa862-121">**DestroyMeshContainer**</span></span>](id3dxallocatehierarchy--destroymeshcontainer.md) | <span data-ttu-id="aa862-122">Solicita la desasignación de un objeto de contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="aa862-122">Requests deallocation of a mesh container object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa862-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa862-123">Remarks</span></span>

<span data-ttu-id="aa862-124">El tipo LPD3DXALLOCATEHIERARCHY se define como un puntero a esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="aa862-124">The LPD3DXALLOCATEHIERARCHY type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a><span data-ttu-id="aa862-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa862-125">Requirements</span></span>



| <span data-ttu-id="aa862-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa862-126">Requirement</span></span> | <span data-ttu-id="aa862-127">Value</span><span class="sxs-lookup"><span data-stu-id="aa862-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa862-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa862-128">Header</span></span><br/>  | <dl> <span data-ttu-id="aa862-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa862-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="aa862-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa862-130">Library</span></span><br/> | <dl> <span data-ttu-id="aa862-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa862-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="aa862-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa862-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa862-133">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="aa862-133">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
