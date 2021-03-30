---
title: Función D3DX11PreprocessShaderFromMemory (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la API de D3DPreprocess. Cree un sombreador a partir de la memoria sin compilarlo.
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- Función D3DX11PreprocessShaderFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a94633270fe0f4e462e60915de862be8693daa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998503"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a><span data-ttu-id="596e2-106">D3DX11PreprocessShaderFromMemory función)</span><span class="sxs-lookup"><span data-stu-id="596e2-106">D3DX11PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="596e2-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="596e2-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="596e2-108">En lugar de usar esta función, se recomienda usar la API de [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="596e2-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="596e2-109">Cree un sombreador a partir de la memoria sin compilarlo.</span><span class="sxs-lookup"><span data-stu-id="596e2-109">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="596e2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="596e2-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="596e2-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="596e2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="596e2-112">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="596e2-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="596e2-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="596e2-114">Puntero a la memoria que contiene el sombreador.</span><span class="sxs-lookup"><span data-stu-id="596e2-114">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="596e2-115">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="596e2-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-116">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="596e2-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="596e2-117">Tamaño del sombreador.</span><span class="sxs-lookup"><span data-stu-id="596e2-117">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="596e2-118">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="596e2-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-119">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="596e2-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="596e2-120">Nombre del sombreador.</span><span class="sxs-lookup"><span data-stu-id="596e2-120">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="596e2-121">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="596e2-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-122">Tipo: **D3D11 de \_ sombreador \_ \* const**</span><span class="sxs-lookup"><span data-stu-id="596e2-122">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="596e2-123">Una matriz terminada en NULL de macros de sombreador; Establezca este **valor en NULL** para no especificar ninguna macro.</span><span class="sxs-lookup"><span data-stu-id="596e2-123">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="596e2-124">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="596e2-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-125">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="596e2-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="596e2-126">Puntero a una interfaz de inclusión; Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="596e2-126">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="596e2-127">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="596e2-127">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-128">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="596e2-128">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="596e2-129">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="596e2-129">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="596e2-130">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="596e2-130">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="596e2-131">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="596e2-131">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-132">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="596e2-132">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="596e2-133">Puntero a la memoria que contiene el sombreador sin compilar.</span><span class="sxs-lookup"><span data-stu-id="596e2-133">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="596e2-134">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="596e2-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-135">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="596e2-135">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="596e2-136">Dirección de un puntero a la memoria que contiene errores de creación de efectos, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="596e2-136">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="596e2-137">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="596e2-137">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="596e2-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="596e2-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="596e2-139">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="596e2-139">A pointer to the return value.</span></span> <span data-ttu-id="596e2-140">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="596e2-140">May be **NULL**.</span></span> <span data-ttu-id="596e2-141">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="596e2-141">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="596e2-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="596e2-142">Return value</span></span>

<span data-ttu-id="596e2-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="596e2-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="596e2-144">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="596e2-144">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="596e2-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="596e2-145">Requirements</span></span>



| <span data-ttu-id="596e2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="596e2-146">Requirement</span></span> | <span data-ttu-id="596e2-147">Value</span><span class="sxs-lookup"><span data-stu-id="596e2-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="596e2-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="596e2-148">Header</span></span><br/>  | <dl> <span data-ttu-id="596e2-149"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="596e2-149"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="596e2-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="596e2-150">Library</span></span><br/> | <dl> <span data-ttu-id="596e2-151"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="596e2-151"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="596e2-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="596e2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="596e2-153">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="596e2-153">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

