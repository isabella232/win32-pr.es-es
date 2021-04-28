---
description: 'Método ID3DXMATRIXStack::LoadMatrix (D3dx9math.h): carga la matriz dada en la matriz actual.'
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: Método ID3DXMATRIXStack::LoadMatrix (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2ee7e5cae4d28b81b805faa4f113d0819f1eae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093543"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="5df2b-103">Método ID3DXMATRIXStack::LoadMatrix (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5df2b-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="5df2b-104">Carga la matriz dada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="5df2b-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5df2b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5df2b-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="5df2b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5df2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5df2b-107">*pMat* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5df2b-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5df2b-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5df2b-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5df2b-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) cargada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="5df2b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5df2b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5df2b-110">Return value</span></span>

<span data-ttu-id="5df2b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5df2b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5df2b-112">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5df2b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5df2b-113">Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5df2b-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5df2b-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5df2b-114">Remarks</span></span>

<span data-ttu-id="5df2b-115">Tenga en cuenta que este método no agrega un elemento a la pila; en su lugar, reemplaza la matriz actual por la matriz proporcionada.</span><span class="sxs-lookup"><span data-stu-id="5df2b-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="5df2b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5df2b-116">Requirements</span></span>



| <span data-ttu-id="5df2b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5df2b-117">Requirement</span></span> | <span data-ttu-id="5df2b-118">Value</span><span class="sxs-lookup"><span data-stu-id="5df2b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5df2b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5df2b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5df2b-120"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5df2b-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5df2b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5df2b-121">Library</span></span><br/> | <dl> <span data-ttu-id="5df2b-122"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5df2b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5df2b-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5df2b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5df2b-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5df2b-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5df2b-125">**ID3DXMATRIXStack::LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="5df2b-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




