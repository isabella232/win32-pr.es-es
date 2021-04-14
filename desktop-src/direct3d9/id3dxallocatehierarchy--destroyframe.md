---
description: Solicita la desasignación de un objeto de marco.
ms.assetid: b2793744-1bba-4a2b-938c-44ed316358fd
title: ID3DXAllocateHierarchy::D método estroyFrame (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4a394501b9967d3f7cb6d3f6b2f30db168438278
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424511"
---
# <a name="id3dxallocatehierarchydestroyframe-method"></a><span data-ttu-id="985db-103">ID3DXAllocateHierarchy::D método estroyFrame</span><span class="sxs-lookup"><span data-stu-id="985db-103">ID3DXAllocateHierarchy::DestroyFrame method</span></span>

<span data-ttu-id="985db-104">Solicita la desasignación de un objeto de marco.</span><span class="sxs-lookup"><span data-stu-id="985db-104">Requests deallocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="985db-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="985db-105">Syntax</span></span>


```C++
HRESULT DestroyFrame(
  [in] LPD3DXFRAME pFrameToFree
);
```



## <a name="parameters"></a><span data-ttu-id="985db-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="985db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="985db-107">*pFrameToFree* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="985db-107">*pFrameToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="985db-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="985db-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="985db-109">Puntero al marco que se va a desasignar.</span><span class="sxs-lookup"><span data-stu-id="985db-109">Pointer to the frame to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="985db-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="985db-110">Return value</span></span>

<span data-ttu-id="985db-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="985db-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="985db-112">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="985db-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="985db-113">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="985db-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="985db-114">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="985db-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="985db-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="985db-115">Requirements</span></span>



| <span data-ttu-id="985db-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="985db-116">Requirement</span></span> | <span data-ttu-id="985db-117">Value</span><span class="sxs-lookup"><span data-stu-id="985db-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="985db-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="985db-118">Header</span></span><br/>  | <dl> <span data-ttu-id="985db-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="985db-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="985db-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="985db-120">Library</span></span><br/> | <dl> <span data-ttu-id="985db-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="985db-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="985db-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="985db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985db-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="985db-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 




