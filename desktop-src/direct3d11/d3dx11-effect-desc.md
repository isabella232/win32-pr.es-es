---
title: D3DX11_EFFECT_DESC estructura (D3dx11effect. h)
description: Describe un efecto.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987229"
---
# <a name="d3dx11_effect_desc-structure"></a><span data-ttu-id="09059-104">D3DX11 \_ Effect ( \_ estructura de DESC)</span><span class="sxs-lookup"><span data-stu-id="09059-104">D3DX11\_EFFECT\_DESC structure</span></span>

<span data-ttu-id="09059-105">Describe un efecto.</span><span class="sxs-lookup"><span data-stu-id="09059-105">Describes an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="09059-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09059-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a><span data-ttu-id="09059-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="09059-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="09059-108">**ConstantBuffers**</span><span class="sxs-lookup"><span data-stu-id="09059-108">**ConstantBuffers**</span></span>
</dt> <dd>

<span data-ttu-id="09059-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09059-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="09059-110">Número de búferes de constantes en este efecto.</span><span class="sxs-lookup"><span data-stu-id="09059-110">Number of constant buffers in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="09059-111">**GlobalVariables**</span><span class="sxs-lookup"><span data-stu-id="09059-111">**GlobalVariables**</span></span>
</dt> <dd>

<span data-ttu-id="09059-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09059-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="09059-113">Número de variables globales en este efecto.</span><span class="sxs-lookup"><span data-stu-id="09059-113">Number of global variables in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="09059-114">**InterfaceVariables**</span><span class="sxs-lookup"><span data-stu-id="09059-114">**InterfaceVariables**</span></span>
</dt> <dd>

<span data-ttu-id="09059-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09059-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="09059-116">Número de interfaces globales en este efecto.</span><span class="sxs-lookup"><span data-stu-id="09059-116">Number of global interfaces in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="09059-117">**Descrita**</span><span class="sxs-lookup"><span data-stu-id="09059-117">**Techniques**</span></span>
</dt> <dd>

<span data-ttu-id="09059-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09059-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="09059-119">Número de técnicas de este efecto.</span><span class="sxs-lookup"><span data-stu-id="09059-119">Number of techniques in this effect.</span></span>

</dd> <dt>

<span data-ttu-id="09059-120">**Grupos**</span><span class="sxs-lookup"><span data-stu-id="09059-120">**Groups**</span></span>
</dt> <dd>

<span data-ttu-id="09059-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="09059-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="09059-122">Número de grupos en este efecto.</span><span class="sxs-lookup"><span data-stu-id="09059-122">Number of groups in this effect.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09059-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="09059-123">Remarks</span></span>

<span data-ttu-id="09059-124">D3DX11 \_ efecto \_ desc se usa con [**ID3DX11Effect:: GetDesc**](id3dx11effect-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="09059-124">D3DX11\_EFFECT\_DESC is used with [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="09059-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09059-125">Requirements</span></span>



| <span data-ttu-id="09059-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="09059-126">Requirement</span></span> | <span data-ttu-id="09059-127">Value</span><span class="sxs-lookup"><span data-stu-id="09059-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="09059-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09059-128">Header</span></span><br/> | <dl> <span data-ttu-id="09059-129"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="09059-129"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09059-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="09059-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09059-131">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="09059-131">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

