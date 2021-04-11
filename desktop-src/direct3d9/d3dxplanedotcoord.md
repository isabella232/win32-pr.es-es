---
description: Calcula el producto escalar de un plano y un vector 3D. Se supone que el parámetro w del vector es 1.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: Función D3DXPlaneDotCoord (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280240"
---
# <a name="d3dxplanedotcoord-function"></a><span data-ttu-id="d12ba-104">D3DXPlaneDotCoord función)</span><span class="sxs-lookup"><span data-stu-id="d12ba-104">D3DXPlaneDotCoord function</span></span>

<span data-ttu-id="d12ba-105">Calcula el producto escalar de un plano y un vector 3D.</span><span class="sxs-lookup"><span data-stu-id="d12ba-105">Computes the dot product of a plane and a 3D vector.</span></span> <span data-ttu-id="d12ba-106">Se supone que el parámetro w del vector es 1.</span><span class="sxs-lookup"><span data-stu-id="d12ba-106">The w parameter of the vector is assumed to be 1.</span></span>

## <a name="syntax"></a><span data-ttu-id="d12ba-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d12ba-107">Syntax</span></span>


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="d12ba-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d12ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d12ba-109">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d12ba-109">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d12ba-110">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="d12ba-110">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="d12ba-111">Puntero a una estructura de [**D3DXPLANE**](d3dxplane.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="d12ba-111">Pointer to a source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d12ba-112">*PV* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d12ba-112">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d12ba-113">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d12ba-113">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="d12ba-114">Puntero a una estructura de [**D3DXVECTOR3**](d3dxvector3.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="d12ba-114">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d12ba-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d12ba-115">Return value</span></span>

<span data-ttu-id="d12ba-116">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d12ba-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d12ba-117">Producto de punto del plano y Vector 3D.</span><span class="sxs-lookup"><span data-stu-id="d12ba-117">The dot product of the plane and 3D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d12ba-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d12ba-118">Remarks</span></span>

<span data-ttu-id="d12ba-119">Dado un plano (a, b, c, d) y un vector 3D (x, y, z), el valor devuelto de esta función es \* x + b \* y + c \* z + d \* 1.</span><span class="sxs-lookup"><span data-stu-id="d12ba-119">Given a plane (a, b, c, d) and a 3D vector (x, y, z) the return value of this function is a\*x + b\*y + c\*z + d\*1.</span></span> <span data-ttu-id="d12ba-120">La función **D3DXPlaneDotCoord** es útil para determinar la relación del plano con una coordenada en el espacio 3D.</span><span class="sxs-lookup"><span data-stu-id="d12ba-120">The **D3DXPlaneDotCoord** function is useful for determining the plane's relationship with a coordinate in 3D space.</span></span>

## <a name="requirements"></a><span data-ttu-id="d12ba-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d12ba-121">Requirements</span></span>



| <span data-ttu-id="d12ba-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d12ba-122">Requirement</span></span> | <span data-ttu-id="d12ba-123">Value</span><span class="sxs-lookup"><span data-stu-id="d12ba-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d12ba-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d12ba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d12ba-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d12ba-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d12ba-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d12ba-126">Library</span></span><br/> | <dl> <span data-ttu-id="d12ba-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d12ba-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d12ba-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="d12ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d12ba-129">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="d12ba-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="d12ba-130">**D3DXPlaneDot**</span><span class="sxs-lookup"><span data-stu-id="d12ba-130">**D3DXPlaneDot**</span></span>](d3dxplanedot.md)
</dt> <dt>

[<span data-ttu-id="d12ba-131">**D3DXPlaneDotNormal**</span><span class="sxs-lookup"><span data-stu-id="d12ba-131">**D3DXPlaneDotNormal**</span></span>](d3dxplanedotnormal.md)
</dt> </dl>

 

 
