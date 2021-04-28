---
description: 'Función D3DXQuaternionRotationMatrix (D3dx9math.h): crea un cuaternión a partir de una matriz de rotación.'
ms.assetid: 4fafb1aa-5d6f-46e6-84b1-e0bac22952d2
title: Función D3DXQuaternionRotationMatrix (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9b0ff8529f32d398ac208cff3214fccfdb2ade81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094013"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx9mathh"></a><span data-ttu-id="c8e1c-103">Función D3DXQuaternionRotationMatrix (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c8e1c-103">D3DXQuaternionRotationMatrix function (D3dx9math.h)</span></span>

<span data-ttu-id="c8e1c-104">Crea un cuaternión a partir de una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="c8e1c-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e1c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8e1c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c8e1c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8e1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e1c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c8e1c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8e1c-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8e1c-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c8e1c-109">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="c8e1c-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c8e1c-110">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c8e1c-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8e1c-111">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8e1c-111">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c8e1c-112">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="c8e1c-112">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e1c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8e1c-113">Return value</span></span>

<span data-ttu-id="c8e1c-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8e1c-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c8e1c-115">Puntero a la [**estructura D3DXQUATERNION**](d3dxquaternion.md) creada a partir de una matriz de rotación.</span><span class="sxs-lookup"><span data-stu-id="c8e1c-115">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e1c-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c8e1c-116">Remarks</span></span>

<span data-ttu-id="c8e1c-117">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="c8e1c-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="c8e1c-118">De este modo, la **función D3DXQuaternionRotationMatrix** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="c8e1c-118">In this way, the **D3DXQuaternionRotationMatrix** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="c8e1c-119">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="c8e1c-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e1c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8e1c-120">Requirements</span></span>



| <span data-ttu-id="c8e1c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e1c-121">Requirement</span></span> | <span data-ttu-id="c8e1c-122">Value</span><span class="sxs-lookup"><span data-stu-id="c8e1c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e1c-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8e1c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c8e1c-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e1c-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c8e1c-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8e1c-125">Library</span></span><br/> | <dl> <span data-ttu-id="c8e1c-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8e1c-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8e1c-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c8e1c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e1c-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c8e1c-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="c8e1c-129">**D3DXQuaternionRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="c8e1c-129">**D3DXQuaternionRotationAxis**</span></span>](d3dxquaternionrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="c8e1c-130">**D3DXQuaternionRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="c8e1c-130">**D3DXQuaternionRotationYawPitchRoll**</span></span>](d3dxquaternionrotationyawpitchroll.md)
</dt> </dl>

 

 




