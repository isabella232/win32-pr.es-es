---
description: Bloquea un búfer de vértice y obtiene un puntero a la memoria del búfer de vértices.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'ID3DXBaseMesh:: LockVertexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718260"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a><span data-ttu-id="9f42c-103">ID3DXBaseMesh:: LockVertexBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="9f42c-103">ID3DXBaseMesh::LockVertexBuffer method</span></span>

<span data-ttu-id="9f42c-104">Bloquea un búfer de vértice y obtiene un puntero a la memoria del búfer de vértices.</span><span class="sxs-lookup"><span data-stu-id="9f42c-104">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f42c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f42c-105">Syntax</span></span>


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a><span data-ttu-id="9f42c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f42c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f42c-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9f42c-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f42c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9f42c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9f42c-109">Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="9f42c-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="9f42c-110">Para este método, las marcas válidas son:</span><span class="sxs-lookup"><span data-stu-id="9f42c-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="9f42c-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="9f42c-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="9f42c-112">\_No se \_ pudo \_ Actualizar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="9f42c-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="9f42c-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="9f42c-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="9f42c-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9f42c-114">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="9f42c-115">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="9f42c-115">D3DLOCK\_NOOVERWRITE</span></span>

<span data-ttu-id="9f42c-116">Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="9f42c-116">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f42c-117">*ppData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9f42c-117">*ppData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9f42c-118">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9f42c-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9f42c-119">\*Puntero void a un búfer que contiene los datos de vértices.</span><span class="sxs-lookup"><span data-stu-id="9f42c-119">VOID\* pointer to a buffer containing the vertex data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f42c-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f42c-120">Return value</span></span>

<span data-ttu-id="9f42c-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9f42c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9f42c-122">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9f42c-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9f42c-123">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9f42c-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f42c-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f42c-124">Remarks</span></span>

<span data-ttu-id="9f42c-125">Al trabajar con búferes de vértices, se permite realizar varias llamadas de bloqueo; sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo.</span><span class="sxs-lookup"><span data-stu-id="9f42c-125">When working with vertex buffers, you are allowed to make multiple lock calls; however, you must ensure that the number of lock calls match the number of unlock calls.</span></span> <span data-ttu-id="9f42c-126">Las llamadas a DrawPrimitive no se realizarán correctamente con ningún recuento de bloqueos pendientes en ningún búfer de vértice establecido actualmente.</span><span class="sxs-lookup"><span data-stu-id="9f42c-126">DrawPrimitive calls will not succeed with any outstanding lock count on any currently set vertex buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f42c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f42c-127">Requirements</span></span>



| <span data-ttu-id="9f42c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f42c-128">Requirement</span></span> | <span data-ttu-id="9f42c-129">Value</span><span class="sxs-lookup"><span data-stu-id="9f42c-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f42c-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f42c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="9f42c-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f42c-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9f42c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f42c-132">Library</span></span><br/> | <dl> <span data-ttu-id="9f42c-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f42c-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9f42c-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="9f42c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f42c-135">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="9f42c-135">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
