---
title: D3DX11_PASS_DESC estructura (D3dx11effect. h)
description: Describe un paso de efecto, que contiene el estado de la canalización.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987204"
---
# <a name="d3dx11_pass_desc-structure"></a><span data-ttu-id="a8743-104">D3DX11 \_ Pass \_ DESC (estructura)</span><span class="sxs-lookup"><span data-stu-id="a8743-104">D3DX11\_PASS\_DESC structure</span></span>

<span data-ttu-id="a8743-105">Describe un paso de efecto, que contiene el estado de la canalización.</span><span class="sxs-lookup"><span data-stu-id="a8743-105">Describes an effect pass, which contains pipeline state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8743-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8743-106">Syntax</span></span>


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a><span data-ttu-id="a8743-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8743-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8743-108">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a8743-108">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="a8743-109">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8743-109">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8743-110">Nombre de este paso (**null** si no es anónimo).</span><span class="sxs-lookup"><span data-stu-id="a8743-110">Name of this pass (**NULL** if not anonymous).</span></span>

</dd> <dt>

<span data-ttu-id="a8743-111">**Anotaciones**</span><span class="sxs-lookup"><span data-stu-id="a8743-111">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="a8743-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8743-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8743-113">Número de anotaciones de este paso.</span><span class="sxs-lookup"><span data-stu-id="a8743-113">Number of annotations on this pass.</span></span>

</dd> <dt>

<span data-ttu-id="a8743-114">**pIAInputSignature**</span><span class="sxs-lookup"><span data-stu-id="a8743-114">**pIAInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="a8743-115">Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="a8743-115">Type: **[**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="a8743-116">Signatura del sombreador de vértices o del sombreador de geometría (si no hay ningún sombreador de vértices) o **null** si no existe ninguno.</span><span class="sxs-lookup"><span data-stu-id="a8743-116">Signature from the vertex shader or geometry shader (if there is no vertex shader) or **NULL** if neither exists.</span></span>

</dd> <dt>

<span data-ttu-id="a8743-117">**IAInputSignatureSize**</span><span class="sxs-lookup"><span data-stu-id="a8743-117">**IAInputSignatureSize**</span></span>
</dt> <dd>

<span data-ttu-id="a8743-118">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8743-118">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8743-119">Tamaño de Singature en bytes.</span><span class="sxs-lookup"><span data-stu-id="a8743-119">Singature size in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a8743-120">**StencilRef**</span><span class="sxs-lookup"><span data-stu-id="a8743-120">**StencilRef**</span></span>
</dt> <dd>

<span data-ttu-id="a8743-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8743-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8743-122">El valor de referencia de la galería de símbolos usado en el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="a8743-122">The stencil-reference value used in the depth-stencil state.</span></span>

</dd> <dt>

<span data-ttu-id="a8743-123">**SampleMask**</span><span class="sxs-lookup"><span data-stu-id="a8743-123">**SampleMask**</span></span>
</dt> <dd>

<span data-ttu-id="a8743-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8743-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8743-125">La máscara de ejemplo para el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="a8743-125">The sample mask for the blend state.</span></span>

</dd> <dt>

<span data-ttu-id="a8743-126">**BlendFactor**</span><span class="sxs-lookup"><span data-stu-id="a8743-126">**BlendFactor**</span></span>
</dt> <dd>

<span data-ttu-id="a8743-127">Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a8743-127">Type: **[**FLOAT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="a8743-128">Factores de mezcla por componente (RGBA) para el estado de Blend.</span><span class="sxs-lookup"><span data-stu-id="a8743-128">The per-component blend factors (RGBA) for the blend state.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8743-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8743-129">Remarks</span></span>

<span data-ttu-id="a8743-130">D3DX11 \_ Pass \_ desc se usa con [**ID3DX11EffectPass:: GetDesc**](id3dx11effectpass-getdesc.md).</span><span class="sxs-lookup"><span data-stu-id="a8743-130">D3DX11\_PASS\_DESC is used with [**ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8743-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8743-131">Requirements</span></span>



| <span data-ttu-id="a8743-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8743-132">Requirement</span></span> | <span data-ttu-id="a8743-133">Value</span><span class="sxs-lookup"><span data-stu-id="a8743-133">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8743-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8743-134">Header</span></span><br/> | <dl> <span data-ttu-id="a8743-135"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8743-135"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8743-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8743-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8743-137">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="a8743-137">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

