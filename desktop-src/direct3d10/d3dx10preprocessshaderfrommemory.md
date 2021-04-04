---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda usar la API de D3DPreprocess. Cree un sombreador a partir de la memoria sin compilarlo.
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: Función D3DX10PreprocessShaderFromMemory (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d06e46a5cd6b86420543b380f74273be032c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821319"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a><span data-ttu-id="840d5-104">D3DX10PreprocessShaderFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="840d5-104">D3DX10PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="840d5-105">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="840d5-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="840d5-106">Cree un sombreador a partir de la memoria sin compilarlo.</span><span class="sxs-lookup"><span data-stu-id="840d5-106">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="840d5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="840d5-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="840d5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="840d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="840d5-109">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="840d5-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="840d5-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="840d5-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="840d5-111">Puntero a la memoria que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="840d5-111">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="840d5-112">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="840d5-112">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="840d5-113">Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="840d5-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="840d5-114">Tamaño del sombreador.</span><span class="sxs-lookup"><span data-stu-id="840d5-114">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="840d5-115">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="840d5-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="840d5-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="840d5-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="840d5-117">Nombre del sombreador.</span><span class="sxs-lookup"><span data-stu-id="840d5-117">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="840d5-118">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="840d5-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="840d5-119">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="840d5-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="840d5-120">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="840d5-120">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="840d5-121">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="840d5-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="840d5-122">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="840d5-122">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="840d5-123">Un puntero a una interfaz de inclusión (vea la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="840d5-123">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="840d5-124">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="840d5-124">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="840d5-125">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="840d5-125">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="840d5-126">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="840d5-126">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="840d5-127">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="840d5-127">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="840d5-128">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="840d5-128">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="840d5-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="840d5-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="840d5-130">Puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene el sombreador sin compilar.</span><span class="sxs-lookup"><span data-stu-id="840d5-130">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="840d5-131">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="840d5-131">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="840d5-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="840d5-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="840d5-133">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de creación de efectos, si los hubiera.</span><span class="sxs-lookup"><span data-stu-id="840d5-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="840d5-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="840d5-134">Return value</span></span>

<span data-ttu-id="840d5-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="840d5-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="840d5-136">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="840d5-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="840d5-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="840d5-137">Requirements</span></span>



| <span data-ttu-id="840d5-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="840d5-138">Requirement</span></span> | <span data-ttu-id="840d5-139">Value</span><span class="sxs-lookup"><span data-stu-id="840d5-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="840d5-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="840d5-140">Header</span></span><br/>  | <dl> <span data-ttu-id="840d5-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="840d5-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="840d5-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="840d5-142">Library</span></span><br/> | <dl> <span data-ttu-id="840d5-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="840d5-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="840d5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="840d5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="840d5-145">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="840d5-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
