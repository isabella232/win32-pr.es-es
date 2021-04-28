---
description: 'Función D3DXMatrixMultiply (D3dx9math.h): determina el producto de dos matrices.'
ms.assetid: 160c801a-6589-4a0d-8e90-7e7a99fbd5f7
title: Función D3DXMatrixMultiply (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixMultiply
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d183fc3c79797bab886d3a40211448ccf57d552
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107553"
---
# <a name="d3dxmatrixmultiply-function-d3dx9mathh"></a><span data-ttu-id="e3bd1-103">Función D3DXMatrixMultiply (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e3bd1-103">D3DXMatrixMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="e3bd1-104">Determina el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="e3bd1-104">Determines the product of two matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3bd1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3bd1-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixMultiply(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXMATRIX *pM1,
  _In_    const D3DXMATRIX *pM2
);
```



## <a name="parameters"></a><span data-ttu-id="e3bd1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3bd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3bd1-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3bd1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bd1-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3bd1-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3bd1-109">Puntero a la [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e3bd1-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e3bd1-110">*pM1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e3bd1-110">*pM1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bd1-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3bd1-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3bd1-112">Puntero a una estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="e3bd1-112">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e3bd1-113">*pM2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e3bd1-113">*pM2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3bd1-114">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e3bd1-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3bd1-115">Puntero a una estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="e3bd1-115">Pointer to a source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3bd1-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3bd1-116">Return value</span></span>

<span data-ttu-id="e3bd1-117">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="e3bd1-117">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e3bd1-118">Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que es el producto de dos matrices.</span><span class="sxs-lookup"><span data-stu-id="e3bd1-118">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the product of two matrices.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3bd1-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e3bd1-119">Remarks</span></span>

<span data-ttu-id="e3bd1-120">El resultado representa la transformación M1 seguida de la transformación M2 (Out = M1 \* M2).</span><span class="sxs-lookup"><span data-stu-id="e3bd1-120">The result represents the transformation M1 followed by the transformation M2 (Out = M1 \* M2).</span></span>

<span data-ttu-id="e3bd1-121">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="e3bd1-121">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="e3bd1-122">De esta manera, la **función D3DXMatrixMultiply** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="e3bd1-122">In this way, the **D3DXMatrixMultiply** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3bd1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3bd1-123">Requirements</span></span>



| <span data-ttu-id="e3bd1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3bd1-124">Requirement</span></span> | <span data-ttu-id="e3bd1-125">Value</span><span class="sxs-lookup"><span data-stu-id="e3bd1-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3bd1-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3bd1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e3bd1-127"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e3bd1-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e3bd1-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3bd1-128">Library</span></span><br/> | <dl> <span data-ttu-id="e3bd1-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3bd1-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e3bd1-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e3bd1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3bd1-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e3bd1-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e3bd1-132">**D3DXQuaternionMultiply**</span><span class="sxs-lookup"><span data-stu-id="e3bd1-132">**D3DXQuaternionMultiply**</span></span>](d3dxquaternionmultiply.md)
</dt> </dl>

 

 




