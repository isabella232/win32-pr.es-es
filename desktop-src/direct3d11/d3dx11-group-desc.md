---
title: D3DX11_GROUP_DESC estructura (D3dx11effect. h)
description: Describe un grupo de efectos.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083808"
---
# <a name="d3dx11_group_desc-structure"></a><span data-ttu-id="38da9-104">D3DX11 \_ Group \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="38da9-104">D3DX11\_GROUP\_DESC structure</span></span>

<span data-ttu-id="38da9-105">Describe un grupo de efectos.</span><span class="sxs-lookup"><span data-stu-id="38da9-105">Describes an effect group.</span></span>

## <a name="syntax"></a><span data-ttu-id="38da9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38da9-106">Syntax</span></span>


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a><span data-ttu-id="38da9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="38da9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="38da9-108">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="38da9-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="38da9-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="38da9-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="38da9-110">Nombre de este grupo (solo **null si es** global).</span><span class="sxs-lookup"><span data-stu-id="38da9-110">Name of this group (only **NULL** if global).</span></span>

</dd> <dt>

<span data-ttu-id="38da9-111">**Descrita**</span><span class="sxs-lookup"><span data-stu-id="38da9-111">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="38da9-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="38da9-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="38da9-113">Número de técnicas contenidas en el grupo.</span><span class="sxs-lookup"><span data-stu-id="38da9-113">Number of techniques contained in group.</span></span>

</dd> <dt>

<span data-ttu-id="38da9-114">**Anotaciones**</span><span class="sxs-lookup"><span data-stu-id="38da9-114">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="38da9-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="38da9-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="38da9-116">Número de anotaciones de este grupo.</span><span class="sxs-lookup"><span data-stu-id="38da9-116">Number of annotations on this group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38da9-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="38da9-117">Remarks</span></span>

<span data-ttu-id="38da9-118">D3DX11 \_ grupo \_ desc se usa con [**ID3DX11EffectTechnique:: GetDesc**](id3dx11effecttechnique-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="38da9-118">D3DX11\_GROUP\_DESC is used with [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38da9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38da9-119">Requirements</span></span>



| <span data-ttu-id="38da9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="38da9-120">Requirement</span></span> | <span data-ttu-id="38da9-121">Value</span><span class="sxs-lookup"><span data-stu-id="38da9-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="38da9-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38da9-122">Header</span></span><br/> | <dl> <span data-ttu-id="38da9-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="38da9-123"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38da9-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="38da9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38da9-125">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="38da9-125">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

