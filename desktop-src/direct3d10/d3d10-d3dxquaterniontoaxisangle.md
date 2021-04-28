---
description: 'Función D3DXQuaternionToAxisAngle (D3DX10Math.h): calcula el eje y el ángulo de rotación de un cuaternión.'
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: Función D3DXQuaternionToAxisAngle (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108703"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a><span data-ttu-id="38f6f-103">Función D3DXQuaternionToAxisAngle (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="38f6f-103">D3DXQuaternionToAxisAngle function (D3DX10Math.h)</span></span>

<span data-ttu-id="38f6f-104">Calcula el eje y el ángulo de rotación de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="38f6f-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38f6f-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="38f6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38f6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f6f-107">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="38f6f-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f6f-108">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="38f6f-108">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="38f6f-109">Puntero al [**D3DXQUATERNION de origen.**](d3d10-d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="38f6f-109">Pointer to the source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).</span></span>

</dd> <dt>

<span data-ttu-id="38f6f-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="38f6f-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f6f-111">Tipo: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="38f6f-111">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="38f6f-112">Esta función devuelve un puntero a [**un D3DXVECTOR3**](d3d10-d3dxvector3.md) que identifica el eje de rotación del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="38f6f-112">This function returns a pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="38f6f-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="38f6f-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38f6f-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38f6f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38f6f-115">Esta función devuelve un puntero a un valor FLOAT que identifica el ángulo de rotación del cuaternión en radianes.</span><span class="sxs-lookup"><span data-stu-id="38f6f-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f6f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38f6f-116">Return value</span></span>

<span data-ttu-id="38f6f-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="38f6f-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="38f6f-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="38f6f-118">Remarks</span></span>

<span data-ttu-id="38f6f-119">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="38f6f-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="38f6f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38f6f-120">Requirements</span></span>



| <span data-ttu-id="38f6f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="38f6f-121">Requirement</span></span> | <span data-ttu-id="38f6f-122">Value</span><span class="sxs-lookup"><span data-stu-id="38f6f-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38f6f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38f6f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="38f6f-124"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="38f6f-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="38f6f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38f6f-125">Library</span></span><br/> | <dl> <span data-ttu-id="38f6f-126"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="38f6f-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="38f6f-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="38f6f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f6f-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="38f6f-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
