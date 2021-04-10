---
description: Obtiene una matriz de punteros a matrices transpuestas.
ms.assetid: b859ff2f-cf62-4619-b8be-b940fa0513b3
title: 'ID3DXBaseEffect:: GetMatrixTransposePointerArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposePointerArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e69c01395582691e6fdd0a695991ff1f726a362b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280501"
---
# <a name="id3dxbaseeffectgetmatrixtransposepointerarray-method"></a><span data-ttu-id="733f5-103">ID3DXBaseEffect:: GetMatrixTransposePointerArray (método)</span><span class="sxs-lookup"><span data-stu-id="733f5-103">ID3DXBaseEffect::GetMatrixTransposePointerArray method</span></span>

<span data-ttu-id="733f5-104">Obtiene una matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="733f5-104">Gets an array of pointers to transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="733f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="733f5-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposePointerArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX **ppMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="733f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="733f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733f5-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="733f5-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733f5-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="733f5-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="733f5-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="733f5-109">Unique identifier.</span></span> <span data-ttu-id="733f5-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="733f5-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="733f5-111">*ppMatrix* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="733f5-111">*ppMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="733f5-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="733f5-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\*\***</span></span>

<span data-ttu-id="733f5-113">Matriz de punteros a matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="733f5-113">Array of pointers to transposed matrices.</span></span> <span data-ttu-id="733f5-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="733f5-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="733f5-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="733f5-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="733f5-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="733f5-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="733f5-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="733f5-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733f5-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="733f5-118">Return value</span></span>

<span data-ttu-id="733f5-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="733f5-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="733f5-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="733f5-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="733f5-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="733f5-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="733f5-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="733f5-122">Remarks</span></span>

<span data-ttu-id="733f5-123">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector está contenido en una columna.</span><span class="sxs-lookup"><span data-stu-id="733f5-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="733f5-124">Si las matrices de destino son mayores que las matrices de origen, solo se rellenarán los componentes de la parte superior izquierda de cada matriz de destino y los demás componentes de la matriz de destino se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="733f5-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="733f5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="733f5-125">Requirements</span></span>



| <span data-ttu-id="733f5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="733f5-126">Requirement</span></span> | <span data-ttu-id="733f5-127">Value</span><span class="sxs-lookup"><span data-stu-id="733f5-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="733f5-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="733f5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="733f5-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="733f5-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="733f5-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="733f5-130">Library</span></span><br/> | <dl> <span data-ttu-id="733f5-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="733f5-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="733f5-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="733f5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733f5-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="733f5-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="733f5-134">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="733f5-134">**GetMatrixTransposeArray**</span></span>](id3dxbaseeffect--getmatrixtransposearray.md)
</dt> </dl>

 

 
