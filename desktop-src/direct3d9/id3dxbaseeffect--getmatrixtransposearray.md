---
description: Obtiene una matriz de matrices transpuestas.
ms.assetid: fbfcb2e4-82ca-4f79-923e-35749c5b9586
title: 'ID3DXBaseEffect:: GetMatrixTransposeArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTransposeArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c5f3709a31067b82e9752a9e97db6f3a2a323a19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821498"
---
# <a name="id3dxbaseeffectgetmatrixtransposearray-method"></a><span data-ttu-id="89c6f-103">ID3DXBaseEffect:: GetMatrixTransposeArray (método)</span><span class="sxs-lookup"><span data-stu-id="89c6f-103">ID3DXBaseEffect::GetMatrixTransposeArray method</span></span>

<span data-ttu-id="89c6f-104">Obtiene una matriz de matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="89c6f-104">Gets an array of transposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89c6f-105">Syntax</span></span>


```C++
HRESULT GetMatrixTransposeArray(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix,
  [in]  UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="89c6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89c6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c6f-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89c6f-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6f-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="89c6f-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="89c6f-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="89c6f-109">Unique identifier.</span></span> <span data-ttu-id="89c6f-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="89c6f-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="89c6f-111">*pMatrix* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="89c6f-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6f-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="89c6f-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="89c6f-113">Devuelve una matriz de matrices transpuestas.</span><span class="sxs-lookup"><span data-stu-id="89c6f-113">Returns an array of transposed matrices.</span></span> <span data-ttu-id="89c6f-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="89c6f-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="89c6f-115">*Recuento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="89c6f-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c6f-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="89c6f-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="89c6f-117">Número de matrices de la matriz.</span><span class="sxs-lookup"><span data-stu-id="89c6f-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c6f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89c6f-118">Return value</span></span>

<span data-ttu-id="89c6f-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89c6f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89c6f-120">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="89c6f-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="89c6f-121">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="89c6f-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="89c6f-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89c6f-122">Remarks</span></span>

<span data-ttu-id="89c6f-123">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector está contenido en una columna.</span><span class="sxs-lookup"><span data-stu-id="89c6f-123">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="89c6f-124">Si las matrices de destino son mayores que las matrices de origen, solo se rellenarán los componentes de la parte superior izquierda de cada matriz de destino y los demás componentes de la matriz de destino se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="89c6f-124">If the destination matrices are larger than the source matrices, only the upper-left components of each destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c6f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89c6f-125">Requirements</span></span>



| <span data-ttu-id="89c6f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="89c6f-126">Requirement</span></span> | <span data-ttu-id="89c6f-127">Value</span><span class="sxs-lookup"><span data-stu-id="89c6f-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c6f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89c6f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="89c6f-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="89c6f-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="89c6f-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89c6f-130">Library</span></span><br/> | <dl> <span data-ttu-id="89c6f-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89c6f-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="89c6f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="89c6f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c6f-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="89c6f-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="89c6f-134">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="89c6f-134">**SetMatrixTransposeArray**</span></span>](id3dxbaseeffect--setmatrixtransposearray.md)
</dt> </dl>

 

 
