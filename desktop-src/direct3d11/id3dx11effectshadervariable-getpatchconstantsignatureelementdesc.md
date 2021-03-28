---
title: Método ID3DX11EffectShaderVariable GetPatchConstantSignatureElementDesc (D3dx11effect. h)
description: Obtiene una descripción de la firma de la constante patch.
ms.assetid: 72a86cf6-ace2-4306-ac5c-37d888c087f7
keywords:
- Método GetPatchConstantSignatureElementDesc Direct3D 11
- Método GetPatchConstantSignatureElementDesc Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetPatchConstantSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetPatchConstantSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fcbc8f7c1bc34b0da42dd08c255a04a6d2fc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998659"
---
# <a name="id3dx11effectshadervariablegetpatchconstantsignatureelementdesc-method"></a><span data-ttu-id="2ce57-106">ID3DX11EffectShaderVariable:: GetPatchConstantSignatureElementDesc (método)</span><span class="sxs-lookup"><span data-stu-id="2ce57-106">ID3DX11EffectShaderVariable::GetPatchConstantSignatureElementDesc method</span></span>

<span data-ttu-id="2ce57-107">Obtiene una descripción de la firma de la constante patch.</span><span class="sxs-lookup"><span data-stu-id="2ce57-107">Get a patch constant signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce57-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ce57-108">Syntax</span></span>


```C++
HRESULT GetPatchConstantSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="2ce57-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ce57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce57-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="2ce57-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="2ce57-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ce57-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ce57-112">Índice de sombreador basado en cero.</span><span class="sxs-lookup"><span data-stu-id="2ce57-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="2ce57-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="2ce57-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="2ce57-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2ce57-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2ce57-115">Índice de elemento basado en cero.</span><span class="sxs-lookup"><span data-stu-id="2ce57-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="2ce57-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="2ce57-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="2ce57-117">Tipo: **[ **\_ parámetro de firma D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="2ce57-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="2ce57-118">Un puntero a una descripción de parámetro (vea [**D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="2ce57-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce57-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ce57-119">Return value</span></span>

<span data-ttu-id="2ce57-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ce57-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ce57-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2ce57-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce57-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2ce57-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2ce57-123">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="2ce57-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2ce57-124">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="2ce57-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2ce57-125">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2ce57-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2ce57-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ce57-126">Requirements</span></span>



| <span data-ttu-id="2ce57-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ce57-127">Requirement</span></span> | <span data-ttu-id="2ce57-128">Value</span><span class="sxs-lookup"><span data-stu-id="2ce57-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce57-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ce57-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2ce57-130"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ce57-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2ce57-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ce57-131">Library</span></span><br/> | <dl> <span data-ttu-id="2ce57-132"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="2ce57-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce57-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ce57-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce57-134">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="2ce57-134">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

