---
description: Transforma un plano mediante una matriz. La matriz de entrada es la transposición inversa de la transformación real.
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: Función D3DXPlaneTransform (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1b3c3390d84cd0d9c876afac6243ab90ca515e11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362718"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a><span data-ttu-id="c14ec-104">Función D3DXPlaneTransform (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c14ec-104">D3DXPlaneTransform function (D3DX10Math.h)</span></span>

<span data-ttu-id="c14ec-105">Transforma un plano mediante una matriz.</span><span class="sxs-lookup"><span data-stu-id="c14ec-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="c14ec-106">La matriz de entrada es la transposición inversa de la transformación real.</span><span class="sxs-lookup"><span data-stu-id="c14ec-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c14ec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c14ec-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c14ec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c14ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c14ec-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c14ec-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c14ec-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c14ec-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c14ec-111">Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md) que contiene el plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="c14ec-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that contains the resulting transformed plane.</span></span> <span data-ttu-id="c14ec-112">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c14ec-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="c14ec-113">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c14ec-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14ec-114">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="c14ec-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c14ec-115">Puntero a la estructura D3DXPLANE de entrada, que contiene el plano que se va a transformar.</span><span class="sxs-lookup"><span data-stu-id="c14ec-115">Pointer to the input D3DXPLANE structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="c14ec-116">El vector (a, b, c) que describe el plano debe normalizarse antes de que se llame a esta función.</span><span class="sxs-lookup"><span data-stu-id="c14ec-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="c14ec-117">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c14ec-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="c14ec-118">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c14ec-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c14ec-119">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c14ec-119">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c14ec-120">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen, que contiene los valores de la transformación.</span><span class="sxs-lookup"><span data-stu-id="c14ec-120">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="c14ec-121">Esta matriz debe contener la transposición inversa de los valores de transformación.</span><span class="sxs-lookup"><span data-stu-id="c14ec-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c14ec-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c14ec-122">Return value</span></span>

<span data-ttu-id="c14ec-123">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="c14ec-123">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="c14ec-124">Puntero a una estructura D3DXPLANE que representa el plano transformado.</span><span class="sxs-lookup"><span data-stu-id="c14ec-124">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="c14ec-125">Este es el mismo valor que se devuelve en el parámetro pOut para que esta función se pueda usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="c14ec-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="c14ec-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c14ec-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="c14ec-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c14ec-127">Examples</span></span>

<span data-ttu-id="c14ec-128">En este ejemplo se transforma un plano aplicando una escala no uniforme.</span><span class="sxs-lookup"><span data-stu-id="c14ec-128">This example transforms a plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="c14ec-129">AX + por + cz + DW = 0 describe un plano.</span><span class="sxs-lookup"><span data-stu-id="c14ec-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="c14ec-130">El primer plano se crea con (a, b, c, d) = (0, 1, 1, 0), que es un plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="c14ec-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="c14ec-131">Después del escalado, el nuevo plano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), que muestra el nuevo plano que se va a describir mediante 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="c14ec-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="c14ec-132">El parámetro pM contiene la transposición inversa de la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="c14ec-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="c14ec-133">Este método requiere la TRANSPOSE inversa para que el vector normal del plano transformado también se pueda transformar correctamente.</span><span class="sxs-lookup"><span data-stu-id="c14ec-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="c14ec-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c14ec-134">Requirements</span></span>



| <span data-ttu-id="c14ec-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c14ec-135">Requirement</span></span> | <span data-ttu-id="c14ec-136">Value</span><span class="sxs-lookup"><span data-stu-id="c14ec-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c14ec-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c14ec-137">Header</span></span><br/>  | <dl> <span data-ttu-id="c14ec-138"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c14ec-138"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c14ec-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c14ec-139">Library</span></span><br/> | <dl> <span data-ttu-id="c14ec-140"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c14ec-140"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c14ec-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c14ec-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14ec-142">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c14ec-142">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
