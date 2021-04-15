---
description: Ensamble un sombreador.
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: Función D3DXAssembleShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e748764eec94ea1f555c225c34680392610c9f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649455"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="8a21e-103">D3DXAssembleShaderFromResource función)</span><span class="sxs-lookup"><span data-stu-id="8a21e-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="8a21e-104">Ensamble un sombreador.</span><span class="sxs-lookup"><span data-stu-id="8a21e-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a21e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a21e-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="8a21e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8a21e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a21e-107">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a21e-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a21e-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a21e-109">Identificador de un módulo que contiene la descripción del efecto.</span><span class="sxs-lookup"><span data-stu-id="8a21e-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="8a21e-110">Si este parámetro es **null**, se usará el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="8a21e-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="8a21e-111">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a21e-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a21e-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a21e-113">Puntero a una cadena que especifica el nombre del recurso.</span><span class="sxs-lookup"><span data-stu-id="8a21e-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="8a21e-114">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="8a21e-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8a21e-115">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="8a21e-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="8a21e-116">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="8a21e-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8a21e-117">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a21e-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="8a21e-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="8a21e-119">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="8a21e-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="8a21e-120">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8a21e-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a21e-121">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a21e-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="8a21e-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="8a21e-123">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="8a21e-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="8a21e-124">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="8a21e-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="8a21e-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a21e-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8a21e-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8a21e-127">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="8a21e-127">Compile options identified by various flags.</span></span> <span data-ttu-id="8a21e-128">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8a21e-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="8a21e-129">Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="8a21e-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="8a21e-130">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a21e-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a21e-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8a21e-132">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="8a21e-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="8a21e-133">Este búfer contiene el código del sombreador compilado, así como cualquier información de la tabla de símbolos y de depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="8a21e-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="8a21e-134">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8a21e-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a21e-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8a21e-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8a21e-136">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="8a21e-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="8a21e-137">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="8a21e-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="8a21e-138">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="8a21e-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a21e-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a21e-139">Return value</span></span>

<span data-ttu-id="8a21e-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a21e-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a21e-141">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a21e-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8a21e-142">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8a21e-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a21e-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a21e-143">Remarks</span></span>

<span data-ttu-id="8a21e-144">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="8a21e-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="8a21e-145">Si se define Unicode, la llamada de función se resuelve como D3DXAssembleShaderFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="8a21e-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="8a21e-146">De lo contrario, la llamada de función se resuelve como D3DXAssembleShaderFromResourceA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="8a21e-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a21e-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a21e-147">Requirements</span></span>



| <span data-ttu-id="8a21e-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a21e-148">Requirement</span></span> | <span data-ttu-id="8a21e-149">Value</span><span class="sxs-lookup"><span data-stu-id="8a21e-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a21e-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a21e-150">Header</span></span><br/>  | <dl> <span data-ttu-id="8a21e-151"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a21e-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8a21e-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a21e-152">Library</span></span><br/> | <dl> <span data-ttu-id="8a21e-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a21e-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8a21e-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a21e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a21e-155">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="8a21e-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="8a21e-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="8a21e-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="8a21e-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="8a21e-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
