---
description: Devuelve el conjugado de un cuaternión.
ms.assetid: f690fdd8-7805-4fc1-9064-4f249d5f7c4f
title: Función D3DXQuaternionConjugate (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionConjugate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbf288724dbdede9d98ec4ee21afd1bb57dd7a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280406"
---
# <a name="d3dxquaternionconjugate-function"></a><span data-ttu-id="eb01e-103">D3DXQuaternionConjugate función)</span><span class="sxs-lookup"><span data-stu-id="eb01e-103">D3DXQuaternionConjugate function</span></span>

<span data-ttu-id="eb01e-104">Devuelve el conjugado de un cuaternión.</span><span class="sxs-lookup"><span data-stu-id="eb01e-104">Returns the conjugate of a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb01e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb01e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionConjugate(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="eb01e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb01e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb01e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eb01e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb01e-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb01e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="eb01e-109">Puntero a la estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="eb01e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="eb01e-110">*pQ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eb01e-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb01e-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="eb01e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="eb01e-112">Puntero a la estructura de [**D3DXQUATERNION**](d3dxquaternion.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="eb01e-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb01e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb01e-113">Return value</span></span>

<span data-ttu-id="eb01e-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="eb01e-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="eb01e-115">Puntero a una estructura [**D3DXQUATERNION**](d3dxquaternion.md) que es el conjugado del cuaternión.</span><span class="sxs-lookup"><span data-stu-id="eb01e-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the conjugate of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb01e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb01e-116">Remarks</span></span>

<span data-ttu-id="eb01e-117">Dado un cuaternión (x, y, z, w), la función **D3DXQuaternionConjugate** devolverá el cuaternión (-x,-y,-z, w).</span><span class="sxs-lookup"><span data-stu-id="eb01e-117">Given a quaternion (x, y, z, w), the **D3DXQuaternionConjugate** function will return the quaternion (-x, -y, -z, w).</span></span>

<span data-ttu-id="eb01e-118">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="eb01e-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="eb01e-119">De esta manera, la función **D3DXQuaternionConjugate** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="eb01e-119">In this way, the **D3DXQuaternionConjugate** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="eb01e-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="eb01e-120">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb01e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb01e-121">Requirements</span></span>



| <span data-ttu-id="eb01e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb01e-122">Requirement</span></span> | <span data-ttu-id="eb01e-123">Value</span><span class="sxs-lookup"><span data-stu-id="eb01e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb01e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb01e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eb01e-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb01e-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="eb01e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb01e-126">Library</span></span><br/> | <dl> <span data-ttu-id="eb01e-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb01e-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eb01e-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb01e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb01e-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="eb01e-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="eb01e-130">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="eb01e-130">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




