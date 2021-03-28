---
title: Método ID3DX11EffectShaderVariable GetPixelShader (D3dx11effect. h)
description: Obtiene un sombreador de píxeles.
ms.assetid: 4ce4b248-23b9-4135-a2b4-262e63247688
keywords:
- Método GetPixelShader Direct3D 11
- Método GetPixelShader Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetPixelShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPixelShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6588fd9afb7e58308f0fbc120705d4a22d9f2ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548059"
---
# <a name="id3dx11effectshadervariablegetpixelshader-method"></a><span data-ttu-id="b394c-106">ID3DX11EffectShaderVariable:: GetPixelShader (método)</span><span class="sxs-lookup"><span data-stu-id="b394c-106">ID3DX11EffectShaderVariable::GetPixelShader method</span></span>

<span data-ttu-id="b394c-107">Obtiene un sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="b394c-107">Get a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b394c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b394c-108">Syntax</span></span>


```C++
HRESULT GetPixelShader(
   UINT              ShaderIndex,
   ID3D11PixelShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="b394c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b394c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b394c-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="b394c-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="b394c-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b394c-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b394c-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="b394c-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="b394c-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="b394c-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="b394c-114">Tipo: **[ **ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="b394c-114">Type: **[**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader)\*\***</span></span>

<span data-ttu-id="b394c-115">Un puntero a un puntero [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) que se establecerá en el sombreador de píxeles de la devolución.</span><span class="sxs-lookup"><span data-stu-id="b394c-115">A pointer to an [**ID3D11PixelShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11pixelshader) pointer that will be set to the pixel shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b394c-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b394c-116">Return value</span></span>

<span data-ttu-id="b394c-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b394c-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b394c-118">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b394c-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b394c-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b394c-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b394c-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="b394c-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b394c-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="b394c-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b394c-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b394c-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b394c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b394c-123">Requirements</span></span>



| <span data-ttu-id="b394c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b394c-124">Requirement</span></span> | <span data-ttu-id="b394c-125">Value</span><span class="sxs-lookup"><span data-stu-id="b394c-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b394c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b394c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b394c-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b394c-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b394c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b394c-128">Library</span></span><br/> | <dl> <span data-ttu-id="b394c-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="b394c-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b394c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="b394c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b394c-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="b394c-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

