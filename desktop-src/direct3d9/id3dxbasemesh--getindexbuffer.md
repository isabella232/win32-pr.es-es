---
description: 'Método ID3DXBaseMesh::GetIndexBuffer: recupera los datos de un búfer de índice.'
ms.assetid: 8e14a047-a8a6-4763-88c7-3b439044eeb4
title: Método ID3DXBaseMesh::GetIndexBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetIndexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 40e57193a2bf9a47ed0c57e6d13644441fbc42ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115433"
---
# <a name="id3dxbasemeshgetindexbuffer-method"></a><span data-ttu-id="f8da6-103">Método ID3DXBaseMesh::GetIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="f8da6-103">ID3DXBaseMesh::GetIndexBuffer method</span></span>

<span data-ttu-id="f8da6-104">Recupera los datos de un búfer de índice.</span><span class="sxs-lookup"><span data-stu-id="f8da6-104">Retrieves the data in an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8da6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8da6-105">Syntax</span></span>


```C++
HRESULT GetIndexBuffer(
  [out, retval] LPDIRECT3DINDEXBUFFER9 *ppIB
);
```



## <a name="parameters"></a><span data-ttu-id="f8da6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8da6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8da6-107">*ppIB* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f8da6-107">*ppIB* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f8da6-108">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="f8da6-108">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="f8da6-109">Dirección de un puntero a una [**interfaz IDirect3DIndexBuffer9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) que representa el objeto de búfer de índice asociado a la malla.</span><span class="sxs-lookup"><span data-stu-id="f8da6-109">Address of a pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8da6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8da6-110">Return value</span></span>

<span data-ttu-id="f8da6-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8da6-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8da6-112">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8da6-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f8da6-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f8da6-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8da6-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8da6-114">Requirements</span></span>



| <span data-ttu-id="f8da6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8da6-115">Requirement</span></span> | <span data-ttu-id="f8da6-116">Value</span><span class="sxs-lookup"><span data-stu-id="f8da6-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8da6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8da6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f8da6-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="f8da6-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f8da6-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8da6-119">Library</span></span><br/> | <dl> <span data-ttu-id="f8da6-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8da6-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8da6-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f8da6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8da6-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="f8da6-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
