---
description: 'Función D3DXPlaneIntersectLine (D3dx9math.h): busca la intersección entre un plano y una línea.'
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: Función D3DXPlaneIntersectLine (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9b89508079b0b400135f4ae39fd6fdfaed61952
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098073"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a><span data-ttu-id="3124e-103">Función D3DXPlaneIntersectLine (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="3124e-103">D3DXPlaneIntersectLine function (D3dx9math.h)</span></span>

<span data-ttu-id="3124e-104">Busca la intersección entre un plano y una línea.</span><span class="sxs-lookup"><span data-stu-id="3124e-104">Finds the intersection between a plane and a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="3124e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3124e-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="3124e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3124e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3124e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3124e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3124e-108">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3124e-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3124e-109">Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que identifica la intersección entre el plano y la línea especificados.</span><span class="sxs-lookup"><span data-stu-id="3124e-109">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, identifying the intersection between the specified plane and line.</span></span>

</dd> <dt>

<span data-ttu-id="3124e-110">*pP* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3124e-110">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3124e-111">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="3124e-111">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="3124e-112">Puntero a la estructura [**D3DXPLANE de**](d3dxplane.md) origen.</span><span class="sxs-lookup"><span data-stu-id="3124e-112">Pointer to the source [**D3DXPLANE**](d3dxplane.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="3124e-113">*pV1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3124e-113">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3124e-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3124e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3124e-115">Puntero a una estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen, definiendo un punto inicial de línea.</span><span class="sxs-lookup"><span data-stu-id="3124e-115">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line starting point.</span></span>

</dd> <dt>

<span data-ttu-id="3124e-116">*pV2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="3124e-116">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3124e-117">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="3124e-117">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3124e-118">Puntero a una estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen, definiendo un punto final de línea.</span><span class="sxs-lookup"><span data-stu-id="3124e-118">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure, defining a line ending point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3124e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3124e-119">Return value</span></span>

<span data-ttu-id="3124e-120">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="3124e-120">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="3124e-121">Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es la intersección entre el plano y la línea especificados.</span><span class="sxs-lookup"><span data-stu-id="3124e-121">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure that is the intersection between the specified plane and line.</span></span>

## <a name="remarks"></a><span data-ttu-id="3124e-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3124e-122">Remarks</span></span>

<span data-ttu-id="3124e-123">Si la línea es paralela al plano, **se devuelve NULL.**</span><span class="sxs-lookup"><span data-stu-id="3124e-123">If the line is parallel to the plane, **NULL** is returned.</span></span>

<span data-ttu-id="3124e-124">El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.*</span><span class="sxs-lookup"><span data-stu-id="3124e-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="3124e-125">De esta manera, la **función D3DXPlaneIntersectLine** se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="3124e-125">In this way, the **D3DXPlaneIntersectLine** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3124e-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3124e-126">Requirements</span></span>



| <span data-ttu-id="3124e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3124e-127">Requirement</span></span> | <span data-ttu-id="3124e-128">Value</span><span class="sxs-lookup"><span data-stu-id="3124e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3124e-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3124e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3124e-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="3124e-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="3124e-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3124e-131">Library</span></span><br/> | <dl> <span data-ttu-id="3124e-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3124e-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3124e-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3124e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3124e-134">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="3124e-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




