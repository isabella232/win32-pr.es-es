---
description: Obtiene una matriz de nontransposed.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'ID3DXBaseEffect:: GetMatrix (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708086"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a><span data-ttu-id="90218-103">ID3DXBaseEffect:: GetMatrix (método)</span><span class="sxs-lookup"><span data-stu-id="90218-103">ID3DXBaseEffect::GetMatrix method</span></span>

<span data-ttu-id="90218-104">Obtiene una matriz de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="90218-104">Gets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="90218-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90218-105">Syntax</span></span>


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="90218-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="90218-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90218-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="90218-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90218-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="90218-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="90218-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="90218-109">Unique identifier.</span></span> <span data-ttu-id="90218-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="90218-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="90218-111">*pMatrix* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="90218-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90218-112">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="90218-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="90218-113">Devuelve una matriz de nontransposed.</span><span class="sxs-lookup"><span data-stu-id="90218-113">Returns a nontransposed matrix.</span></span> <span data-ttu-id="90218-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="90218-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90218-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="90218-115">Return value</span></span>

<span data-ttu-id="90218-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="90218-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="90218-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="90218-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="90218-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="90218-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="90218-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90218-119">Remarks</span></span>

<span data-ttu-id="90218-120">Una matriz nontransposed contiene datos principales de fila; es decir, cada vector está incluido en una fila.</span><span class="sxs-lookup"><span data-stu-id="90218-120">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="90218-121">Si la matriz de destino es mayor que la matriz de origen, solo se rellenarán los componentes de la parte superior izquierda de la matriz de destino y los demás componentes se establecerán en cero.</span><span class="sxs-lookup"><span data-stu-id="90218-121">If the destination matrix is larger than the source matrix, only the upper-left components of the destination matrix will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="90218-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90218-122">Requirements</span></span>



| <span data-ttu-id="90218-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="90218-123">Requirement</span></span> | <span data-ttu-id="90218-124">Value</span><span class="sxs-lookup"><span data-stu-id="90218-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="90218-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90218-125">Header</span></span><br/>  | <dl> <span data-ttu-id="90218-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="90218-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="90218-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90218-127">Library</span></span><br/> | <dl> <span data-ttu-id="90218-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90218-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="90218-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="90218-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90218-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="90218-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="90218-131">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="90218-131">**SetMatrix**</span></span>](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




