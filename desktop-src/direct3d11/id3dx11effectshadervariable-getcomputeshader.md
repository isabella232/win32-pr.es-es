---
title: Método ID3DX11EffectShaderVariable GetComputeShader (D3dx11effect. h)
description: Obtener un sombreador de cálculo.
ms.assetid: 16a48be1-4e73-4206-837f-615f8d624086
keywords:
- Método GetComputeShader Direct3D 11
- Método GetComputeShader Direct3D 11, interfaz ID3DX11EffectShaderVariable
- Interfaz ID3DX11EffectShaderVariable Direct3D 11, método GetComputeShader
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable.GetComputeShader
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c9312a7d603370d53c0721574623733c9e75da8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280526"
---
# <a name="id3dx11effectshadervariablegetcomputeshader-method"></a><span data-ttu-id="917a2-106">ID3DX11EffectShaderVariable:: GetComputeShader (método)</span><span class="sxs-lookup"><span data-stu-id="917a2-106">ID3DX11EffectShaderVariable::GetComputeShader method</span></span>

<span data-ttu-id="917a2-107">Obtener un sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="917a2-107">Get a compute shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="917a2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="917a2-108">Syntax</span></span>


```C++
HRESULT GetComputeShader(
   UINT                ShaderIndex,
   ID3D11ComputeShader **ppPS
);
```



## <a name="parameters"></a><span data-ttu-id="917a2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="917a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="917a2-110">*ShaderIndex*</span><span class="sxs-lookup"><span data-stu-id="917a2-110">*ShaderIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="917a2-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="917a2-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="917a2-112">Índice del sombreador de cálculo.</span><span class="sxs-lookup"><span data-stu-id="917a2-112">Index of the compute shader.</span></span>

</dd> <dt>

<span data-ttu-id="917a2-113">*ppPS*</span><span class="sxs-lookup"><span data-stu-id="917a2-113">*ppPS*</span></span> 
</dt> <dd>

<span data-ttu-id="917a2-114">Tipo: **[ **ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***</span><span class="sxs-lookup"><span data-stu-id="917a2-114">Type: **[**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader)\*\***</span></span>

<span data-ttu-id="917a2-115">Puntero a un puntero [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) que se establecerá en el sombreador de cálculo en la devolución.</span><span class="sxs-lookup"><span data-stu-id="917a2-115">Pointer to an [**ID3D11ComputeShader**](/windows/win32/api/d3d11/nn-d3d11-id3d11computeshader) pointer that will be set to the compute shader on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="917a2-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="917a2-116">Return value</span></span>

<span data-ttu-id="917a2-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="917a2-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="917a2-118">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="917a2-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="917a2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="917a2-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="917a2-120">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="917a2-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="917a2-121">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="917a2-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="917a2-122">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="917a2-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="917a2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="917a2-123">Requirements</span></span>



| <span data-ttu-id="917a2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="917a2-124">Requirement</span></span> | <span data-ttu-id="917a2-125">Value</span><span class="sxs-lookup"><span data-stu-id="917a2-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="917a2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="917a2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="917a2-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="917a2-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="917a2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="917a2-128">Library</span></span><br/> | <dl> <span data-ttu-id="917a2-129"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="917a2-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="917a2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="917a2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917a2-131">ID3DX11EffectShaderVariable</span><span class="sxs-lookup"><span data-stu-id="917a2-131">ID3DX11EffectShaderVariable</span></span>](id3dx11effectshadervariable.md)
</dt> </dl>

 

