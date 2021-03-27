---
title: D3DX11_TECHNIQUE_DESC estructura (D3dx11effect. h)
description: Describe una técnica de efecto.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821263"
---
# <a name="d3dx11_technique_desc-structure"></a><span data-ttu-id="0bfa7-104">D3DX11 \_ técnica \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="0bfa7-104">D3DX11\_TECHNIQUE\_DESC structure</span></span>

<span data-ttu-id="0bfa7-105">Describe una técnica de efecto.</span><span class="sxs-lookup"><span data-stu-id="0bfa7-105">Describes an effect technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bfa7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0bfa7-106">Syntax</span></span>


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a><span data-ttu-id="0bfa7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0bfa7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0bfa7-108">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0bfa7-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="0bfa7-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0bfa7-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0bfa7-110">Nombre de esta técnica (NULL si no es anónima).</span><span class="sxs-lookup"><span data-stu-id="0bfa7-110">Name of this technique (NULL if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="0bfa7-111">**Paso**</span><span class="sxs-lookup"><span data-stu-id="0bfa7-111">**Passes**</span></span>
</dt> <dd>

<span data-ttu-id="0bfa7-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0bfa7-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0bfa7-113">Número de pasos contenidos en la técnica.</span><span class="sxs-lookup"><span data-stu-id="0bfa7-113">Number of passes contained in the technique.</span></span>

</dd> <dt>

<span data-ttu-id="0bfa7-114">**Anotaciones**</span><span class="sxs-lookup"><span data-stu-id="0bfa7-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="0bfa7-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="0bfa7-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="0bfa7-116">Número de anotaciones en esta técnica.</span><span class="sxs-lookup"><span data-stu-id="0bfa7-116">Number of annotations on this technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0bfa7-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0bfa7-117">Remarks</span></span>

<span data-ttu-id="0bfa7-118">D3DX11 \_ técnica \_ desc se usa con [**ID3DX11EffectTechnique:: GetDesc**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="0bfa7-118">D3DX11\_TECHNIQUE\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bfa7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bfa7-119">Requirements</span></span>



| <span data-ttu-id="0bfa7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bfa7-120">Requirement</span></span> | <span data-ttu-id="0bfa7-121">Value</span><span class="sxs-lookup"><span data-stu-id="0bfa7-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bfa7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0bfa7-122">Header</span></span><br/> | <dl> <span data-ttu-id="0bfa7-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bfa7-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bfa7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="0bfa7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bfa7-125">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="0bfa7-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

