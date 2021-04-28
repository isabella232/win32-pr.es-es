---
description: 'Función D3DXCreateEffect: cree un efecto a partir de una descripción de efecto ASCII o binario.'
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: Función D3DXCreateEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6821375dfc672d4937c335cf85dab12ba31b726c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115783"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="8220e-103">Función D3DXCreateEffect</span><span class="sxs-lookup"><span data-stu-id="8220e-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="8220e-104">Cree un efecto a partir de una descripción de efecto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="8220e-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8220e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8220e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="8220e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8220e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8220e-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8220e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8220e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8220e-109">Puntero al dispositivo que creará el efecto.</span><span class="sxs-lookup"><span data-stu-id="8220e-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="8220e-110">Vea [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)</span><span class="sxs-lookup"><span data-stu-id="8220e-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="8220e-111">*pSrcData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8220e-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8220e-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8220e-113">Puntero a un búfer que contiene una descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="8220e-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="8220e-114">*SrcDataLen* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8220e-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8220e-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8220e-116">Longitud de los datos del efecto, en bytes.</span><span class="sxs-lookup"><span data-stu-id="8220e-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8220e-117">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8220e-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="8220e-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="8220e-119">Matriz **opcional terminada** en NULL de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen definiciones de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="8220e-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="8220e-120">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="8220e-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8220e-121">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8220e-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="8220e-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="8220e-123">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="8220e-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="8220e-124">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="8220e-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="8220e-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8220e-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8220e-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8220e-127">Si *pSrcData contiene* un efecto de texto, flags puede ser una combinación de marcas [D3DXSHADER](d3dxshader-flags.md) y [marcas D3DXFX;](d3dxfx.md) de lo contrario, *pSrcData* contiene un efecto binario y las únicas marcas respetadas son las marcas D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="8220e-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="8220e-128">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8220e-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="8220e-129">Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8220e-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="8220e-130">*pPool* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="8220e-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-131">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="8220e-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="8220e-132">Puntero a un [**objeto ID3DXEffectPool**](id3dxeffectpool.md) que se usará para los parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="8220e-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="8220e-133">Si este valor es **NULL,** no se compartirá ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="8220e-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="8220e-134">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8220e-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-135">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="8220e-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="8220e-136">Devuelve un puntero a una [**interfaz ID3DXEffect.**](id3dxeffect.md)</span><span class="sxs-lookup"><span data-stu-id="8220e-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8220e-137">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8220e-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8220e-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8220e-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8220e-139">Devuelve un búfer que contiene una lista de errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="8220e-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8220e-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8220e-140">Return value</span></span>

<span data-ttu-id="8220e-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8220e-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8220e-142">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8220e-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8220e-143">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8220e-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="8220e-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8220e-144">Requirements</span></span>



| <span data-ttu-id="8220e-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="8220e-145">Requirement</span></span> | <span data-ttu-id="8220e-146">Value</span><span class="sxs-lookup"><span data-stu-id="8220e-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8220e-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8220e-147">Header</span></span><br/>  | <dl> <span data-ttu-id="8220e-148"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="8220e-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8220e-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8220e-149">Library</span></span><br/> | <dl> <span data-ttu-id="8220e-150"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8220e-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8220e-151">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8220e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8220e-152">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="8220e-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="8220e-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="8220e-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="8220e-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="8220e-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
