---
title: Método ID3DX11EffectPass GetPixelShaderDesc (D3dx11effect. h)
description: Obtiene una descripción del sombreador de píxeles.
ms.assetid: 5772f197-7ac5-4492-9a41-eedb1a8b22c9
keywords:
- Método GetPixelShaderDesc Direct3D 11
- Método GetPixelShaderDesc Direct3D 11, interfaz ID3DX11EffectPass
- Interfaz ID3DX11EffectPass Direct3D 11, método GetPixelShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetPixelShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c04479a58eed0aa94616f0ffc092f17d52d9af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986922"
---
# <a name="id3dx11effectpassgetpixelshaderdesc-method"></a><span data-ttu-id="80901-106">ID3DX11EffectPass:: GetPixelShaderDesc (método)</span><span class="sxs-lookup"><span data-stu-id="80901-106">ID3DX11EffectPass::GetPixelShaderDesc method</span></span>

<span data-ttu-id="80901-107">Obtiene una descripción del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="80901-107">Get a pixel-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="80901-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80901-108">Syntax</span></span>


```C++
HRESULT GetPixelShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="80901-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80901-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80901-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="80901-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="80901-111">Tipo: **[ **D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="80901-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="80901-112">Un puntero a una descripción del sombreador de píxeles (vea [**D3DX11 \_ Pass \_ Shader \_ DESC**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="80901-112">A pointer to a pixel-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80901-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80901-113">Return value</span></span>

<span data-ttu-id="80901-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80901-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80901-115">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="80901-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="80901-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="80901-116">Remarks</span></span>

<span data-ttu-id="80901-117">Un paso de efecto puede contener asignaciones de estado de representación y asignaciones de objetos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="80901-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="80901-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="80901-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="80901-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="80901-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="80901-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="80901-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80901-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80901-121">Requirements</span></span>



| <span data-ttu-id="80901-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="80901-122">Requirement</span></span> | <span data-ttu-id="80901-123">Value</span><span class="sxs-lookup"><span data-stu-id="80901-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80901-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80901-124">Header</span></span><br/>  | <dl> <span data-ttu-id="80901-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="80901-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="80901-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80901-126">Library</span></span><br/> | <dl> <span data-ttu-id="80901-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="80901-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80901-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="80901-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80901-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="80901-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





