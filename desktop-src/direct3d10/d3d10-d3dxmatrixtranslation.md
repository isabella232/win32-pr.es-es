---
description: Cree una matriz de traslación.
ms.assetid: a3565a06-22af-4ded-8835-da4c7ae81805
title: Función D3DXMatrixTranslation (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7abf55e5b51091de5d823ba837cdc8ad51e3940b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721525"
---
# <a name="d3dxmatrixtranslation-function-d3dx10mathh"></a><span data-ttu-id="a8600-103">Función D3DXMatrixTranslation (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="a8600-103">D3DXMatrixTranslation function (D3DX10Math.h)</span></span>

<span data-ttu-id="a8600-104">Cree una matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="a8600-104">Create a translation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8600-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8600-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a><span data-ttu-id="a8600-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8600-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8600-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a8600-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8600-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8600-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a8600-109">Matriz que se convertirá en una matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="a8600-109">The matrix that will become a translation matrix.</span></span> <span data-ttu-id="a8600-110">Vea [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="a8600-110">See [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8600-111">*x* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a8600-111">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8600-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8600-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8600-113">Componente x de la traducción.</span><span class="sxs-lookup"><span data-stu-id="a8600-113">The x-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="a8600-114">*y* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a8600-114">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8600-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8600-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8600-116">Componente y de la traducción.</span><span class="sxs-lookup"><span data-stu-id="a8600-116">The y-component of the translation.</span></span>

</dd> <dt>

<span data-ttu-id="a8600-117">*z* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="a8600-117">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8600-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8600-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a8600-119">Componente z de la traducción.</span><span class="sxs-lookup"><span data-stu-id="a8600-119">The z-component of the translation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8600-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8600-120">Return value</span></span>

<span data-ttu-id="a8600-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="a8600-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="a8600-122">Matriz de traslación.</span><span class="sxs-lookup"><span data-stu-id="a8600-122">The translation matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8600-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8600-123">Requirements</span></span>



| <span data-ttu-id="a8600-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8600-124">Requirement</span></span> | <span data-ttu-id="a8600-125">Value</span><span class="sxs-lookup"><span data-stu-id="a8600-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8600-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8600-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a8600-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8600-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="a8600-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8600-128">Library</span></span><br/> | <dl> <span data-ttu-id="a8600-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8600-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a8600-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8600-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8600-131">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="a8600-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
