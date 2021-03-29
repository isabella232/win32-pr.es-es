---
title: Método ID3DX11EffectDepthStencilViewVariable GetDepthStencil (D3dx11effect. h)
description: Obtener un recurso de vista de estarcido de profundidad.
ms.assetid: 7d94d98b-7070-41ee-9a9d-fe848f8914f2
keywords:
- Método GetDepthStencil Direct3D 11
- Método GetDepthStencil Direct3D 11, interfaz ID3DX11EffectDepthStencilViewVariable
- Interfaz ID3DX11EffectDepthStencilViewVariable Direct3D 11, método GetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49206f051922982ac77265e68fa3d7b7397d1348
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987121"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencil-method"></a><span data-ttu-id="9045f-106">ID3DX11EffectDepthStencilViewVariable:: GetDepthStencil (método)</span><span class="sxs-lookup"><span data-stu-id="9045f-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencil method</span></span>

<span data-ttu-id="9045f-107">Obtener un recurso de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="9045f-107">Get a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="9045f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9045f-108">Syntax</span></span>


```C++
HRESULT GetDepthStencil(
   ID3D11DepthStencilView **ppResource
);
```



## <a name="parameters"></a><span data-ttu-id="9045f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9045f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9045f-110">*ppResource*</span><span class="sxs-lookup"><span data-stu-id="9045f-110">*ppResource*</span></span> 
</dt> <dd>

<span data-ttu-id="9045f-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="9045f-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="9045f-112">Dirección de un puntero a una interfaz de vista de galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="9045f-112">The address of a pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="9045f-113">Vea [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="9045f-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9045f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9045f-114">Return value</span></span>

<span data-ttu-id="9045f-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9045f-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9045f-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9045f-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9045f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9045f-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9045f-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="9045f-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="9045f-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="9045f-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="9045f-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="9045f-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9045f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9045f-121">Requirements</span></span>



| <span data-ttu-id="9045f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9045f-122">Requirement</span></span> | <span data-ttu-id="9045f-123">Value</span><span class="sxs-lookup"><span data-stu-id="9045f-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9045f-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9045f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9045f-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9045f-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="9045f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9045f-126">Library</span></span><br/> | <dl> <span data-ttu-id="9045f-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="9045f-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9045f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="9045f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9045f-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="9045f-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





