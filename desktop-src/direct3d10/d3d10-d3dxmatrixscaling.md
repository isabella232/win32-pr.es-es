---
description: 'Función D3DXMatrixScaling (D3DX10Math.h): crea una matriz que se escala a lo largo del eje X, el eje Y y el eje Z.'
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: Función D3DXMatrixScaling (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bf11b2196953775fb41412ad484a77ab00ae578e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108933"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="48e7d-103">Función D3DXMatrixScaling (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="48e7d-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="48e7d-104">Crea una matriz que se escala a lo largo del eje X, el eje Y y el eje Z.</span><span class="sxs-lookup"><span data-stu-id="48e7d-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e7d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48e7d-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="48e7d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="48e7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e7d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="48e7d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="48e7d-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="48e7d-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="48e7d-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="48e7d-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="48e7d-110">*sx* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="48e7d-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e7d-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e7d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e7d-112">Factor de escalado que se aplica a lo largo del eje X.</span><span class="sxs-lookup"><span data-stu-id="48e7d-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="48e7d-113">*sy* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="48e7d-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e7d-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e7d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e7d-115">Factor de escalado que se aplica a lo largo del eje Y.</span><span class="sxs-lookup"><span data-stu-id="48e7d-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="48e7d-116">*sz* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="48e7d-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e7d-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48e7d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48e7d-118">Factor de escalado que se aplica a lo largo del eje Z.</span><span class="sxs-lookup"><span data-stu-id="48e7d-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48e7d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48e7d-119">Return value</span></span>

<span data-ttu-id="48e7d-120">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="48e7d-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="48e7d-121">Puntero a la transformación de escalado D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="48e7d-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="48e7d-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48e7d-122">Remarks</span></span>

<span data-ttu-id="48e7d-123">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="48e7d-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="48e7d-124">De esta manera, la función D3DXMatrixScaling se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="48e7d-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="48e7d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48e7d-125">Requirements</span></span>



| <span data-ttu-id="48e7d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="48e7d-126">Requirement</span></span> | <span data-ttu-id="48e7d-127">Value</span><span class="sxs-lookup"><span data-stu-id="48e7d-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48e7d-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="48e7d-128">Header</span></span><br/>  | <dl> <span data-ttu-id="48e7d-129"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="48e7d-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="48e7d-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48e7d-130">Library</span></span><br/> | <dl> <span data-ttu-id="48e7d-131"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="48e7d-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="48e7d-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="48e7d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e7d-133">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="48e7d-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
