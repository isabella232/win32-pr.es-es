---
description: Crea una matriz de identidad.
ms.assetid: 0dd6d4fb-284c-4d01-9a85-63aa08e71723
title: Función D3DXMatrixIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 10dffa12a379754006ca65d1239be96632a68b93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003764"
---
# <a name="d3dxmatrixidentity-function"></a><span data-ttu-id="780da-103">D3DXMatrixIdentity función)</span><span class="sxs-lookup"><span data-stu-id="780da-103">D3DXMatrixIdentity function</span></span>

<span data-ttu-id="780da-104">Crea una matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="780da-104">Creates an identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="780da-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="780da-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixIdentity(
  _Inout_ D3DXMATRIX *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="780da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="780da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780da-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="780da-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="780da-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="780da-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="780da-109">Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="780da-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780da-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="780da-110">Return value</span></span>

<span data-ttu-id="780da-111">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="780da-111">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="780da-112">Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que es la matriz de identidad.</span><span class="sxs-lookup"><span data-stu-id="780da-112">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is the identity matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="780da-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="780da-113">Remarks</span></span>

<span data-ttu-id="780da-114">La matriz de identidad es una matriz en la que todos los coeficientes son 0 excepto los \[ \] \[ coeficientes 1, 1 2, 2 \] \[ 3, 3 \] \[ 4, 4 \] , que se establecen en 1.</span><span class="sxs-lookup"><span data-stu-id="780da-114">The identity matrix is a matrix in which all coefficients are 0 except the \[1,1\]\[2,2\]\[3,3\]\[4,4\] coefficients, which are set to 1.</span></span> <span data-ttu-id="780da-115">La matriz de identidad es especial, ya que, cuando se aplica a los vértices, no cambian.</span><span class="sxs-lookup"><span data-stu-id="780da-115">The identity matrix is special in that when it is applied to vertices, they are unchanged.</span></span> <span data-ttu-id="780da-116">La matriz de identidad se usa como punto de partida para las matrices que modificarán los valores de los vértices para crear rotaciones, traducciones y cualquier otra transformación que pueda representarse mediante una matriz de 4 x4.</span><span class="sxs-lookup"><span data-stu-id="780da-116">The identity matrix is used as the starting point for matrices that will modify vertex values to create rotations, translations, and any other transformations that can be represented by a 4 x4 matrix.</span></span>

<span data-ttu-id="780da-117">El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="780da-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="780da-118">De esta manera, la función **D3DXMatrixIdentity** se puede usar como parámetro de otra función.</span><span class="sxs-lookup"><span data-stu-id="780da-118">In this way, the **D3DXMatrixIdentity** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="780da-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="780da-119">Requirements</span></span>



| <span data-ttu-id="780da-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="780da-120">Requirement</span></span> | <span data-ttu-id="780da-121">Value</span><span class="sxs-lookup"><span data-stu-id="780da-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="780da-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="780da-122">Header</span></span><br/>  | <dl> <span data-ttu-id="780da-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="780da-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="780da-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="780da-124">Library</span></span><br/> | <dl> <span data-ttu-id="780da-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="780da-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="780da-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="780da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="780da-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="780da-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="780da-128">**D3DXMatrixIsIdentity**</span><span class="sxs-lookup"><span data-stu-id="780da-128">**D3DXMatrixIsIdentity**</span></span>](d3dxmatrixisidentity.md)
</dt> </dl>

 

 




