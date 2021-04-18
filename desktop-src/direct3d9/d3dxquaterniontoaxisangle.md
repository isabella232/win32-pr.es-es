---
description: Calcula el eje de un cuaternión y el ángulo de rotación.
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: Función D3DXQuaternionToAxisAngle (D3dx9math. h)
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
ms.openlocfilehash: ecf8e6d1b1383a6e698f742351ee19ae75fd5bdc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717709"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a><span data-ttu-id="687e5-103">Función D3DXQuaternionToAxisAngle (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="687e5-103">D3DXQuaternionToAxisAngle function (D3dx9math.h)</span></span>

<span data-ttu-id="687e5-104">Calcula el eje de un cuaternión y el ángulo de rotación.</span><span class="sxs-lookup"><span data-stu-id="687e5-104">Computes a quaternion's axis and angle of rotation.</span></span>

## <a name="syntax"></a><span data-ttu-id="687e5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="687e5-105">Syntax</span></span>


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a><span data-ttu-id="687e5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="687e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="687e5-107">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="687e5-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="687e5-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="687e5-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="687e5-109">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="687e5-109">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="687e5-110">*pAxis* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="687e5-110">*pAxis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="687e5-111">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="687e5-111">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="687e5-112">Esta función devuelve un puntero a una estructura [**D3DXVECTOR3**](d3dxvector3.md) que identifica el eje de la rotación del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="687e5-112">This function returns a pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that identifies the quaternion's axis of rotation.</span></span>

</dd> <dt>

<span data-ttu-id="687e5-113">*pAngle* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="687e5-113">*pAngle* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="687e5-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="687e5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="687e5-115">Esta función devuelve un puntero a un valor FLOAT que identifica el ángulo de rotación del cuaternión en radianes.</span><span class="sxs-lookup"><span data-stu-id="687e5-115">This function returns a pointer to a FLOAT value that identifies the quaternion's angle of rotation in radians.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="687e5-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="687e5-116">Return value</span></span>

<span data-ttu-id="687e5-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="687e5-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="687e5-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="687e5-118">Remarks</span></span>

<span data-ttu-id="687e5-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="687e5-119">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="687e5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="687e5-120">Requirements</span></span>



| <span data-ttu-id="687e5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="687e5-121">Requirement</span></span> | <span data-ttu-id="687e5-122">Value</span><span class="sxs-lookup"><span data-stu-id="687e5-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="687e5-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="687e5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="687e5-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="687e5-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="687e5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="687e5-125">Library</span></span><br/> | <dl> <span data-ttu-id="687e5-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="687e5-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="687e5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="687e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="687e5-128">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="687e5-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
