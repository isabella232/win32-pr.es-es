---
description: Bloquee el búfer de índice.
ms.assetid: b68aff75-9ba6-4088-b35f-f56d700d1aff
title: 'ID3DXPatchMesh:: LockIndexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81dc410262ff21ea972d4c501ac3b5d26a361642
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548134"
---
# <a name="id3dxpatchmeshlockindexbuffer-method"></a><span data-ttu-id="4366a-103">ID3DXPatchMesh:: LockIndexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="4366a-103">ID3DXPatchMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="4366a-104">Bloquee el búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="4366a-104">Lock the index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="4366a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4366a-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="4366a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4366a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4366a-107">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="4366a-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4366a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4366a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4366a-109">Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="4366a-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="4366a-110">Para este método, las marcas válidas son:</span><span class="sxs-lookup"><span data-stu-id="4366a-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="4366a-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="4366a-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="4366a-112">\_No se \_ pudo \_ Actualizar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="4366a-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="4366a-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="4366a-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="4366a-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4366a-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="4366a-115">Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="4366a-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="4366a-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4366a-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4366a-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4366a-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4366a-118">\*Puntero void a un búfer de memoria que contiene los datos de índice devueltos.</span><span class="sxs-lookup"><span data-stu-id="4366a-118">VOID\* pointer to a memory buffer containing the returned index data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4366a-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4366a-119">Return value</span></span>

<span data-ttu-id="4366a-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4366a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4366a-121">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4366a-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4366a-122">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4366a-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4366a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4366a-123">Remarks</span></span>

<span data-ttu-id="4366a-124">Normalmente, el búfer de índice está bloqueado, se escribe en él y, a continuación, se desbloquea para leerlo.</span><span class="sxs-lookup"><span data-stu-id="4366a-124">The index buffer is usually locked, written to, and then unlocked for reading.</span></span> <span data-ttu-id="4366a-125">Los búferes de índice de la malla de revisión son búferes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4366a-125">Patch mesh index buffers are 16-bit buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="4366a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4366a-126">Requirements</span></span>



| <span data-ttu-id="4366a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4366a-127">Requirement</span></span> | <span data-ttu-id="4366a-128">Value</span><span class="sxs-lookup"><span data-stu-id="4366a-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4366a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4366a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4366a-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4366a-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4366a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4366a-131">Library</span></span><br/> | <dl> <span data-ttu-id="4366a-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4366a-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4366a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="4366a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4366a-134">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="4366a-134">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> <dt>

[<span data-ttu-id="4366a-135">**D3DXCreatePatchMesh**</span><span class="sxs-lookup"><span data-stu-id="4366a-135">**D3DXCreatePatchMesh**</span></span>](d3dxcreatepatchmesh.md)
</dt> </dl>

 

 
