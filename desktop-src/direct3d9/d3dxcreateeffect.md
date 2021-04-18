---
description: Cree un efecto a partir de una descripción de efectos ASCII o binarios.
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: Función D3DXCreateEffect (D3DX9Effect. h)
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
ms.openlocfilehash: 3d5ac013617368ba4d702815d79aa411ea2988b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721473"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="4298d-103">D3DXCreateEffect función)</span><span class="sxs-lookup"><span data-stu-id="4298d-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="4298d-104">Cree un efecto a partir de una descripción de efectos ASCII o binarios.</span><span class="sxs-lookup"><span data-stu-id="4298d-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4298d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4298d-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="4298d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4298d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4298d-107">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4298d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4298d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4298d-109">Puntero al dispositivo que va a crear el efecto.</span><span class="sxs-lookup"><span data-stu-id="4298d-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="4298d-110">Vea [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="4298d-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="4298d-111">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4298d-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4298d-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4298d-113">Puntero a un búfer que contiene una descripción de efecto.</span><span class="sxs-lookup"><span data-stu-id="4298d-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="4298d-114">*SrcDataLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4298d-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4298d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4298d-116">Longitud de los datos del efecto, en bytes.</span><span class="sxs-lookup"><span data-stu-id="4298d-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4298d-117">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4298d-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="4298d-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="4298d-119">Una matriz opcional terminada en **null** de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen las definiciones del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="4298d-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="4298d-120">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="4298d-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4298d-121">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4298d-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="4298d-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="4298d-123">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="4298d-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="4298d-124">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="4298d-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="4298d-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4298d-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4298d-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4298d-127">Si *pSrcData* contiene un efecto de texto, las marcas pueden ser una combinación de marcas de [D3DXSHADER](d3dxshader-flags.md) y marcas de [D3DXFX](d3dxfx.md) ; de lo contrario, *pSrcData* contiene un efecto binario y las únicas marcas respetadas son marcas D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="4298d-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="4298d-128">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4298d-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="4298d-129">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="4298d-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="4298d-130">*pPool* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4298d-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-131">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="4298d-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="4298d-132">Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) que se va a usar para los parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="4298d-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="4298d-133">Si este valor es **null**, no se compartirá ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="4298d-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="4298d-134">*ppEffect* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4298d-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-135">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="4298d-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="4298d-136">Devuelve un puntero a una interfaz [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="4298d-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="4298d-137">*ppCompilationErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4298d-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4298d-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4298d-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4298d-139">Devuelve un búfer que contiene una lista de errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="4298d-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4298d-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4298d-140">Return value</span></span>

<span data-ttu-id="4298d-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4298d-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4298d-142">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4298d-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4298d-143">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4298d-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4298d-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4298d-144">Requirements</span></span>



| <span data-ttu-id="4298d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="4298d-145">Requirement</span></span> | <span data-ttu-id="4298d-146">Value</span><span class="sxs-lookup"><span data-stu-id="4298d-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4298d-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4298d-147">Header</span></span><br/>  | <dl> <span data-ttu-id="4298d-148"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4298d-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4298d-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4298d-149">Library</span></span><br/> | <dl> <span data-ttu-id="4298d-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4298d-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4298d-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="4298d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4298d-152">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="4298d-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="4298d-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="4298d-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="4298d-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="4298d-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
