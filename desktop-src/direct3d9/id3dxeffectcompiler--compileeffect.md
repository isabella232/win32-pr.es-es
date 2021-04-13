---
description: Compilar un efecto.
ms.assetid: be6f862a-5091-4a06-a27a-308e81360129
title: 'ID3DXEffectCompiler:: CompileEffect (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6552d0216cd05c40c122657270c02e0886438da1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362469"
---
# <a name="id3dxeffectcompilercompileeffect-method"></a><span data-ttu-id="be8f7-103">ID3DXEffectCompiler:: CompileEffect (método)</span><span class="sxs-lookup"><span data-stu-id="be8f7-103">ID3DXEffectCompiler::CompileEffect method</span></span>

<span data-ttu-id="be8f7-104">Compilar un efecto.</span><span class="sxs-lookup"><span data-stu-id="be8f7-104">Compile an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="be8f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be8f7-105">Syntax</span></span>


```C++
HRESULT CompileEffect(
  [in]          DWORD        Flags,
  [out, retval] LPD3DXBUFFER *ppEffect,
  [out, retval] LPD3DXBUFFER *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="be8f7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be8f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be8f7-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="be8f7-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be8f7-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="be8f7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="be8f7-109">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="be8f7-109">Compile options identified by various flags.</span></span> <span data-ttu-id="be8f7-110">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="be8f7-110">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="be8f7-111">Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="be8f7-111">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="be8f7-112">*ppEffect* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="be8f7-112">*ppEffect* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="be8f7-113">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="be8f7-113">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="be8f7-114">Búfer que contiene el efecto compilado.</span><span class="sxs-lookup"><span data-stu-id="be8f7-114">Buffer containing the compiled effect.</span></span> <span data-ttu-id="be8f7-115">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="be8f7-115">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="be8f7-116">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="be8f7-116">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="be8f7-117">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="be8f7-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="be8f7-118">Búfer que contiene al menos el primer mensaje de error de compilación que se produjo.</span><span class="sxs-lookup"><span data-stu-id="be8f7-118">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="be8f7-119">Esto incluye los errores del compilador y los errores de compilación de lenguaje de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="be8f7-119">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="be8f7-120">Para obtener más información sobre el acceso al búfer, vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="be8f7-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be8f7-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be8f7-121">Return value</span></span>

<span data-ttu-id="be8f7-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="be8f7-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="be8f7-123">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be8f7-123">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="be8f7-124">Si los argumentos no son válidos, el método devolverá D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="be8f7-124">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="be8f7-125">Si se produce un error en el método, el valor devuelto será E \_ producirá un error.</span><span class="sxs-lookup"><span data-stu-id="be8f7-125">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="be8f7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be8f7-126">Requirements</span></span>



| <span data-ttu-id="be8f7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="be8f7-127">Requirement</span></span> | <span data-ttu-id="be8f7-128">Value</span><span class="sxs-lookup"><span data-stu-id="be8f7-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="be8f7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be8f7-129">Header</span></span><br/>  | <dl> <span data-ttu-id="be8f7-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="be8f7-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="be8f7-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be8f7-131">Library</span></span><br/> | <dl> <span data-ttu-id="be8f7-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be8f7-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="be8f7-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="be8f7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8f7-134">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="be8f7-134">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> </dl>

 

 
