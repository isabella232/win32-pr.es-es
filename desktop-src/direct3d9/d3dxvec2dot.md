---
description: Determina el producto de punto de dos vectores 2D.
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: Función D3DXVec2Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 79b65127c415695b3df9f927b6edff8fcdd5c58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707818"
---
# <a name="d3dxvec2dot-function"></a><span data-ttu-id="bb138-103">D3DXVec2Dot función)</span><span class="sxs-lookup"><span data-stu-id="bb138-103">D3DXVec2Dot function</span></span>

<span data-ttu-id="bb138-104">Determina el producto de punto de dos vectores 2D.</span><span class="sxs-lookup"><span data-stu-id="bb138-104">Determines the dot product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb138-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb138-105">Syntax</span></span>


```C++
FLOAT D3DXVec2Dot(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="bb138-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb138-107">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb138-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb138-108">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb138-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="bb138-109">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="bb138-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb138-110">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bb138-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb138-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bb138-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="bb138-112">Puntero a una estructura de [**D3DXVECTOR2**](d3dxvector2.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="bb138-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb138-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb138-113">Return value</span></span>

<span data-ttu-id="bb138-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb138-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb138-115">Producto escalar.</span><span class="sxs-lookup"><span data-stu-id="bb138-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb138-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb138-116">Requirements</span></span>



| <span data-ttu-id="bb138-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb138-117">Requirement</span></span> | <span data-ttu-id="bb138-118">Value</span><span class="sxs-lookup"><span data-stu-id="bb138-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb138-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb138-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bb138-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb138-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="bb138-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb138-121">Library</span></span><br/> | <dl> <span data-ttu-id="bb138-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb138-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb138-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb138-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb138-124">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="bb138-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="bb138-125">**D3DXVec2CCW**</span><span class="sxs-lookup"><span data-stu-id="bb138-125">**D3DXVec2CCW**</span></span>](d3dxvec2ccw.md)
</dt> </dl>

 

 
