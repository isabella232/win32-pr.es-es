---
description: 'Función D3DXFloat16To32Array (D3dx9math.h): convierte una matriz de flotantes de 16 bits en flotantes de 32 bits.'
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Función D3DXFloat16To32Array (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 171b148b112cf2064d0d9a3f89451ab0fc8c2d75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107603"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="02e2f-103">Función D3DXFloat16To32Array (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="02e2f-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="02e2f-104">Convierte una matriz de flotantes de 16 bits en flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="02e2f-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e2f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02e2f-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="02e2f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02e2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e2f-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="02e2f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="02e2f-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="02e2f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="02e2f-109">Puntero a la matriz de flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="02e2f-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="02e2f-110">*pIn* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="02e2f-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e2f-111">Tipo: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="02e2f-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="02e2f-112">Puntero a una matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="02e2f-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="02e2f-113">*n* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="02e2f-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e2f-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="02e2f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="02e2f-115">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="02e2f-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e2f-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02e2f-116">Return value</span></span>

<span data-ttu-id="02e2f-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="02e2f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="02e2f-118">Puntero a una matriz de flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="02e2f-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e2f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02e2f-119">Requirements</span></span>



| <span data-ttu-id="02e2f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e2f-120">Requirement</span></span> | <span data-ttu-id="02e2f-121">Value</span><span class="sxs-lookup"><span data-stu-id="02e2f-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02e2f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02e2f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="02e2f-123"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="02e2f-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="02e2f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02e2f-124">Library</span></span><br/> | <dl> <span data-ttu-id="02e2f-125"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="02e2f-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02e2f-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="02e2f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e2f-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="02e2f-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
