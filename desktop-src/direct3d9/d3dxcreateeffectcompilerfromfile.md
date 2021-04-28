---
description: 'Función D3DXCreateEffectCompilerFromFile: crea un compilador de efectos a partir de una descripción de efecto ASCII.'
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: Función D3DXCreateEffectCompilerFromFile (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0c054b31b1ab70d1378c794be13058204b994ee2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087983"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="fcbb2-103">Función D3DXCreateEffectCompilerFromFile</span><span class="sxs-lookup"><span data-stu-id="fcbb2-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="fcbb2-104">Crea un compilador de efectos a partir de una descripción de efecto ASCII.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcbb2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fcbb2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="fcbb2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fcbb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcbb2-107">*pSrcFile* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fcbb2-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbb2-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcbb2-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcbb2-109">Puntero al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-109">Pointer to the filename.</span></span> <span data-ttu-id="fcbb2-110">Este parámetro admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="fcbb2-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fcbb2-112">*pDefines* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fcbb2-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbb2-113">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="fcbb2-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="fcbb2-114">Matriz **opcional terminada** en NULL de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen definiciones de preprocesador.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="fcbb2-115">Este valor puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="fcbb2-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fcbb2-116">*pInclude* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="fcbb2-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbb2-117">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="fcbb2-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="fcbb2-118">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se usará para controlar \# las directivas include.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="fcbb2-119">Si este valor es **NULL,** se respetará includes al compilar desde un archivo o se producirá un error cuando se compile desde un recurso \# o memoria.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="fcbb2-120">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="fcbb2-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbb2-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fcbb2-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fcbb2-122">Opciones de compilación identificadas por varias marcas (vea [D3DXSHADER Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="fcbb2-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="fcbb2-123">El compilador HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="fcbb2-124">Vea [Effect-Compiler Tool para](../direct3dtools/fxc.md) obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="fcbb2-125">*ppEffectCompiler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fcbb2-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbb2-126">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcbb2-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="fcbb2-127">Dirección de un puntero a una [**interfaz ID3DXEffectCompiler,**](id3dxeffectcompiler.md) que contiene el compilador de efectos.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="fcbb2-128">*ppParseErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fcbb2-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fcbb2-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="fcbb2-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="fcbb2-130">Dirección de un puntero a una [**interfaz ID3DXBuffer,**](id3dxbuffer.md) que contiene los mensajes de error que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="fcbb2-131">Este parámetro se puede establecer en **NULL para** omitir los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcbb2-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcbb2-132">Return value</span></span>

<span data-ttu-id="fcbb2-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fcbb2-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fcbb2-134">Si la función se realiza correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fcbb2-135">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcbb2-136">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcbb2-136">Remarks</span></span>

<span data-ttu-id="fcbb2-137">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fcbb2-138">De lo contrario, el tipo de datos LPCTSTR se resuelve en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="fcbb2-139">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="fcbb2-140">Si se define Unicode, la llamada de función se resuelve en D3DXCreateEffectCompilerFromFileW.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="fcbb2-141">De lo contrario, la llamada de función se resuelve en D3DXCreateEffectCompilerFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="fcbb2-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcbb2-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcbb2-142">Requirements</span></span>



| <span data-ttu-id="fcbb2-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcbb2-143">Requirement</span></span> | <span data-ttu-id="fcbb2-144">Value</span><span class="sxs-lookup"><span data-stu-id="fcbb2-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcbb2-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fcbb2-145">Header</span></span><br/>  | <dl> <span data-ttu-id="fcbb2-146"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="fcbb2-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="fcbb2-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fcbb2-147">Library</span></span><br/> | <dl> <span data-ttu-id="fcbb2-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fcbb2-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fcbb2-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fcbb2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcbb2-150">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="fcbb2-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="fcbb2-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="fcbb2-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="fcbb2-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="fcbb2-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
