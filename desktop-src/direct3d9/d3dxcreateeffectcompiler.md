---
description: Crea un compilador de efectos a partir de una descripción de efectos ASCII.
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: Función D3DXCreateEffectCompiler (D3DX9Effect. h)
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
ms.openlocfilehash: 513b11ba12abe05126c122f8bc9bfcfa978df3fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821399"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="f2f60-103">D3DXCreateEffectCompiler función)</span><span class="sxs-lookup"><span data-stu-id="f2f60-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="f2f60-104">Crea un compilador de efectos a partir de una descripción de efectos ASCII.</span><span class="sxs-lookup"><span data-stu-id="f2f60-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2f60-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f2f60-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f2f60-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f2f60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2f60-107">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f60-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f60-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2f60-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2f60-109">Puntero a un búfer que contiene una descripción de efecto.</span><span class="sxs-lookup"><span data-stu-id="f2f60-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="f2f60-110">*SrcDataLen* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f60-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f60-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2f60-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2f60-112">Longitud, en bytes, de los datos del efecto.</span><span class="sxs-lookup"><span data-stu-id="f2f60-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="f2f60-113">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f60-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f60-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2f60-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="f2f60-115">Una matriz opcional terminada en **null** de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen las definiciones del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="f2f60-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="f2f60-116">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="f2f60-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f2f60-117">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f2f60-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f60-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="f2f60-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="f2f60-119">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="f2f60-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="f2f60-120">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="f2f60-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="f2f60-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="f2f60-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f60-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2f60-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2f60-123">Opciones de compilación identificadas por varias marcas (consulte [marcas D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="f2f60-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="f2f60-124">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f2f60-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="f2f60-125">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="f2f60-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="f2f60-126">*ppEffectCompiler* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f2f60-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f60-127">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2f60-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="f2f60-128">Dirección de un puntero a una interfaz [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) que contiene el compilador de efectos.</span><span class="sxs-lookup"><span data-stu-id="f2f60-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="f2f60-129">*ppParseErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f2f60-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2f60-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="f2f60-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="f2f60-131">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) que contiene los mensajes de error que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="f2f60-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="f2f60-132">Este parámetro se puede establecer en **null** para omitir los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="f2f60-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2f60-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2f60-133">Return value</span></span>

<span data-ttu-id="f2f60-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f2f60-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f2f60-135">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2f60-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f2f60-136">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f2f60-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2f60-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2f60-137">Requirements</span></span>



| <span data-ttu-id="f2f60-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2f60-138">Requirement</span></span> | <span data-ttu-id="f2f60-139">Value</span><span class="sxs-lookup"><span data-stu-id="f2f60-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2f60-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2f60-140">Header</span></span><br/>  | <dl> <span data-ttu-id="f2f60-141"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2f60-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f2f60-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f2f60-142">Library</span></span><br/> | <dl> <span data-ttu-id="f2f60-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2f60-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f2f60-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f2f60-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2f60-145">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="f2f60-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="f2f60-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="f2f60-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="f2f60-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="f2f60-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
