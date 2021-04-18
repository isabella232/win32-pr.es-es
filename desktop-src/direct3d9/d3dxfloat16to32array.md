---
description: Convierte una matriz de tipos flotantes de 16 bits en flotantes de 32 bits.
ms.assetid: cabb2888-76e4-403b-99ab-f7d62478bf43
title: Función D3DXFloat16To32Array (D3dx9math. h)
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
ms.openlocfilehash: 6760ce36341883c26030df91d3d46b5b21fdb012
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721459"
---
# <a name="d3dxfloat16to32array-function-d3dx9mathh"></a><span data-ttu-id="85003-103">Función D3DXFloat16To32Array (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="85003-103">D3DXFloat16To32Array function (D3dx9math.h)</span></span>

<span data-ttu-id="85003-104">Convierte una matriz de tipos flotantes de 16 bits en flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="85003-104">Converts an array of 16-bit floats to 32-bit floats.</span></span>

## <a name="syntax"></a><span data-ttu-id="85003-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85003-105">Syntax</span></span>


```C++
FLOAT* D3DXFloat16To32Array(
  _Inout_       FLOAT       *pOut,
  _In_    const D3DXFLOAT16 *pIn,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="85003-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85003-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85003-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="85003-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85003-108">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="85003-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85003-109">Puntero a la matriz de los flotantes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="85003-109">Pointer to the array of 32-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="85003-110">*código pIn* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85003-110">*pIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85003-111">Tipo: **const [**D3DXFLOAT16**](d3dxfloat16.md) \***</span><span class="sxs-lookup"><span data-stu-id="85003-111">Type: **const [**D3DXFLOAT16**](d3dxfloat16.md)\***</span></span>

<span data-ttu-id="85003-112">Puntero a una matriz de flotantes de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="85003-112">Pointer to an array of 16-bit floats.</span></span>

</dd> <dt>

<span data-ttu-id="85003-113">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85003-113">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85003-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="85003-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="85003-115">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="85003-115">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85003-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85003-116">Return value</span></span>

<span data-ttu-id="85003-117">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="85003-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="85003-118">Puntero a una matriz de floats de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="85003-118">Pointer to an array of 32-bit floats.</span></span>

## <a name="requirements"></a><span data-ttu-id="85003-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85003-119">Requirements</span></span>



| <span data-ttu-id="85003-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85003-120">Requirement</span></span> | <span data-ttu-id="85003-121">Value</span><span class="sxs-lookup"><span data-stu-id="85003-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="85003-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85003-122">Header</span></span><br/>  | <dl> <span data-ttu-id="85003-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="85003-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="85003-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85003-124">Library</span></span><br/> | <dl> <span data-ttu-id="85003-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85003-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="85003-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="85003-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85003-127">Funciones matemáticas</span><span class="sxs-lookup"><span data-stu-id="85003-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
