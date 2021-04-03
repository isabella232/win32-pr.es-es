---
description: Transforma una matriz de planos en una matriz. Los vectores que describen cada plano se deben normalizar.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Función D3DXPlaneTransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 128b9c8c73db81faa877295e993504a7a510cd4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083764"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="46628-104">Función D3DXPlaneTransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="46628-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="46628-105">Transforma una matriz de planos en una matriz.</span><span class="sxs-lookup"><span data-stu-id="46628-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="46628-106">Los vectores que describen cada plano se deben normalizar.</span><span class="sxs-lookup"><span data-stu-id="46628-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="46628-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46628-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="46628-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46628-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46628-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="46628-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46628-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="46628-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="46628-111">Puntero a la estructura [**D3DXPLANE**](d3d10-d3dxplane.md) que contiene el plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="46628-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="46628-112">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="46628-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="46628-113">Retrasos  \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46628-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46628-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46628-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46628-115">Paso de cada plano transformado.</span><span class="sxs-lookup"><span data-stu-id="46628-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="46628-116">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46628-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46628-117">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="46628-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="46628-118">Puntero a la estructura D3DXPLANE de entrada, que contiene la matriz de los planos que se van a transformar.</span><span class="sxs-lookup"><span data-stu-id="46628-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="46628-119">El vector (a, b, c) que describe el plano debe normalizarse antes de que se llame a esta función.</span><span class="sxs-lookup"><span data-stu-id="46628-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="46628-120">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="46628-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="46628-121">*PStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46628-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46628-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46628-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46628-123">Paso de cada plano no transformado.</span><span class="sxs-lookup"><span data-stu-id="46628-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="46628-124">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46628-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46628-125">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="46628-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="46628-126">Puntero a la estructura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origen, que contiene la transposición inversa de los valores de transformación.</span><span class="sxs-lookup"><span data-stu-id="46628-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="46628-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46628-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46628-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46628-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46628-129">Número de planos que se van a transformar.</span><span class="sxs-lookup"><span data-stu-id="46628-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46628-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46628-130">Return value</span></span>

<span data-ttu-id="46628-131">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="46628-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="46628-132">Puntero a una estructura D3DXPLANE que representa el plano transformado.</span><span class="sxs-lookup"><span data-stu-id="46628-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="46628-133">Este es el mismo valor que se devuelve en el parámetro pOut para que esta función se pueda usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="46628-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="46628-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46628-134">Remarks</span></span>

<span data-ttu-id="46628-135">En este ejemplo se transforma un plano aplicando una escala no uniforme.</span><span class="sxs-lookup"><span data-stu-id="46628-135">This example transforms one plane by applying a non-uniform scale.</span></span>


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



<span data-ttu-id="46628-136">AX + por + cz + DW = 0 describe un plano.</span><span class="sxs-lookup"><span data-stu-id="46628-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="46628-137">El primer plano se crea con (a, b, c, d) = (0, 1, 1, 0), que es un plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="46628-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="46628-138">Después del escalado, el nuevo plano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), que muestra el nuevo plano que se va a describir mediante 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="46628-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="46628-139">El parámetro pM contiene la transposición inversa de la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="46628-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="46628-140">Este método requiere la TRANSPOSE inversa para que el vector normal del plano transformado también se pueda transformar correctamente.</span><span class="sxs-lookup"><span data-stu-id="46628-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="46628-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46628-141">Requirements</span></span>



| <span data-ttu-id="46628-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="46628-142">Requirement</span></span> | <span data-ttu-id="46628-143">Value</span><span class="sxs-lookup"><span data-stu-id="46628-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46628-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46628-144">Header</span></span><br/>  | <dl> <span data-ttu-id="46628-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="46628-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="46628-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46628-146">Library</span></span><br/> | <dl> <span data-ttu-id="46628-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46628-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46628-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="46628-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46628-149">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="46628-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
