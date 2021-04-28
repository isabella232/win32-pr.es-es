---
description: 'Función D3DXQuaternionRotationMatrix (D3DX10Math.h): crea un cuaternión a partir de una matriz de rotación.'
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: Función D3DXQuaternionRotationMatrix (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cb923c135d436b36fe032d344366fdee687d27a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103153"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="fd3b6-103">Función D3DXQuaternionRotationMatrix (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="fd3b6-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="fd3b6-104">Crea un cuaternión a partir de una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd3b6-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="fd3b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd3b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd3b6-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fd3b6-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3b6-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd3b6-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fd3b6-109">Puntero a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fd3b6-110">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fd3b6-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3b6-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd3b6-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd3b6-112">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd3b6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd3b6-113">Return value</span></span>

<span data-ttu-id="fd3b6-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd3b6-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fd3b6-115">Puntero a la estructura D3DXQUATERNION creada a partir de una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd3b6-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fd3b6-116">Remarks</span></span>

<span data-ttu-id="fd3b6-117">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fd3b6-118">De este modo, la función D3DXQuaternionRotationMatrix se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fd3b6-119">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="fd3b6-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd3b6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd3b6-120">Requirements</span></span>



| <span data-ttu-id="fd3b6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd3b6-121">Requirement</span></span> | <span data-ttu-id="fd3b6-122">Value</span><span class="sxs-lookup"><span data-stu-id="fd3b6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd3b6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd3b6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fd3b6-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="fd3b6-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd3b6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd3b6-125">Library</span></span><br/> | <dl> <span data-ttu-id="fd3b6-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd3b6-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd3b6-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fd3b6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3b6-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="fd3b6-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
