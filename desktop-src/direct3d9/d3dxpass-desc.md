---
description: Describe un paso para un objeto de efecto.
ms.assetid: 398e6120-7bdf-425b-a8aa-cc0eb74ffa3a
title: D3DXPASS_DESC estructura (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPASS_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a147f737057a5b2cff6ea436d9d2e47920a67a4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362429"
---
# <a name="d3dxpass_desc-structure"></a><span data-ttu-id="dfc53-103">D3DXPASS \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="dfc53-103">D3DXPASS\_DESC structure</span></span>

<span data-ttu-id="dfc53-104">Describe un paso para un objeto de efecto.</span><span class="sxs-lookup"><span data-stu-id="dfc53-104">Describes a pass for an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfc53-105">Syntax</span></span>


```C++
typedef struct D3DXPASS_DESC {
  LPCSTR      Name;
  UINT        Annotations;
  const DWORD *pVertexShaderFunction;
  const DWORD *pPixelShaderFunction;
} D3DXPASS_DESC, *LPD3DXPASS_DESC;
```



## <a name="members"></a><span data-ttu-id="dfc53-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="dfc53-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dfc53-107">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="dfc53-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="dfc53-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfc53-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dfc53-109">Valor de cadena usado para el paso.</span><span class="sxs-lookup"><span data-stu-id="dfc53-109">String value used for the pass.</span></span>

</dd> <dt>

<span data-ttu-id="dfc53-110">**Anotaciones**</span><span class="sxs-lookup"><span data-stu-id="dfc53-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="dfc53-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfc53-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dfc53-112">Las anotaciones son datos específicos del usuario que se pueden adjuntar a cualquier técnica, paso o parámetro.</span><span class="sxs-lookup"><span data-stu-id="dfc53-112">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="dfc53-113">Consulte [Agregar información a los parámetros de efectos con \_ anotaciones](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="dfc53-113">See [Add Information to Effect Parameters with\_Annotations](using-an-effect.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfc53-114">**pVertexShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="dfc53-114">**pVertexShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="dfc53-115">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dfc53-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="dfc53-116">Puntero a la función de sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="dfc53-116">Pointer to the vertex shader function.</span></span> <span data-ttu-id="dfc53-117">Si se crea un efecto con [D3DXFX \_ no \_ clonable](d3dxfx.md), esta estructura devolverá un puntero **nulo** cuando lo llame [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="dfc53-117">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfc53-118">**pPixelShaderFunction**</span><span class="sxs-lookup"><span data-stu-id="dfc53-118">**pPixelShaderFunction**</span></span>
</dt> <dd>

<span data-ttu-id="dfc53-119">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dfc53-119">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="dfc53-120">Puntero a la función de sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="dfc53-120">Pointer to the pixel shader function.</span></span> <span data-ttu-id="dfc53-121">Si se crea un efecto con [D3DXFX \_ no \_ clonable](d3dxfx.md), esta estructura devolverá un puntero **nulo** cuando lo llame [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span><span class="sxs-lookup"><span data-stu-id="dfc53-121">If an effect is created with [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md), this structure will return a **NULL** pointer when called by [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dfc53-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfc53-122">Requirements</span></span>



| <span data-ttu-id="dfc53-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfc53-123">Requirement</span></span> | <span data-ttu-id="dfc53-124">Value</span><span class="sxs-lookup"><span data-stu-id="dfc53-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc53-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfc53-125">Header</span></span><br/> | <dl> <span data-ttu-id="dfc53-126"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfc53-126"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfc53-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="dfc53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc53-128">Estructuras de efectos</span><span class="sxs-lookup"><span data-stu-id="dfc53-128">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="dfc53-129">**GetPassDesc**</span><span class="sxs-lookup"><span data-stu-id="dfc53-129">**GetPassDesc**</span></span>](id3dxbaseeffect--getpassdesc.md)
</dt> </dl>

 

 
