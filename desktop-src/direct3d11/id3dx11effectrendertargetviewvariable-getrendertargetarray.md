---
title: Método ID3DX11EffectRenderTargetViewVariable GetRenderTargetArray (D3dx11effect. h)
description: Obtiene una matriz de destinos de representación.
ms.assetid: cc98a3b3-c2a2-48d0-86a8-77b914a199ec
keywords:
- Método GetRenderTargetArray Direct3D 11
- Método GetRenderTargetArray Direct3D 11, interfaz ID3DX11EffectRenderTargetViewVariable
- Interfaz ID3DX11EffectRenderTargetViewVariable Direct3D 11, método GetRenderTargetArray
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.GetRenderTargetArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3521b05bbc4e603264b993b6fe7b677a5cf46aee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998730"
---
# <a name="id3dx11effectrendertargetviewvariablegetrendertargetarray-method"></a><span data-ttu-id="3adb6-106">ID3DX11EffectRenderTargetViewVariable:: GetRenderTargetArray (método)</span><span class="sxs-lookup"><span data-stu-id="3adb6-106">ID3DX11EffectRenderTargetViewVariable::GetRenderTargetArray method</span></span>

<span data-ttu-id="3adb6-107">Obtiene una matriz de destinos de representación.</span><span class="sxs-lookup"><span data-stu-id="3adb6-107">Get an array of render-targets.</span></span>

## <a name="syntax"></a><span data-ttu-id="3adb6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3adb6-108">Syntax</span></span>


```C++
HRESULT GetRenderTargetArray(
   ID3D11RenderTargetView **ppResources,
   UINT                   Offset,
   UINT                   Count
);
```



## <a name="parameters"></a><span data-ttu-id="3adb6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3adb6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3adb6-110">*ppResources*</span><span class="sxs-lookup"><span data-stu-id="3adb6-110">*ppResources*</span></span> 
</dt> <dd>

<span data-ttu-id="3adb6-111">Tipo: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span><span class="sxs-lookup"><span data-stu-id="3adb6-111">Type: **[**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\*\***</span></span>

<span data-ttu-id="3adb6-112">Puntero a una matriz de interfaces de representación-destino-vista.</span><span class="sxs-lookup"><span data-stu-id="3adb6-112">A pointer to an array of render-target-view interfaces.</span></span> <span data-ttu-id="3adb6-113">Vea [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span><span class="sxs-lookup"><span data-stu-id="3adb6-113">See [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).</span></span>

</dd> <dt>

<span data-ttu-id="3adb6-114">*Offset*</span><span class="sxs-lookup"><span data-stu-id="3adb6-114">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="3adb6-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3adb6-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3adb6-116">Índice de base cero de la matriz para obtener la primera interfaz.</span><span class="sxs-lookup"><span data-stu-id="3adb6-116">The zero-based array index to get the first interface.</span></span>

</dd> <dt>

<span data-ttu-id="3adb6-117">*Recuento*</span><span class="sxs-lookup"><span data-stu-id="3adb6-117">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="3adb6-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3adb6-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3adb6-119">Número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="3adb6-119">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3adb6-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3adb6-120">Return value</span></span>

<span data-ttu-id="3adb6-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3adb6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3adb6-122">Devuelve uno de los siguientes [códigos de retorno de Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3adb6-122">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3adb6-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3adb6-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3adb6-124">El SDK de DirectX no proporciona archivos binarios compilados para efectos.</span><span class="sxs-lookup"><span data-stu-id="3adb6-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3adb6-125">Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3adb6-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3adb6-126">Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3adb6-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3adb6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3adb6-127">Requirements</span></span>



| <span data-ttu-id="3adb6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3adb6-128">Requirement</span></span> | <span data-ttu-id="3adb6-129">Value</span><span class="sxs-lookup"><span data-stu-id="3adb6-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3adb6-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3adb6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3adb6-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3adb6-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3adb6-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3adb6-132">Library</span></span><br/> | <dl> <span data-ttu-id="3adb6-133"><dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt></span><span class="sxs-lookup"><span data-stu-id="3adb6-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3adb6-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="3adb6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3adb6-135">ID3DX11EffectRenderTargetViewVariable</span><span class="sxs-lookup"><span data-stu-id="3adb6-135">ID3DX11EffectRenderTargetViewVariable</span></span>](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

