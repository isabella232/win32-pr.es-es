---
description: Crea un ID3DXEffectCompiler a partir de una descripción de efectos ASCII.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: Función D3DXCreateEffectCompilerFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280369"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a><span data-ttu-id="723fc-103">D3DXCreateEffectCompilerFromResource función)</span><span class="sxs-lookup"><span data-stu-id="723fc-103">D3DXCreateEffectCompilerFromResource function</span></span>

<span data-ttu-id="723fc-104">Crea un [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) a partir de una descripción de efectos ASCII.</span><span class="sxs-lookup"><span data-stu-id="723fc-104">Creates an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="723fc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="723fc-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="723fc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="723fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="723fc-107">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="723fc-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="723fc-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="723fc-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="723fc-109">Identificador de un módulo que contiene la descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="723fc-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="723fc-110">Si este parámetro es **null**, se usará el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="723fc-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="723fc-111">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="723fc-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="723fc-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="723fc-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="723fc-113">Puntero al recurso.</span><span class="sxs-lookup"><span data-stu-id="723fc-113">Pointer to the resource.</span></span> <span data-ttu-id="723fc-114">Este parámetro admite cadenas Unicode y ANSI.</span><span class="sxs-lookup"><span data-stu-id="723fc-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="723fc-115">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="723fc-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="723fc-116">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="723fc-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="723fc-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="723fc-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="723fc-118">Una matriz opcional terminada en **null** de estructuras [**D3DXMACRO**](d3dxmacro.md) que describen las definiciones del preprocesador.</span><span class="sxs-lookup"><span data-stu-id="723fc-118">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="723fc-119">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="723fc-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="723fc-120">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="723fc-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="723fc-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="723fc-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="723fc-122">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="723fc-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="723fc-123">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="723fc-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="723fc-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="723fc-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="723fc-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="723fc-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="723fc-126">Opciones de compilación identificadas por varias marcas (consulte [marcas D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="723fc-126">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="723fc-127">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="723fc-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="723fc-128">Consulte [herramienta de compilador de efectos](../direct3dtools/fxc.md) para más información.</span><span class="sxs-lookup"><span data-stu-id="723fc-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="723fc-129">*ppEffectCompiler* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="723fc-129">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="723fc-130">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="723fc-130">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="723fc-131">Dirección de un puntero a una interfaz [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) que contiene el compilador de efectos.</span><span class="sxs-lookup"><span data-stu-id="723fc-131">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="723fc-132">*ppParseErrors* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="723fc-132">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="723fc-133">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="723fc-133">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="723fc-134">Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) , que contiene los mensajes de error que se produjeron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="723fc-134">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="723fc-135">Este parámetro se puede establecer en **null** para omitir los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="723fc-135">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="723fc-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="723fc-136">Return value</span></span>

<span data-ttu-id="723fc-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="723fc-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="723fc-138">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="723fc-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="723fc-139">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="723fc-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="723fc-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="723fc-140">Remarks</span></span>

<span data-ttu-id="723fc-141">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="723fc-141">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="723fc-142">De lo contrario, el tipo de datos LPCTSTR se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="723fc-142">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="723fc-143">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="723fc-143">The compiler setting also determines the function version.</span></span> <span data-ttu-id="723fc-144">Si se define Unicode, la llamada de función se resuelve como D3DXCreateEffectCompilerFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="723fc-144">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromResourceW.</span></span> <span data-ttu-id="723fc-145">De lo contrario, la llamada de función se resuelve como D3DXCreateEffectCompilerFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="723fc-145">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="723fc-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="723fc-146">Requirements</span></span>



| <span data-ttu-id="723fc-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="723fc-147">Requirement</span></span> | <span data-ttu-id="723fc-148">Value</span><span class="sxs-lookup"><span data-stu-id="723fc-148">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="723fc-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="723fc-149">Header</span></span><br/>  | <dl> <span data-ttu-id="723fc-150"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="723fc-150"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="723fc-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="723fc-151">Library</span></span><br/> | <dl> <span data-ttu-id="723fc-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="723fc-152"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="723fc-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="723fc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723fc-154">Funciones de efecto</span><span class="sxs-lookup"><span data-stu-id="723fc-154">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="723fc-155">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="723fc-155">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="723fc-156">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="723fc-156">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
