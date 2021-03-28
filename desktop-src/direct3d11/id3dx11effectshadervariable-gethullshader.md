---
title: Método ID3DX11EffectShaderVariable GetHullShader (D3dx11effect. h)
description: Obtener un sombreador de casco.
ms.assetid: 18b2a8fc-2c53-4858-9aaa-00d0dc86adee
keywords:
- Método GetHullShader Direct3D 11
- Método GetHullShader Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetHullShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetHullShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7eac8e6e095eb1ddbba93d68bec87e85e0c4e22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998755"
---
# <a name="id3dx11effectshadervariablegethullshader-method"></a><span data-ttu-id="49d14-106">ID3DX11EffectShaderVariable:: GetHullShader (método)</span><span class="sxs-lookup"><span data-stu-id="49d14-106">ID3DX11EffectShaderVariable::GetHullShader method</span></span>

<span data-ttu-id="49d14-107">Obtener un sombreador de casco.</span><span class="sxs-lookup"><span data-stu-id="49d14-107">Get a hull shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="49d14-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49d14-108">Syntax</span></span>


```C++
HRESULT GetHullShader(
   UINT             ShaderIndex,
   ID3D11HullShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="49d14-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49d14-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49d14-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="49d14-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="49d14-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="49d14-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="49d14-112">Índice del sombreador.</span><span class="sxs-lookup"><span data-stu-id="49d14-112">Index of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="49d14-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="49d14-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="49d14-114">Tipo: **[ **ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="49d14-114">Type: **[**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader)\*\***</span></span>

<span data-ttu-id="49d14-115">Un puntero a un puntero [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) que se establecerá en el sombreador de casco en la devolución.</span><span class="sxs-lookup"><span data-stu-id="49d14-115">A pointer to an [**ID3D11HullShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11hullshader) pointer that will be set to the hull shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49d14-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49d14-116">Return value</span></span>

<span data-ttu-id="49d14-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49d14-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49d14-118">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="49d14-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49d14-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49d14-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49d14-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="49d14-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="49d14-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="49d14-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="49d14-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="49d14-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="49d14-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49d14-123">Requirements</span></span>



| <span data-ttu-id="49d14-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="49d14-124">Requirement</span></span> | <span data-ttu-id="49d14-125">Value</span><span class="sxs-lookup"><span data-stu-id="49d14-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49d14-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49d14-126">Header</span></span><br/>  | <dl> <span data-ttu-id="49d14-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="49d14-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="49d14-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49d14-128">Library</span></span><br/> | <dl> <span data-ttu-id="49d14-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="49d14-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49d14-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="49d14-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49d14-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="49d14-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

