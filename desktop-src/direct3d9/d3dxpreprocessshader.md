---
description: Preprocesa un sombreador sin realizar la compilación. Esto resuelve todas las \# definiciones e \# incluye, y proporciona un sombreador independiente para la compilación posterior.
ms.assetid: d91258ed-6206-487a-aa81-e7c2bcea21ea
title: Función D3DXPreprocessShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 042cebe4e678ac1715a37ec3425ec0f21561797c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547830"
---
# <a name="d3dxpreprocessshader-function"></a><span data-ttu-id="254cc-104">D3DXPreprocessShader función)</span><span class="sxs-lookup"><span data-stu-id="254cc-104">D3DXPreprocessShader function</span></span>

<span data-ttu-id="254cc-105">Preprocesa un sombreador sin realizar la compilación.</span><span class="sxs-lookup"><span data-stu-id="254cc-105">Preprocesses a shader without performing compilation.</span></span> <span data-ttu-id="254cc-106">Esto resuelve todas las \# definiciones e \# incluye, y proporciona un sombreador independiente para la compilación posterior.</span><span class="sxs-lookup"><span data-stu-id="254cc-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="254cc-107">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="254cc-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="254cc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="254cc-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataSize,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="254cc-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="254cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="254cc-110">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="254cc-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254cc-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="254cc-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="254cc-112">Puntero a una cadena que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="254cc-112">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="254cc-113">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="254cc-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254cc-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="254cc-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="254cc-115">Longitud de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="254cc-115">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="254cc-116">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="254cc-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254cc-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="254cc-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="254cc-118">Una matriz opcional de estructuras [**D3DXMACRO**](d3dxmacro.md) terminada en **null** .</span><span class="sxs-lookup"><span data-stu-id="254cc-118">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="254cc-119">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="254cc-119">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="254cc-120">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="254cc-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="254cc-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="254cc-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="254cc-122">Puntero de interfaz opcional, [**ID3DXInclude**](id3dxinclude.md), que se va a usar para controlar las \# directivas Include.</span><span class="sxs-lookup"><span data-stu-id="254cc-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="254cc-123">Si este valor es **null**, se \# respetarán las inclusiones al compilar desde un archivo o se producirá un error al compilarse a partir de un recurso o de una memoria.</span><span class="sxs-lookup"><span data-stu-id="254cc-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="254cc-124">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="254cc-124">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="254cc-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="254cc-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="254cc-126">Devuelve un búfer que contiene una sola cadena grande que representa la secuencia de token con formato resultante.</span><span class="sxs-lookup"><span data-stu-id="254cc-126">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="254cc-127">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="254cc-127">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="254cc-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="254cc-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="254cc-129">Devuelve un búfer que contiene una lista de errores y advertencias que se encontraron durante la compilación.</span><span class="sxs-lookup"><span data-stu-id="254cc-129">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="254cc-130">Estos son los mismos mensajes que muestra el depurador cuando se ejecuta en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="254cc-130">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="254cc-131">Este valor puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="254cc-131">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="254cc-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="254cc-132">Return value</span></span>

<span data-ttu-id="254cc-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="254cc-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="254cc-134">Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="254cc-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="254cc-135">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="254cc-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="254cc-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="254cc-136">Requirements</span></span>



| <span data-ttu-id="254cc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="254cc-137">Requirement</span></span> | <span data-ttu-id="254cc-138">Value</span><span class="sxs-lookup"><span data-stu-id="254cc-138">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="254cc-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="254cc-139">Header</span></span><br/>  | <dl> <span data-ttu-id="254cc-140"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="254cc-140"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="254cc-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="254cc-141">Library</span></span><br/> | <dl> <span data-ttu-id="254cc-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="254cc-142"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="254cc-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="254cc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="254cc-144">Funciones del sombreador</span><span class="sxs-lookup"><span data-stu-id="254cc-144">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="254cc-145">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="254cc-145">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="254cc-146">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="254cc-146">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
