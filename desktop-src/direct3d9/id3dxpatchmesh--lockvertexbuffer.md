---
description: Bloquee el búfer de vértices.
ms.assetid: f7e4f27d-1b40-4b0d-8173-48a0b15cfc95
title: 'ID3DXPatchMesh:: LockVertexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d88d8a1da7ae544c5647fc844cda4966cfee7b10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914769"
---
# <a name="id3dxpatchmeshlockvertexbuffer-method"></a><span data-ttu-id="cf4df-103">ID3DXPatchMesh:: LockVertexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="cf4df-103">ID3DXPatchMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="cf4df-104">Bloquee el búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="cf4df-104">Lock the vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf4df-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="cf4df-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cf4df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf4df-107">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="cf4df-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4df-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cf4df-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cf4df-109">Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="cf4df-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="cf4df-110">Para este método, las marcas válidas son:</span><span class="sxs-lookup"><span data-stu-id="cf4df-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="cf4df-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="cf4df-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="cf4df-112">\_No se \_ pudo \_ Actualizar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="cf4df-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="cf4df-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="cf4df-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="cf4df-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="cf4df-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="cf4df-115">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="cf4df-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="cf4df-116">Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="cf4df-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="cf4df-117">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cf4df-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4df-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cf4df-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cf4df-119">\*Puntero void a un búfer de memoria que contiene los datos de vértice devueltos.</span><span class="sxs-lookup"><span data-stu-id="cf4df-119">VOID\* pointer to a memory buffer containing the returned vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf4df-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cf4df-120">Return value</span></span>

<span data-ttu-id="cf4df-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf4df-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf4df-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cf4df-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cf4df-123">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cf4df-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf4df-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf4df-124">Remarks</span></span>

<span data-ttu-id="cf4df-125">Normalmente, el búfer de vértices se bloquea, se escribe en él y, a continuación, se desbloquea para leerlo.</span><span class="sxs-lookup"><span data-stu-id="cf4df-125">The vertex buffer is usually locked, written to, and then unlocked for reading.</span></span>

<span data-ttu-id="cf4df-126">Las mallas de revisión utilizan búferes de índice de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cf4df-126">Patch meshes use 16-bit index buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf4df-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf4df-127">Requirements</span></span>



| <span data-ttu-id="cf4df-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf4df-128">Requirement</span></span> | <span data-ttu-id="cf4df-129">Value</span><span class="sxs-lookup"><span data-stu-id="cf4df-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4df-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf4df-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cf4df-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf4df-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cf4df-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf4df-132">Library</span></span><br/> | <dl> <span data-ttu-id="cf4df-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf4df-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf4df-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf4df-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4df-135">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="cf4df-135">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
