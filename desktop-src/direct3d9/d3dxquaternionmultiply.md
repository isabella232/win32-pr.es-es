---
description: 'Función D3DXQuaternionMultiply (D3dx9math.h): multiplica dos cuaterniones.'
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Función D3DXQuaternionMultiply (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7250484e4943e8b077a63e35951c17a44eaf2de3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118043"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a><span data-ttu-id="fce9b-103">Función D3DXQuaternionMultiply (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="fce9b-103">D3DXQuaternionMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="fce9b-104">Multiplica dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="fce9b-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fce9b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fce9b-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="fce9b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fce9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fce9b-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fce9b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fce9b-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fce9b-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fce9b-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fce9b-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fce9b-110">*pQ1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fce9b-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fce9b-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fce9b-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fce9b-112">Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="fce9b-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fce9b-113">*pQ2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fce9b-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fce9b-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fce9b-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fce9b-115">Puntero a una estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="fce9b-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fce9b-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fce9b-116">Return value</span></span>

<span data-ttu-id="fce9b-117">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fce9b-117">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fce9b-118">Puntero a una [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el producto de dos cuaterniones.</span><span class="sxs-lookup"><span data-stu-id="fce9b-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="fce9b-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fce9b-119">Remarks</span></span>

<span data-ttu-id="fce9b-120">El resultado representa la rotación Q1 seguida de la rotación Q2 (Out = Q2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="fce9b-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="fce9b-121">Esto se hace para que **D3DXQuaternionMultiply** mantenga la misma semántica que [**D3DXMatrixMultiply,**](d3dxmatrixmultiply.md) ya que los cuaterniones de unidad se pueden considerar como otra manera de representar matrices de rotación.</span><span class="sxs-lookup"><span data-stu-id="fce9b-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="fce9b-122">Las transformaciones se concatenan en el mismo orden para las funciones **D3DXQuaternionMultiply** y [**D3DXMatrixMultiply.**](d3dxmatrixmultiply.md)</span><span class="sxs-lookup"><span data-stu-id="fce9b-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) functions.</span></span> <span data-ttu-id="fce9b-123">Por ejemplo, suponiendo que mX y mY representen las mismas rotaciones que qX y qY, m y q representarán las mismas rotaciones.</span><span class="sxs-lookup"><span data-stu-id="fce9b-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="fce9b-124">La multiplicación de cuaterniones no es conmutativa.</span><span class="sxs-lookup"><span data-stu-id="fce9b-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="fce9b-125">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="fce9b-125">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="fce9b-126">De este modo, la **función D3DXQuaternionMultiply** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="fce9b-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fce9b-127">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="fce9b-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fce9b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fce9b-128">Requirements</span></span>



| <span data-ttu-id="fce9b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fce9b-129">Requirement</span></span> | <span data-ttu-id="fce9b-130">Value</span><span class="sxs-lookup"><span data-stu-id="fce9b-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fce9b-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fce9b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fce9b-132"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fce9b-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fce9b-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fce9b-133">Library</span></span><br/> | <dl> <span data-ttu-id="fce9b-134"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fce9b-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fce9b-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fce9b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fce9b-136">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fce9b-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fce9b-137">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="fce9b-137">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




