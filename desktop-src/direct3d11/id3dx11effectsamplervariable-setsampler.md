---
title: Método ID3DX11EffectSamplerVariable SetSampler (D3dx11effect. h)
description: Establezca el estado de muestra.
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- Método SetSampler Direct3D 11
- Método SetSampler Direct3D 11, interfaz ID3DX11EffectSamplerVariable
- Interfaz ID3DX11EffectSamplerVariable Direct3D 11, método SetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77a68adef00ac980b532e2fcd877e71eb63dc470
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362639"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a><span data-ttu-id="4288b-106">ID3DX11EffectSamplerVariable:: SetSampler (método)</span><span class="sxs-lookup"><span data-stu-id="4288b-106">ID3DX11EffectSamplerVariable::SetSampler method</span></span>

<span data-ttu-id="4288b-107">Establezca el estado de muestra.</span><span class="sxs-lookup"><span data-stu-id="4288b-107">Set sampler state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4288b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4288b-108">Syntax</span></span>


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a><span data-ttu-id="4288b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4288b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4288b-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="4288b-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="4288b-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4288b-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4288b-112">Índice en una matriz de interfaces de muestra.</span><span class="sxs-lookup"><span data-stu-id="4288b-112">Index into an array of sampler interfaces.</span></span> <span data-ttu-id="4288b-113">Si solo hay una interfaz de muestra, use 0.</span><span class="sxs-lookup"><span data-stu-id="4288b-113">If there is only one sampler interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="4288b-114">*pSampler*</span><span class="sxs-lookup"><span data-stu-id="4288b-114">*pSampler*</span></span> 
</dt> <dd>

<span data-ttu-id="4288b-115">Tipo: **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span><span class="sxs-lookup"><span data-stu-id="4288b-115">Type: **[**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***</span></span>

<span data-ttu-id="4288b-116">Puntero a una interfaz [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) que contiene el estado de la muestra.</span><span class="sxs-lookup"><span data-stu-id="4288b-116">Pointer to an [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) interface containing the sampler state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4288b-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4288b-117">Return value</span></span>

<span data-ttu-id="4288b-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4288b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4288b-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="4288b-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4288b-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4288b-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4288b-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="4288b-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4288b-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="4288b-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4288b-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4288b-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4288b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4288b-124">Requirements</span></span>



| <span data-ttu-id="4288b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4288b-125">Requirement</span></span> | <span data-ttu-id="4288b-126">Value</span><span class="sxs-lookup"><span data-stu-id="4288b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4288b-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4288b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4288b-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4288b-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4288b-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4288b-129">Library</span></span><br/> | <dl> <span data-ttu-id="4288b-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="4288b-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4288b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="4288b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4288b-132">ID3DX11EffectSamplerVariable</span><span class="sxs-lookup"><span data-stu-id="4288b-132">ID3DX11EffectSamplerVariable</span></span>](id3dx11effectsamplervariable.md)
</dt> </dl>

 

