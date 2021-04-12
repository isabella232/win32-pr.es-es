---
description: Carga la matriz especificada en la matriz actual.
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'ID3DXMATRIXStack:: LoadMatrix (método) (D3DX10. h)'
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
ms.openlocfilehash: ce6b99abf4c9a82a8b9d1c7643a1098d19e18c15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362802"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="e9630-103">ID3DXMATRIXStack:: LoadMatrix (método) (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="e9630-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="e9630-104">Carga la matriz especificada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e9630-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9630-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9630-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e9630-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9630-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9630-107">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e9630-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9630-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e9630-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e9630-109">Puntero a la estructura D3DXMATRIX cargada en la matriz actual.</span><span class="sxs-lookup"><span data-stu-id="e9630-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9630-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9630-110">Return value</span></span>

<span data-ttu-id="e9630-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9630-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9630-112">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9630-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e9630-113">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e9630-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9630-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9630-114">Remarks</span></span>

<span data-ttu-id="e9630-115">Tenga en cuenta que este método no agrega un elemento a la pila; en su lugar, reemplaza la matriz actual por la matriz proporcionada.</span><span class="sxs-lookup"><span data-stu-id="e9630-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9630-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9630-116">Requirements</span></span>



| <span data-ttu-id="e9630-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9630-117">Requirement</span></span> | <span data-ttu-id="e9630-118">Value</span><span class="sxs-lookup"><span data-stu-id="e9630-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9630-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9630-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e9630-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9630-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9630-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9630-121">Library</span></span><br/> | <dl> <span data-ttu-id="e9630-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9630-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9630-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9630-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9630-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="e9630-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e9630-125">Interfaces de D3DX</span><span class="sxs-lookup"><span data-stu-id="e9630-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
