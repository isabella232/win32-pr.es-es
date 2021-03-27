---
title: Método ID3DX11EffectShaderVariable GetShaderDesc (D3dx11effect. h)
description: Obtener una descripción del sombreador.
ms.assetid: 7dd667d3-c500-4486-b279-a165befe8733
keywords:
- Método GetShaderDesc Direct3D 11
- Método GetShaderDesc Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c76730d1ad5f3de35e273034d3a17beb71fb7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987103"
---
# <a name="id3dx11effectshadervariablegetshaderdesc-method"></a><span data-ttu-id="8cc3d-106">ID3DX11EffectShaderVariable:: GetShaderDesc (método)</span><span class="sxs-lookup"><span data-stu-id="8cc3d-106">ID3DX11EffectShaderVariable::GetShaderDesc method</span></span>

<span data-ttu-id="8cc3d-107">Obtener una descripción del sombreador.</span><span class="sxs-lookup"><span data-stu-id="8cc3d-107">Get a shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc3d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cc3d-108">Syntax</span></span>


```C++
HRESULT GetShaderDesc(
   UINT                      ShaderIndex,
   D3DX11_EFFECT_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="8cc3d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cc3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc3d-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="8cc3d-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="8cc3d-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8cc3d-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8cc3d-112">Un índice basado en cero.</span><span class="sxs-lookup"><span data-stu-id="8cc3d-112">A zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="8cc3d-113">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="8cc3d-113">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="8cc3d-114">Tipo: **[ **D3DX11 \_ Effect \_ Shader \_ DESC**](d3dx11-effect-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="8cc3d-114">Type: **[**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)\***</span></span>

<span data-ttu-id="8cc3d-115">Un puntero a una descripción del sombreador (vea [**D3DX11 \_ Effect \_ Shader \_ DESC**](d3dx11-effect-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="8cc3d-115">A pointer to a shader description (see [**D3DX11\_EFFECT\_SHADER\_DESC**](d3dx11-effect-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc3d-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8cc3d-116">Return value</span></span>

<span data-ttu-id="8cc3d-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8cc3d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8cc3d-118">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8cc3d-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc3d-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8cc3d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8cc3d-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="8cc3d-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="8cc3d-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="8cc3d-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="8cc3d-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="8cc3d-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8cc3d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc3d-123">Requirements</span></span>



| <span data-ttu-id="8cc3d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc3d-124">Requirement</span></span> | <span data-ttu-id="8cc3d-125">Value</span><span class="sxs-lookup"><span data-stu-id="8cc3d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc3d-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cc3d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="8cc3d-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc3d-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="8cc3d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8cc3d-128">Library</span></span><br/> | <dl> <span data-ttu-id="8cc3d-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="8cc3d-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cc3d-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="8cc3d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc3d-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="8cc3d-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

