---
description: Valida una malla de revisión, devolviendo el número de vértices degenerados y revisiones.
ms.assetid: a95ff9d9-d476-42ac-8d7e-1dc42418f763
title: Función D3DXValidPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXValidPatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 87d7fbe15c78a8b768d845e6a23cc084b69f3e02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003797"
---
# <a name="d3dxvalidpatchmesh-function"></a><span data-ttu-id="862d0-103">D3DXValidPatchMesh función)</span><span class="sxs-lookup"><span data-stu-id="862d0-103">D3DXValidPatchMesh function</span></span>

<span data-ttu-id="862d0-104">Valida una malla de revisión, devolviendo el número de vértices degenerados y revisiones.</span><span class="sxs-lookup"><span data-stu-id="862d0-104">Validates a patch mesh, returning the number of degenerate vertices and patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="862d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="862d0-105">Syntax</span></span>


```C++
HRESULT D3DXValidPatchMesh(
  _In_  LPD3DXPATCHMESH pMeshIn,
  _Out_ DWORD           *pNumDegenerateVertices,
  _Out_ DWORD           *pNumDegeneratePatches,
  _Out_ LPD3DXBUFFER    *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="862d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="862d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="862d0-107">*pMeshIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="862d0-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="862d0-108">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="862d0-108">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)**</span></span>

<span data-ttu-id="862d0-109">Puntero a una interfaz [**ID3DXPatchMesh**](id3dxpatchmesh.md) que representa la malla de revisión que se va a probar.</span><span class="sxs-lookup"><span data-stu-id="862d0-109">Pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the patch mesh to be tested.</span></span>

</dd> <dt>

<span data-ttu-id="862d0-110">*pNumDegenerateVertices* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="862d0-110">*pNumDegenerateVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="862d0-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="862d0-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="862d0-112">Devuelve el número de vértices degenerados en la malla de la revisión.</span><span class="sxs-lookup"><span data-stu-id="862d0-112">Returns the number of degenerate vertices in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="862d0-113">*pNumDegeneratePatches* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="862d0-113">*pNumDegeneratePatches* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="862d0-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="862d0-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="862d0-115">Devuelve el número de revisiones degeneradas en la malla de la revisión.</span><span class="sxs-lookup"><span data-stu-id="862d0-115">Returns the number of degenerate patches in the patch mesh.</span></span>

</dd> <dt>

<span data-ttu-id="862d0-116">*ppErrorsAndWarnings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="862d0-116">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="862d0-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="862d0-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="862d0-118">Devuelve un puntero a un búfer que contiene una cadena de errores y advertencias que explican los problemas detectados en la malla de la revisión.</span><span class="sxs-lookup"><span data-stu-id="862d0-118">Returns a pointer to a buffer containing a string of errors and warnings that explain the problems found in the patch mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="862d0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="862d0-119">Return value</span></span>

<span data-ttu-id="862d0-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="862d0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="862d0-121">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="862d0-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="862d0-122">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="862d0-122">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="862d0-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="862d0-123">Remarks</span></span>

<span data-ttu-id="862d0-124">Este método valida la malla comprobando si hay índices no válidos.</span><span class="sxs-lookup"><span data-stu-id="862d0-124">This method validates the mesh by checking for invalid indices.</span></span> <span data-ttu-id="862d0-125">La información del error está disponible en la salida del depurador.</span><span class="sxs-lookup"><span data-stu-id="862d0-125">Error information is available from the debugger output.</span></span>

## <a name="requirements"></a><span data-ttu-id="862d0-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="862d0-126">Requirements</span></span>



| <span data-ttu-id="862d0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="862d0-127">Requirement</span></span> | <span data-ttu-id="862d0-128">Value</span><span class="sxs-lookup"><span data-stu-id="862d0-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="862d0-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="862d0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="862d0-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="862d0-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="862d0-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="862d0-131">Library</span></span><br/> | <dl> <span data-ttu-id="862d0-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="862d0-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="862d0-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="862d0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862d0-134">Funciones de malla</span><span class="sxs-lookup"><span data-stu-id="862d0-134">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
