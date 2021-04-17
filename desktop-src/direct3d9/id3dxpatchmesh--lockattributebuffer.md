---
description: Bloquea el búfer de atributo.
ms.assetid: 6e05e613-ca93-41b0-a3b3-a9564ada3b0c
title: 'ID3DXPatchMesh:: LockAttributeBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71e50fdc27f3f50b560324c74f5a1609f900772d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670266"
---
# <a name="id3dxpatchmeshlockattributebuffer-method"></a><span data-ttu-id="80175-103">ID3DXPatchMesh:: LockAttributeBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="80175-103">ID3DXPatchMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="80175-104">Bloquea el búfer de atributo.</span><span class="sxs-lookup"><span data-stu-id="80175-104">Locks the attribute buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="80175-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80175-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]          DWORD flags,
  [out, retval] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="80175-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80175-107">*marcas* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="80175-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80175-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80175-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80175-109">Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="80175-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="80175-110">Para este método, las marcas válidas son:</span><span class="sxs-lookup"><span data-stu-id="80175-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="80175-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="80175-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="80175-112">\_No se \_ pudo \_ Actualizar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="80175-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="80175-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="80175-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="80175-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="80175-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="80175-115">Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="80175-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="80175-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="80175-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="80175-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="80175-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="80175-118">Dirección de un puntero a un búfer que contiene un valor DWORD para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="80175-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80175-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80175-119">Return value</span></span>

<span data-ttu-id="80175-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80175-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80175-121">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="80175-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="80175-122">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="80175-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="80175-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80175-123">Remarks</span></span>

<span data-ttu-id="80175-124">Normalmente, el búfer de atributo está bloqueado, se escribe en él y, a continuación, se desbloquea para leerlo.</span><span class="sxs-lookup"><span data-stu-id="80175-124">The attribute buffer is usually locked, written to, and then unlocked for reading.</span></span>

## <a name="requirements"></a><span data-ttu-id="80175-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80175-125">Requirements</span></span>



| <span data-ttu-id="80175-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="80175-126">Requirement</span></span> | <span data-ttu-id="80175-127">Value</span><span class="sxs-lookup"><span data-stu-id="80175-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80175-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80175-128">Header</span></span><br/>  | <dl> <span data-ttu-id="80175-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="80175-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="80175-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80175-130">Library</span></span><br/> | <dl> <span data-ttu-id="80175-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80175-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="80175-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="80175-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80175-133">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="80175-133">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
