---
description: Devuelve el factor determinante de una matriz.
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: Función D3DXMatrixDeterminant (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 53d90d70e75ba4bb92dbed3abe7ee06eae1ae6e4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362441"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="49ea0-103">Función D3DXMatrixDeterminant (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="49ea0-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="49ea0-104">Devuelve el factor determinante de una matriz.</span><span class="sxs-lookup"><span data-stu-id="49ea0-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ea0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49ea0-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="49ea0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49ea0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ea0-107">*p. m* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49ea0-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea0-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="49ea0-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="49ea0-109">Puntero a la estructura de [**D3DXMATRIX**](d3dxmatrix.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="49ea0-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ea0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49ea0-110">Return value</span></span>

<span data-ttu-id="49ea0-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49ea0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49ea0-112">Devuelve el factor determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="49ea0-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ea0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ea0-113">Requirements</span></span>



| <span data-ttu-id="49ea0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ea0-114">Requirement</span></span> | <span data-ttu-id="49ea0-115">Value</span><span class="sxs-lookup"><span data-stu-id="49ea0-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49ea0-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49ea0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="49ea0-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="49ea0-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="49ea0-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49ea0-118">Library</span></span><br/> | <dl> <span data-ttu-id="49ea0-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49ea0-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="49ea0-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="49ea0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ea0-121">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="49ea0-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
