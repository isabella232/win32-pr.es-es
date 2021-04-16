---
description: Cargar datos secundarios de marco desde un archivo. x.
ms.assetid: 79d251f3-c661-42e3-9385-84aabd58fd4f
title: 'ID3DXLoadUserData:: LoadFrameChildData (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53bde98f0e756fd1baff4c509179f15e8489e74f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548102"
---
# <a name="id3dxloaduserdataloadframechilddata-method"></a><span data-ttu-id="8b36a-103">ID3DXLoadUserData:: LoadFrameChildData (método)</span><span class="sxs-lookup"><span data-stu-id="8b36a-103">ID3DXLoadUserData::LoadFrameChildData method</span></span>

<span data-ttu-id="8b36a-104">Cargar datos secundarios de marco desde un archivo. x.</span><span class="sxs-lookup"><span data-stu-id="8b36a-104">Load frame child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b36a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b36a-105">Syntax</span></span>


```C++
HRESULT LoadFrameChildData(
  [in] LPD3DXFRAME    pFrame,
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="8b36a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b36a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b36a-107">*pFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b36a-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b36a-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="8b36a-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="8b36a-109">Puntero a un contenedor de malla.</span><span class="sxs-lookup"><span data-stu-id="8b36a-109">Pointer to a mesh container.</span></span> <span data-ttu-id="8b36a-110">Vea [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="8b36a-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b36a-111">*pXofChildData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8b36a-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b36a-112">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="8b36a-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="8b36a-113">Puntero a una estructura de datos de archivo. x.</span><span class="sxs-lookup"><span data-stu-id="8b36a-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="8b36a-114">Esto se define en Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="8b36a-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b36a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b36a-115">Return value</span></span>

<span data-ttu-id="8b36a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8b36a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8b36a-117">Un programador de aplicaciones implementa los valores devueltos de este método.</span><span class="sxs-lookup"><span data-stu-id="8b36a-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="8b36a-118">En general, si no se produce ningún error, programe el método para devolver D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b36a-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="8b36a-119">De lo contrario, programe el método para que devuelva un mensaje de error adecuado de D3DERR o D3DXERR, ya que esto hará que [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) también produzca un error y devuelva el error.</span><span class="sxs-lookup"><span data-stu-id="8b36a-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b36a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b36a-120">Requirements</span></span>



| <span data-ttu-id="8b36a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b36a-121">Requirement</span></span> | <span data-ttu-id="8b36a-122">Value</span><span class="sxs-lookup"><span data-stu-id="8b36a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b36a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b36a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8b36a-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b36a-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8b36a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b36a-125">Library</span></span><br/> | <dl> <span data-ttu-id="8b36a-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b36a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8b36a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b36a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b36a-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="8b36a-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 




