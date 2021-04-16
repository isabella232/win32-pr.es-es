---
description: Obtiene los atributos de la revisión.
ms.assetid: 601a3275-25ea-4e16-8297-a9fc1f5fdd49
title: 'ID3DXPatchMesh:: GetPatchInfo (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.GetPatchInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70308857aa66551ed371dbe511acb6bd2d211bfb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670247"
---
# <a name="id3dxpatchmeshgetpatchinfo-method"></a><span data-ttu-id="cdedb-103">ID3DXPatchMesh:: GetPatchInfo (método)</span><span class="sxs-lookup"><span data-stu-id="cdedb-103">ID3DXPatchMesh::GetPatchInfo method</span></span>

<span data-ttu-id="cdedb-104">Obtiene los atributos de la revisión.</span><span class="sxs-lookup"><span data-stu-id="cdedb-104">Gets the attributes of the patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdedb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdedb-105">Syntax</span></span>


```C++
HRESULT GetPatchInfo(
  [out, retval] LPD3DXPATCHINFO PatchInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cdedb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdedb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdedb-107">*PatchInfo* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cdedb-107">*PatchInfo* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cdedb-108">Tipo: **[ **LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="cdedb-108">Type: **[**LPD3DXPATCHINFO**](d3dxpatchinfo.md)**</span></span>

<span data-ttu-id="cdedb-109">Puntero a las estructuras que contienen los atributos patch.</span><span class="sxs-lookup"><span data-stu-id="cdedb-109">Pointer to the structures containing the patch attributes.</span></span> <span data-ttu-id="cdedb-110">Para obtener más información sobre los atributos de revisión, vea [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="cdedb-110">For more information about patch attributes, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdedb-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdedb-111">Return value</span></span>

<span data-ttu-id="cdedb-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cdedb-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cdedb-113">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cdedb-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cdedb-114">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cdedb-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdedb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdedb-115">Requirements</span></span>



| <span data-ttu-id="cdedb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdedb-116">Requirement</span></span> | <span data-ttu-id="cdedb-117">Value</span><span class="sxs-lookup"><span data-stu-id="cdedb-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdedb-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cdedb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cdedb-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdedb-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cdedb-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdedb-120">Library</span></span><br/> | <dl> <span data-ttu-id="cdedb-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdedb-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cdedb-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdedb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdedb-123">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="cdedb-123">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 




