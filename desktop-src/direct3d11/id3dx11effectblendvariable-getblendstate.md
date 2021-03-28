---
title: Método ID3DX11EffectBlendVariable GetBlendState (D3dx11effect. h)
description: Obtiene un puntero a una interfaz de estado de mezcla.
ms.assetid: ab4ee765-b5ad-4dc3-9b00-48052528d3bd
keywords:
- Método GetBlendState Direct3D 11
- Método GetBlendState Direct3D 11, interfaz ID3DX11EffectBlendVariable
- Interfaz ID3DX11EffectBlendVariable Direct3D 11, método GetBlendState
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable.GetBlendState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48092b496fa8a38be7c9dd8aea67a26e8b56f4f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362704"
---
# <a name="id3dx11effectblendvariablegetblendstate-method"></a><span data-ttu-id="6fe97-106">ID3DX11EffectBlendVariable:: GetBlendState (método)</span><span class="sxs-lookup"><span data-stu-id="6fe97-106">ID3DX11EffectBlendVariable::GetBlendState method</span></span>

<span data-ttu-id="6fe97-107">Obtiene un puntero a una interfaz de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="6fe97-107">Get a pointer to a blend-state interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe97-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6fe97-108">Syntax</span></span>


```C++
HRESULT GetBlendState(
   UINT             Index,
   ID3D11BlendState **ppBlendState
);
```



## <a name="parameters"></a><span data-ttu-id="6fe97-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6fe97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe97-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="6fe97-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe97-111">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6fe97-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6fe97-112">Índice en una matriz de interfaces de estado de mezcla.</span><span class="sxs-lookup"><span data-stu-id="6fe97-112">Index into an array of blend-state interfaces.</span></span> <span data-ttu-id="6fe97-113">Si solo hay una interfaz de estado de mezcla, use 0.</span><span class="sxs-lookup"><span data-stu-id="6fe97-113">If there is only one blend-state interface, use 0.</span></span>

</dd> <dt>

<span data-ttu-id="6fe97-114">*ppBlendState*</span><span class="sxs-lookup"><span data-stu-id="6fe97-114">*ppBlendState*</span></span> 
</dt> <dd>

<span data-ttu-id="6fe97-115">Tipo: **[ **ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span><span class="sxs-lookup"><span data-stu-id="6fe97-115">Type: **[**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)\*\***</span></span>

<span data-ttu-id="6fe97-116">La dirección de un puntero a una interfaz de estado de mezcla (vea [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span><span class="sxs-lookup"><span data-stu-id="6fe97-116">The address of a pointer to a blend-state interface (see [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe97-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6fe97-117">Return value</span></span>

<span data-ttu-id="6fe97-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6fe97-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6fe97-119">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6fe97-119">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6fe97-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fe97-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6fe97-121">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="6fe97-121">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6fe97-122">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="6fe97-122">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6fe97-123">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="6fe97-123">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6fe97-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fe97-124">Requirements</span></span>



| <span data-ttu-id="6fe97-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fe97-125">Requirement</span></span> | <span data-ttu-id="6fe97-126">Value</span><span class="sxs-lookup"><span data-stu-id="6fe97-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe97-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6fe97-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6fe97-128"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fe97-128"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6fe97-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fe97-129">Library</span></span><br/> | <dl> <span data-ttu-id="6fe97-130"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="6fe97-130"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fe97-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6fe97-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe97-132">ID3DX11EffectBlendVariable</span><span class="sxs-lookup"><span data-stu-id="6fe97-132">ID3DX11EffectBlendVariable</span></span>](id3dx11effectblendvariable.md)
</dt> </dl>

 

