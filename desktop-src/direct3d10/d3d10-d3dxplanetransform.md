---
description: 'Función D3DXPlaneTransform (D3DX10Math.h): transforma un plano mediante una matriz. La matriz de entrada es la transpuesta inversa de la transformación real.'
ms.assetid: ded06eac-4086-47e8-bc55-c37959afc22d
title: Función D3DXPlaneTransform (D3DX10Math.h)
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
ms.openlocfilehash: 9b1d16ba2a29d42614c388a6207503ad32dd5e0f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108793"
---
# <a name="d3dxplanetransform-function-d3dx10mathh"></a><span data-ttu-id="b0555-104">Función D3DXPlaneTransform (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="b0555-104">D3DXPlaneTransform function (D3DX10Math.h)</span></span>

<span data-ttu-id="b0555-105">Transforma un plano mediante una matriz.</span><span class="sxs-lookup"><span data-stu-id="b0555-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="b0555-106">La matriz de entrada es la transpuesta inversa de la transformación real.</span><span class="sxs-lookup"><span data-stu-id="b0555-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0555-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0555-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="b0555-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0555-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0555-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b0555-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0555-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0555-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="b0555-111">Puntero al [**D3DXPLANE**](d3d10-d3dxplane.md) que contiene el plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="b0555-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) that contains the resulting transformed plane.</span></span> <span data-ttu-id="b0555-112">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b0555-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="b0555-113">*pP* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b0555-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0555-114">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="b0555-114">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="b0555-115">Puntero a la estructura D3DXPLANE de entrada, que contiene el plano que se va a transformar.</span><span class="sxs-lookup"><span data-stu-id="b0555-115">Pointer to the input D3DXPLANE structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="b0555-116">El vector (a,b,c) que describe el plano debe normalizarse antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="b0555-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="b0555-117">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b0555-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="b0555-118">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="b0555-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0555-119">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="b0555-119">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b0555-120">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen, que contiene los valores de transformación.</span><span class="sxs-lookup"><span data-stu-id="b0555-120">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="b0555-121">Esta matriz debe contener la transpuesta inversa de los valores de transformación.</span><span class="sxs-lookup"><span data-stu-id="b0555-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0555-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0555-122">Return value</span></span>

<span data-ttu-id="b0555-123">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0555-123">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="b0555-124">Puntero a una estructura D3DXPLANE, que representa el plano transformado.</span><span class="sxs-lookup"><span data-stu-id="b0555-124">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="b0555-125">Este es el mismo valor devuelto en el parámetro pOut para que esta función se pueda usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="b0555-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0555-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0555-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="b0555-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b0555-127">Examples</span></span>

<span data-ttu-id="b0555-128">En este ejemplo se transforma un plano aplicando una escala no uniforme.</span><span class="sxs-lookup"><span data-stu-id="b0555-128">This example transforms a plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="b0555-129">Un plano se describe mediante ax + by + dw + dw = 0.</span><span class="sxs-lookup"><span data-stu-id="b0555-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="b0555-130">El primer plano se crea con (a,b,c,d) = (0,1,1,0), que es un plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="b0555-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="b0555-131">Después del escalado, el nuevo plano contiene (a,b,c,d) = (0, 0,353f, 0,235f, 0), que muestra el nuevo plano descrito por 0,353y + 0,235z = 0.</span><span class="sxs-lookup"><span data-stu-id="b0555-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="b0555-132">El parámetro pM contiene la transpuesta inversa de la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="b0555-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="b0555-133">Este método requiere la transpuesta inversa para que el vector normal del plano transformado también se pueda transformar correctamente.</span><span class="sxs-lookup"><span data-stu-id="b0555-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0555-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0555-134">Requirements</span></span>



| <span data-ttu-id="b0555-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0555-135">Requirement</span></span> | <span data-ttu-id="b0555-136">Value</span><span class="sxs-lookup"><span data-stu-id="b0555-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0555-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0555-137">Header</span></span><br/>  | <dl> <span data-ttu-id="b0555-138"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0555-138"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b0555-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0555-139">Library</span></span><br/> | <dl> <span data-ttu-id="b0555-140"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0555-140"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0555-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b0555-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0555-142">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="b0555-142">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
