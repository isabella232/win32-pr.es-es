---
description: 'Función D3DXMatrixDeterminant (D3dx9math.h): devuelve el determinante de una matriz.'
ms.assetid: 711ba616-4c90-41d1-b9d5-0893b3e47284
title: Función D3DXMatrixDeterminant (D3dx9math.h)
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
ms.openlocfilehash: 8d54651e11f1b3de02803d9ea123ca7eff24d7a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098173"
---
# <a name="d3dxmatrixdeterminant-function-d3dx9mathh"></a><span data-ttu-id="c76ae-103">Función D3DXMatrixDeterminant (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="c76ae-103">D3DXMatrixDeterminant function (D3dx9math.h)</span></span>

<span data-ttu-id="c76ae-104">Devuelve el determinante de una matriz.</span><span class="sxs-lookup"><span data-stu-id="c76ae-104">Returns the determinant of a matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76ae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c76ae-105">Syntax</span></span>


```C++
FLOAT D3DXMatrixDeterminant(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c76ae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c76ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c76ae-107">*pM* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="c76ae-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c76ae-108">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c76ae-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c76ae-109">Puntero a la estructura [**D3DXMATRIX de**](d3dxmatrix.md) origen.</span><span class="sxs-lookup"><span data-stu-id="c76ae-109">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c76ae-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c76ae-110">Return value</span></span>

<span data-ttu-id="c76ae-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c76ae-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c76ae-112">Devuelve el determinante de la matriz.</span><span class="sxs-lookup"><span data-stu-id="c76ae-112">Returns the determinant of the matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c76ae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c76ae-113">Requirements</span></span>



| <span data-ttu-id="c76ae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c76ae-114">Requirement</span></span> | <span data-ttu-id="c76ae-115">Value</span><span class="sxs-lookup"><span data-stu-id="c76ae-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c76ae-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c76ae-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c76ae-117"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="c76ae-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="c76ae-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c76ae-118">Library</span></span><br/> | <dl> <span data-ttu-id="c76ae-119"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c76ae-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c76ae-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c76ae-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76ae-121">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="c76ae-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
