---
description: Preprocesa un archivo de sombreador sin realizar la compilación. Esto resuelve todas las \# definiciones e \# incluye, y proporciona un sombreador independiente para la compilación posterior.
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: Función D3DXPreprocessShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba9cf35418bbbe6fe4b39341031fd1e056b27dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362555"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a><span data-ttu-id="7248b-104">D3DXPreprocessShaderFromFile función)</span><span class="sxs-lookup"><span data-stu-id="7248b-104">D3DXPreprocessShaderFromFile function</span></span>

<span data-ttu-id="7248b-105">Preprocesa un archivo de sombreador sin realizar la compilación.</span><span class="sxs-lookup"><span data-stu-id="7248b-105">Preprocesses a shader file without performing compilation.</span></span> <span data-ttu-id="7248b-106">Esto resuelve todas las \# definiciones e \# incluye, y proporciona un sombreador independiente para la compilación posterior.</span><span class="sxs-lookup"><span data-stu-id="7248b-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="7248b-107">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="7248b-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7248b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7248b-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="7248b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7248b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7248b-110">*pSrcFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7248b-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7248b-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7248b-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7248b-112">Puntero a una cadena que especifica el nombre de archivo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="7248b-112">Pointer to a string that specifies the filename of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="7248b-113">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7248b-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7248b-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7248b-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7248b-115">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="7248b-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="7248b-116">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7248b-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7248b-117">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7248b-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7248b-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7248b-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7248b-119">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="7248b-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7248b-120">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="7248b-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7248b-121">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7248b-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7248b-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7248b-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7248b-123">Devuelve un búfer que contiene una sola cadena grande que representa la secuencia de token con formato resultante.</span><span class="sxs-lookup"><span data-stu-id="7248b-123">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="7248b-124">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7248b-124">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7248b-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7248b-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7248b-126">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="7248b-126">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="7248b-127">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="7248b-127">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="7248b-128">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7248b-128">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7248b-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7248b-129">Return value</span></span>

<span data-ttu-id="7248b-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7248b-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7248b-131">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7248b-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7248b-132">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7248b-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7248b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7248b-133">Requirements</span></span>



| <span data-ttu-id="7248b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7248b-134">Requirement</span></span> | <span data-ttu-id="7248b-135">Value</span><span class="sxs-lookup"><span data-stu-id="7248b-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7248b-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7248b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="7248b-137"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7248b-137"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7248b-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7248b-138">Library</span></span><br/> | <dl> <span data-ttu-id="7248b-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7248b-139"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7248b-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="7248b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7248b-141">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="7248b-141">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="7248b-142">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="7248b-142">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> <dt>

[<span data-ttu-id="7248b-143">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="7248b-143">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
