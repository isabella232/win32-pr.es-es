---
description: 'Estructura D3DXFLOAT16 (D3dx9math.h): describe un vector de punto flotante de 16 bits.'
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Estructura D3DXFLOAT16 (D3dx9math.h)
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
ms.openlocfilehash: dc878575de4338a2a399f329362d79ff2e7654f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094273"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="9344e-103">Estructura D3DXFLOAT16 (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="9344e-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="9344e-104">Describe un vector de punto flotante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9344e-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="9344e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9344e-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="9344e-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="9344e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9344e-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="9344e-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="9344e-108">Tipo: **[ **WORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9344e-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9344e-109">Datos de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9344e-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9344e-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9344e-110">Remarks</span></span>

<span data-ttu-id="9344e-111">Los programadores de C++ pueden aprovechar la sobrecarga de operadores y la conversión de tipos con las extensiones [**D3DXFLOAT16**](d3dxfloat16-extensions.md), que implementan constructores sobrecargados y operadores de asignación, unario y binario (incluida la igualdad).</span><span class="sxs-lookup"><span data-stu-id="9344e-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="9344e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9344e-112">Requirements</span></span>



| <span data-ttu-id="9344e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9344e-113">Requirement</span></span> | <span data-ttu-id="9344e-114">Value</span><span class="sxs-lookup"><span data-stu-id="9344e-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9344e-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9344e-115">Header</span></span><br/> | <dl> <span data-ttu-id="9344e-116"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="9344e-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9344e-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9344e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9344e-118">Estructuras D3DX</span><span class="sxs-lookup"><span data-stu-id="9344e-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
