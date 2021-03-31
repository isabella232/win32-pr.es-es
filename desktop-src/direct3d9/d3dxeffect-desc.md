---
description: Describe un objeto de efecto.
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: D3DXEFFECT_DESC estructura (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: c8e7a3a2adf19514e2e4d1c6f61dbea888ce033d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821095"
---
# <a name="d3dxeffect_desc-structure"></a><span data-ttu-id="c2e8d-103">D3DXEFFECT \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="c2e8d-103">D3DXEFFECT\_DESC structure</span></span>

<span data-ttu-id="c2e8d-104">Describe un objeto de efecto.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-104">Describes an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2e8d-105">Syntax</span></span>


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="c2e8d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c2e8d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2e8d-107">**Creador**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="c2e8d-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c2e8d-109">Cadena que contiene el nombre del creador del efecto.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-109">String that contains the name of the effect creator.</span></span>

</dd> <dt>

<span data-ttu-id="c2e8d-110">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-110">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="c2e8d-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c2e8d-112">Número de parámetros utilizados para el efecto.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-112">Number of parameters used for effect.</span></span>

</dd> <dt>

<span data-ttu-id="c2e8d-113">**Descrita**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-113">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="c2e8d-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c2e8d-115">Número de técnicas que pueden representar el efecto.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-115">Number of techniques that can render the effect.</span></span>

</dd> <dt>

<span data-ttu-id="c2e8d-116">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-116">**Functions**</span></span>
</dt> <dd>

<span data-ttu-id="c2e8d-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2e8d-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c2e8d-118">Número de funciones que pueden representar el efecto.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-118">Number of functions that can render the effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2e8d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2e8d-119">Remarks</span></span>

<span data-ttu-id="c2e8d-120">Un objeto Effect puede contener varias técnicas de representación y parámetros para el mismo efecto.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-120">An effect object can contain multiple rendering techniques and parameters for the same effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e8d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e8d-121">Requirements</span></span>



| <span data-ttu-id="c2e8d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e8d-122">Requirement</span></span> | <span data-ttu-id="c2e8d-123">Value</span><span class="sxs-lookup"><span data-stu-id="c2e8d-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e8d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c2e8d-124">Header</span></span><br/> | <dl> <span data-ttu-id="c2e8d-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e8d-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e8d-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2e8d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e8d-127">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="c2e8d-127">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
