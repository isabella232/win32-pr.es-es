---
description: 'Función D3DXMatrixPerspectiveRH (D3DX10Math.h): crea una matriz de proyección de perspectiva a la derecha.'
ms.assetid: 324c8a21-24ef-4b3a-aac1-a753e26076d4
title: Función D3DXMatrixPerspectiveRH (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 03ffd99d016023612daa3de96ae29275d71074a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109013"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx10mathh"></a><span data-ttu-id="b8dfb-103">Función D3DXMatrixPerspectiveRH (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="b8dfb-103">D3DXMatrixPerspectiveRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b8dfb-104">Crea una matriz de proyección de perspectiva a la derecha.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8dfb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8dfb-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="b8dfb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8dfb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8dfb-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b8dfb-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8dfb-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8dfb-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b8dfb-109">Puntero a la [**estructura D3DXMATRIX**](d3d10-d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b8dfb-110">*w* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8dfb-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8dfb-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8dfb-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8dfb-112">Ancho del volumen de vista en el plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b8dfb-113">*h* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8dfb-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8dfb-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8dfb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8dfb-115">Alto del volumen de vista en el plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b8dfb-116">*zn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b8dfb-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8dfb-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8dfb-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8dfb-118">Valor Z del plano de vista cercano.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="b8dfb-119">*y* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b8dfb-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8dfb-120">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8dfb-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8dfb-121">Valor Z del plano de vista lejano.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8dfb-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8dfb-122">Return value</span></span>

<span data-ttu-id="b8dfb-123">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b8dfb-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b8dfb-124">Puntero a una estructura D3DXMATRIX que es una matriz de proyección de perspectiva a la derecha.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8dfb-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b8dfb-125">Remarks</span></span>

<span data-ttu-id="b8dfb-126">Todos los parámetros de la función D3DXMatrixPerspectiveRH son distancias en el espacio de la cámara.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-126">All the parameters of the D3DXMatrixPerspectiveRH function are distances in camera space.</span></span> <span data-ttu-id="b8dfb-127">Los parámetros describen las dimensiones del volumen de vista.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="b8dfb-128">El valor devuelto para esta función es el mismo valor devuelto en el parámetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-128">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b8dfb-129">De este modo, la función D3DXMatrixPerspectiveRH se puede usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-129">In this way, the D3DXMatrixPerspectiveRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b8dfb-130">Esta función usa la siguiente fórmula para calcular la matriz devuelta.</span><span class="sxs-lookup"><span data-stu-id="b8dfb-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="b8dfb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8dfb-131">Requirements</span></span>



| <span data-ttu-id="b8dfb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8dfb-132">Requirement</span></span> | <span data-ttu-id="b8dfb-133">Value</span><span class="sxs-lookup"><span data-stu-id="b8dfb-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8dfb-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8dfb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="b8dfb-135"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b8dfb-135"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b8dfb-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8dfb-136">Library</span></span><br/> | <dl> <span data-ttu-id="b8dfb-137"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8dfb-137"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b8dfb-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b8dfb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8dfb-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b8dfb-139">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
