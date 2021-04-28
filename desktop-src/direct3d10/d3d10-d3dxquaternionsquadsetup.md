---
description: 'Función D3DXQuaternionSquadSetup (D3DX10Math.h): configura puntos de control para la interpolación de cuadrángulo esférico.'
ms.assetid: c66227bd-8cc1-4173-9dc2-5aab9d57301e
title: Función D3DXQuaternionSquadSetup (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquadSetup
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8d8a778473c0b07ef984facce9c42f947755a74a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108723"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx10mathh"></a><span data-ttu-id="272d2-103">Función D3DXQuaternionSquadSetup (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="272d2-103">D3DXQuaternionSquadSetup function (D3DX10Math.h)</span></span>

<span data-ttu-id="272d2-104">Configura puntos de control para la interpolación de cuadrángulo esférica.</span><span class="sxs-lookup"><span data-stu-id="272d2-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="272d2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="272d2-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _In_       D3DXQUATERNION *pAOut,
  _In_       D3DXQUATERNION *pBOut,
  _In_       D3DXQUATERNION *pCOut,
  _In_ const D3DXQUATERNION *pQ0,
  _In_ const D3DXQUATERNION *pQ1,
  _In_ const D3DXQUATERNION *pQ2,
  _In_ const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="272d2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="272d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="272d2-107">*pAOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="272d2-107">*pAOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="272d2-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="272d2-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="272d2-109">Puntero a AOut.</span><span class="sxs-lookup"><span data-stu-id="272d2-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="272d2-110">*pBOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="272d2-110">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="272d2-111">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="272d2-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="272d2-112">Puntero a BOut.</span><span class="sxs-lookup"><span data-stu-id="272d2-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="272d2-113">*pCOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="272d2-113">*pCOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="272d2-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="272d2-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="272d2-115">Puntero a COut.</span><span class="sxs-lookup"><span data-stu-id="272d2-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="272d2-116">*pQ0* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="272d2-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="272d2-117">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="272d2-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="272d2-118">Puntero al punto de control de entrada, Q0.</span><span class="sxs-lookup"><span data-stu-id="272d2-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="272d2-119">*pQ1* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="272d2-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="272d2-120">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="272d2-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="272d2-121">Puntero al punto de control de entrada, Q1.</span><span class="sxs-lookup"><span data-stu-id="272d2-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="272d2-122">*pQ2* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="272d2-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="272d2-123">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="272d2-123">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="272d2-124">Puntero al punto de control de entrada, Q2.</span><span class="sxs-lookup"><span data-stu-id="272d2-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="272d2-125">*pQ3* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="272d2-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="272d2-126">Tipo: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="272d2-126">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="272d2-127">Puntero al punto de control de entrada, Q3.</span><span class="sxs-lookup"><span data-stu-id="272d2-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="272d2-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="272d2-128">Return value</span></span>

<span data-ttu-id="272d2-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="272d2-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="272d2-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="272d2-130">Remarks</span></span>

<span data-ttu-id="272d2-131">Esta función toma cuatro puntos de control, que se proporcionan a las entradas pQ0, pQ1, pQ2 y pQ3.</span><span class="sxs-lookup"><span data-stu-id="272d2-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="272d2-132">A continuación, la función modifica estos valores para buscar una curva que fluya a lo largo de la ruta de acceso más corta.</span><span class="sxs-lookup"><span data-stu-id="272d2-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="272d2-133">Los valores de q0, q2 y q3 se calculan como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="272d2-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="272d2-134">Una vez calculados los nuevos valores de Q, los valores de AOut, BOut y COut se calculan de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="272d2-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="272d2-135">AOut = q1 \* e<sup> \[ -0.25\ \* (\ Ln \[ Exp(q1) \* q2 \] \ +\ Ln \[ Exp(q1) \* q0 \ \] )\ \] </sup></span><span class="sxs-lookup"><span data-stu-id="272d2-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="272d2-136">BOut = q2 \* e<sup> \[ -0.25\ \* (\ Ln \[ Exp(q2) \* q3 \] \ +\ Ln \[ Exp(q2) \* q1 \ \] )\ \] </sup></span><span class="sxs-lookup"><span data-stu-id="272d2-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="272d2-137">COut = q2</span><span class="sxs-lookup"><span data-stu-id="272d2-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="272d2-138">Ln es el método de API [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) y Exp es el método de API [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="272d2-138">Ln is the API method [**D3DXQuaternionLn**](d3d10-d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3d10-d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="272d2-139">Use [**D3DXQuaternionNormalize para cualquier**](d3d10-d3dxquaternionnormalize.md) entrada de cuaternión que aún no esté normalizada.</span><span class="sxs-lookup"><span data-stu-id="272d2-139">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="272d2-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="272d2-140">Examples</span></span>

<span data-ttu-id="272d2-141">En el ejemplo siguiente se muestra cómo usar un conjunto de claves de cuaternión (Q0, Q1, Q2, Q3) para calcular los puntos de cuadrángulo internos (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="272d2-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="272d2-142">Esto garantiza que las tangentes sean continuas en segmentos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="272d2-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="272d2-143">En el ejemplo de código siguiente se muestra cómo puede interpolar entre Q1 y Q2.</span><span class="sxs-lookup"><span data-stu-id="272d2-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


```
// Rotation about the z-axis
D3DXQUATERNION Q0 = D3DXQUATERNION(0,  0, 0.707f, -.707f);
D3DXQUATERNION Q1 = D3DXQUATERNION(0,  0, 0.000f, 1.000f);
D3DXQUATERNION Q2 = D3DXQUATERNION(0,  0, 0.707f, 0.707f);
D3DXQUATERNION Q3 = D3DXQUATERNION(0,  0, 1.000f, 0.000f);
D3DXQUATERNION A, B, C, Qt;
FLOAT time = 0.5f;

D3DXQuaternionSquadSetup(&A, &B, &C, &Q0, &Q1, &Q2, &Q3);
D3DXQuaternionSquad(&Qt, &Q1, &A, &B, &C, time);
```



> [!Note]
>
> -   <span data-ttu-id="272d2-144">C es +/- Q2 en función del resultado de la función.</span><span class="sxs-lookup"><span data-stu-id="272d2-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="272d2-145">Qt es el resultado de la función.</span><span class="sxs-lookup"><span data-stu-id="272d2-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="272d2-146">El resultado es una rotación de 45 grados alrededor del eje Z para el tiempo = 0,5.</span><span class="sxs-lookup"><span data-stu-id="272d2-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="272d2-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="272d2-147">Requirements</span></span>



| <span data-ttu-id="272d2-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="272d2-148">Requirement</span></span> | <span data-ttu-id="272d2-149">Value</span><span class="sxs-lookup"><span data-stu-id="272d2-149">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="272d2-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="272d2-150">Header</span></span><br/>  | <dl> <span data-ttu-id="272d2-151"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="272d2-151"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="272d2-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="272d2-152">Library</span></span><br/> | <dl> <span data-ttu-id="272d2-153"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="272d2-153"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="272d2-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="272d2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="272d2-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="272d2-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
