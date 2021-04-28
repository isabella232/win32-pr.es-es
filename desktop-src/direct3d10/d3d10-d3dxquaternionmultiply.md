---
description: 'Función D3DXQuaternionMultiply (D3DX10Math.h): multiplica dos cuaterniones.'
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: Función D3DXQuaternionMultiply (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4f84ecac1eb910f4b3c97aba6ed42691c70b5b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103163"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a><span data-ttu-id="3fbe4-103">Función D3DXQuaternionMultiply (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="3fbe4-103">D3DXQuaternionMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="3fbe4-104">Multiplica dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fbe4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fbe4-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="3fbe4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fbe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fbe4-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3fbe4-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fbe4-108">Tipo: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fbe4-108">Type: **[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3fbe4-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="3fbe4-110">*pQ1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3fbe4-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fbe4-111">Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="3fbe4-111">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3fbe4-112">Puntero a una estructura [**D3DXQUATERNION de**](d3d10-d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-112">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3fbe4-113">*pQ2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3fbe4-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fbe4-114">Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="3fbe4-114">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3fbe4-115">Puntero a una estructura [**D3DXQUATERNION de**](d3d10-d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-115">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fbe4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fbe4-116">Return value</span></span>

<span data-ttu-id="3fbe4-117">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="3fbe4-117">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="3fbe4-118">Puntero a una [**estructura D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el producto de dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fbe4-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fbe4-119">Remarks</span></span>

<span data-ttu-id="3fbe4-120">El resultado representa la rotación Q1 seguida de la rotación Q2 (Out = Q2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="3fbe4-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="3fbe4-121">Esto se hace para que **D3DXQuaternionMultiply** mantenga la misma semántica que [**D3DXMatrixMultiply,**](d3d10-d3dxmatrixmultiply.md) ya que los cuaterniones de unidad se pueden considerar como otra manera de representar matrices de rotación.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="3fbe4-122">Las transformaciones se concatenan en el mismo orden para las funciones **D3DXQuaternionMultiply** y [**D3DXMatrixMultiply.**](d3d10-d3dxmatrixmultiply.md)</span><span class="sxs-lookup"><span data-stu-id="3fbe4-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) Functions.</span></span> <span data-ttu-id="3fbe4-123">Por ejemplo, suponiendo que mX y mY representen las mismas rotaciones que qX y qY, m y q representarán las mismas rotaciones.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="3fbe4-124">La multiplicación de cuaterniones no es conmutativa.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="3fbe4-125">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="3fbe4-126">De este modo, la **función D3DXQuaternionMultiply** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="3fbe4-127">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="3fbe4-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fbe4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fbe4-128">Requirements</span></span>



| <span data-ttu-id="3fbe4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fbe4-129">Requirement</span></span> | <span data-ttu-id="3fbe4-130">Value</span><span class="sxs-lookup"><span data-stu-id="3fbe4-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbe4-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fbe4-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3fbe4-132"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3fbe4-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="3fbe4-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fbe4-133">Library</span></span><br/> | <dl> <span data-ttu-id="3fbe4-134"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fbe4-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3fbe4-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3fbe4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbe4-136">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="3fbe4-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
