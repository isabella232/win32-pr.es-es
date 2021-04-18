---
title: Método ID3DX11EffectRenderTargetViewVariable GetRenderTarget (D3dx11effect. h)
description: Obtiene un destino de representación.
ms.assetid: 96984d0a-b8f4-444a-9683-3c37d8274d75
keywords:
- Método GetRenderTarget Direct3D 11
- Método GetRenderTarget Direct3D 11, interfaz ID3DX11EffectRenderTargetViewVariable
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11, método GetRenderTarget
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa86dd3a5c950e18ae97ba1987ee0f44b9f658c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998731"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertarget-method"></a><span data-ttu-id="109c1-106">ID3DX11EffectRenderTargetViewVariable:: GetRenderTarget (método)</span><span class="sxs-lookup"><span data-stu-id="109c1-106">ID3DX11EffectRenderTargetViewVariable::GetRenderTarget method</span></span>

<span data-ttu-id="109c1-107">Obtiene un destino de representación.</span><span class="sxs-lookup"><span data-stu-id="109c1-107">Get a render-target.</span></span>

## <a name="syntax"></a><span data-ttu-id="109c1-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="109c1-108">Syntax</span></span>


```C++
HRESULT GetRenderTarget(
   ID3D11RenderTargetView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="109c1-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="109c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="109c1-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="109c1-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="109c1-111">Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="109c1-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="109c1-112">Dirección de un puntero a una interfaz de vista de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="109c1-112">The address of a pointer to a render-target-view interface.</span></span> <span data-ttu-id="109c1-113">Vea [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="109c1-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="109c1-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="109c1-114">Return value</span></span>

<span data-ttu-id="109c1-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="109c1-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="109c1-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="109c1-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="109c1-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="109c1-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="109c1-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="109c1-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="109c1-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="109c1-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="109c1-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="109c1-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="109c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="109c1-121">Requirements</span></span>



| <span data-ttu-id="109c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="109c1-122">Requirement</span></span> | <span data-ttu-id="109c1-123">Value</span><span class="sxs-lookup"><span data-stu-id="109c1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="109c1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="109c1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="109c1-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="109c1-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="109c1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="109c1-126">Library</span></span><br/> | <dl> <span data-ttu-id="109c1-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="109c1-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="109c1-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="109c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="109c1-129">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="109c1-129">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





