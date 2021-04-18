---
description: Crea un compilador de efectos a partir de una descripción de efectos ASCII.
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: Función D3DXCreateEffectCompilerFromFile (D3DX9Effect. h)
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
ms.openlocfilehash: fe27683078f77d7d444bd3a763fc326e749f7517
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721472"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="422c0-103">D3DXCreateEffectCompilerFromFile función)</span><span class="sxs-lookup"><span data-stu-id="422c0-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="422c0-104">Crea un compilador de efectos a partir de una descripción de efectos ASCII.</span><span class="sxs-lookup"><span data-stu-id="422c0-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="422c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="422c0-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="422c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="422c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="422c0-107">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="422c0-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="422c0-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="422c0-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="422c0-109">Puntero al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="422c0-109">Pointer to the filename.</span></span> <span data-ttu-id="422c0-110">Este parámetro admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="422c0-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="422c0-111">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="422c0-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="422c0-112">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="422c0-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="422c0-113">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="422c0-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="422c0-114">Una matriz opcional terminada en **null** de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen las definiciones del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="422c0-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="422c0-115">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="422c0-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="422c0-116">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="422c0-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="422c0-117">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="422c0-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="422c0-118">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="422c0-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="422c0-119">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="422c0-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="422c0-120">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="422c0-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="422c0-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="422c0-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="422c0-122">Opciones de compilación identificadas por varias marcas (consulte [marcas D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="422c0-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="422c0-123">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="422c0-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="422c0-124">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="422c0-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="422c0-125">*ppEffectCompiler* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="422c0-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="422c0-126">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="422c0-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="422c0-127">Dirección de un puntero a una interfaz [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) que contiene el compilador de efectos.</span><span class="sxs-lookup"><span data-stu-id="422c0-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="422c0-128">*ppParseErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="422c0-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="422c0-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="422c0-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="422c0-130">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene los mensajes de error que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="422c0-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="422c0-131">Este parámetro se puede establecer en **null** para omitir los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="422c0-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="422c0-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="422c0-132">Return value</span></span>

<span data-ttu-id="422c0-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="422c0-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="422c0-134">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="422c0-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="422c0-135">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="422c0-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="422c0-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="422c0-136">Remarks</span></span>

<span data-ttu-id="422c0-137">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="422c0-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="422c0-138">De lo contrario, el tipo de datos LPCTSTR se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="422c0-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="422c0-139">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="422c0-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="422c0-140">Si se define Unicode, la llamada de función se resuelve como D3DXCreateEffectCompilerFromFileW.</span><span class="sxs-lookup"><span data-stu-id="422c0-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="422c0-141">De lo contrario, la llamada de función se resuelve como D3DXCreateEffectCompilerFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="422c0-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="422c0-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="422c0-142">Requirements</span></span>



| <span data-ttu-id="422c0-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="422c0-143">Requirement</span></span> | <span data-ttu-id="422c0-144">Value</span><span class="sxs-lookup"><span data-stu-id="422c0-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="422c0-145">Encabezado</span><span class="sxs-lookup"><span data-stu-id="422c0-145">Header</span></span><br/>  | <dl> <span data-ttu-id="422c0-146"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="422c0-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="422c0-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="422c0-147">Library</span></span><br/> | <dl> <span data-ttu-id="422c0-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="422c0-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="422c0-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="422c0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="422c0-150">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="422c0-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="422c0-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="422c0-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="422c0-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="422c0-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
