---
description: Convierte los datos representativos de punto en información de adyacencia de malla.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'ID3DXBaseMesh:: ConvertPointRepsToAdjacency (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b1c38d7790d575bdf6794e0e21f1c4043e80257c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707852"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a><span data-ttu-id="322b4-103">ID3DXBaseMesh:: ConvertPointRepsToAdjacency (método)</span><span class="sxs-lookup"><span data-stu-id="322b4-103">ID3DXBaseMesh::ConvertPointRepsToAdjacency method</span></span>

<span data-ttu-id="322b4-104">Convierte los datos representativos de punto en información de adyacencia de malla.</span><span class="sxs-lookup"><span data-stu-id="322b4-104">Converts point representative data to mesh adjacency information.</span></span>

## <a name="syntax"></a><span data-ttu-id="322b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="322b4-105">Syntax</span></span>


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="322b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="322b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="322b4-107">*pPRep* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="322b4-107">*pPRep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="322b4-108">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="322b4-108">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="322b4-109">Puntero a una matriz de un valor DWORD por cada vértice de la malla que contiene datos representativos de puntos.</span><span class="sxs-lookup"><span data-stu-id="322b4-109">Pointer to an array of one DWORD per vertex of the mesh that contains point representative data.</span></span> <span data-ttu-id="322b4-110">Este parámetro es opcional.</span><span class="sxs-lookup"><span data-stu-id="322b4-110">This parameter is optional.</span></span> <span data-ttu-id="322b4-111">Si se proporciona un valor **null** , este parámetro se interpretará como una matriz de "identidad".</span><span class="sxs-lookup"><span data-stu-id="322b4-111">Supplying a **NULL** value will cause this parameter to be interpreted as an "identity" array.</span></span>

</dd> <dt>

<span data-ttu-id="322b4-112">*pAdjacency* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="322b4-112">*pAdjacency* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="322b4-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="322b4-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="322b4-114">Puntero a una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="322b4-114">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="322b4-115">El número de bytes de esta matriz debe ser al menos 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).</span><span class="sxs-lookup"><span data-stu-id="322b4-115">The number of bytes in this array must be at least 3 \* [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="322b4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="322b4-116">Return value</span></span>

<span data-ttu-id="322b4-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="322b4-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="322b4-118">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="322b4-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="322b4-119">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="322b4-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="322b4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="322b4-120">Requirements</span></span>



| <span data-ttu-id="322b4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="322b4-121">Requirement</span></span> | <span data-ttu-id="322b4-122">Value</span><span class="sxs-lookup"><span data-stu-id="322b4-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="322b4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="322b4-123">Header</span></span><br/>  | <dl> <span data-ttu-id="322b4-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="322b4-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="322b4-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="322b4-125">Library</span></span><br/> | <dl> <span data-ttu-id="322b4-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="322b4-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="322b4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="322b4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="322b4-128">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="322b4-128">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
