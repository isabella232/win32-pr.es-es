---
description: 'Método ID3DXMATRIXStack::LoadMatrix (D3DX10.h): carga la matriz dada en la matriz actual.'
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: Método ID3DXMATRIXStack::LoadMatrix (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 20c80f578abd5e35c89f3ecccedd2ab7fd59e812
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107963"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="824e1-103">Método ID3DXMATRIXStack::LoadMatrix (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="824e1-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="824e1-104">Carga la matriz dada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="824e1-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="824e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="824e1-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="824e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="824e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="824e1-107">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="824e1-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="824e1-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="824e1-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="824e1-109">Puntero a la estructura D3DXMATRIX cargada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="824e1-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="824e1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="824e1-110">Return value</span></span>

<span data-ttu-id="824e1-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="824e1-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="824e1-112">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="824e1-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="824e1-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="824e1-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="824e1-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="824e1-114">Remarks</span></span>

<span data-ttu-id="824e1-115">Tenga en cuenta que este método no agrega un elemento a la pila; en su lugar, reemplaza la matriz actual por la matriz proporcionada.</span><span class="sxs-lookup"><span data-stu-id="824e1-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="824e1-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="824e1-116">Requirements</span></span>



| <span data-ttu-id="824e1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="824e1-117">Requirement</span></span> | <span data-ttu-id="824e1-118">Value</span><span class="sxs-lookup"><span data-stu-id="824e1-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="824e1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="824e1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="824e1-120"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="824e1-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="824e1-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="824e1-121">Library</span></span><br/> | <dl> <span data-ttu-id="824e1-122"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="824e1-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="824e1-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="824e1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824e1-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="824e1-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="824e1-125">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="824e1-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
