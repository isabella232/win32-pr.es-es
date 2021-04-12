---
description: Crea una matriz de proyección de perspectiva a la izquierda basada en un campo visual.
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: Función D3DXMatrixPerspectiveFovLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91b25a2e319236485c2c290b55acb94954a4791d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280441"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a><span data-ttu-id="f3f1c-103">Función D3DXMatrixPerspectiveFovLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f3f1c-103">D3DXMatrixPerspectiveFovLH function (D3dx9math.h)</span></span>

<span data-ttu-id="f3f1c-104">Crea una matriz de proyección de perspectiva a la izquierda basada en un campo visual.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f1c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3f1c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="f3f1c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f1c-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f3f1c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f1c-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3f1c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3f1c-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f3f1c-110">*fovy* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3f1c-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f1c-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3f1c-112">Campo de vista en la dirección y, en radianes.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="f3f1c-113">*Aspecto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f3f1c-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f1c-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3f1c-115">Relación de aspecto, definida como el ancho del espacio de la vista dividido por el alto.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="f3f1c-116">*Zn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3f1c-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f1c-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3f1c-118">Valor Z del plano de vista próximo.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="f3f1c-119">*ZF* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f3f1c-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f1c-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3f1c-121">Valor Z del plano de vista lejano.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f1c-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f3f1c-122">Return value</span></span>

<span data-ttu-id="f3f1c-123">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="f3f1c-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="f3f1c-124">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es una matriz de proyección de perspectiva izquierda.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3f1c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3f1c-125">Remarks</span></span>

<span data-ttu-id="f3f1c-126">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="f3f1c-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="f3f1c-127">De esta manera, la función **D3DXMatrixPerspectiveFovLH** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-127">In this way, the **D3DXMatrixPerspectiveFovLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f3f1c-128">Para cambiar el eje de relación de aspecto, use la fórmula de cálculo: fovy = 2 \* Math. atan (Math. tan (fovy \* 0,5)/aspecto).</span><span class="sxs-lookup"><span data-stu-id="f3f1c-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="f3f1c-129">Como alternativa, agregue las variables de relación de aspecto X e Y en la estructura para escalar el espacio de la vista vertical: fovy = 2 \* Math. atan (Math. tan (fovy \* 0,5)/Aspect), aspecto = aspectX \* aspecto Y.</span><span class="sxs-lookup"><span data-stu-id="f3f1c-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="f3f1c-130">Esta función calcula la matriz devuelta como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="f3f1c-130">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="f3f1c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3f1c-131">Requirements</span></span>



| <span data-ttu-id="f3f1c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3f1c-132">Requirement</span></span> | <span data-ttu-id="f3f1c-133">Value</span><span class="sxs-lookup"><span data-stu-id="f3f1c-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f1c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3f1c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f3f1c-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f1c-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f3f1c-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3f1c-136">Library</span></span><br/> | <dl> <span data-ttu-id="f3f1c-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3f1c-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f3f1c-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3f1c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f1c-139">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f3f1c-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f3f1c-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="f3f1c-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="f3f1c-142">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-142">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="f3f1c-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="f3f1c-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="f3f1c-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
