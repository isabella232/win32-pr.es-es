---
title: Método ID3DX11EffectShaderVariable GetOutputSignatureElementDesc (D3dx11effect. h)
description: Obtiene una descripción de la firma de salida.
ms.assetid: 05f43a57-18fa-4be7-814e-ffbe53837cab
keywords:
- Método GetOutputSignatureElementDesc Direct3D 11
- Método GetOutputSignatureElementDesc Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetOutputSignatureElementDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetOutputSignatureElementDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29545754be560a3a7710adf23963566a324d8a3f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998664"
---
# <a name="id3dx11effectshadervariablegetoutputsignatureelementdesc-method"></a><span data-ttu-id="283f0-106">ID3DX11EffectShaderVariable:: GetOutputSignatureElementDesc (método)</span><span class="sxs-lookup"><span data-stu-id="283f0-106">ID3DX11EffectShaderVariable::GetOutputSignatureElementDesc method</span></span>

<span data-ttu-id="283f0-107">Obtiene una descripción de la firma de salida.</span><span class="sxs-lookup"><span data-stu-id="283f0-107">Get an output-signature description.</span></span>

## <a name="syntax"></a><span data-ttu-id="283f0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="283f0-108">Syntax</span></span>


```C++
HRESULT GetOutputSignatureElementDesc(
   UINT                           ShaderIndex,
   UINT                           Element,
   D3D11_SIGNATURE_PARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="283f0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="283f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="283f0-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="283f0-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="283f0-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="283f0-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="283f0-112">Índice de sombreador basado en cero.</span><span class="sxs-lookup"><span data-stu-id="283f0-112">A zero-based shader index.</span></span>

</dd> <dt>

<span data-ttu-id="283f0-113">*Element*</span><span class="sxs-lookup"><span data-stu-id="283f0-113">*Element*</span></span> 
</dt> <dd>

<span data-ttu-id="283f0-114">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="283f0-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="283f0-115">Índice de elemento basado en cero.</span><span class="sxs-lookup"><span data-stu-id="283f0-115">A zero-based element index.</span></span>

</dd> <dt>

<span data-ttu-id="283f0-116">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="283f0-116">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="283f0-117">Tipo: **[ **\_ parámetro de firma D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span><span class="sxs-lookup"><span data-stu-id="283f0-117">Type: **[**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)\***</span></span>

<span data-ttu-id="283f0-118">Un puntero a una descripción de parámetro (vea [**D3D11 \_ Signature \_ Parameter \_ DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span><span class="sxs-lookup"><span data-stu-id="283f0-118">A pointer to a parameter description (see [**D3D11\_SIGNATURE\_PARAMETER\_DESC**](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="283f0-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="283f0-119">Return value</span></span>

<span data-ttu-id="283f0-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="283f0-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="283f0-121">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="283f0-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="283f0-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="283f0-122">Remarks</span></span>

<span data-ttu-id="283f0-123">Un efecto contiene uno o varios sombreadores; cada sombreador tiene una firma de entrada y salida; cada firma contiene uno o más elementos (o parámetros).</span><span class="sxs-lookup"><span data-stu-id="283f0-123">An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters).</span></span> <span data-ttu-id="283f0-124">El índice del sombreador identifica el sombreador y el índice del elemento identifica el elemento (o parámetro) de la firma del sombreador.</span><span class="sxs-lookup"><span data-stu-id="283f0-124">The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.</span></span>

> [!Note]  
> <span data-ttu-id="283f0-125">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="283f0-125">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="283f0-126">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="283f0-126">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="283f0-127">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="283f0-127">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="283f0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="283f0-128">Requirements</span></span>



| <span data-ttu-id="283f0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="283f0-129">Requirement</span></span> | <span data-ttu-id="283f0-130">Value</span><span class="sxs-lookup"><span data-stu-id="283f0-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="283f0-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="283f0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="283f0-132"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="283f0-132"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="283f0-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="283f0-133">Library</span></span><br/> | <dl> <span data-ttu-id="283f0-134"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="283f0-134"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="283f0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="283f0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="283f0-136">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="283f0-136">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

