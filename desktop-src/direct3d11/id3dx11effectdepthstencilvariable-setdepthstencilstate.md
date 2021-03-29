---
title: Método ID3DX11EffectDepthStencilVariable SetDepthStencilState (D3dx11effect. h)
description: Establece el estado de la galería de símbolos de profundidad.
ms.assetid: 4ece246f-4466-4790-8f38-450b67fff7c6
keywords:
- Método SetDepthStencilState Direct3D 11
- Método SetDepthStencilState Direct3D 11, interfaz ID3DX11EffectDepthStencilVariable
- Interfaz ID3DX11EffectDepthStencilVariable Direct3D 11, método SetDepthStencilState
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.SetDepthStencilState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b82fac869cb15bced76fdc1335967c6f7d017f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987127"
---
# <a name="id3dx11effectdepthstencilvariablesetdepthstencilstate-method"></a><span data-ttu-id="449e7-106">ID3DX11EffectDepthStencilVariable:: SetDepthStencilState (método)</span><span class="sxs-lookup"><span data-stu-id="449e7-106">ID3DX11EffectDepthStencilVariable::SetDepthStencilState method</span></span>

<span data-ttu-id="449e7-107">Establece el estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="449e7-107">Sets the depth stencil state.</span></span>

## <a name="syntax"></a><span data-ttu-id="449e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="449e7-108">Syntax</span></span>


```C++
HRESULT SetDepthStencilState(
   UINT                    Index,
   ID3D11DepthStencilState *pDepthStencilState
);
```



## <a name="parameters"></a><span data-ttu-id="449e7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="449e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="449e7-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="449e7-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="449e7-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="449e7-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="449e7-112">Índice en una matriz de interfaces de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="449e7-112">Index into an array of depth-stencil interfaces.</span></span> <span data-ttu-id="449e7-113">Si solo hay una interfaz de estarcido de profundidad, use 0.</span><span class="sxs-lookup"><span data-stu-id="449e7-113">If there is only one depth-stencil interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="449e7-114">*pDepthStencilState*</span><span class="sxs-lookup"><span data-stu-id="449e7-114">*pDepthStencilState*</span></span> 
</dt> <dd>

<span data-ttu-id="449e7-115">Tipo: **[ **ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span><span class="sxs-lookup"><span data-stu-id="449e7-115">Type: **[**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate)\***</span></span>

<span data-ttu-id="449e7-116">Puntero a una interfaz [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) que contiene el nuevo estado de la galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="449e7-116">Pointer to an [**ID3D11DepthStencilState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilstate) interface containing the new depth stencil state.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="449e7-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="449e7-117">Return value</span></span>

<span data-ttu-id="449e7-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="449e7-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="449e7-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="449e7-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="449e7-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="449e7-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="449e7-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="449e7-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="449e7-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="449e7-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="449e7-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="449e7-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="449e7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="449e7-124">Requirements</span></span>



| <span data-ttu-id="449e7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="449e7-125">Requirement</span></span> | <span data-ttu-id="449e7-126">Value</span><span class="sxs-lookup"><span data-stu-id="449e7-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="449e7-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="449e7-127">Header</span></span><br/>  | <dl> <span data-ttu-id="449e7-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="449e7-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="449e7-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="449e7-129">Library</span></span><br/> | <dl> <span data-ttu-id="449e7-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="449e7-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="449e7-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="449e7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="449e7-132">ID3DX11EffectDepthStencilVariable</span><span class="sxs-lookup"><span data-stu-id="449e7-132">ID3DX11EffectDepthStencilVariable</span></span>](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

