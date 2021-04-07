---
description: Obtiene una matriz de punteros a matrices de nontransposed.
ms.assetid: ee9f752d-a06a-43a3-b4ce-d1d585ba8c08
title: 'ID3DXBaseEffect:: GetMatrixPointerArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixPointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a841c321e641b74841a76432eab8b016f396f61a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003969"
---
# <a name="id3dxbaseeffectgetmatrixpointerarray-method"></a><span data-ttu-id="a343d-103">ID3DXBaseEffect:: GetMatrixPointerArray (método)</span><span class="sxs-lookup"><span data-stu-id="a343d-103">ID3DXBaseEffect::GetMatrixPointerArray method</span></span>

<span data-ttu-id="a343d-104">Obtiene una matriz de punteros a matrices de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="a343d-104">Gets an array of pointers to nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="a343d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a343d-105">Syntax</span></span>


```C++
HRESULT GetMatrixPointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="a343d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a343d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a343d-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a343d-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a343d-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a343d-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a343d-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="a343d-109">Unique identifier.</span></span> <span data-ttu-id="a343d-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="a343d-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="a343d-111">*ppMatrix* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a343d-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a343d-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a343d-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="a343d-113">Matriz de punteros a matrices de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="a343d-113">Array of pointers to nontransposed matrices.</span></span> <span data-ttu-id="a343d-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a343d-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a343d-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a343d-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a343d-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a343d-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a343d-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="a343d-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a343d-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a343d-118">Return value</span></span>

<span data-ttu-id="a343d-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a343d-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a343d-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a343d-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a343d-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="a343d-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="a343d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a343d-122">Remarks</span></span>

<span data-ttu-id="a343d-123">Una matriz nontransposed contiene datos principales de fila; es decir, cada vector está incluido en una fila.</span><span class="sxs-lookup"><span data-stu-id="a343d-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="a343d-124">Si las matrices de destino son mayores que las matrices de origen, solo se rellenarán los componentes de la parte superior izquierda de cada matriz de destino y los demás componentes de la matriz de destino se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="a343d-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a343d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a343d-125">Requirements</span></span>



| <span data-ttu-id="a343d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a343d-126">Requirement</span></span> | <span data-ttu-id="a343d-127">Value</span><span class="sxs-lookup"><span data-stu-id="a343d-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a343d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a343d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a343d-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a343d-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a343d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a343d-130">Library</span></span><br/> | <dl> <span data-ttu-id="a343d-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a343d-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a343d-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a343d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a343d-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="a343d-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="a343d-134">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="a343d-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
