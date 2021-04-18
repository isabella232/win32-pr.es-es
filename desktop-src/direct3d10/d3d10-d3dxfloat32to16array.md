---
description: Convierte una matriz de tipos Float de 32 bits en flotantes de 16 bits.
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Función D3DXFloat32To16Array (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat32To16Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a4c116212be0ffa71ee35939d0a30a40cbb773b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698361"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="f8cbb-103">Función D3DXFloat32To16Array (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f8cbb-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="f8cbb-104">Convierte una matriz de tipos Float de 32 bits en flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8cbb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8cbb-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="f8cbb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8cbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8cbb-107">*pOut* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8cbb-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8cbb-108">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8cbb-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="f8cbb-109">Puntero a la matriz de los flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="f8cbb-110">*código pIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f8cbb-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8cbb-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f8cbb-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f8cbb-112">Puntero a una matriz de floats de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="f8cbb-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8cbb-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8cbb-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8cbb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8cbb-115">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8cbb-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8cbb-116">Return value</span></span>

<span data-ttu-id="f8cbb-117">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="f8cbb-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="f8cbb-118">Puntero a una matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="f8cbb-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8cbb-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8cbb-119">Requirements</span></span>



| <span data-ttu-id="f8cbb-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8cbb-120">Requirement</span></span> | <span data-ttu-id="f8cbb-121">Value</span><span class="sxs-lookup"><span data-stu-id="f8cbb-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cbb-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8cbb-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f8cbb-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8cbb-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f8cbb-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8cbb-124">Library</span></span><br/> | <dl> <span data-ttu-id="f8cbb-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8cbb-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8cbb-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8cbb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8cbb-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="f8cbb-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
