---
description: Convierte la información de proximidad de la malla en una matriz de representantes de puntos.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'ID3DXBaseMesh:: ConvertAdjacencyToPointReps (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a4827473cce115f742a85b99732d09a2c5efa4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280295"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a><span data-ttu-id="d8542-103">ID3DXBaseMesh:: ConvertAdjacencyToPointReps (método)</span><span class="sxs-lookup"><span data-stu-id="d8542-103">ID3DXBaseMesh::ConvertAdjacencyToPointReps method</span></span>

<span data-ttu-id="d8542-104">Convierte la información de proximidad de la malla en una matriz de representantes de puntos.</span><span class="sxs-lookup"><span data-stu-id="d8542-104">Converts mesh adjacency information to an array of point representatives.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8542-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8542-105">Syntax</span></span>


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a><span data-ttu-id="d8542-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8542-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8542-107">*pAdjacency* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8542-107">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8542-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d8542-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d8542-109">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="d8542-109">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="d8542-110">El número de bytes de esta matriz debe ser al menos 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="d8542-110">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> <dt>

<span data-ttu-id="d8542-111">*pPRep* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d8542-111">*pPRep* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8542-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8542-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d8542-113">Puntero a una matriz de un valor DWORD por cada vértice de la malla que se rellenará con datos representativos de puntos.</span><span class="sxs-lookup"><span data-stu-id="d8542-113">Pointer to an array of one DWORD per vertex of the mesh that will be filled with point representative data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8542-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8542-114">Return value</span></span>

<span data-ttu-id="d8542-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8542-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8542-116">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d8542-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d8542-117">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d8542-117">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8542-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8542-118">Requirements</span></span>



| <span data-ttu-id="d8542-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8542-119">Requirement</span></span> | <span data-ttu-id="d8542-120">Value</span><span class="sxs-lookup"><span data-stu-id="d8542-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8542-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8542-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d8542-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8542-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d8542-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8542-123">Library</span></span><br/> | <dl> <span data-ttu-id="d8542-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8542-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8542-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8542-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8542-126">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d8542-126">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
