---
description: 'Función D3DXFloat16To32Array (D3DX10Math.h): convierte una matriz de flotantes de 16 bits en flotantes de 32 bits.'
ms.assetid: cf07a21d-9ea3-4fbe-ab8f-564e2bbb8d60
title: Función D3DXFloat16To32Array (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFloat16To32Array
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ae624fb05ce10447bd3b9082e171dc01224baaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113293"
---
# <a name="d3dxfloat16to32array-function-d3dx10mathh"></a><span data-ttu-id="35443-103">Función D3DXFloat16To32Array (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="35443-103">D3DXFloat16To32Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="35443-104">Convierte una matriz de flotantes de 16 bits en flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="35443-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="35443-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35443-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _In_       FLOAT       *pOut,
  _In_ const D3DXFLOAT16 *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="35443-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35443-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35443-107">*pOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="35443-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35443-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="35443-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="35443-109">Puntero a la matriz de flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="35443-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="35443-110">*pIn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="35443-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35443-111">Tipo: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="35443-111">Type: **const [**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="35443-112">Puntero a una matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="35443-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="35443-113">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="35443-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35443-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="35443-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="35443-115">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="35443-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35443-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35443-116">Return value</span></span>

<span data-ttu-id="35443-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="35443-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="35443-118">Puntero a una matriz de flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="35443-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="35443-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35443-119">Requirements</span></span>



| <span data-ttu-id="35443-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="35443-120">Requirement</span></span> | <span data-ttu-id="35443-121">Value</span><span class="sxs-lookup"><span data-stu-id="35443-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35443-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35443-122">Header</span></span><br/>  | <dl> <span data-ttu-id="35443-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="35443-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="35443-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35443-124">Library</span></span><br/> | <dl> <span data-ttu-id="35443-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="35443-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="35443-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="35443-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35443-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="35443-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
