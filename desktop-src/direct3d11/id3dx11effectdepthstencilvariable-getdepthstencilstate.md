---
title: Método ID3DX11EffectDepthStencilVariable GetDepthStencilState (D3dx11effect. h)
description: Obtiene un puntero a una interfaz de estarcido de profundidad.
ms.assetid: 3e8f7fc6-960c-45f5-9276-9aa2a5e7a6c9
keywords:
- Método GetDepthStencilState Direct3D 11
- Método GetDepthStencilState Direct3D 11, interfaz ID3DX11EffectDepthStencilVariable
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11, método GetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e9276c7a126d5441361a4d449c4ee2ece70d995
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987132"
---
# <a name="id3dx11effectdepthstencilvariablegetdepthstencilstate-method"></a><span data-ttu-id="6d83a-106">ID3DX11EffectDepthStencilVariable:: GetDepthStencilState (método)</span><span class="sxs-lookup"><span data-stu-id="6d83a-106">ID3DX11EffectDepthStencilVariable::GetDepthStencilState method</span></span>

<span data-ttu-id="6d83a-107">Obtiene un puntero a una interfaz de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6d83a-107">Get a pointer to a depth-stencil interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d83a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d83a-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState **ppDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="6d83a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d83a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d83a-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="6d83a-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="6d83a-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6d83a-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6d83a-112">Índice en una matriz de interfaces de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="6d83a-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="6d83a-113">Si solo hay una interfaz de estarcido de profundidad, use 0.</span><span class="sxs-lookup"><span data-stu-id="6d83a-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="6d83a-114">*ppDepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="6d83a-114">*ppDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="6d83a-115">Tipo: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="6d83a-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\*\***</span></span>

<span data-ttu-id="6d83a-116">La dirección de un puntero a una interfaz de estado de mezcla (vea [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span><span class="sxs-lookup"><span data-stu-id="6d83a-116">The address of a pointer to a blend-state interface (see [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d83a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d83a-117">Return value</span></span>

<span data-ttu-id="6d83a-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d83a-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d83a-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6d83a-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d83a-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d83a-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6d83a-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="6d83a-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6d83a-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6d83a-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6d83a-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6d83a-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d83a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d83a-124">Requirements</span></span>



| <span data-ttu-id="6d83a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d83a-125">Requirement</span></span> | <span data-ttu-id="6d83a-126">Value</span><span class="sxs-lookup"><span data-stu-id="6d83a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d83a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d83a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6d83a-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d83a-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6d83a-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d83a-129">Library</span></span><br/> | <dl> <span data-ttu-id="6d83a-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="6d83a-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d83a-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d83a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d83a-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="6d83a-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

