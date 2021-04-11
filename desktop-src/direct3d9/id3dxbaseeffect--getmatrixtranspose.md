---
description: Obtiene una matriz transpuesta.
ms.assetid: 255c1e20-0a60-49eb-abaa-66a67322ce73
title: 'ID3DXBaseEffect:: GetMatrixTranspose (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f52a7b528a7853278f5e1b902c3907e8d48fa40f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362777"
---
# <a name="id3dxbaseeffectgetmatrixtranspose-method"></a><span data-ttu-id="c5868-103">ID3DXBaseEffect:: GetMatrixTranspose (método)</span><span class="sxs-lookup"><span data-stu-id="c5868-103">ID3DXBaseEffect::GetMatrixTranspose method</span></span>

<span data-ttu-id="c5868-104">Obtiene una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="c5868-104">Gets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5868-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5868-105">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="c5868-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5868-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c5868-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5868-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c5868-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c5868-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="c5868-109">Unique identifier.</span></span> <span data-ttu-id="c5868-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c5868-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5868-111">*pMatrix* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c5868-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5868-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5868-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c5868-113">Devuelve una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="c5868-113">Returns a transposed matrix.</span></span> <span data-ttu-id="c5868-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="c5868-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5868-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5868-115">Return value</span></span>

<span data-ttu-id="c5868-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5868-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5868-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5868-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c5868-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c5868-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5868-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5868-119">Remarks</span></span>

<span data-ttu-id="c5868-120">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector está contenido en una columna.</span><span class="sxs-lookup"><span data-stu-id="c5868-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="c5868-121">Si la matriz de destino es mayor que la matriz de origen, solo se rellenarán los elementos de la parte superior izquierda de la matriz de destino y los demás componentes de la matriz de destino se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="c5868-121">If the destination matrix is larger than the source matrix, only the upper-left elements of the destination matrix will be filled, and the remaining destination matrix components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5868-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5868-122">Requirements</span></span>



| <span data-ttu-id="c5868-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5868-123">Requirement</span></span> | <span data-ttu-id="c5868-124">Value</span><span class="sxs-lookup"><span data-stu-id="c5868-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5868-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5868-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c5868-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5868-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c5868-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5868-127">Library</span></span><br/> | <dl> <span data-ttu-id="c5868-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5868-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c5868-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5868-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5868-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="c5868-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="c5868-131">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="c5868-131">**SetMatrixTranspose**</span></span>](id3dxbaseeffect--setmatrixtranspose.md)
</dt> </dl>

 

 




