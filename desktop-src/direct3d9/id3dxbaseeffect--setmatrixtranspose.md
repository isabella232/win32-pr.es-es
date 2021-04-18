---
description: Establece una matriz transpuesta.
ms.assetid: d340b058-6ba5-43ec-b398-111064965730
title: 'ID3DXBaseEffect:: SetMatrixTranspose (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: f62847f7b15899389cbd5f207ce810b0ed0dd119
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721429"
---
# <a name="id3dxbaseeffectsetmatrixtranspose-method"></a><span data-ttu-id="50665-103">ID3DXBaseEffect:: SetMatrixTranspose (método)</span><span class="sxs-lookup"><span data-stu-id="50665-103">ID3DXBaseEffect::SetMatrixTranspose method</span></span>

<span data-ttu-id="50665-104">Establece una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="50665-104">Sets a transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="50665-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50665-105">Syntax</span></span>


```C++
HRESULT SetMatrixTranspose(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="50665-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50665-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50665-107">*hParameter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50665-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50665-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="50665-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="50665-109">Identificador único.</span><span class="sxs-lookup"><span data-stu-id="50665-109">Unique identifier.</span></span> <span data-ttu-id="50665-110">Vea [identificadores (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="50665-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="50665-111">*pMatrix* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50665-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50665-112">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="50665-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50665-113">Puntero a una matriz transpuesta.</span><span class="sxs-lookup"><span data-stu-id="50665-113">Pointer to a transposed matrix.</span></span> <span data-ttu-id="50665-114">Vea [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="50665-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50665-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50665-115">Return value</span></span>

<span data-ttu-id="50665-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50665-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50665-117">Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="50665-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="50665-118">Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="50665-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="50665-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50665-119">Remarks</span></span>

<span data-ttu-id="50665-120">Una matriz transpuesta contiene datos principales de columna; es decir, cada vector está contenido en una columna.</span><span class="sxs-lookup"><span data-stu-id="50665-120">A transposed matrix contains column-major data; that is, each vector is contained in a column.</span></span>

<span data-ttu-id="50665-121">Si la matriz de destino es menor que la matriz de origen, se omitirán los componentes adicionales de la matriz de origen.</span><span class="sxs-lookup"><span data-stu-id="50665-121">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="50665-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50665-122">Requirements</span></span>



| <span data-ttu-id="50665-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="50665-123">Requirement</span></span> | <span data-ttu-id="50665-124">Value</span><span class="sxs-lookup"><span data-stu-id="50665-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50665-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50665-125">Header</span></span><br/>  | <dl> <span data-ttu-id="50665-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="50665-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="50665-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50665-127">Library</span></span><br/> | <dl> <span data-ttu-id="50665-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50665-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="50665-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="50665-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50665-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="50665-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="50665-131">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="50665-131">**GetMatrixTranspose**</span></span>](id3dxbaseeffect--getmatrixtranspose.md)
</dt> </dl>

 

 




