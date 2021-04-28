---
description: 'Función D3DXCreateEffectFromFile: cree un efecto a partir de una descripción de efecto ASCII o binario.'
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: Función D3DXCreateEffectFromFile (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d8b2afdd1e8008bc8e03efa670e5a4b37b6dc9f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094323"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="4e8d6-103">Función D3DXCreateEffectFromFile</span><span class="sxs-lookup"><span data-stu-id="4e8d6-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="4e8d6-104">Cree un efecto a partir de una descripción de efecto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e8d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e8d6-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="4e8d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e8d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e8d6-107">*pDevice* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4e8d6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8d6-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4e8d6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4e8d6-109">Puntero al dispositivo que creará el efecto.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="4e8d6-110">Vea [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)</span><span class="sxs-lookup"><span data-stu-id="4e8d6-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="4e8d6-111">*pSrcFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4e8d6-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8d6-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e8d6-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e8d6-113">Puntero al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-113">Pointer to the filename.</span></span> <span data-ttu-id="4e8d6-114">Este parámetro admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="4e8d6-115">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4e8d6-116">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4e8d6-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8d6-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e8d6-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="4e8d6-118">Matriz opcional terminada en NULL de definiciones de macro de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="4e8d6-119">Vea [**D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="4e8d6-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e8d6-120">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4e8d6-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8d6-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="4e8d6-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="4e8d6-122">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="4e8d6-123">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="4e8d6-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="4e8d6-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8d6-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e8d6-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e8d6-126">Si *pSrcFile* contiene un efecto de texto, flags puede ser una combinación de marcas [D3DXSHADER](d3dxshader-flags.md) y [marcas D3DXFX;](d3dxfx.md) De lo contrario, *pSrcFile* contiene un efecto binario y las únicas marcas respetadas son las marcas D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="4e8d6-127">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="4e8d6-128">Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="4e8d6-129">*pPool* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4e8d6-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8d6-130">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="4e8d6-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="4e8d6-131">Puntero a un [**objeto ID3DXEffectPool**](id3dxeffectpool.md) que se usará para los parámetros compartidos.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="4e8d6-132">Si este valor es **NULL,** no se compartirá ningún parámetro.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="4e8d6-133">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4e8d6-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8d6-134">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e8d6-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="4e8d6-135">Devuelve un puntero a un búfer que contiene el efecto compilado.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="4e8d6-136">Vea [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="4e8d6-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e8d6-137">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4e8d6-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e8d6-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e8d6-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4e8d6-139">Devuelve un puntero a un búfer que contiene una lista de errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="4e8d6-140">Vea [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="4e8d6-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e8d6-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e8d6-141">Return value</span></span>

<span data-ttu-id="4e8d6-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e8d6-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e8d6-143">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e8d6-144">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e8d6-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e8d6-145">Remarks</span></span>

<span data-ttu-id="4e8d6-146">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4e8d6-147">De lo contrario, el tipo de datos LPCTSTR se resuelve en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="4e8d6-148">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4e8d6-149">Si se define Unicode, la llamada de función se resuelve en D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="4e8d6-150">De lo contrario, la llamada de función se resuelve en D3DXCreateEffectFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="4e8d6-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e8d6-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e8d6-151">Requirements</span></span>



| <span data-ttu-id="4e8d6-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e8d6-152">Requirement</span></span> | <span data-ttu-id="4e8d6-153">Value</span><span class="sxs-lookup"><span data-stu-id="4e8d6-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e8d6-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e8d6-154">Header</span></span><br/>  | <dl> <span data-ttu-id="4e8d6-155"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="4e8d6-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4e8d6-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e8d6-156">Library</span></span><br/> | <dl> <span data-ttu-id="4e8d6-157"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e8d6-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4e8d6-158">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4e8d6-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e8d6-159">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="4e8d6-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="4e8d6-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="4e8d6-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="4e8d6-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="4e8d6-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
