---
description: Crea una matriz que se escala a lo largo del eje x, el eje y y el eje z.
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: Función D3DXMatrixScaling (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7cfc14fc1d514f68f2881d26c4729440d709af93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717568"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a><span data-ttu-id="fc506-103">Función D3DXMatrixScaling (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fc506-103">D3DXMatrixScaling function (D3dx9math.h)</span></span>

<span data-ttu-id="fc506-104">Crea una matriz que se escala a lo largo del eje x, el eje y y el eje z.</span><span class="sxs-lookup"><span data-stu-id="fc506-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc506-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc506-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="fc506-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc506-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fc506-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc506-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc506-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc506-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fc506-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fc506-110">*SX* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc506-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc506-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc506-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc506-112">Factor de escala que se aplica a lo largo del eje x.</span><span class="sxs-lookup"><span data-stu-id="fc506-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fc506-113">*SY* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc506-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc506-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc506-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc506-115">Factor de escala que se aplica a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="fc506-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="fc506-116">*SZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc506-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc506-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc506-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc506-118">Factor de escala que se aplica a lo largo del eje z.</span><span class="sxs-lookup"><span data-stu-id="fc506-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc506-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc506-119">Return value</span></span>

<span data-ttu-id="fc506-120">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc506-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fc506-121">Puntero a la transformación de escala [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="fc506-121">Pointer to the scaling transformation [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc506-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc506-122">Remarks</span></span>

<span data-ttu-id="fc506-123">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="fc506-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fc506-124">De esta manera, la función **D3DXMatrixScaling** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="fc506-124">In this way, the **D3DXMatrixScaling** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc506-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc506-125">Requirements</span></span>



| <span data-ttu-id="fc506-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc506-126">Requirement</span></span> | <span data-ttu-id="fc506-127">Value</span><span class="sxs-lookup"><span data-stu-id="fc506-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc506-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc506-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fc506-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc506-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fc506-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fc506-130">Library</span></span><br/> | <dl> <span data-ttu-id="fc506-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc506-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fc506-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc506-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc506-133">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fc506-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
