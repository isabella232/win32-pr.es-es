---
description: Ensamble un sombreador.
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: Función D3DXAssembleShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6e355f6ce51158f72757f771114346899557c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707920"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="414ff-103">D3DXAssembleShaderFromFile función)</span><span class="sxs-lookup"><span data-stu-id="414ff-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="414ff-104">Ensamble un sombreador.</span><span class="sxs-lookup"><span data-stu-id="414ff-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="414ff-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="414ff-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="414ff-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="414ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="414ff-107">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="414ff-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="414ff-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="414ff-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="414ff-109">Puntero a una cadena que especifica el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="414ff-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="414ff-110">Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="414ff-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="414ff-111">De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="414ff-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="414ff-112">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="414ff-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="414ff-113">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="414ff-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="414ff-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="414ff-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="414ff-115">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="414ff-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="414ff-116">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="414ff-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="414ff-117">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="414ff-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="414ff-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="414ff-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="414ff-119">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="414ff-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="414ff-120">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="414ff-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="414ff-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="414ff-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="414ff-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="414ff-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="414ff-123">Opciones de compilación identificadas por varias marcas.</span><span class="sxs-lookup"><span data-stu-id="414ff-123">Compile options identified by various flags.</span></span> <span data-ttu-id="414ff-124">El compilador de HLSL de Direct3D 10 es ahora el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="414ff-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="414ff-125">Consulte [marcas de D3DXSHADER](d3dxshader-flags.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="414ff-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="414ff-126">*ppShader* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="414ff-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="414ff-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="414ff-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="414ff-128">Devuelve un búfer que contiene el sombreador creado.</span><span class="sxs-lookup"><span data-stu-id="414ff-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="414ff-129">Este búfer contiene el código del sombreador compilado, así como cualquier información de la tabla de símbolos y de depuración incrustada.</span><span class="sxs-lookup"><span data-stu-id="414ff-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="414ff-130">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="414ff-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="414ff-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="414ff-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="414ff-132">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="414ff-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="414ff-133">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="414ff-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="414ff-134">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="414ff-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="414ff-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="414ff-135">Return value</span></span>

<span data-ttu-id="414ff-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="414ff-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="414ff-137">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="414ff-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="414ff-138">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="414ff-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="414ff-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="414ff-139">Remarks</span></span>

<span data-ttu-id="414ff-140">La configuración del compilador también determina la versión de la función.</span><span class="sxs-lookup"><span data-stu-id="414ff-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="414ff-141">Si se define Unicode, la llamada de función se resuelve como D3DXAssembleShaderFromFileW.</span><span class="sxs-lookup"><span data-stu-id="414ff-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="414ff-142">De lo contrario, la llamada de función se resuelve como D3DXAssembleShaderFromFileA porque se usan cadenas ANSI.</span><span class="sxs-lookup"><span data-stu-id="414ff-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="414ff-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="414ff-143">Requirements</span></span>



| <span data-ttu-id="414ff-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="414ff-144">Requirement</span></span> | <span data-ttu-id="414ff-145">Value</span><span class="sxs-lookup"><span data-stu-id="414ff-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="414ff-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="414ff-146">Header</span></span><br/>  | <dl> <span data-ttu-id="414ff-147"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="414ff-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="414ff-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="414ff-148">Library</span></span><br/> | <dl> <span data-ttu-id="414ff-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="414ff-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="414ff-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="414ff-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414ff-151">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="414ff-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="414ff-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="414ff-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="414ff-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="414ff-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
