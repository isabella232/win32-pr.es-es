---
title: Función D3DX11CreateAsyncShaderPreprocessProcessor (D3DX11async. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Vea la sección Comentarios. Cree un procesador de datos para un sombreador de forma asincrónica.
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- Función D3DX11CreateAsyncShaderPreprocessProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e58b267f186e5fd0104b10e9f9423f407aaf13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003898"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="cd220-106">D3DX11CreateAsyncShaderPreprocessProcessor función)</span><span class="sxs-lookup"><span data-stu-id="cd220-106">D3DX11CreateAsyncShaderPreprocessProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="cd220-107">La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="cd220-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="cd220-108">Vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="cd220-108">See Remarks.</span></span>

 

<span data-ttu-id="cd220-109">Cree un procesador de datos para un sombreador de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cd220-109">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd220-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd220-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="cd220-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd220-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd220-112">*pFileName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd220-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd220-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cd220-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cd220-114">Cadena que contiene el nombre de archivo del sombreador.</span><span class="sxs-lookup"><span data-stu-id="cd220-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="cd220-115">*pDefines* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd220-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd220-116">Tipo: **D3D11 de \_ sombreador \_ \* const**</span><span class="sxs-lookup"><span data-stu-id="cd220-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="cd220-117">Una matriz terminada en NULL de macros de sombreador; Establezca este **valor en NULL** para no especificar ninguna macro.</span><span class="sxs-lookup"><span data-stu-id="cd220-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="cd220-118">*pInclude* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cd220-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd220-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="cd220-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="cd220-120">Puntero a una interfaz de inclusión; Establezca este **valor en NULL** para especificar que no hay ningún archivo de inclusión.</span><span class="sxs-lookup"><span data-stu-id="cd220-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="cd220-121">*ppShaderText* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cd220-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd220-122">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="cd220-122">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="cd220-123">Dirección de un puntero a un búfer que contiene el texto ASCII del sombreador.</span><span class="sxs-lookup"><span data-stu-id="cd220-123">Address of a pointer to a buffer that contains the ASCII text of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="cd220-124">*ppErrorBuffer* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cd220-124">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd220-125">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="cd220-125">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="cd220-126">Dirección de un puntero a un búfer que contiene errores de compilación.</span><span class="sxs-lookup"><span data-stu-id="cd220-126">Address of a pointer to a buffer that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="cd220-127">*ppDataProcessor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cd220-127">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd220-128">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cd220-128">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="cd220-129">Dirección de un puntero a un búfer que contiene el procesador de datos creado (vea la [**interfaz ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="cd220-129">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd220-130">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd220-130">Return value</span></span>

<span data-ttu-id="cd220-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd220-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd220-132">El valor devuelto es uno de los valores que se muestran en [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cd220-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd220-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd220-133">Remarks</span></span>

<span data-ttu-id="cd220-134">No hay ninguna implementación del cargador asincrónico fuera de D3DX 10 y D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="cd220-134">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="cd220-135">En el caso de las aplicaciones de la tienda Windows, los ejemplos de DirectX (por ejemplo, el [ejemplo de tutorial de Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluyen el módulo **BasicLoader** que usa el modelo de programación asincrónica Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="cd220-135">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="cd220-136">En el caso de las aplicaciones de escritorio de Win32, puede usar la [Runtime de simultaneidad](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo similar a la Windows Runtime modelo de programación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="cd220-136">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd220-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd220-137">Requirements</span></span>



| <span data-ttu-id="cd220-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd220-138">Requirement</span></span> | <span data-ttu-id="cd220-139">Value</span><span class="sxs-lookup"><span data-stu-id="cd220-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd220-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd220-140">Header</span></span><br/>  | <dl> <span data-ttu-id="cd220-141"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd220-141"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="cd220-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd220-142">Library</span></span><br/> | <dl> <span data-ttu-id="cd220-143"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd220-143"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="cd220-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd220-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd220-145">Funciones de D3DX</span><span class="sxs-lookup"><span data-stu-id="cd220-145">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

