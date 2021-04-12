---
description: Crea un cuaternión a partir de una matriz de rotación.
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: Función D3DXQuaternionRotationMatrix (D3DX10Math. h)
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
ms.openlocfilehash: 1caccf47e03388ffb85f2e12a5d0203f3fe839bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280458"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="63bcf-103">Función D3DXQuaternionRotationMatrix (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="63bcf-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="63bcf-104">Crea un cuaternión a partir de una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="63bcf-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="63bcf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63bcf-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="63bcf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63bcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63bcf-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="63bcf-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="63bcf-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="63bcf-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="63bcf-109">Puntero al [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="63bcf-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="63bcf-110">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63bcf-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63bcf-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="63bcf-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="63bcf-112">Puntero a la estructura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="63bcf-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63bcf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63bcf-113">Return value</span></span>

<span data-ttu-id="63bcf-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="63bcf-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="63bcf-115">Puntero a la estructura D3DXQUATERNION creada a partir de una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="63bcf-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="63bcf-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63bcf-116">Remarks</span></span>

<span data-ttu-id="63bcf-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="63bcf-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="63bcf-118">De esta manera, la función D3DXQuaternionRotationMatrix se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="63bcf-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="63bcf-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="63bcf-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="63bcf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63bcf-120">Requirements</span></span>



| <span data-ttu-id="63bcf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="63bcf-121">Requirement</span></span> | <span data-ttu-id="63bcf-122">Value</span><span class="sxs-lookup"><span data-stu-id="63bcf-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63bcf-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63bcf-123">Header</span></span><br/>  | <dl> <span data-ttu-id="63bcf-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="63bcf-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="63bcf-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63bcf-125">Library</span></span><br/> | <dl> <span data-ttu-id="63bcf-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63bcf-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="63bcf-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="63bcf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63bcf-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="63bcf-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
