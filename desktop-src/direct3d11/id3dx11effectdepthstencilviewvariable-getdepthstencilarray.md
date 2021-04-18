---
title: Método ID3DX11EffectDepthStencilViewVariable GetDepthStencilArray (D3dx11effect. h)
description: Obtiene una matriz de recursos de vista de estarcido de profundidad.
ms.assetid: 92b2d9b1-6cf8-4523-88e0-bcd09b95477c
keywords:
- Método GetDepthStencilArray Direct3D 11
- Método GetDepthStencilArray Direct3D 11, interfaz ID3DX11EffectDepthStencilViewVariable
- Interfaz ID3DX11EffectDepthStencilViewVariable Direct3D 11, método GetDepthStencilArray
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilViewVariable.GetDepthStencilArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7b886049413be542108257a47a3b1e3899910
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987120"
---
# <a name="id3dx11effectdepthstencilviewvariablegetdepthstencilarray-method"></a><span data-ttu-id="02915-106">ID3DX11EffectDepthStencilViewVariable:: GetDepthStencilArray (método)</span><span class="sxs-lookup"><span data-stu-id="02915-106">ID3DX11EffectDepthStencilViewVariable::GetDepthStencilArray method</span></span>

<span data-ttu-id="02915-107">Obtiene una matriz de recursos de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="02915-107">Get an array of depth-stencil-view resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="02915-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02915-108">Syntax</span></span>


```C++
HRESULT GetDepthStencilArray(
   ID3D11DepthStencilView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="02915-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="02915-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02915-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="02915-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="02915-111">Tipo: **[ **ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span><span class="sxs-lookup"><span data-stu-id="02915-111">Type: **[**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)\*\***</span></span>

<span data-ttu-id="02915-112">Puntero a una matriz de interfaces de vista de estarcido de profundidad.</span><span class="sxs-lookup"><span data-stu-id="02915-112">A pointer to an array of depth-stencil-view interfaces.</span></span> <span data-ttu-id="02915-113">Vea [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="02915-113">See [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview).</span></span>

</dd> <dt>

<span data-ttu-id="02915-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="02915-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="02915-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="02915-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="02915-116">Índice de base cero de la matriz para obtener la primera interfaz.</span><span class="sxs-lookup"><span data-stu-id="02915-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="02915-117">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="02915-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="02915-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="02915-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="02915-119">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="02915-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02915-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02915-120">Return value</span></span>

<span data-ttu-id="02915-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02915-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02915-122">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="02915-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02915-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02915-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="02915-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="02915-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="02915-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="02915-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="02915-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="02915-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="02915-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02915-127">Requirements</span></span>



| <span data-ttu-id="02915-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="02915-128">Requirement</span></span> | <span data-ttu-id="02915-129">Value</span><span class="sxs-lookup"><span data-stu-id="02915-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02915-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="02915-130">Header</span></span><br/>  | <dl> <span data-ttu-id="02915-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="02915-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="02915-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02915-132">Library</span></span><br/> | <dl> <span data-ttu-id="02915-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="02915-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02915-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="02915-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02915-135">ID3DX11EffectDepthStencilViewVariable</span><span class="sxs-lookup"><span data-stu-id="02915-135">ID3DX11EffectDepthStencilViewVariable</span></span>](id3dx11effectdepthstencilviewvariable.md)
</dt> </dl>

 

