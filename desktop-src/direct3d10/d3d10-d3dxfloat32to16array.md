---
description: 'Función D3DXFloat32To16Array (D3DX10Math.h): convierte una matriz de flotantes de 32 bits en flotantes de 16 bits.'
ms.assetid: 2114cf25-cc83-4c4a-9db5-ecc0f8ff1e85
title: Función D3DXFloat32To16Array (D3DX10Math.h)
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
ms.openlocfilehash: 600cc2cd333aaea08b38c252c206c1a74c1ca059
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103523"
---
# <a name="d3dxfloat32to16array-function-d3dx10mathh"></a><span data-ttu-id="e4bcd-103">Función D3DXFloat32To16Array (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="e4bcd-103">D3DXFloat32To16Array function (D3DX10Math.h)</span></span>

<span data-ttu-id="e4bcd-104">Convierte una matriz de flotantes de 32 bits en flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e4bcd-104">Converts an array of 32-bit floats to 16-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4bcd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e4bcd-105">Syntax</span></span>


```C++
D3DXFLOAT16* D3DXFloat32To16Array(
  _In_       D3DXFLOAT16 *pOut,
  _In_ const FLOAT       *pIn,
  _In_       UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="e4bcd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e4bcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4bcd-107">*pOut* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e4bcd-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4bcd-108">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4bcd-108">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="e4bcd-109">Puntero a la matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e4bcd-109">Pointer to the array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="e4bcd-110">*pIn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="e4bcd-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4bcd-111">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4bcd-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4bcd-112">Puntero a una matriz de flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e4bcd-112">Pointer to an array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="e4bcd-113">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="e4bcd-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4bcd-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4bcd-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4bcd-115">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="e4bcd-115">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4bcd-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e4bcd-116">Return value</span></span>

<span data-ttu-id="e4bcd-117">Tipo: **[ **D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4bcd-117">Type: **[**D3DXFLOAT16**](../direct3d9/d3dxfloat16.md)\***</span></span>

<span data-ttu-id="e4bcd-118">Puntero a una matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e4bcd-118">Pointer to an array of 16-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4bcd-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4bcd-119">Requirements</span></span>



| <span data-ttu-id="e4bcd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4bcd-120">Requirement</span></span> | <span data-ttu-id="e4bcd-121">Value</span><span class="sxs-lookup"><span data-stu-id="e4bcd-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4bcd-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4bcd-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e4bcd-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e4bcd-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4bcd-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4bcd-124">Library</span></span><br/> | <dl> <span data-ttu-id="e4bcd-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4bcd-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4bcd-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4bcd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4bcd-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="e4bcd-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
