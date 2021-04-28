---
description: 'Función D3DXCreateEffectCompiler: crea un compilador de efectos a partir de una descripción del efecto ASCII.'
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: Función D3DXCreateEffectCompiler (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 38ab58ed15609d468d25f4406353448e4fd6adb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115773"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="a7563-103">Función D3DXCreateEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="a7563-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="a7563-104">Crea un compilador de efectos a partir de una descripción del efecto ASCII.</span><span class="sxs-lookup"><span data-stu-id="a7563-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7563-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7563-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="a7563-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7563-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7563-107">*pSrcData* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a7563-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7563-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7563-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7563-109">Puntero a un búfer que contiene una descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="a7563-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="a7563-110">*SrcDataLen* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a7563-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7563-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7563-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7563-112">Longitud, en bytes, de los datos de efecto.</span><span class="sxs-lookup"><span data-stu-id="a7563-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="a7563-113">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a7563-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7563-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="a7563-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="a7563-115">Matriz **opcional terminada** en NULL de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen definiciones de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="a7563-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="a7563-116">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a7563-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a7563-117">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a7563-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7563-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="a7563-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="a7563-119">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="a7563-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="a7563-120">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="a7563-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="a7563-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a7563-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7563-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7563-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7563-123">Opciones de compilación identificadas por varias marcas (vea [D3DXSHADER Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="a7563-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="a7563-124">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="a7563-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="a7563-125">Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a7563-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="a7563-126">*ppEffectCompiler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7563-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7563-127">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7563-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="a7563-128">Dirección de un puntero a una [**interfaz ID3DXEffectCompiler**](id3dxeffectcompiler.md) que contiene el compilador de efectos.</span><span class="sxs-lookup"><span data-stu-id="a7563-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="a7563-129">*ppParseErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7563-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7563-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7563-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a7563-131">Dirección de un puntero a una [**interfaz ID3DXBuffer**](id3dxbuffer.md) que contiene los mensajes de error que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="a7563-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="a7563-132">Este parámetro se puede establecer en **NULL para** omitir los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="a7563-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7563-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7563-133">Return value</span></span>

<span data-ttu-id="a7563-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7563-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7563-135">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7563-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a7563-136">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a7563-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7563-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7563-137">Requirements</span></span>



| <span data-ttu-id="a7563-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7563-138">Requirement</span></span> | <span data-ttu-id="a7563-139">Value</span><span class="sxs-lookup"><span data-stu-id="a7563-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7563-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7563-140">Header</span></span><br/>  | <dl> <span data-ttu-id="a7563-141"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="a7563-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a7563-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7563-142">Library</span></span><br/> | <dl> <span data-ttu-id="a7563-143"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7563-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a7563-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a7563-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7563-145">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="a7563-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="a7563-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="a7563-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="a7563-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="a7563-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
