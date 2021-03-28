---
title: Función D3DX11PreprocessShaderFromFile (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Tenga en cuenta que, en lugar de usar esta función, se recomienda usar la API de D3DPreprocess. Cree un sombreador a partir de un archivo sin compilarlo.
ms.assetid: aab08efd-b6b0-44e5-bd68-f32c242d9e94
keywords:
- Función D3DX11PreprocessShaderFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1987ef25688e83a48059805f79af4dc8a88c1ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986994"
---
# <a name="d3dx11preprocessshaderfromfile-function"></a><span data-ttu-id="05c21-106">D3DX11PreprocessShaderFromFile función)</span><span class="sxs-lookup"><span data-stu-id="05c21-106">D3DX11PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="05c21-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="05c21-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="05c21-108">En lugar de usar esta función, se recomienda usar la API de [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="05c21-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="05c21-109">Cree un sombreador a partir de un archivo sin compilarlo.</span><span class="sxs-lookup"><span data-stu-id="05c21-109">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="05c21-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05c21-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="05c21-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05c21-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05c21-112">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c21-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c21-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="05c21-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="05c21-114">Nombre del archivo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="05c21-114">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="05c21-115">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c21-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c21-116">Tipo: **D3D11 de \_ sombreador \_ \* const**</span><span class="sxs-lookup"><span data-stu-id="05c21-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="05c21-117">Una matriz terminada en NULL de macros de sombreador; Establezca este **valor en NULL** para no especificar ninguna macro.</span><span class="sxs-lookup"><span data-stu-id="05c21-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="05c21-118">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c21-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c21-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="05c21-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="05c21-120">Puntero a una interfaz de inclusión; Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="05c21-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="05c21-121">*pPump* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="05c21-121">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05c21-122">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="05c21-122">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="05c21-123">Un puntero a una interfaz de bombeo de subprocesos (consulte la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="05c21-123">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="05c21-124">Use **null** para especificar que esta función no debe devolver hasta que se complete.</span><span class="sxs-lookup"><span data-stu-id="05c21-124">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="05c21-125">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="05c21-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05c21-126">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="05c21-126">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="05c21-127">Puntero a la memoria que contiene el sombreador sin compilar.</span><span class="sxs-lookup"><span data-stu-id="05c21-127">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="05c21-128">*ppErrorMsgs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="05c21-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05c21-129">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="05c21-129">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="05c21-130">Dirección de un puntero a la memoria que contiene errores de creación de efectos, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="05c21-130">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="05c21-131">*pHResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="05c21-131">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05c21-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="05c21-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="05c21-133">Puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="05c21-133">A pointer to the return value.</span></span> <span data-ttu-id="05c21-134">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="05c21-134">May be **NULL**.</span></span> <span data-ttu-id="05c21-135">Si *pPump* no es **null**, *pHResult* debe ser una ubicación de memoria válida hasta que se complete la ejecución asincrónica.</span><span class="sxs-lookup"><span data-stu-id="05c21-135">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05c21-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05c21-136">Return value</span></span>

<span data-ttu-id="05c21-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="05c21-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="05c21-138">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="05c21-138">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05c21-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05c21-139">Requirements</span></span>



| <span data-ttu-id="05c21-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="05c21-140">Requirement</span></span> | <span data-ttu-id="05c21-141">Value</span><span class="sxs-lookup"><span data-stu-id="05c21-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05c21-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05c21-142">Header</span></span><br/>  | <dl> <span data-ttu-id="05c21-143"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="05c21-143"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="05c21-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05c21-144">Library</span></span><br/> | <dl> <span data-ttu-id="05c21-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05c21-145"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="05c21-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="05c21-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05c21-147">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="05c21-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

