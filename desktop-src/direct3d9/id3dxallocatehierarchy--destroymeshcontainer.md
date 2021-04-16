---
description: Solicita la desasignación de un objeto de contenedor de malla.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: ID3DXAllocateHierarchy::D método estroyMeshContainer (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548118"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a><span data-ttu-id="7e423-103">ID3DXAllocateHierarchy::D método estroyMeshContainer</span><span class="sxs-lookup"><span data-stu-id="7e423-103">ID3DXAllocateHierarchy::DestroyMeshContainer method</span></span>

<span data-ttu-id="7e423-104">Solicita la desasignación de un objeto de contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="7e423-104">Requests deallocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e423-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e423-105">Syntax</span></span>


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a><span data-ttu-id="7e423-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e423-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e423-107">*pMeshContainerToFree* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e423-107">*pMeshContainerToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e423-108">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="7e423-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="7e423-109">Puntero al objeto de contenedor de malla que se va a desasignar.</span><span class="sxs-lookup"><span data-stu-id="7e423-109">Pointer to the mesh container object to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e423-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e423-110">Return value</span></span>

<span data-ttu-id="7e423-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e423-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e423-112">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="7e423-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="7e423-113">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e423-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="7e423-114">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="7e423-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e423-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e423-115">Requirements</span></span>



| <span data-ttu-id="7e423-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e423-116">Requirement</span></span> | <span data-ttu-id="7e423-117">Value</span><span class="sxs-lookup"><span data-stu-id="7e423-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e423-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7e423-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7e423-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e423-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7e423-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7e423-120">Library</span></span><br/> | <dl> <span data-ttu-id="7e423-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e423-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e423-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e423-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e423-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="7e423-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




