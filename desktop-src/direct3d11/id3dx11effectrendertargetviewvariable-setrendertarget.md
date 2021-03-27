---
title: Método ID3DX11EffectRenderTargetViewVariable SetRenderTarget (D3dx11effect. h)
description: Establezca un destino de representación.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Método SetRenderTarget Direct3D 11
- Método SetRenderTarget Direct3D 11, interfaz ID3DX11EffectRenderTargetViewVariable
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11, método SetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914826"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a><span data-ttu-id="6d3d5-106">ID3DX11EffectRenderTargetViewVariable:: SetRenderTarget (método)</span><span class="sxs-lookup"><span data-stu-id="6d3d5-106">ID3DX11EffectRenderTargetViewVariable::SetRenderTarget method</span></span>

<span data-ttu-id="6d3d5-107">Establezca un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="6d3d5-107">Set a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3d5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d3d5-108">Syntax</span></span>


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="6d3d5-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d3d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d3d5-110">*código fuente*</span><span class="sxs-lookup"><span data-stu-id="6d3d5-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="6d3d5-111">Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span><span class="sxs-lookup"><span data-stu-id="6d3d5-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***</span></span>

<span data-ttu-id="6d3d5-112">Puntero a una interfaz de presentación-destino-vista.</span><span class="sxs-lookup"><span data-stu-id="6d3d5-112">A pointer to a render-target-view interface.</span></span> <span data-ttu-id="6d3d5-113">Vea [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="6d3d5-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d3d5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d3d5-114">Return value</span></span>

<span data-ttu-id="6d3d5-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d3d5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d3d5-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6d3d5-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d3d5-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d3d5-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6d3d5-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="6d3d5-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6d3d5-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6d3d5-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6d3d5-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6d3d5-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d3d5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d3d5-121">Requirements</span></span>



| <span data-ttu-id="6d3d5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d3d5-122">Requirement</span></span> | <span data-ttu-id="6d3d5-123">Value</span><span class="sxs-lookup"><span data-stu-id="6d3d5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3d5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d3d5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6d3d5-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3d5-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6d3d5-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d3d5-126">Library</span></span><br/> | <dl> <span data-ttu-id="6d3d5-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="6d3d5-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d3d5-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d3d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d3d5-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="6d3d5-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





