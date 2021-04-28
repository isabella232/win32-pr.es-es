---
description: 'Función D3DXPlaneTransformArray (D3DX10Math.h): transforma una matriz de planos por una matriz. Los vectores que describen cada plano deben normalizarse.'
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Función D3DXPlaneTransformArray (D3DX10Math.h)
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
ms.openlocfilehash: d8b02b64fd13e7466980340056fceccc1da784cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103263"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="11a42-104">Función D3DXPlaneTransformArray (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="11a42-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="11a42-105">Transforma una matriz de planos por una matriz.</span><span class="sxs-lookup"><span data-stu-id="11a42-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="11a42-106">Los vectores que describen cada plano deben normalizarse.</span><span class="sxs-lookup"><span data-stu-id="11a42-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="11a42-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11a42-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="11a42-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11a42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11a42-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="11a42-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="11a42-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="11a42-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="11a42-111">Puntero a la [**estructura D3DXPLANE**](d3d10-d3dxplane.md) que contiene el plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="11a42-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="11a42-112">Vea Ejemplo.</span><span class="sxs-lookup"><span data-stu-id="11a42-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="11a42-113">*OutStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="11a42-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a42-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11a42-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11a42-115">El paso de cada plano transformado.</span><span class="sxs-lookup"><span data-stu-id="11a42-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="11a42-116">*pP* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="11a42-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a42-117">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="11a42-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="11a42-118">Puntero a la estructura D3DXPLANE de entrada, que contiene la matriz de planos que se va a transformar.</span><span class="sxs-lookup"><span data-stu-id="11a42-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="11a42-119">El vector (a, b, c) que describe el plano debe normalizarse antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="11a42-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="11a42-120">Vea Ejemplo.</span><span class="sxs-lookup"><span data-stu-id="11a42-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="11a42-121">*PStride* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="11a42-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a42-122">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11a42-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11a42-123">El paso de cada plano no transformado.</span><span class="sxs-lookup"><span data-stu-id="11a42-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="11a42-124">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="11a42-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a42-125">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="11a42-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="11a42-126">Puntero a la estructura [**D3DXMATRIX de**](d3d10-d3dxmatrix.md) origen, que contiene la transpuesta inversa de los valores de transformación.</span><span class="sxs-lookup"><span data-stu-id="11a42-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="11a42-127">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="11a42-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11a42-128">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11a42-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11a42-129">Número de planos que se transformarán.</span><span class="sxs-lookup"><span data-stu-id="11a42-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11a42-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11a42-130">Return value</span></span>

<span data-ttu-id="11a42-131">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="11a42-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="11a42-132">Puntero a una estructura D3DXPLANE, que representa el plano transformado.</span><span class="sxs-lookup"><span data-stu-id="11a42-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="11a42-133">Este es el mismo valor devuelto en el parámetro pOut para que esta función se pueda usar como parámetro para otra función.</span><span class="sxs-lookup"><span data-stu-id="11a42-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="11a42-134">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11a42-134">Remarks</span></span>

<span data-ttu-id="11a42-135">En este ejemplo se transforma un plano aplicando una escala no uniforme.</span><span class="sxs-lookup"><span data-stu-id="11a42-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="11a42-136">Un plano se describe mediante ax + by + dw + dw = 0.</span><span class="sxs-lookup"><span data-stu-id="11a42-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="11a42-137">El primer plano se crea con (a,b,c,d) = (0,1,1,0), que es un plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="11a42-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="11a42-138">Después del escalado, el nuevo plano contiene (a,b,c,d) = (0, 0,353f, 0,235f, 0), que muestra el nuevo plano descrito por 0,353y + 0,235z = 0.</span><span class="sxs-lookup"><span data-stu-id="11a42-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="11a42-139">El parámetro pM contiene la transpuesta inversa de la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="11a42-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="11a42-140">Este método requiere la transponer inversa para que el vector normal del plano transformado también se pueda transformar correctamente.</span><span class="sxs-lookup"><span data-stu-id="11a42-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="11a42-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11a42-141">Requirements</span></span>



| <span data-ttu-id="11a42-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="11a42-142">Requirement</span></span> | <span data-ttu-id="11a42-143">Value</span><span class="sxs-lookup"><span data-stu-id="11a42-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11a42-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11a42-144">Header</span></span><br/>  | <dl> <span data-ttu-id="11a42-145"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="11a42-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="11a42-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11a42-146">Library</span></span><br/> | <dl> <span data-ttu-id="11a42-147"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="11a42-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11a42-148">Consulte también</span><span class="sxs-lookup"><span data-stu-id="11a42-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11a42-149">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="11a42-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
