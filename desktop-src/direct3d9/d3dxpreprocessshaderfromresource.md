---
description: Preprocesa un recurso de sombreador sin realizar la compilación. Esto resuelve todas las \# definiciones e \# incluye, y proporciona un sombreador independiente para la compilación posterior.
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: Función D3DXPreprocessShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c45073d0b84ef6fb33d378c4c18f862f55c6b84a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362530"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a><span data-ttu-id="19448-104">D3DXPreprocessShaderFromResource función)</span><span class="sxs-lookup"><span data-stu-id="19448-104">D3DXPreprocessShaderFromResource function</span></span>

<span data-ttu-id="19448-105">Preprocesa un recurso de sombreador sin realizar la compilación.</span><span class="sxs-lookup"><span data-stu-id="19448-105">Preprocesses a shader resource without performing compilation.</span></span> <span data-ttu-id="19448-106">Esto resuelve todas las \# definiciones e \# incluye, y proporciona un sombreador independiente para la compilación posterior.</span><span class="sxs-lookup"><span data-stu-id="19448-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="19448-107">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="19448-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="19448-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19448-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="19448-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19448-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19448-110">*hSrcModule* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19448-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19448-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19448-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19448-112">Identificador del módulo que contiene el recurso de sombreador.</span><span class="sxs-lookup"><span data-stu-id="19448-112">Handle to the module that holds the shader resource.</span></span> <span data-ttu-id="19448-113">Si este valor es **null**, se usará el módulo actual.</span><span class="sxs-lookup"><span data-stu-id="19448-113">If this value is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="19448-114">*pSrcResource* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19448-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19448-115">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19448-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19448-116">Cadena que representa el nombre del recurso en el módulo.</span><span class="sxs-lookup"><span data-stu-id="19448-116">String that represents the name of the resource in the module.</span></span>

</dd> <dt>

<span data-ttu-id="19448-117">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19448-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19448-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="19448-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="19448-119">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="19448-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="19448-120">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="19448-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19448-121">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="19448-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19448-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="19448-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="19448-123">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="19448-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="19448-124">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="19448-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="19448-125">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="19448-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19448-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="19448-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="19448-127">Devuelve un búfer que contiene una sola cadena grande que representa la secuencia de token con formato resultante.</span><span class="sxs-lookup"><span data-stu-id="19448-127">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="19448-128">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="19448-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19448-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="19448-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="19448-130">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="19448-130">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="19448-131">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="19448-131">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="19448-132">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="19448-132">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19448-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19448-133">Return value</span></span>

<span data-ttu-id="19448-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19448-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19448-135">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="19448-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="19448-136">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="19448-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="19448-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19448-137">Requirements</span></span>



| <span data-ttu-id="19448-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="19448-138">Requirement</span></span> | <span data-ttu-id="19448-139">Value</span><span class="sxs-lookup"><span data-stu-id="19448-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19448-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19448-140">Header</span></span><br/>  | <dl> <span data-ttu-id="19448-141"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="19448-141"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="19448-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19448-142">Library</span></span><br/> | <dl> <span data-ttu-id="19448-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="19448-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="19448-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="19448-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19448-145">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="19448-145">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="19448-146">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="19448-146">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="19448-147">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="19448-147">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> </dl>

 

 
