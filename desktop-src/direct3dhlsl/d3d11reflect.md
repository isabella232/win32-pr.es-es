---
title: D3D11Reflect función)
description: Obtiene un puntero a una interfaz de reflexión.
ms.assetid: 855097c7-988b-4ab6-90c5-e5dd0bc9e1e0
keywords:
- D3D11Reflect de función HLSL
topic_type:
- apiref
api_name:
- D3D11Reflect
api_location:
- D3dcompiler_47.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54a1f388ebb122398ad33c3a8d942496fa55393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157244"
---
# <a name="d3d11reflect-function"></a><span data-ttu-id="c3d2a-104">D3D11Reflect función)</span><span class="sxs-lookup"><span data-stu-id="c3d2a-104">D3D11Reflect function</span></span>

<span data-ttu-id="c3d2a-105">Obtiene un puntero a una interfaz de reflexión.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-105">Gets a pointer to a reflection interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d2a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3d2a-106">Syntax</span></span>

``` syntax
HRESULT D3D11Reflect(
  in  LPCVOID pSrcData,
  in  SIZE_T SrcDataSize,
  out ID3D11ShaderReflection ppReflector
);
```

## <a name="parameters"></a><span data-ttu-id="c3d2a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3d2a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3d2a-108">*pSrcData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3d2a-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d2a-109">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3d2a-109">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3d2a-110">Un puntero a los datos de origen como código HLSL compilado.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-110">A pointer to source data as compiled HLSL code.</span></span>

</dd> <dt>

<span data-ttu-id="c3d2a-111">*SrcDataSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3d2a-111">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d2a-112">Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3d2a-112">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3d2a-113">Longitud de *pSrcData*.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-113">Length of *pSrcData*.</span></span>

</dd> <dt>

<span data-ttu-id="c3d2a-114">*ppReflector* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c3d2a-114">*ppReflector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3d2a-115">Tipo: **[ **ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span><span class="sxs-lookup"><span data-stu-id="c3d2a-115">Type: **[**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection)\*\***</span></span>

<span data-ttu-id="c3d2a-116">Dirección de un puntero a la interfaz [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) .</span><span class="sxs-lookup"><span data-stu-id="c3d2a-116">The address of a pointer to the [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3d2a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3d2a-117">Return value</span></span>

<span data-ttu-id="c3d2a-118">Tipo: **[ **HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c3d2a-118">Type: **[**HRESULT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c3d2a-119">Devuelve uno de los códigos de retorno descritos en el tema [códigos de retorno de Direct3D 11](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span><span class="sxs-lookup"><span data-stu-id="c3d2a-119">Returns one of the return codes described in the topic [Direct3D 11 Return Codes](/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues).</span></span>

## <a name="remarks"></a><span data-ttu-id="c3d2a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3d2a-120">Remarks</span></span>

<span data-ttu-id="c3d2a-121">La función de compilador **D3D11Reflect** insertada es un contenedor para la función del compilador [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="c3d2a-121">The inline **D3D11Reflect** compiler function is a wrapper for the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) compiler function.</span></span> <span data-ttu-id="c3d2a-122">**D3D11Reflect** solo puede recuperar una interfaz [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-122">**D3D11Reflect** can retrieve only a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span> <span data-ttu-id="c3d2a-123">**D3DReflect** puede recuperar una interfaz de **ID3D11ShaderReflection** o una interfaz de reflexión de direct3d 10 o Direct3D 10,1, por ejemplo, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span><span class="sxs-lookup"><span data-stu-id="c3d2a-123">**D3DReflect** can retrieve a **ID3D11ShaderReflection** interface or a Direct3D 10 or Direct3D 10.1 reflection interface, for example, [**ID3D10ShaderReflection**](/windows/desktop/api/d3d10shader/nn-d3d10shader-id3d10shaderreflection).</span></span>

<span data-ttu-id="c3d2a-124">El código del sombreador contiene metadatos que se pueden inspeccionar mediante las API de reflexión.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-124">Shader code contains metadata that can be inspected using the reflection APIs.</span></span>

<span data-ttu-id="c3d2a-125">En el código siguiente se muestra cómo recuperar una interfaz [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="c3d2a-125">The following code shows how to retrieve a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) interface from a shader.</span></span>


```C++
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3D11Reflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            &pReflector);
```



## <a name="requirements"></a><span data-ttu-id="c3d2a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3d2a-126">Requirements</span></span>



| <span data-ttu-id="c3d2a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3d2a-127">Requirement</span></span> | <span data-ttu-id="c3d2a-128">Value</span><span class="sxs-lookup"><span data-stu-id="c3d2a-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3d2a-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c3d2a-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c3d2a-130"><dt>D3DCompiler. INL</dt></span><span class="sxs-lookup"><span data-stu-id="c3d2a-130"><dt>D3DCompiler.inl</dt></span></span> </dl>     |
| <span data-ttu-id="c3d2a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3d2a-131">Library</span></span><br/> | <dl> <span data-ttu-id="c3d2a-132"><dt>D3dcompiler \_ 47. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3d2a-132"><dt>D3dcompiler\_47.lib</dt></span></span> </dl> |
| <span data-ttu-id="c3d2a-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3d2a-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3d2a-134"><dt>\_47.dllD3dcompiler</dt></span><span class="sxs-lookup"><span data-stu-id="c3d2a-134"><dt>D3dcompiler\_47.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3d2a-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3d2a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3d2a-136">Funciones</span><span class="sxs-lookup"><span data-stu-id="c3d2a-136">Functions</span></span>](dx-graphics-d3dcompiler-reference-functions.md)
</dt> </dl>

 

