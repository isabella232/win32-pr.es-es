---
description: 'Función D3DXPlaneTransform (D3dx9math.h): transforma un plano mediante una matriz. La matriz de entrada es la transpuesta inversa de la transformación real.'
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: Función D3DXPlaneTransform (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1f1f6ffc45098ba8f8b689e6f6212e5bec4fd679
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098023"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a><span data-ttu-id="67bc8-104">Función D3DXPlaneTransform (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="67bc8-104">D3DXPlaneTransform function (D3dx9math.h)</span></span>

<span data-ttu-id="67bc8-105">Transforma un plano mediante una matriz.</span><span class="sxs-lookup"><span data-stu-id="67bc8-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="67bc8-106">La matriz de entrada es la transpuesta inversa de la transformación real.</span><span class="sxs-lookup"><span data-stu-id="67bc8-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="67bc8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67bc8-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="67bc8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67bc8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67bc8-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="67bc8-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="67bc8-110">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="67bc8-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="67bc8-111">Puntero a la [**estructura D3DXPLANE**](d3dxplane.md) que contiene el plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="67bc8-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="67bc8-112">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="67bc8-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="67bc8-113">*pP* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="67bc8-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67bc8-114">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="67bc8-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="67bc8-115">Puntero a la estructura [**D3DXPLANE de**](d3dxplane.md) entrada, que contiene el plano que se transformará.</span><span class="sxs-lookup"><span data-stu-id="67bc8-115">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="67bc8-116">El vector (a,b,c) que describe el plano debe normalizarse antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="67bc8-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="67bc8-117">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="67bc8-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="67bc8-118">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="67bc8-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67bc8-119">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="67bc8-119">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="67bc8-120">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen, que contiene los valores de transformación.</span><span class="sxs-lookup"><span data-stu-id="67bc8-120">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="67bc8-121">Esta matriz debe contener la transpuesta inversa de los valores de transformación.</span><span class="sxs-lookup"><span data-stu-id="67bc8-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67bc8-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67bc8-122">Return value</span></span>

<span data-ttu-id="67bc8-123">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="67bc8-123">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="67bc8-124">Puntero a una [**estructura D3DXPLANE,**](d3dxplane.md) que representa el plano transformado.</span><span class="sxs-lookup"><span data-stu-id="67bc8-124">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="67bc8-125">Este es el mismo valor devuelto en el parámetro pOut para que esta función se pueda usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="67bc8-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="67bc8-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67bc8-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="67bc8-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="67bc8-127">Examples</span></span>

<span data-ttu-id="67bc8-128">En este ejemplo se transforma un plano aplicando una escala no uniforme.</span><span class="sxs-lookup"><span data-stu-id="67bc8-128">This example transforms a plane by applying a non-uniform scale.</span></span>


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



<span data-ttu-id="67bc8-129">Un plano se describe por ax + by + dw + dw = 0.</span><span class="sxs-lookup"><span data-stu-id="67bc8-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="67bc8-130">El primer plano se crea con (a,b,c,d) = (0,1,1,0), que es un plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="67bc8-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="67bc8-131">Después del escalado, el nuevo plano contiene (a,b,c,d) = (0, 0,353f, 0,235f, 0), que muestra el nuevo plano descrito por 0,353y + 0,235z = 0.</span><span class="sxs-lookup"><span data-stu-id="67bc8-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="67bc8-132">El parámetro pM contiene la transpuesta inversa de la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="67bc8-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="67bc8-133">Este método requiere la transponer inversa para que el vector normal del plano transformado también se pueda transformar correctamente.</span><span class="sxs-lookup"><span data-stu-id="67bc8-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="67bc8-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67bc8-134">Requirements</span></span>



| <span data-ttu-id="67bc8-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="67bc8-135">Requirement</span></span> | <span data-ttu-id="67bc8-136">Value</span><span class="sxs-lookup"><span data-stu-id="67bc8-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67bc8-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67bc8-137">Header</span></span><br/>  | <dl> <span data-ttu-id="67bc8-138"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="67bc8-138"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="67bc8-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67bc8-139">Library</span></span><br/> | <dl> <span data-ttu-id="67bc8-140"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="67bc8-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="67bc8-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="67bc8-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67bc8-142">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="67bc8-142">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="67bc8-143">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="67bc8-143">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="67bc8-144">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="67bc8-144">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="67bc8-145">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="67bc8-145">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="67bc8-146">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="67bc8-146">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="67bc8-147">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="67bc8-147">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="67bc8-148">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="67bc8-148">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 




