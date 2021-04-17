---
description: Configura los puntos de control para la interpolación Quadrangle esférica.
ms.assetid: f800d457-8546-49a1-800e-e5c27af96710
title: Función D3DXQuaternionSquadSetup (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 04bae9dafbb9df90fdcccee830a1eecb64c1430f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717710"
---
# <a name="d3dxquaternionsquadsetup-function-d3dx9mathh"></a><span data-ttu-id="4d738-103">Función D3DXQuaternionSquadSetup (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="4d738-103">D3DXQuaternionSquadSetup function (D3dx9math.h)</span></span>

<span data-ttu-id="4d738-104">Configura los puntos de control para la interpolación Quadrangle esférica.</span><span class="sxs-lookup"><span data-stu-id="4d738-104">Sets up control points for spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d738-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d738-105">Syntax</span></span>


```C++
void D3DXQuaternionSquadSetup(
  _Out_       D3DXQUATERNION *pAOut,
  _Out_       D3DXQUATERNION *pBOut,
  _Out_       D3DXQUATERNION *pCOut,
  _In_  const D3DXQUATERNION *pQ0,
  _In_  const D3DXQUATERNION *pQ1,
  _In_  const D3DXQUATERNION *pQ2,
  _In_  const D3DXQUATERNION *pQ3
);
```



## <a name="parameters"></a><span data-ttu-id="4d738-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d738-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d738-107">*pAOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4d738-107">*pAOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d738-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d738-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4d738-109">Puntero a sobre.</span><span class="sxs-lookup"><span data-stu-id="4d738-109">Pointer to AOut.</span></span>

</dd> <dt>

<span data-ttu-id="4d738-110">*pBOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4d738-110">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d738-111">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d738-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4d738-112">Puntero que va a estar cerca.</span><span class="sxs-lookup"><span data-stu-id="4d738-112">Pointer to BOut.</span></span>

</dd> <dt>

<span data-ttu-id="4d738-113">*pCOut* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4d738-113">*pCOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d738-114">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="4d738-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4d738-115">Puntero a COut.</span><span class="sxs-lookup"><span data-stu-id="4d738-115">Pointer to COut.</span></span>

</dd> <dt>

<span data-ttu-id="4d738-116">*pQ0* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d738-116">*pQ0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d738-117">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d738-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4d738-118">Puntero al punto de control de entrada, q0.</span><span class="sxs-lookup"><span data-stu-id="4d738-118">Pointer to the input control point, Q0.</span></span>

</dd> <dt>

<span data-ttu-id="4d738-119">*pQ1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d738-119">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d738-120">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d738-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4d738-121">Puntero en el punto de control de entrada, Q1.</span><span class="sxs-lookup"><span data-stu-id="4d738-121">Pointer to the input control point, Q1.</span></span>

</dd> <dt>

<span data-ttu-id="4d738-122">*pQ2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d738-122">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d738-123">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d738-123">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4d738-124">Puntero en el punto de control de entrada, T2.</span><span class="sxs-lookup"><span data-stu-id="4d738-124">Pointer to the input control point, Q2.</span></span>

</dd> <dt>

<span data-ttu-id="4d738-125">*pQ3* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4d738-125">*pQ3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d738-126">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="4d738-126">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="4d738-127">Puntero al punto de control de entrada, Q3.</span><span class="sxs-lookup"><span data-stu-id="4d738-127">Pointer to the input control point, Q3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d738-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d738-128">Return value</span></span>

<span data-ttu-id="4d738-129">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4d738-129">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d738-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d738-130">Remarks</span></span>

<span data-ttu-id="4d738-131">Esta función toma cuatro puntos de control, que se proporcionan a las entradas pQ0, pQ1, pQ2 y pQ3.</span><span class="sxs-lookup"><span data-stu-id="4d738-131">This function takes four control points, which are supplied to the inputs pQ0, pQ1, pQ2, and pQ3.</span></span> <span data-ttu-id="4d738-132">A continuación, la función modifica estos valores para buscar una curva que fluya a lo largo de la ruta más corta.</span><span class="sxs-lookup"><span data-stu-id="4d738-132">The function then alters these values to find a curve that flows along the shortest path.</span></span> <span data-ttu-id="4d738-133">Los valores de q0, T2 y Q3 se calculan como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="4d738-133">The values of q0, q2, and q3 are calculated as shown below.</span></span>


```
q0 = |Q0 + Q1| < |Q0 - Q1| ? -Q0 : Q0
q2 = |Q1 + Q2| < |Q1 - Q2| ? -Q2 : Q2
q3 = |Q2 + Q3| < |Q2 - Q3| ? -Q3 : Q3
```



<span data-ttu-id="4d738-134">Una vez calculados los nuevos valores Q, los valores de sobre, cerca de y COut se calculan de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="4d738-134">Having calculated the new Q values, the values for AOut, BOut, and COut are calculated as follows:</span></span>

<span data-ttu-id="4d738-135">Sobre = Q1 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (Q1) \* T2 \] \ + \ LN \[ exp (Q1) \* q0 \] \) \ \] </sup></span><span class="sxs-lookup"><span data-stu-id="4d738-135">AOut = q1 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q1)\*q2\]\ +\ Ln\[Exp(q1)\*q0\]\ )\ \]</sup></span></span>

<span data-ttu-id="4d738-136">Cerca de = T2 \* e<sup> \[ -0,25 \ \* (\ LN \[ exp (T2) \* Q3 \] \ + \ LN \[ exp (T2) \* Q1 \] \) \] \</sup></span><span class="sxs-lookup"><span data-stu-id="4d738-136">BOut = q2 \* e<sup>\[-0.25\ \*(\ Ln\[Exp(q2)\*q3\]\ +\ Ln\[Exp(q2)\*q1\]\ )\ \]</sup></span></span>

<span data-ttu-id="4d738-137">COut = T2</span><span class="sxs-lookup"><span data-stu-id="4d738-137">COut = q2</span></span>

> [!Note]  
> <span data-ttu-id="4d738-138">LN es el método de API [**D3DXQuaternionLn**](d3dxquaternionln.md) y exp es el método de API [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span><span class="sxs-lookup"><span data-stu-id="4d738-138">Ln is the API method [**D3DXQuaternionLn**](d3dxquaternionln.md) and Exp is the API method [**D3DXQuaternionExp**](d3dxquaternionexp.md).</span></span>

 

<span data-ttu-id="4d738-139">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para cualquier entrada de cuaternión que no esté ya normalizada.</span><span class="sxs-lookup"><span data-stu-id="4d738-139">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

### <a name="examples"></a><span data-ttu-id="4d738-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4d738-140">Examples</span></span>

<span data-ttu-id="4d738-141">En el ejemplo siguiente se muestra cómo usar un conjunto de claves de cuaternión (q0, Q1, T2, Q3) para calcular los puntos de Quadrangle internos (A, B, C).</span><span class="sxs-lookup"><span data-stu-id="4d738-141">The following example shows how to use a set of quaternion keys (Q0, Q1, Q2, Q3) to compute the inner quadrangle points (A, B, C).</span></span> <span data-ttu-id="4d738-142">Esto garantiza que las tangentes sean continuas entre segmentos adyacentes.</span><span class="sxs-lookup"><span data-stu-id="4d738-142">This ensures that the tangents are continuous across adjacent segments.</span></span>


```
      A     B
Q0    Q1    Q2    Q3
```



<span data-ttu-id="4d738-143">En el ejemplo de código siguiente se muestra cómo se puede interpolar entre Q1 y T2.</span><span class="sxs-lookup"><span data-stu-id="4d738-143">The following code example demonstrates how you can interpolate between Q1 and Q2.</span></span>


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
> -   <span data-ttu-id="4d738-144">C es +/-T2 según el resultado de la función.</span><span class="sxs-lookup"><span data-stu-id="4d738-144">C is +/- Q2 depending on the result of the function.</span></span>
> -   <span data-ttu-id="4d738-145">QT es el resultado de la función.</span><span class="sxs-lookup"><span data-stu-id="4d738-145">Qt is the result of the function.</span></span>
>
> <span data-ttu-id="4d738-146">El resultado es un giro de 45 grados alrededor del eje z para Time = 0,5.</span><span class="sxs-lookup"><span data-stu-id="4d738-146">The result is a rotation of 45 degrees around the z-axis for time = 0.5.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4d738-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d738-147">Requirements</span></span>



| <span data-ttu-id="4d738-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d738-148">Requirement</span></span> | <span data-ttu-id="4d738-149">Value</span><span class="sxs-lookup"><span data-stu-id="4d738-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d738-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4d738-150">Header</span></span><br/>  | <dl> <span data-ttu-id="4d738-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d738-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4d738-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d738-152">Library</span></span><br/> | <dl> <span data-ttu-id="4d738-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d738-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4d738-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d738-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d738-155">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="4d738-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4d738-156">**D3DXQuaternionSquad**</span><span class="sxs-lookup"><span data-stu-id="4d738-156">**D3DXQuaternionSquad**</span></span>](d3dxquaternionsquad.md)
</dt> </dl>

 

 




