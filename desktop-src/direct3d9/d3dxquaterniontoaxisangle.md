---
description: 'Función D3DXQuaternionToAxisAngle (D3dx9math.h): calcula el eje y el ángulo de rotación de un cuaternión.'
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Función D3DXQuaternionToAxisAngle (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8613a9d14c5e33b0f9f4e719a02ac9a6d70d1119
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117983"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="0d22f-103">Función D3DXQuaternionToAxisAngle (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="0d22f-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="0d22f-104">Calcula el eje y el ángulo de rotación de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="0d22f-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d22f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d22f-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="0d22f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d22f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d22f-107">*pQ* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="0d22f-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d22f-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="0d22f-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="0d22f-109">Puntero a la estructura [**D3DXQUATERNION de**](d3dxquaternion.md) origen.</span><span class="sxs-lookup"><span data-stu-id="0d22f-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0d22f-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0d22f-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d22f-111">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d22f-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="0d22f-112">Esta función devuelve un puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que identifica el eje de rotación del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="0d22f-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="0d22f-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0d22f-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d22f-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d22f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="0d22f-115">Esta función devuelve un puntero a un valor FLOAT que identifica el ángulo de rotación del cuaternión en radianes.</span><span class="sxs-lookup"><span data-stu-id="0d22f-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d22f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d22f-116">Return value</span></span>

<span data-ttu-id="0d22f-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0d22f-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d22f-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0d22f-118">Remarks</span></span>

<span data-ttu-id="0d22f-119">Use [**D3DXQuaternionNormalize para cualquier**](d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="0d22f-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d22f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d22f-120">Requirements</span></span>



| <span data-ttu-id="0d22f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d22f-121">Requirement</span></span> | <span data-ttu-id="0d22f-122">Value</span><span class="sxs-lookup"><span data-stu-id="0d22f-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d22f-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d22f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0d22f-124"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="0d22f-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0d22f-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d22f-125">Library</span></span><br/> | <dl> <span data-ttu-id="0d22f-126"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d22f-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0d22f-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0d22f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d22f-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="0d22f-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
