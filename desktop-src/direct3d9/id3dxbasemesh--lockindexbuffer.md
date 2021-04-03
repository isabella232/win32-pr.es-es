---
description: Bloquea un búfer de índice y obtiene un puntero a la memoria del búfer de índice.
ms.assetid: c8941164-1f2a-4aed-b0bd-8130aac61da4
title: 'ID3DXBaseMesh:: LockIndexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 388915d0d11ff910c19a2c70b305597a79cd04bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083702"
---
# <a name="id3dxbasemeshlockindexbuffer-method"></a><span data-ttu-id="21ed9-103">ID3DXBaseMesh:: LockIndexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="21ed9-103">ID3DXBaseMesh::LockIndexBuffer method</span></span>

<span data-ttu-id="21ed9-104">Bloquea un búfer de índice y obtiene un puntero a la memoria del búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="21ed9-104">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ed9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="21ed9-105">Syntax</span></span>


```C++
HRESULT LockIndexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="21ed9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21ed9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ed9-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="21ed9-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21ed9-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21ed9-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21ed9-109">Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="21ed9-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="21ed9-110">Para este método, las marcas válidas son:</span><span class="sxs-lookup"><span data-stu-id="21ed9-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="21ed9-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="21ed9-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="21ed9-112">\_No se \_ pudo \_ Actualizar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="21ed9-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="21ed9-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="21ed9-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="21ed9-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="21ed9-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="21ed9-115">Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="21ed9-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="21ed9-116">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="21ed9-116">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="21ed9-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="21ed9-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="21ed9-118">\*Puntero void a un búfer que contiene los datos del índice.</span><span class="sxs-lookup"><span data-stu-id="21ed9-118">VOID\* pointer to a buffer containing the index data.</span></span> <span data-ttu-id="21ed9-119">El número de índices de este búfer será igual a [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span><span class="sxs-lookup"><span data-stu-id="21ed9-119">The count of indices in this buffer will be equal to [**ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21ed9-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21ed9-120">Return value</span></span>

<span data-ttu-id="21ed9-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21ed9-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21ed9-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21ed9-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21ed9-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="21ed9-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="21ed9-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21ed9-124">Remarks</span></span>

<span data-ttu-id="21ed9-125">Al trabajar con búferes de índice, se permite realizar varias llamadas de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="21ed9-125">When working with index buffers, you are allowed to make multiple lock calls.</span></span> <span data-ttu-id="21ed9-126">Sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="21ed9-126">However, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="21ed9-127">Las llamadas a DrawPrimitive no se realizarán correctamente con ningún recuento de bloqueos pendientes en ningún búfer de índice establecido actualmente.</span><span class="sxs-lookup"><span data-stu-id="21ed9-127">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set index buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ed9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21ed9-128">Requirements</span></span>



| <span data-ttu-id="21ed9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="21ed9-129">Requirement</span></span> | <span data-ttu-id="21ed9-130">Value</span><span class="sxs-lookup"><span data-stu-id="21ed9-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21ed9-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21ed9-131">Header</span></span><br/>  | <dl> <span data-ttu-id="21ed9-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="21ed9-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="21ed9-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21ed9-133">Library</span></span><br/> | <dl> <span data-ttu-id="21ed9-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21ed9-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21ed9-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="21ed9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ed9-136">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="21ed9-136">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
