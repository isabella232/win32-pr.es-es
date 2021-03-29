---
description: Transforma una matriz de planos en una matriz. Los vectores que describen cada plano se deben normalizar.
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: Función D3DXPlaneTransformArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9a213b17aca9999ef0028fdceb4bb4321d47660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678767"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a><span data-ttu-id="36491-104">Función D3DXPlaneTransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="36491-104">D3DXPlaneTransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="36491-105">Transforma una matriz de planos en una matriz.</span><span class="sxs-lookup"><span data-stu-id="36491-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="36491-106">Los vectores que describen cada plano se deben normalizar.</span><span class="sxs-lookup"><span data-stu-id="36491-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="36491-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36491-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="36491-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36491-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36491-109">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="36491-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="36491-110">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="36491-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="36491-111">Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) que contiene el plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="36491-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="36491-112">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="36491-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="36491-113">Retrasos  \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="36491-113">*OutStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36491-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36491-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36491-115">Paso de cada plano transformado.</span><span class="sxs-lookup"><span data-stu-id="36491-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="36491-116">*PP* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36491-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36491-117">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="36491-117">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="36491-118">Puntero a la estructura [**D3DXPLANE**](d3dxplane.md) de entrada, que contiene la matriz de los planos que se van a transformar.</span><span class="sxs-lookup"><span data-stu-id="36491-118">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="36491-119">El vector (a, b, c) que describe el plano debe normalizarse antes de que se llame a esta función.</span><span class="sxs-lookup"><span data-stu-id="36491-119">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="36491-120">Vea el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="36491-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="36491-121">*PStride* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36491-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36491-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36491-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36491-123">Paso de cada plano no transformado.</span><span class="sxs-lookup"><span data-stu-id="36491-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="36491-124">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="36491-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36491-125">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="36491-125">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="36491-126">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) de origen, que contiene la transposición inversa de los valores de transformación.</span><span class="sxs-lookup"><span data-stu-id="36491-126">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="36491-127">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36491-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36491-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36491-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36491-129">Número de planos que se van a transformar.</span><span class="sxs-lookup"><span data-stu-id="36491-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36491-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36491-130">Return value</span></span>

<span data-ttu-id="36491-131">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="36491-131">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="36491-132">Puntero a una estructura [**D3DXPLANE**](d3dxplane.md) que representa el plano transformado.</span><span class="sxs-lookup"><span data-stu-id="36491-132">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="36491-133">Este es el mismo valor que se devuelve en el parámetro *pOut* para que esta función se pueda usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="36491-133">This is the same value returned in the *pOut* parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="36491-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36491-134">Remarks</span></span>

<span data-ttu-id="36491-135">En este ejemplo se transforma un plano aplicando una escala no uniforme.</span><span class="sxs-lookup"><span data-stu-id="36491-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="36491-136">AX + por + cz + DW = 0 describe un plano.</span><span class="sxs-lookup"><span data-stu-id="36491-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="36491-137">El primer plano se crea con (a, b, c, d) = (0, 1, 1, 0), que es un plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="36491-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="36491-138">Después del escalado, el nuevo plano contiene (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), que muestra el nuevo plano que se va a describir mediante 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="36491-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="36491-139">El parámetro *PM* contiene la transposición inversa de la matriz de transformación.</span><span class="sxs-lookup"><span data-stu-id="36491-139">The parameter *pM* contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="36491-140">Este método requiere la TRANSPOSE inversa para que el vector normal del plano transformado también se pueda transformar correctamente.</span><span class="sxs-lookup"><span data-stu-id="36491-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="36491-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36491-141">Requirements</span></span>



| <span data-ttu-id="36491-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="36491-142">Requirement</span></span> | <span data-ttu-id="36491-143">Value</span><span class="sxs-lookup"><span data-stu-id="36491-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="36491-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36491-144">Header</span></span><br/>  | <dl> <span data-ttu-id="36491-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="36491-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="36491-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36491-146">Library</span></span><br/> | <dl> <span data-ttu-id="36491-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36491-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="36491-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="36491-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36491-149">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="36491-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="36491-150">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="36491-150">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="36491-151">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="36491-151">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="36491-152">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="36491-152">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="36491-153">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="36491-153">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="36491-154">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="36491-154">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="36491-155">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="36491-155">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 
