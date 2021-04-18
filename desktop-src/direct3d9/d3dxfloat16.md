---
description: Describe un vector de punto flotante de 16 bits.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Estructura D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 4b469c770b811ed11ec21b21d2b449df1fd75b1c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721460"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="a8274-103">Estructura D3DXFLOAT16 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="a8274-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="a8274-104">Describe un vector de punto flotante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a8274-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8274-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8274-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="a8274-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8274-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8274-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a8274-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="a8274-108">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a8274-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a8274-109">Datos de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a8274-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8274-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8274-110">Remarks</span></span>

<span data-ttu-id="a8274-111">Los programadores de C++ pueden aprovechar las ventajas de la sobrecarga de operadores y la conversión de tipos con las [**extensiones de D3DXFLOAT16**](d3dxfloat16-extensions.md), que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="a8274-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8274-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8274-112">Requirements</span></span>



| <span data-ttu-id="a8274-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8274-113">Requirement</span></span> | <span data-ttu-id="a8274-114">Value</span><span class="sxs-lookup"><span data-stu-id="a8274-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8274-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8274-115">Header</span></span><br/> | <dl> <span data-ttu-id="a8274-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8274-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8274-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8274-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8274-118">Estructuras de D3DX</span><span class="sxs-lookup"><span data-stu-id="a8274-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
