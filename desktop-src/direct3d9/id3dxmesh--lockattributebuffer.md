---
description: Bloquea el búfer de malla que contiene los datos de atributo de la malla y devuelve un puntero a él.
ms.assetid: 17a321b8-bfb4-4018-869f-6b09e0a811eb
title: 'ID3DXMesh:: LockAttributeBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.LockAttributeBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 901cb98a9d75d08b6412d6fdca841d403064354b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698208"
---
# <a name="id3dxmeshlockattributebuffer-method"></a><span data-ttu-id="a83b4-103">ID3DXMesh:: LockAttributeBuffer (método)</span><span class="sxs-lookup"><span data-stu-id="a83b4-103">ID3DXMesh::LockAttributeBuffer method</span></span>

<span data-ttu-id="a83b4-104">Bloquea el búfer de malla que contiene los datos de atributo de la malla y devuelve un puntero a él.</span><span class="sxs-lookup"><span data-stu-id="a83b4-104">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a83b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a83b4-105">Syntax</span></span>


```C++
HRESULT LockAttributeBuffer(
  [in]  DWORD Flags,
  [out] DWORD **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="a83b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a83b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a83b4-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a83b4-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a83b4-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a83b4-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a83b4-109">Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="a83b4-109">Combination of zero or more locking flags that describe the type of lock to perform.</span></span> <span data-ttu-id="a83b4-110">Para este método, las marcas válidas son:</span><span class="sxs-lookup"><span data-stu-id="a83b4-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="a83b4-111">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="a83b4-111">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="a83b4-112">\_No se \_ pudo \_ Actualizar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="a83b4-112">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>
-   <span data-ttu-id="a83b4-113">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="a83b4-113">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="a83b4-114">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a83b4-114">D3DLOCK\_READONLY</span></span>

<span data-ttu-id="a83b4-115">Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="a83b4-115">For a description of the flags, see [D3DLOCK](d3dlock.md).</span></span>

</dd> <dt>

<span data-ttu-id="a83b4-116">*ppData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a83b4-116">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a83b4-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a83b4-117">Type: **[**DWORD**](../winprog/windows-data-types.md)\*\***</span></span>

<span data-ttu-id="a83b4-118">Dirección de un puntero a un búfer que contiene un valor DWORD para cada una de las caras de la malla.</span><span class="sxs-lookup"><span data-stu-id="a83b4-118">Address of a pointer to a buffer containing a DWORD for each face in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a83b4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a83b4-119">Return value</span></span>

<span data-ttu-id="a83b4-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a83b4-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a83b4-121">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a83b4-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a83b4-122">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a83b4-122">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a83b4-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a83b4-123">Remarks</span></span>

<span data-ttu-id="a83b4-124">Si se ha llamado a [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) , la malla también tendrá una tabla de atributos a la que se puede tener acceso mediante el método [**ID3DXBaseMesh:: GetAttributeTable**](id3dxbasemesh--getattributetable.md) .</span><span class="sxs-lookup"><span data-stu-id="a83b4-124">If [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) has been called, the mesh will also have an attribute table that can be accessed using the [**ID3DXBaseMesh::GetAttributeTable**](id3dxbasemesh--getattributetable.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a83b4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a83b4-125">Requirements</span></span>



| <span data-ttu-id="a83b4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a83b4-126">Requirement</span></span> | <span data-ttu-id="a83b4-127">Value</span><span class="sxs-lookup"><span data-stu-id="a83b4-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a83b4-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a83b4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a83b4-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a83b4-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a83b4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a83b4-130">Library</span></span><br/> | <dl> <span data-ttu-id="a83b4-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a83b4-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a83b4-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a83b4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a83b4-133">ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="a83b4-133">ID3DXMesh</span></span>](id3dxmesh.md)
</dt> <dt>

[<span data-ttu-id="a83b4-134">**ID3DXMesh::UnlockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="a83b4-134">**ID3DXMesh::UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="a83b4-135">**ID3DXBaseMesh::GetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="a83b4-135">**ID3DXBaseMesh::GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)
</dt> <dt>

[<span data-ttu-id="a83b4-136">**ID3DXMesh::SetAttributeTable**</span><span class="sxs-lookup"><span data-stu-id="a83b4-136">**ID3DXMesh::SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)
</dt> </dl>

 

 
