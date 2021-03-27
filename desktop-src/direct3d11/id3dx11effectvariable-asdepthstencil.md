---
title: Método ID3DX11EffectVariable AsDepthStencil (D3dx11effect. h)
description: Obtiene una variable de estarcido de profundidad.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Método AsDepthStencil Direct3D 11
- Método AsDepthStencil Direct3D 11, interfaz ID3DX11EffectVariable
- Interfaz ID3DX11EffectVariable Direct3D 11, método AsDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 980bd43f51d187252fab1872ba75d04f82820ef8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003864"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a><span data-ttu-id="1b9de-106">ID3DX11EffectVariable:: AsDepthStencil (método)</span><span class="sxs-lookup"><span data-stu-id="1b9de-106">ID3DX11EffectVariable::AsDepthStencil method</span></span>

<span data-ttu-id="1b9de-107">Obtiene una variable de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1b9de-107">Get a depth-stencil variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b9de-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b9de-108">Syntax</span></span>


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a><span data-ttu-id="1b9de-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b9de-109">Parameters</span></span>

<span data-ttu-id="1b9de-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1b9de-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b9de-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b9de-111">Return value</span></span>

<span data-ttu-id="1b9de-112">Tipo: **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b9de-112">Type: **[**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span></span>

<span data-ttu-id="1b9de-113">Puntero a una variable de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1b9de-113">A pointer to a depth-stencil variable.</span></span> <span data-ttu-id="1b9de-114">Vea [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span><span class="sxs-lookup"><span data-stu-id="1b9de-114">See [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1b9de-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b9de-115">Remarks</span></span>

<span data-ttu-id="1b9de-116">AsDepthStencil devuelve una versión de la variable de efecto que se ha especializado en una variable de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1b9de-116">AsDepthStencil returns a version of the effect variable that has been specialized to a depth-stencil variable.</span></span> <span data-ttu-id="1b9de-117">De forma similar a una conversión, esta especialización devolverá un objeto no válido si la variable de efecto no contiene datos de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="1b9de-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil data.</span></span>

<span data-ttu-id="1b9de-118">Las aplicaciones pueden probar la validez del objeto devuelto mediante una llamada a [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="1b9de-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="1b9de-119">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="1b9de-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="1b9de-120">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="1b9de-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="1b9de-121">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1b9de-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1b9de-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b9de-122">Requirements</span></span>



| <span data-ttu-id="1b9de-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b9de-123">Requirement</span></span> | <span data-ttu-id="1b9de-124">Value</span><span class="sxs-lookup"><span data-stu-id="1b9de-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b9de-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b9de-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1b9de-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b9de-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1b9de-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1b9de-127">Library</span></span><br/> | <dl> <span data-ttu-id="1b9de-128"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="1b9de-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b9de-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b9de-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b9de-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="1b9de-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





