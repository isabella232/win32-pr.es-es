---
description: 'Método ID3DXBaseEffect::SetMatrixTranspose: establece una matriz transpuesta.'
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: Método ID3DXBaseEffect::SetMatrixTranspose (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixTranspose
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 384d4a7ed5e1b769218b9290ed6cc0f7f060bd66
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107403"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="14a7e-103">Método ID3DXBaseEffect::SetMatrixTranspose</span><span class="sxs-lookup"><span data-stu-id="14a7e-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="14a7e-104">Establece una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="14a7e-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a7e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14a7e-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="14a7e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14a7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a7e-107">*hParameter* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="14a7e-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a7e-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="14a7e-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="14a7e-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="14a7e-109">Unique identifier.</span></span> <span data-ttu-id="14a7e-110">Vea [Identificadores (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="14a7e-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="14a7e-111">*pMatrix* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="14a7e-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14a7e-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="14a7e-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="14a7e-113">Puntero a una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="14a7e-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="14a7e-114">Vea [**D3DXMATRIX.**](d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="14a7e-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14a7e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14a7e-115">Return value</span></span>

<span data-ttu-id="14a7e-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14a7e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14a7e-117">Si el método se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="14a7e-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="14a7e-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="14a7e-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="14a7e-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="14a7e-119">Remarks</span></span>

<span data-ttu-id="14a7e-120">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector se encuentra en una columna.</span><span class="sxs-lookup"><span data-stu-id="14a7e-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="14a7e-121">Si la matriz de destino es menor que la matriz de origen, se omitirán los componentes adicionales de la matriz de origen.</span><span class="sxs-lookup"><span data-stu-id="14a7e-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a7e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14a7e-122">Requirements</span></span>



| <span data-ttu-id="14a7e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a7e-123">Requirement</span></span> | <span data-ttu-id="14a7e-124">Value</span><span class="sxs-lookup"><span data-stu-id="14a7e-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a7e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14a7e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="14a7e-126"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="14a7e-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="14a7e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14a7e-127">Library</span></span><br/> | <dl> <span data-ttu-id="14a7e-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="14a7e-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="14a7e-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="14a7e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14a7e-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="14a7e-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="14a7e-131">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="14a7e-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




