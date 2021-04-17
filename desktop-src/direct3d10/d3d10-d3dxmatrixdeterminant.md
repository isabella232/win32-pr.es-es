---
description: Devuelve el factor determinante de una matriz.
ms.assetid: b0155c91-1554-42ef-b219-c6cdd2a905b5
title: Función D3DXMatrixDeterminant (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDeterminant
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 11b1092427b12c33d8c34c9f1bbd5e09cf1ccf2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718443"
---
# <a name="d3dxmatrixdeterminant-function-d3dx10mathh"></a><span data-ttu-id="50aed-103">Función D3DXMatrixDeterminant (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="50aed-103">D3DXMatrixDeterminant function (D3DX10Math.h)</span></span>

<span data-ttu-id="50aed-104">Devuelve el factor determinante de una matriz.</span><span class="sxs-lookup"><span data-stu-id="50aed-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="50aed-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50aed-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="50aed-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50aed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50aed-107">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50aed-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50aed-108">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="50aed-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="50aed-109">Puntero a la estructura de D3DXMATRIX de origen.</span><span class="sxs-lookup"><span data-stu-id="50aed-109">Pointer to the source D3DXMATRIX structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50aed-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50aed-110">Return value</span></span>

<span data-ttu-id="50aed-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50aed-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50aed-112">Devuelve el factor determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="50aed-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="50aed-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50aed-113">Requirements</span></span>



| <span data-ttu-id="50aed-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="50aed-114">Requirement</span></span> | <span data-ttu-id="50aed-115">Value</span><span class="sxs-lookup"><span data-stu-id="50aed-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50aed-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50aed-116">Header</span></span><br/>  | <dl> <span data-ttu-id="50aed-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="50aed-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="50aed-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50aed-118">Library</span></span><br/> | <dl> <span data-ttu-id="50aed-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50aed-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="50aed-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="50aed-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50aed-121">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="50aed-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
