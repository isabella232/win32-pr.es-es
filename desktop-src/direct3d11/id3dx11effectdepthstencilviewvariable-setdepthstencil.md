---
title: Método ID3DX11EffectDepthStencilViewVariable SetDepthStencil (D3dx11effect. h)
description: Establezca un recurso de vista de estarcido de profundidad.
ms.assetid: 35cbcd3b-6fc8-448d-a82e-724f91038d07
keywords:
- Método SetDepthStencil Direct3D 11
- Método SetDepthStencil Direct3D 11, interfaz ID3DX11EffectDepthStencilViewVariable
- Interfaz ID3DX11EffectDepthStencilViewVariable Direct3D 11, método SetDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.SetDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 723be51bc769982acf43c19482978bd581cafa13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998478"
---
# <a name="id3dx11effectdepthstencilviewvariablesetdepthstencil-method"></a><span data-ttu-id="0116c-106">ID3DX11EffectDepthStencilViewVariable:: SetDepthStencil (método)</span><span class="sxs-lookup"><span data-stu-id="0116c-106">ID3DX11EffectDepthStencilViewVariable::SetDepthStencil method</span></span>

<span data-ttu-id="0116c-107">Establezca un recurso de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0116c-107">Set a depth-stencil-view resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="0116c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0116c-108">Syntax</span></span>


```C++
HRESULT SetDepthStencil(
   ID3D11DepthStencilView *pResource
);
```



## <a name="parameters"></a><span data-ttu-id="0116c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0116c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0116c-110">*código fuente*</span><span class="sxs-lookup"><span data-stu-id="0116c-110">*pResource*</span></span> 
</dt> <dd>

<span data-ttu-id="0116c-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span><span class="sxs-lookup"><span data-stu-id="0116c-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\***</span></span>

<span data-ttu-id="0116c-112">Puntero a una interfaz de vista de galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="0116c-112">A pointer to a depth-stencil-view interface.</span></span> <span data-ttu-id="0116c-113">Vea [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="0116c-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0116c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0116c-114">Return value</span></span>

<span data-ttu-id="0116c-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0116c-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0116c-116">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0116c-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0116c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0116c-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0116c-118">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="0116c-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="0116c-119">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="0116c-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="0116c-120">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="0116c-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0116c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0116c-121">Requirements</span></span>



| <span data-ttu-id="0116c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0116c-122">Requirement</span></span> | <span data-ttu-id="0116c-123">Value</span><span class="sxs-lookup"><span data-stu-id="0116c-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0116c-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0116c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0116c-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0116c-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0116c-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0116c-126">Library</span></span><br/> | <dl> <span data-ttu-id="0116c-127"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="0116c-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0116c-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0116c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0116c-129">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="0116c-129">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

 





