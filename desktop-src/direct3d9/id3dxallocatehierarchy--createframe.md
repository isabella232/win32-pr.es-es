---
description: Solicita la asignación de un objeto de marco.
ms.assetid: 977e40d6-bf49-44b6-ac95-88e7f778ea50
title: 'ID3DXAllocateHierarchy:: CreateFrame (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6a3a13dd4d3b3dfaffb26632ff6ad5cc8666f86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698332"
---
# <a name="id3dxallocatehierarchycreateframe-method"></a><span data-ttu-id="0f92b-103">ID3DXAllocateHierarchy:: CreateFrame (método)</span><span class="sxs-lookup"><span data-stu-id="0f92b-103">ID3DXAllocateHierarchy::CreateFrame method</span></span>

<span data-ttu-id="0f92b-104">Solicita la asignación de un objeto de marco.</span><span class="sxs-lookup"><span data-stu-id="0f92b-104">Requests allocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f92b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f92b-105">Syntax</span></span>


```C++
HRESULT CreateFrame(
  [in]          LPCSTR      Name,
  [out, retval] LPD3DXFRAME *ppNewFrame
);
```



## <a name="parameters"></a><span data-ttu-id="0f92b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f92b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f92b-107">*Nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="0f92b-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f92b-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f92b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f92b-109">Nombre del marco que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="0f92b-109">Name of the frame to be created.</span></span>

</dd> <dt>

<span data-ttu-id="0f92b-110">*ppNewFrame* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0f92b-110">*ppNewFrame* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0f92b-111">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f92b-111">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="0f92b-112">Devuelve el objeto de marco creado.</span><span class="sxs-lookup"><span data-stu-id="0f92b-112">Returns the created frame object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f92b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f92b-113">Return value</span></span>

<span data-ttu-id="0f92b-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f92b-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f92b-115">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="0f92b-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="0f92b-116">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f92b-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="0f92b-117">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="0f92b-117">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f92b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f92b-118">Requirements</span></span>



| <span data-ttu-id="0f92b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f92b-119">Requirement</span></span> | <span data-ttu-id="0f92b-120">Value</span><span class="sxs-lookup"><span data-stu-id="0f92b-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f92b-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f92b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0f92b-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f92b-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0f92b-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f92b-123">Library</span></span><br/> | <dl> <span data-ttu-id="0f92b-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f92b-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0f92b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f92b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f92b-126">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="0f92b-126">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
