---
description: Tenga en cuenta que, en lugar de usar esta función heredada, se recomienda usar la API de D3DPreprocess. Cree un sombreador a partir de un archivo sin compilarlo.
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: Función D3DX10PreprocessShaderFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e6222febd378b262d9fb9e87a6224968c2d04038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718373"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a><span data-ttu-id="93bef-104">D3DX10PreprocessShaderFromFile función)</span><span class="sxs-lookup"><span data-stu-id="93bef-104">D3DX10PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="93bef-105">En lugar de usar esta función heredada, se recomienda usar la API de [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="93bef-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="93bef-106">Cree un sombreador a partir de un archivo sin compilarlo.</span><span class="sxs-lookup"><span data-stu-id="93bef-106">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bef-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93bef-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="93bef-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93bef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bef-109">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93bef-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bef-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="93bef-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="93bef-111">Nombre del archivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="93bef-111">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="93bef-112">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93bef-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bef-113">Type: **constante [**de \_ sombreador \_**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \*** de tipo const</span><span class="sxs-lookup"><span data-stu-id="93bef-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="93bef-114">Una matriz terminada en NULL de macros de sombreador (consulte la [**\_ \_ macro del sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); establezca este valor en **null** para no especificar macros.</span><span class="sxs-lookup"><span data-stu-id="93bef-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="93bef-115">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93bef-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bef-116">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="93bef-116">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="93bef-117">Un puntero a una interfaz de inclusión (vea la [**interfaz ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="93bef-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="93bef-118">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="93bef-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93bef-119">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="93bef-119">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="93bef-120">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="93bef-120">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="93bef-121">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="93bef-121">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="93bef-122">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="93bef-122">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93bef-123">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="93bef-123">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="93bef-124">Puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene el sombreador sin compilar.</span><span class="sxs-lookup"><span data-stu-id="93bef-124">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="93bef-125">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="93bef-125">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93bef-126">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="93bef-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="93bef-127">La dirección de un puntero a la memoria (vea la [**interfaz ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) que contiene los errores de creación de efectos, si los hubiera.</span><span class="sxs-lookup"><span data-stu-id="93bef-127">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bef-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93bef-128">Return value</span></span>

<span data-ttu-id="93bef-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93bef-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93bef-130">El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="93bef-130">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93bef-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93bef-131">Requirements</span></span>



| <span data-ttu-id="93bef-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="93bef-132">Requirement</span></span> | <span data-ttu-id="93bef-133">Value</span><span class="sxs-lookup"><span data-stu-id="93bef-133">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="93bef-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93bef-134">Header</span></span><br/> | <dl> <span data-ttu-id="93bef-135"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="93bef-135"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93bef-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="93bef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bef-137">Funciones de De uso general</span><span class="sxs-lookup"><span data-stu-id="93bef-137">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
