---
title: D3DX11_EFFECT_SHADER_DESC estructura (D3dx11effect. h)
description: Describe un sombreador de efectos.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914801"
---
# <a name="d3dx11_effect_shader_desc-structure"></a><span data-ttu-id="c0450-104">D3DX11 \_ efecto de la \_ estructura de Descripción del sombreador \_</span><span class="sxs-lookup"><span data-stu-id="c0450-104">D3DX11\_EFFECT\_SHADER\_DESC structure</span></span>

<span data-ttu-id="c0450-105">Describe un sombreador de efectos.</span><span class="sxs-lookup"><span data-stu-id="c0450-105">Describes an effect shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0450-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0450-106">Syntax</span></span>


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a><span data-ttu-id="c0450-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0450-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c0450-108">**pInputSignature**</span><span class="sxs-lookup"><span data-stu-id="c0450-108">**pInputSignature**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-109">Tipo: **const [**byte**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="c0450-109">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="c0450-110">Se pasa a CreateInputLayout.</span><span class="sxs-lookup"><span data-stu-id="c0450-110">Passed into CreateInputLayout.</span></span> <span data-ttu-id="c0450-111">Solo es válido en un sombreador de vértices o sombreador de geometría.</span><span class="sxs-lookup"><span data-stu-id="c0450-111">Only valid on a vertex shader or geometry shader.</span></span> <span data-ttu-id="c0450-112">Vea [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="c0450-112">See [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="c0450-113">**IsInline**</span><span class="sxs-lookup"><span data-stu-id="c0450-113">**IsInline**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-114">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0450-114">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c0450-115">**True** si el sombreador está definido en línea; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c0450-115">**TRUE** is the shader is defined inline; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c0450-116">**pBytecode**</span><span class="sxs-lookup"><span data-stu-id="c0450-116">**pBytecode**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-117">Tipo: **const [**byte**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="c0450-117">Type: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

</dd> <dd>

<span data-ttu-id="c0450-118">Código de bytes del sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0450-118">Shader bytecode.</span></span>

</dd> <dt>

<span data-ttu-id="c0450-119">**BytecodeLength**</span><span class="sxs-lookup"><span data-stu-id="c0450-119">**BytecodeLength**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-120">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0450-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c0450-121">Longitud de pBytecode.</span><span class="sxs-lookup"><span data-stu-id="c0450-121">The length of pBytecode.</span></span>

</dd> <dt>

<span data-ttu-id="c0450-122">**SODecls**</span><span class="sxs-lookup"><span data-stu-id="c0450-122">**SODecls**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-123">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0450-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c0450-124">Cadena de declaración de salida de flujo (para el sombreador de geometría con el fin de hacerlo).</span><span class="sxs-lookup"><span data-stu-id="c0450-124">Stream out declaration string (for geometry shader with SO).</span></span>

</dd> <dt>

<span data-ttu-id="c0450-125">**RasterizedStream**</span><span class="sxs-lookup"><span data-stu-id="c0450-125">**RasterizedStream**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-126">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0450-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c0450-127">Indica qué secuencia se rasteriza.</span><span class="sxs-lookup"><span data-stu-id="c0450-127">Indicates which stream is rasterized.</span></span> <span data-ttu-id="c0450-128">Los sombreadores de geometría D3D11 pueden generar hasta cuatro flujos de datos, uno de los cuales se puede rasterizar.</span><span class="sxs-lookup"><span data-stu-id="c0450-128">D3D11 geometry shaders can output up to four streams of data, one of which can be rasterized.</span></span>

</dd> <dt>

<span data-ttu-id="c0450-129">**NumInputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="c0450-129">**NumInputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-130">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0450-130">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c0450-131">Número de entradas de la firma de entrada.</span><span class="sxs-lookup"><span data-stu-id="c0450-131">Number of entries in the input signature.</span></span>

</dd> <dt>

<span data-ttu-id="c0450-132">**NumOutputSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="c0450-132">**NumOutputSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-133">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0450-133">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c0450-134">Número de entradas de la firma de salida.</span><span class="sxs-lookup"><span data-stu-id="c0450-134">Number of entries in the output signature.</span></span>

</dd> <dt>

<span data-ttu-id="c0450-135">**NumPatchConstantSignatureEntries**</span><span class="sxs-lookup"><span data-stu-id="c0450-135">**NumPatchConstantSignatureEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c0450-136">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c0450-136">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="c0450-137">Número de entradas de la firma de la constante patch.</span><span class="sxs-lookup"><span data-stu-id="c0450-137">Number of entries in the patch constant signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0450-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0450-138">Remarks</span></span>

<span data-ttu-id="c0450-139">D3DX11 \_ Effect \_ Shader \_ desc se usa con [**ID3DX11EffectShaderVariable:: GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span><span class="sxs-lookup"><span data-stu-id="c0450-139">D3DX11\_EFFECT\_SHADER\_DESC is used with [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0450-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0450-140">Requirements</span></span>



| <span data-ttu-id="c0450-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0450-141">Requirement</span></span> | <span data-ttu-id="c0450-142">Value</span><span class="sxs-lookup"><span data-stu-id="c0450-142">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0450-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0450-143">Header</span></span><br/> | <dl> <span data-ttu-id="c0450-144"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0450-144"><dt>D3dx11effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0450-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0450-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0450-146">Effects 11 estructuras</span><span class="sxs-lookup"><span data-stu-id="c0450-146">Effects 11 Structures</span></span>](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

