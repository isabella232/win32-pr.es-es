---
description: Determina el producto de punto de dos vectores 4D.
ms.assetid: 565dede8-6cc8-4313-9480-2f252cac94f2
title: Función D3DXVec4Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0ef075a768fe9b70a38a4bc3d88b094359bd546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424416"
---
# <a name="d3dxvec4dot-function"></a><span data-ttu-id="68fae-103">D3DXVec4Dot función)</span><span class="sxs-lookup"><span data-stu-id="68fae-103">D3DXVec4Dot function</span></span>

<span data-ttu-id="68fae-104">Determina el producto de punto de dos vectores 4D.</span><span class="sxs-lookup"><span data-stu-id="68fae-104">Determines the dot product of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="68fae-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68fae-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Dot(
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="68fae-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68fae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68fae-107">*pV1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68fae-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68fae-108">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="68fae-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="68fae-109">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="68fae-109">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="68fae-110">*pV2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68fae-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68fae-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="68fae-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="68fae-112">Puntero a una estructura de [**D3DXVECTOR4**](d3dxvector4.md) de origen.</span><span class="sxs-lookup"><span data-stu-id="68fae-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68fae-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68fae-113">Return value</span></span>

<span data-ttu-id="68fae-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68fae-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68fae-115">Producto escalar.</span><span class="sxs-lookup"><span data-stu-id="68fae-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="68fae-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68fae-116">Requirements</span></span>



| <span data-ttu-id="68fae-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="68fae-117">Requirement</span></span> | <span data-ttu-id="68fae-118">Value</span><span class="sxs-lookup"><span data-stu-id="68fae-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68fae-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68fae-119">Header</span></span><br/>  | <dl> <span data-ttu-id="68fae-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="68fae-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="68fae-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68fae-121">Library</span></span><br/> | <dl> <span data-ttu-id="68fae-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68fae-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68fae-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="68fae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68fae-124">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="68fae-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="68fae-125">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="68fae-125">**D3DXVec4Cross**</span></span>](d3dxvec4cross.md)
</dt> </dl>

 

 
